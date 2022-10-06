We’re going to explore a range of computing topics as a [[discipline]] and a technology. 

Computers are the lifeblood of today’s world. If they were to suddenly turn off, all at once, the power grid would shut down, cars would crash, planes would fall, water treatment
plants would stop, stock markets would freeze, trucks with food wouldn’t know where to
deliver, and employees wouldn’t get paid.Even many non-computer objects - like shirts and chairs – are made in factories run by computers.

Computing really has transformed nearly every aspect of our lives.

And this isn’t the first time we’ve seen
[[this sort of]] technology-driven global change.

Advances in manufacturing during the Industrial
Revolution brought a new scale to human [[civilization]]

- in agriculture, industry and domestic life.

Mechanization meant superior harvests and
more food, mass produced goods, cheaper and

faster travel and communication, and usually
a better quality of life.

And computing technology is doing the same
right now – from automated farming and medical

equipment, to global telecommunications and
educational opportunities, and new frontiers

like Virtual Reality and Self Driving Cars.

We are living in a time likely to be remembered
as the Electronic Age.

With billions of transistors in just your
smartphones, computers can seem 
pretty complicated,

but really, they’re just simple machines
that perform complex actions through many

layers of abstraction.

So in this series, we’re going break down
those layers, and build up from simple 1’s

and 0’s, to logic units, CPUs, operating
systems, the entire Internet and beyond.

And don’t worry, in the same way someone
buying t-shirts on a webpage doesn’t need

to know how that webpage was programmed, or
the web designer doesn’t need to know how

all the packets are routed, or router engineers
don’t need to know about transistor logic,

this series will build on previous episodes
but not be dependent on them.

By the end of this series, I hope that you
can better contextualize computing’s role

both in your own life and society, and how
humanity's (arguably) greatest invention is 

just in its infancy, with its biggest impacts
yet to come.

But before we get into all that, we should
start at computing’s origins, because although

electronic computers are relatively new, the
need for computation is not.
The earliest recognized device for computing

was the abacus, invented in Mesopotamia around
2500 BCE.

It’s essentially a hand operated calculator,
that helps add and subtract many numbers.

It also stores the current state of the computation,
much like your hard drive does today.

The abacus was created because, the scale
of society had become greater than what a

single person could keep and manipulate in
their mind.

There might be thousands of people in a village
or tens of thousands of cattle.

There are many variants of the abacus, but
let’s look at a really basic version with

each row representing a different power of
ten.

So each bead on the bottom row represents
a single unit, in the next row they represent

10, the row above 100, and so on.

Let’s say we have 3 heads of cattle represented
by 3 beads on the bottom row on the right side.

If we were to buy 4 more cattle we would just
slide 4 more beads to the right for a total of 7.

But if we were to add 5 more after the first
3 we would run out of beads, so we would slide

everything back to the left, slide one bead
on the second row to the right, representing

ten, and then add the final 2 beads on the
bottom row for a total of 12.

This is particularly useful with large numbers.

So if we were to add 1,251 we would just add
1 to the bottom row, 5 to the second row,

2 to the third row, and 1 to the fourth row
- we don’t have to add in our head and the

abacus stores the total for us.

Over the next 4000 years, humans developed
all sorts of clever computing devices, like

the astrolabe, which enabled ships to calculate
their latitude at sea.

Or the slide rule, for assisting with multiplication
and division.

And there are literally hundred of types of
clocks created that could be used to calculate

sunrise, tides, positions of celestial bodies,
and even just the time.

Each one of these devices made something that
was previously laborious to calculate much

faster, easier, and often more accurate –– it
lowered the barrier to entry, and at the same

time, amplified our mental abilities –– take
note, this is a theme we’re going to touch

on a lot in this series.

As early computer pioneer Charles Babbage
said: “At each increase of knowledge, as

well as on the contrivance of every new tool,
human labour becomes abridged.”

However, none of these devices were called
“computers”.

The earliest documented use of the word “computer”
is from 1613, in a book by Richard Braithwait.

And it wasn’t a machine at all - it was
a job title.

Braithwait said,
“I have read the truest computer of times,

and the best arithmetician that ever breathed,
and he reduceth thy dayes into a short number”.

In those days, computer was a person who did
calculations, sometimes with the help of machines,

but often not.

This job title persisted until the late 1800s,
when the meaning of computer started shifting

to refer to devices.

Notable among these devices was the Step Reckoner,
built by German polymath Gottfried Leibniz

in 1694.

Leibniz said “... it is beneath the dignity
of excellent men to waste their time in calculation｣

when any peasant could do the work just as
accurately with the aid of a machine.”

It worked kind of like the odometer in your
car, which is really just a machine for adding

up the number of miles your car has driven.
 
The device had a series of gears that turned;
each gear had ten teeth, to represent the

digits from 0 to 9.

Whenever a gear bypassed nine, it rotated 
back to 0 and advanced the adjacent gear by one tooth.

Kind of like when hitting 10 on
that basic abacus.

This worked in reverse when doing subtraction,
too.

With some clever mechanical tricks, the Step
Reckoner was also able to multiply and divide numbers.

Multiplications and divisions are really just
many additions and subtractions.

For example, if we want to divide 17 by 5,
we just subtract 5, then 5, then 5 again,

and then we can’t subtract any more 5’s…
so we know 5 goes into 17 three times, with

2 left over.

