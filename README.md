# CS308-Assignment-2
# Part 1
## 1. Complete the following addition problem in hexadecimal: 32154AAAA + FEDCBA092. Show the answer in hexadecimal and in decimal.
```
Each Hexadecimal "digit" can be represented by 4 bits.

0x32154AAAA = 0011 0010 0001 0101 0100 1010 1010 1010 1010
0xFEDCBA092 = 1111 1110 1101 1100 1011 1010 0000 1001 0010

1 1111 11     11 1 11 1111   1     1       1   
  0011 0010 0001 0101 0100 1010 1010 1010 1010
+ 1111 1110 1101 1100 1011 1010 0000 1001 0010
----------------------------------------------
1 0011 0000 1111 0010 0000 0100 1011 0011 1100 

The result is:
0001 0011 0000 1111 0010 0000 0100 1011 0011 1100

Converted back into hex:
0x130F204B3C

To convert into decimals, one way to do it is by multiplying each hex digit by 16, raised to the power of its position in the number. Starting from the right:
(12*16^0)+(3*16^1)+(11*16^2)+(4*16^3)+(0*16^4)+(2*16^5)+(15*16^6)+(0*16^7)+(3*16^8)+(1*16^9)
12+48+2,816+16,384+0+2,097,152+251,658,240+0+12,884,901,888+68,719,476,736
81,858,153,276
```

## 2. Convert the Decimal number 4048891811 to hexadecimal.
```
To convert from Decimal to Binary, we divide by 2, noting the quotient as an integer and the remainder. We repeat for each quotient until 0. The remainders will form the final binary number.

4,048,891,811 / 2 = 2,024,445,905 % 1
2,024,445,905 / 2 = 1,012,222,952 % 1
1,012,222,952 / 2 = 506,111,476   % 0
506,111,476 / 2   = 253,055,738   % 0
253,055,738 / 2   = 126,527,869   % 0
126,527,869 / 2   = 63,263,934    % 1
63,263,934 / 2    = 31,631,967    % 0
31,631,967 / 2    = 15,815,983    % 1
15,815,983 / 2    = 7,907,991     % 1
7,907,991 / 2     = 3,953,995     % 1
3,953,995 / 2     = 1,976,997     % 1
1,976,997 / 2     = 988,498       % 1
988,498 / 2       = 494,249       % 0
494,249 / 2       = 247,124       % 1
247,124 / 2       = 123,562       % 0
123,562 / 2       = 61,781        % 0
61,781 / 2        = 30,890        % 1
30,890 / 2        = 15,445        % 0
15,445 / 2        = 7,722         % 1
7,722 / 2         = 3,861         % 0
3,861 / 2         = 1,930         % 1
1,930 / 2         = 965           % 0
965 / 2           = 482           % 1
482 / 2           = 241           % 0
241 / 2           = 120           % 1
120 / 2           = 60            % 0
60 / 2            = 30            % 0
30 / 2            = 15            % 0
15 / 2            = 7             % 1
7 / 2             = 3             % 1
3 / 2             = 1             % 1
1 / 2             = 0             % 1

Now we assemble the remainders in reverse order and we obtain the binary equivalent:
1111 0001 0101 0101 0010 1111 1010 0011
```

## 3. Convert the Octal number 2114112 to Decimal.
```
To convert an octal number to decimal we first convert to binary groups of 3 bits:
0o2114112
010 001 001 100 001 001 010

Once in binary format, we can now convert to decimal by multiplying each bit by 2 raised to the power of its position:
1000 1001 1000 0100 1010
(0*2^0)+(1*2^1)+(0*2^2)+(1*2^3)+(0*2^4)+(0*2^5)+(0*2^6)+(1*2^7)+(0*2^8)+(0*2^9)+(0*2^10)+(0*2^11)+(1*2^12)+(0*2^13)+(0*2^14)+(1*2^15)+(0*2^16)+(0*2^17)+(0*2^18)+(1*2^19)
(0)+(2)+(0)+(8)+(0)+(0)+(0)+(128)+(0)+(0)+(0)+(0)+(4096)+(0)+(0)+(32768)+(0)+(0)+(0)+(524288)

The result is:
563,274
```

