# crowd_evacuation
smtp project 2022
this document can be used for discussion

 tasks to do:
come up with a function for person's turning movement
create function for acceleration
start executing our ideas?


what are we gonna vary? 
- density of people (done) 14/5
- width of passage (done) 14/5
- acceleration (panic) (done) 29/5
- ppl grouped tgt (family) //not done

Changelog

14/5: new movement pattern for the people - they actually go somewhere and not just straight! 
Also removed ppl leaking from side of walls
Wall design changed to single gap in middle - makes our life easier

29/5: new model, acceleration and panic functions added
I realise that the reason for people banging walls is the fact people have a maximum speed, as panic level rises to infinity
before coding that in, people did not bang walls
colour codes for people: red = agitated people, green = panicking and close to die
However, the panic was coded as a logarithmic scale so as to avoid the problem of panic possibly becoming negative, so i cannot simulate a person being crushed for minutes (compressive aphyxia takes 15 mins to kill at least)
more realistic movement - to the halfway line at least
qualitative results can be taken here by looking at when the mass in the centre clears/ how few at the sides
