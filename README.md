# Op amp tester

This is a stoopid little op amp tester. This circuit does not do any quantitative tests — you would not use it to determine if an op amp is fake. It just checks basic functionality: Does it amplify a small signal? Put an op amp in one of the sockets, connect power, push the button. If the LEDs light up (all four for quad op amps, two for duals, one for singles) it passes.

This is based on a [blog post](https://tangentsoft.net/elec/opamp-tester.html) by Warren Young. Since I have a bench supply usually set up for ±12 V I got rid of the rail splitter and changed the voltage divider accordingly.

I quadrupled the rest of the circuit to test quad op amps. Then I added sockets for single and dual op amps. The pins on these are just connected to the quad socket, so only one socket should be populated at a time.

I changed the LED resistors to 620R because I can imagine a failure mode in which the op amp puts out +12 V. This will limit LED current to 16.8 mV assuming a forward voltage of 1.6 V. For LEDs with different forward voltage or current limit, adjust these resistors accordingly.

I also added a switch to ground the input, because a good op amp not only should light up the LED when the input is present, it should *not* light it up when the input is absent.



## Build notes

I was out of 13k and 15k resistors when I built this so substituted:

* 12k for 13k
* 11k for 12k
* 12k for 15k
* 1.8k for 2.2k

which works fine.

The Degson pluggable terminal block is what I have on my bench supply wires. Change it if you need to.
