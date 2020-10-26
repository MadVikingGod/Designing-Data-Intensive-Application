# Start
"When building an application we still need to figure out which tools and which approaches are the most appropiate for the task at hand." There is no best soltuion for everything, nor can we be experts in all of them.  The goal of an architech is to apply the best methods for solving the problem.

# Thinking About Data Systems
4 - Like our applications our data can't be modeled effectivly by just one tool.  We will need multiple tools working in conjunction to build most complex system.

5 - "API usually hides those implemetation deatils" this is the goal of all good interfaces.

5 - "There are many factors that may influence the design" - These may change through the life of the product.  It's important when wqorking with a system to consider the goals and constratins of when it was built.

# Reliability
6 - Systems are "fault-tolerant or resilient", in programming we use defensive programming techniques.

7 - "Increase the rate of faults by traggering them deliverately" - This is Caos Engineering.

# Hardware Errors
8 - Error rates are usually based on runtime of machines.  So if you have 10,000 machines running 24/7 and there is an error rate that happens every 100,000 hours, you shoud see that happen twice a day.

Sofware errors are usually per request, so if you are getting 1,000 Requests Per Second (RPS), and the bug happes 1 in a million, that's about once ever 17 minutes.

# Software Errors
8 - Hardware faults are usually random and independent, so it's unlikely that a large ammount of hardware fails at the same time.  This would be like a DC disapearing.

Software by contrast is the oppostite.

8 - Describing some kinds of errors:
- 2nd also call a leak
- 4th thundering heard is an example

9 - "bugs that cause these kinds of software fualts may lie dormant for a long time" Caos engineering is about causing these circumstances so you can know your software handles them.

9 - Titles/roles focused on thinking carefually about topics:
- "assumtions and interactions in the system" - **Architect**
- "thorough testing" - **Test Engineering**
- "process isolation" - not a title but the process **Seperation of Concerns**
- "measuring, monitoring, and analyzing system behavior in production" - **DevOps**
- If a system is expected to provide some guarantee... it can constantly check itself while it is running and raise an alert if a discrepeancy is found" - **SLA**

10 - telemetry from the greek `tele - Remote` and `metron - Measure`

# Scalability
When making a feature we typically ask "Can it scale to our current load?"  What we should ask is "Can it scale to the load when it's done?"

# Describing Load and Performance
11 - Load parameters, why are they different for every system?
An example on 18 is 100,000 RP`S` of 1k vs 3 RP`M` of 2GB, have the same throughput, but wildly different loads on the system.

I would argue that most of the time you want to reach for P95 or higher.

15 - The reasoning is described here.  Typically the users with the slowest experiance are the ones with the most data.  They also tend to be the ones spending the most.

16 - also be ware of meaningless math.

# Approaches for Coping with Load
18 - Warning about 1 tool to rule them all

18 - "it's usually more important to be able to iterate quickly... than it is to scale" 

# Operability: Making Life Easy for Operations
19 "good operations can often work around the limitations of bad (or incomplete) software, but good software cannot run reliably with bad operations" - Best quote of the book

# Simplicity: Managing Complexity
20 - "complexity slows down everyone who needs to work on the system" We should design to remove that complexity

21 - Symptoms of complexity, and possible soltuions:
- "explosion of state space" - stateless services
- "tight coupling of modules" - micro services
- "inconsistent naming and terminology" - Domain Driven Design (DDD)

21 - accidental complexity, everything I touch.

21 - "finding good abstractions is very hard", and finding bad ones means you made the system more complex not less.
