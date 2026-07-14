
module two_bit_comparator(input [1:0]a,b,output gre,equ,less

    );
    wire w0,w1,w2,w3,w4,w5,w6,w7,w8,w9,w10,w11;
    not n1(w0,a[0]);
    not n2(w1,a[1]);
    not n3(w2,b[0]);
    not n4(w3,b[1]);
    and a1_less(w4,w1,w0,b[0]);
    and a2_less(w5,w1,b[1]);
    and a3_less(w6,w0,b[1],b[0]);
    or o1_less(less,w4,w5,w6);
    xnor x1_eq(w7,a[1],b[1]);
    xnor x2_eq(w8,a[0],b[0]);
    and a1_equ(equ,w7,w8);
    and a1_gre(a[0],b[0],w3);
    and a2_gre(a[1],a[0],w2);
    and a3_gre(a[1],w3);
    or o1_gre(gre,w9,w10,w11);
endmodule