The Step Reckoner was able to do this in an
automated way, and was the first machine that

could do all four of these operations.

And this design was so successful it was used
for the next three centuries of calculator design.

Unfortunately, even with mechanical calculators,
most real world problems required many steps

of computation before an answer was determined.

It could take hours or days to generate a
single result.

Also, these hand-crafted machines were expensive,
and not accessible to most of the population.

So, before 20th century, most people experienced
computing through pre-computed tables assembled

by those amazing “human computers” we
talked about.

So if you needed to know the square root of
8 million 6 hundred and 75 thousand 3 hundred

and 9, instead of spending all day hand-cranking
your Step Reckoner, you could look it up in

a huge book full of square root tables in
a minute or so.

Speed and accuracy is particularly important
on the battlefield, and so militaries were

among the first to apply computing to complex
problems.

A particularly difficult problem is accurately
firing artillery shells, which by the 1800s

could travel well over a kilometer (or a bit
more than half a mile).

Add to this varying wind conditions, temperature,
and atmospheric pressure, and even hitting

something as large as a ship was difficult.

Range Tables were created that allowed gunners
to look up environmental conditions and the

distance they wanted to fire, and the table
would tell them the angle to set the canon.

These Range Tables worked so well, they were
used well into World War Two.

The problem was, if you changed the design
of the cannon or of the shell, a whole new

table had to be computed, which was massively
time consuming and inevitably led to errors.

Charles Babbage acknowledged this problem
in 1822 in a paper to the Royal Astronomical

Society entitled: “Note on the application
of machinery to the computation of astronomical

and mathematical tables".

Let’s go to the thought bubble.

Charles Babbage proposed a new mechanical
device called the Difference Engine, a much

more complex machine that could approximate
polynomials.

Polynomials describe the relationship between
several variables - like range and air pressure,

or amount of pizza Carrie Anne eats and happiness.

Polynomials could also be used to approximate
logarithmic and trigonometric functions, which

are a real hassle to calculate by hand.

Babbage started construction in 1823, and
over the next two decades, tried to fabricate

and assemble the 25,000 components, collectively
weighing around 15 tons.

Unfortunately, the project was ultimately abandoned.

But, in 1991, historians finished constructing
a Difference Engine based on Babbage's drawings

and writings - and it worked!

But more importantly, during construction
of the Difference Engine, Babbage imagined

an even more complex machine - the Analytical
Engine.

Unlike the Difference Engine, Step Reckoner
and all other computational devices before

it - the Analytical Engine was a “general
purpose computer”.

It could be used for many things, not just
one particular computation; it could be given

data and run operations in sequence; it had
memory and even a primitive printer.

Like the Difference Engine, it was ahead of
its time, and was never fully constructed.

However, the idea of an “automatic computer”
– one that could guide itself through a

series of operations automatically, was a
huge deal, and would foreshadow computer programs.

English mathematician Ada Lovelace wrote hypothetical
programs for the Analytical Engine, saying,

“A new, a vast, and a powerful language
is developed for the future use of analysis.”

For her work, Ada is often considered the
world’s first programmer.

The Analytical Engine would inspire, arguably,
the first generation of computer scientists,

who incorporated many of Babbage’s ideas
in their machines.

This is why Babbage is often considered the
"father of computing".

Thanks Thought Bubble!

So by the end of the 19th century, computing
devices were used for special purpose tasks

in the sciences and engineering, but rarely
seen in business, government or domestic life.

However, the US government faced a serious
problem for its 1890 census that demanded

the kind of efficiency that only computers
could provide.

The US Constitution requires that a census
be conducted every ten years, for the purposes

of distributing federal funds, representation
in congress, and good stuff like that.

And by 1880, the US population was booming,
mostly due to immigration.

That census took seven years to manually compile
and by the time it was completed, it was already

out of date – and it was predicted that
the 1890 census would take 13 years to compute.

That’s a little problematic when it’s
required every decade!

The Census bureau turned to Herman Hollerith,
who had built a tabulating machine.

His machine was “electro-mechanical” – it
used traditional mechanical systems for keeping

count, like Leibniz’s Step Reckoner –– but
coupled them with electrically-powered components.

Hollerith’s machine used punch cards which
were paper cards with a grid of locations

that can be punched out to represent data.

For example, there was a series of holes for
marital status.

If you were married, you would punch out the
married spot, then when the card was inserted

into Hollerith’s machine, little metal pins
would come down over the card – if a spot

was punched out, the pin would pass through
the hole in the paper and into a little vial

of mercury, which completed the circuit.

This now completed circuit powered an electric
motor, which turned a gear to add one, in

this case, to the “married” total.

Hollerith’s machine was roughly 10x faster
than manual tabulations, and the Census was

completed in just two and a half years - saving
the census office millions of dollars.

Businesses began recognizing the value of
computing, and saw its potential to boost

profits by improving labor- and data-intensive
tasks, like accounting, insurance appraisals,

and inventory management.

To meet this demand, Hollerith founded The
Tabulating Machine Company, which later merged

with other machine makers in 1924 to become
The International Business Machines Corporation

or IBM - which you’ve probably heard of.

These electro-mechanical “business machines”
were a huge success, transforming commerce

and government, and by the mid-1900s, the
explosion in world population and the rise

of globalized trade demanded even faster and
more flexible tools for processing data, setting

the stage for digital computers, which we’ll
talk about next week.

