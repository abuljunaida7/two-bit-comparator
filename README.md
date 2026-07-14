# two-bit-comparator
implementation of two bit comparator
To make a two bit comparator, we need to use combinational circuit.
the logic gates that we are using in this circuit are NOT,AND,OR, and XNOR.
the two bit comparator compares two bit inputs, it has 16 cobinations of inputs.
the logical expression for the circuit is, a<b : a1-bar.a0_bar.b0 + a1_bar.b1 + a0_bar.b1.b0,  a=b : (a1 xnor b1).(a0 xnor b0), a>b : a0.b1_bar.b0 + a1.a0.b0_bar + a1.b1_bar.
