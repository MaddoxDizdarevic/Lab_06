# Number Theory: Addition

In this lab you've learned the basics of number theory as it relates to addition.

## Rubric

| Item | Description | Value |
| ---- | ----------- | ----- |
| Summary Answers | Your writings about what you learned in this lab. | 25% |
| Question 1 | Your answers to the question | 25% |
| Question 2 | Your answers to the question | 25% |
| Question 3 | Your answers to the question | 25% |

## Lab Questions

## Lab Summary
In this lab, the main thing we learned was how to implement and a two-bit adder into verilog, along with a single bit and a half-adder. We then implemented that code into the basys board, which demonstrated how the code functions in real life. 

### 1 - How might you add more than two bits together?

We can add more bits together by increasing the amount of full adders. For example, if we wanted to add 2 three-bit numbers together, we would use one full/half adder for the least significant bit, another full adder for the middle significant bit, and another full adder for the most significant bit (with carry outputs from LSB going into middleSB and carry from middleSB going into MSB adder). This scales proportionately, with the amount of bits equaling the amount of full adders. 

### 2 - What is the importance of the XOR gate in an adder?

The importance of an XOR gate is that it handles the Sum part of the adder. For example, in a one bit adder, if A = 1 and B = 0, the XOR gate would output 1, which is the sum of the two inputs. With more bits, more inputs into the xor gate handles the summing portion of the adder, and an AND gate handles the carry portion. 

### 3 - What is the largest number a two bit adder can handle? What happens when you go over?

The largest number a two bit adder can handle is 3 (e.g. A = 11). If we were to add something like A = 11 and B = 10, this would cause the sum to be a 3 bit number, which is overflow for the adder. When this happens, the adder will simply return the wrong value (i.e. if A = 11 and B = 11, then the real value would be 110, but the adder only outputs 10).
