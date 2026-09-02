# Karel J. Robot: Beeper House

One of the first programs I wrote, from when I was learning Java in 2018. It uses Karel
J. Robot, a teaching framework where you drive simple robots around a grid and drop
"beepers," as a way to practice loops and method decomposition before dealing with real
language features.

Four robots (`robbie`, `bobbie`, `lobbie`, and `door`) move around the grid laying
beepers to draw out a house shape, which is what the program announces when it starts.

## What's worth noticing

Karel robots can only ever turn left. So to turn right, you turn left three times, which
is where the `turnRight()`, `turnUp()`, and `turnAwesome()` helpers come from. That
constraint was the actual lesson: when the primitive you want doesn't exist, you build it
out of the ones you have.

## Running it

This is an Eclipse project, with `KarelJRobot.jar` checked in and already on the
classpath. Clone the repository, then import it with **File → Import → Existing Projects
into Workspace** and run `src/Driver.java`. A window opens and the robots animate at the
delay set by `World.setDelay(50)`.

## Honest notes

This is early work and it reads like it. The movement code is copy-pasted rather than
factored into loops over a list of robots, and each turn helper is hardcoded to one
specific robot instead of taking a robot as a parameter; which is the obvious fix and
exactly the kind of thing I didn't see at the time. Two robots, `filler` and `eraser`,
are declared and never used. `hurdles.kwld` is a world file left over from the starter
project this was built on top of, and the program doesn't load it.

I'm keeping it up because the progression is the point, not because the code is good.
