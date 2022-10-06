---
title:Chapter 5 How Computers Calculate -- the ALU
---
# 5.1 ALU
We've learned the numbers can be represented in binary. Representing like 00101010 binary number is 42 in decimal. Representing  and storing numbers is an important function of a computer, but the real goal is computation, or [[manipulating]] numbers in a structured and purposeful way, like adding two numbers together. These operations are handled by a computer’s **Arithmetic and Logic Unit**, but most people call it by its street name: the **ALU**.

The ALU is the mathematical brain of a computer. When you understand an ALU’s design and function, you’ll understand a fundamental part of modern computers. It is THE thing that does all of the computation in a computer, so basically everything uses it. The *Intel 74181* is perhaps the most famous ALU ever, which was released in 1970. It was the first complete ALU that fit entirely inside of a single chip, Which was a huge engineering feat at the time.

We’re going to take those Boolean logic gates we learned before to build a simple ALU circuit with much of the same functionality as the Intel 74181. And over the next few chapters we’ll use this to construct a computer [[from scratch]]. 

An ALU is really two units in one -- there’s an arithmetic unit and a logic unit. Let's start with the arithmetic unit, which is responsible for handling all numerical operations in a computer, like addition and subtraction. It
also does a bunch of other simple things like add 1 to a number, which is called an [[increment]] operation.

---
# 5.2 Arithmetic Unit
## 5.2.1 Half adder
Firstly, we’re going to focus on the operation that [[underlies]] almost everything else a computer does - adding two numbers together. We could build this circuit entirely out of individual transistors, but that would get
confusing really fast. So we can use a high-level of abstraction and build our components out of logic gates, in this case: AND, OR, NOT and XOR gates. 

The simplest adding circuit that we can build takes two binary digits, and adds them together. So we have two inputs, A and B, and one output, which is the sum of those two digits. Just to [[clarify]]: A, B and the output are all single bits. There are only four possible input combinations. The first three are:
0+0 = 0
1+0 = 1
0+1 = 1
Remember that in binary, 1 is the same as true, and 0 is the same as false. So this set of inputs exactly matches the boolean logic of an XOR gate, and we can use it as our 1-bit adder.

But the fourth input combination, 1 + 1,  is a special case. One plus one equals 2 but there’s no 2 digit in binary, so the result is 0 and the 1 is carried to the next column. So the sum is really 10 in binary. Now, the output of our XOR gate is [[partially]] correct : 1 plus 1, outputs 0. But we need an extra output wire for that carry bit. The carry bit is only “true” when the inputs are 1 AND 1, because that's the only time when the result (two) is bigger than 1 bit can store and [[conveniently]] we have a gate for that - An AND gate, which is only true when both inputs are true. (Figure) This circuit is called a **half adder**. Let's abstract away even this level of detail and encapsulate our newly minted half adder as its own component, which has two input bits: A and B  and two outputs: the sum and the carry bits.

## 5.2.2 Full adder
If you want to add more than 1 + 1, we’re going to need a “**Full Adder**.” That half-adder left us with a carry bit as output. That means that when we move on to the next column in a multi-column addition, we are going to have to add three bits together. A full adder takes three bits as inputs: A, B and C. So the maximum possible input is 1 + 1 + 1, which equals 1 carry out 1, so we still only need two output wires: sum and carry.

We can build a full adder using half adders. To do this, we use a half adder to add A plus B just like before – but then feed that result and input C into a second half adder. Lastly, we need a OR gate to check if either one of the carry bits was true. 

We can go up a level of abstraction and wrap up this full adder as its own component. It takes three inputs, adds them, and outputs the sum and the carry.

