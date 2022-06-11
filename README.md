# crowd_evacuation
smtp project 2022
this document can be used for discussion

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

8/6 and 10/6: all parameters are in the model, ready to be used for investigation.
Vary N (the capitalised one) for number of people, 
h for height of the passage (remember to change the height attribute in the canvas) for tunnel width;
all the values for escalation/de-escalation of panic are arbitrary and can be changed at will.
sadly, wallbang couldn't be resolved without opening up a whole lot of other problems, and it gets worse when people move more slowly (like irl). 
so be it, im calling this code done

List of constants are:
width of tunnel h = 500 (in cm)
Length of space w/2 = 500 (in cm)
speed of people between 1.17 and 1.77 m/s when walking (in other words we assums 100 iterations of the Calculate function is equivalent to 1 second)
acceleration is less than 8 m/s^2 (using the usain bolt figure)
personal space is 46 cm (which is why collision is 46/2(20) = 1.15 times of sum of person radii)
people are considered as 20cm wide cylinders (2D model)
family groups is not implemented and time is not implemented (computational constraints)