## 4. Expand the following table to include decimal numbers from 11 to 16, and expand the table to include hexadecimal numbers.

| Binary | Octal | Decimal | Hexadecimal |
| ------ | ----- | ------- | ----------- |
| 000    | 0     | 0       | 0           |
| 001    | 1     | 1       | 1           |
| 010    | 2     | 2       | 2           |
| 011    | 3     | 3       | 3           |
| 100    | 4     | 4       | 4           |
| 101    | 5     | 5       | 5           |
| 110    | 6     | 6       | 6           |
| 111    | 7     | 7       | 7           |
| 1000   | 10    | 8       | 8           |
| 1001   | 11    | 9       | 9           |
| 1010   | 12    | 10      | A           |
| 1011   | 13    | 11      | B           |
| 1100   | 14    | 12      | C           |
| 1101   | 15    | 13      | D           |
| 1110   | 16    | 14      | E           |
| 1111   | 17    | 15      | F           |
| 10000  | 20    | 16      | 10          |

# Part 2
## NAND
$$x = \overline{A\cdot B}$$

| A   | B   | x   |
| --- | --- | --- |
| 0   | 0   | 1   |
| 0   | 1   | 1   |
| 1   | 0   | 1   |
| 1   | 1   | 0   |
## NOR
$$x = \overline{A + B}$$

| A   | B   | x   |
| --- | --- | --- |
| 0   | 0   | 1   |
| 0   | 1   | 0   |
| 1   | 0   | 0   |
| 1   | 1   | 0   |
## XOR
$$x = (A\cdot \overline{B}) + (\overline{A}\cdot B) $$

| A   | B   | x   |
| --- | --- | --- |
| 0   | 0   | 0   |
| 0   | 1   | 1   |
| 1   | 0   | 1   |
| 1   | 1   | 0   |
## NOT
$$x = \overline{A}$$

| A   | x   |
| --- | --- |
| 0   | 1   |
| 1   | 0   |
## 3-input AND
$$x = A \cdot B \cdot C$$

| A   | B   | C   | x   |
| --- | --- | --- | --- |
| 0   | 0   | 0   | 0   |
| 0   | 0   | 1   | 0   |
| 0   | 1   | 0   | 0   |
| 0   | 1   | 1   | 0   |
| 1   | 0   | 0   | 0   |
| 1   | 0   | 1   | 0   |
| 1   | 1   | 0   | 0   |
| 1   | 1   | 1   | 1   |
# Part 3 Reflexion
### What are fixed-point numbers?
It is a method to represent fractional numbers by providing a part to store the fractional part of the number, after a point that is fixed in its position inside the whole number.
### What is the difference with floating point?
A floating point number achieves essentially the same purpose as a fixed-point, but with a point that can be modified in its position inside the number, enabling more flexibility in representing either bigger numbers with a smaller fractional part, or smaller numbers with a bigger fractional part. It is worth noting that floating point manipulation involves more effort than fixed point.
### What are the practical uses?
Due to using less resources and being faster, fixed-point number manipulation is better suited for small devices like microcontrollers where speed and memory is limited.

> “Fixed-point is ideal for real-time systems with limited speed and memory.”
> — Lyons, R. G. (2010). _Understanding Digital Signal Processing_

Another importance of fixed-point is the consistency that is achieved versus floating-point, since all the numbers are represented in a consistent and repeatable manner.

> “Predictable math makes fixed-point better for real-time safety-critical systems.”
> — Sundararajan, V. (2009). _Fixed-Point Signal Processing_

Importance specifically in the study of fixed-point numbers combines the previously discussed advantages with an understanding of low-level logic and how the hardware handles data in the context of math with the use of overflow, rounding and precision.

> “Fixed-point is key to learning how computers handle data at the lowest level.”
> — Harris, D. M., & Harris, S. L. (2012). _Digital Design and Computer Architecture_
### Conclusion
In conclusion, studying how to manipulate fixed-point numbers enables one to understand and implement faster, more efficient, safer, and better systems.