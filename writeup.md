The car was set up to costant speed of 25 mph, by
putting throttle at costant value of 0.3, unless the
speed gets above 25 mph. This allows to keep speed
almost constant in the simulator.

The only value controlled by PID controller is
steering value.

The PID controller was tuned by hand by first tuning
P coefficient such that wheel movements are "smooth",
and smoothly increase when the car gets out of the middle
of the road. Final value was chosen to be 0.2. The car
ride is visible in P_Tuning.mp4.

Although the car can correct itself, the momentum causes
car to oscillate around center and at some point oscillations
are too big to keep the car on track. To eliminate the oscillations,
I set the D coefficient to 0.6. This allows the car to go through
the curves and drive the whole lap.

During my experiments I noticed that I coefficient is unnecessary and
usually leads to more oscillations. Usually I coefficient is needed
to eliminate steady state error, but it looks like in the simulator
such thing is not present (I checked that keeping steering angle at
0 causes the car to follow a straight line perfectly).
