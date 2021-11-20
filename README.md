clear;
clc;

q0=90;
q1= 20;
q2= 15;
q3 = 5;
q4 = 0;
L0 = 39.44;
L1 = 101.7;
L2 = 101.7;
L3 = 46.7; 


Rz=[ cos(q0) -sin(q0) 0 0;
     sin(q0) cos(q0)  0 0;
     0       0        1 0;
     0       0        0 1];

Lz=[1 0 0 0;
    0 1 0 0;
    0 0 1 L0;
    0 0 0 1];
 

Ry=[cos(q1) 0 sin(q1)  0;
    0       1    0     0;
   -sin(q1) 0 cos(q1)  0;
    0       0    0     1];

Lz=[1 0 0 0;
    0 1 0 0;
    0 0 1 L1;
    0 0 0 1];
 
Ry=[cos(q2) 0 sin(q2)  0;
    0       1    0     0;
   -sin(q2) 0 cos(q2)  0;
    0       0    0     1];

Lx=[1 0 0 L2;
    0 1 0 0;
    0 0 1 0;
    0 0 0 1];

Ry=[cos(q3) 0 sin(q3)  0;
    0       1    0     0;
   -sin(q3) 0 cos(q3)  0;
    0       0    0     1];

Lx=[1 0 0 L3;
    0 1 0 0;
    0 0 1 0;
    0 0 0 1];

Rx=[1    0      0      0;
    0 cos(q4) -sin(q4) 0;
    0 sin(q4) cos(q4)  0;
    0    0      0      1];

H=Rz*Lz*Ry*Lz*Ry*Lx*Ry*Lx*Rx