## 5.2.3 Ripple carry adder
Armed with our new components, we can now build a circuit that takes two, 8-bit numbers – Let’s call them A and B – and adds them together. Let’s start with the very first bit of A and B, which we’ll call A0 and B0. At
this point, there is no carry bit to deal with, because this is our first addition.
So we can use our half adder to add these two bits together. The output is sum0. Now we want to add A1 and B1 together. It's possible there was a carry from the previous addition of A0 and B0, so this time we need to use a full adder that also inputs the carry bit. We output this result as sum1. Then, we take any carry from this full adder, and run it into the next full adder that handles A2 and B2. And we just keep doing this in a big chain until all 8 bits have been added. Notice how the carry bits ripple forward to each subsequent adder. For this reason, this is called an 8-bit **ripple carry adder**. 

Notice how our last full adder has a carry out. If there is a carry into the 9th bit, it means the sum of the two numbers is too large to fit into 8-bits. This is called an [[overflow]]. In general, an overflow occurs when the result of an addition is too large to be represented by the number of bits you are using. This can usually cause errors and unexpected behavior. Famously, the original PacMan arcade game used 8 bits to keep track of what level you were on. This meant that if you made it past level 255 – the largest number storable in 8 bits – to level 256, the ALU overflowed. This caused a bunch of errors and [[glitches]] making the level [[unbeatable]]. The bug became a [[rite]] of passage for the greatest PacMan players. 

So if we want to avoid overflows, we can extend our circuit with more full adders, allowing us to add 16 or 32 bit numbers. This makes overflows less likely to happen, but at the expense of more gates. An additional [[downside]] is that it takes a little bit of time for each of the carries to ripple forward.

## 5.2.4 Other math operations
The ALU’s arithmetic unit also has circuits for other math operations which are built from individual logic gates either. Interestingly, there are no multiply and divide operations. That's because simple ALUs don’t have a circuit for this, and instead just perform a series of additions. Let’s say you want to multiply 12 by 5. That’s the same thing as adding 12 to itself 5 times. However, [[fancier]] processors, like those in your laptop or smartphone, have arithmetic units with [[dedicated]] circuits for multiplication.


---
# 5.3 Logic Unit
Let’s move on to the other half of the ALU: **the Logic Unit**. Instead of arithmetic operations, the Logic Unit performs logical operations, like AND, OR and NOT, which talked about previously.

It also performs simple numerical tests, like checking if a number is negative. For example, here’s a circuit that tests if the output of the ALU is zero. It does this using a bunch of OR gates to see if any of the bits are 1. Even if one single bit is 1, we know the number can’t be zero and then we use a final NOT gate to [[flip]] this input so the output is 1 only if the input number is 0.

The Intel 74181, unlike the 8-bit ALU we made today, could only handle 4-bit inputs. It used about 70 logic gates, and it couldn’t multiply or divide. But it was a huge step forward in [[miniaturization]], opening the doors to more capable and less expensive computers.

This 4-bit ALU circuit is already a lot to take in, but our 8-bit ALU would require hundreds of logic gates to fully build and engineers don’t want to see all that complexity when using an ALU, so they came up with a special symbol to wrap it all up, which looks like a big ‘V’. 

The 8-bit ALU has two inputs, A and B, each with 8 bits. We also need a way to specify what operation the ALU should perform, for example, addition or subtraction. For that, we use a 4-bit operation code which tells the ALU what operation to perform. Such as *1000* might be the command to add, while *1100* is the command for subtract. And the result of that operation on inputs A and B is an 8-bit output.

ALUs also output a series of **Flags**, which are 1-bit outputs for particular [[states]] and [[statuses]]. For example, if we subtract two numbers, and the result is 0, our zero-testing circuit, the one we made earlier, sets the **Zero Flag** to True (1). This is useful if we are trying to determine if two numbers are equal. If we wanted to test if A was less than B, we can use the ALU to calculate A subtract B and look to see if the **Negative Flag** was set to true. If it was, we know that A was smaller than B. There’s also a wire attached to the carry out on the adder we built, so if there is an overflow, we’ll know about it. This is called the **Overflow Flag**.

So now you know how your computer does all its basic mathematical operations digitally with no gears or levers required. We’re going to use this ALU when construct our CPU from now on. But before that, our computer is going to need some memory.

