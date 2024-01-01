# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167910294-bb550548-b1dc-4cba-9044-31d9037d476b.png)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167910648-ced88e69-869c-42e2-9718-a285a3902446.png)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167908180-5fc9d589-1cb5-41f5-b2c8-927e04f5f387.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167908214-25b30a54-db20-4bcb-9385-5f93a1982a09.png)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![image](https://user-images.githubusercontent.com/36288975/167910378-d2d984a7-2815-4d17-8c41-ee4bdf59ec24.png) 

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167908575-59c35afb-50d3-46a2-888c-47478a3179d5.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/167908688-fa93c3e9-8323-4864-947d-c11d163d5a90.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
/* write all the steps invloved */
1.Using nand gates and wires construct SR flip flop.

2.Repeat same steps to construct JK,D,T flipflops.

3.Find RTL logic and timing diagram for all flipflops.



### PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: Hariprasath
RegisterNumber: 23001071 
*/
### PROGRAM 
# SR FlipFlop:
![WhatsApp Image 2023-12-29 at 23 17 08_fdf61b0e](https://github.com/23004027/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138956447/404e1da2-c01a-4c3f-85df-940e374770d3)

# JK FlipFlop:
![WhatsApp Image 2023-12-29 at 23 17 04_542eec8b](https://github.com/23004027/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138956447/72de04de-af22-4494-9da9-e877e9f6fdcb)

# D FlipFlop:
![WhatsApp Image 2023-12-29 at 23 17 04_2f126dbf](https://github.com/23004027/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138956447/ea2161bb-32f5-4242-806d-374157eb776f)

# T FlipFlop:
![WhatsApp Image 2023-12-29 at 23 17 04_8c3e85f7](https://github.com/23004027/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138956447/fb33df13-cfde-410c-a1a1-ead2573e5218)

### RTL LOGIC FOR FLIPFLOPS:
# SR FlipFlop:
![WhatsApp Image 2023-12-29 at 23 17 04_8ab27606](https://github.com/23004027/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138956447/f9fdd09f-9c75-463b-9a36-3f9b378c5464)

# JK FlipFlop:
![WhatsApp Image 2023-12-29 at 23 17 00_b7cf0298](https://github.com/23004027/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138956447/a48b0151-61e2-40c3-9f08-5b18cd2b03f4)

# D FlipFlop:
![WhatsApp Image 2023-12-29 at 23 17 05_2b9bbd5c](https://github.com/23004027/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138956447/6ce580fa-a3bd-4085-96ab-b00eb9d034f1)

# T FlipFlop:
![WhatsApp Image 2023-12-29 at 23 17 03_7555070e](https://github.com/23004027/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138956447/bd780169-8e66-4fa5-b8b0-f949525dfcb0)

### TRUTH TABLE:
# SR FlipFlop:
![WhatsApp Image 2023-12-29 at 23 17 06_b598f48c](https://github.com/23004027/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138956447/159a318f-b141-45d5-b1e9-ddd1a675e599)

# JK FlipFlop:
![WhatsApp Image 2023-12-29 at 23 17 06_b56e8e5a](https://github.com/23004027/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138956447/e66d1f92-b06c-4dc7-8099-eca580c20cf8)

# D FlipFlop:
![WhatsApp Image 2023-12-29 at 23 17 07_bdaffaf9](https://github.com/23004027/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138956447/f5ae06f9-ff5d-415f-b511-0a1dc924497c)

# T FlipFlop:
![WhatsApp Image 2023-12-29 at 23 17 07_ca698933](https://github.com/23004027/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138956447/3d6c8ed4-a73c-46e5-a54c-9aa5c5352c45)

### OUTPUT:
# SR FlipFlop:
![WhatsApp Image 2023-12-29 at 23 17 07_31eaefea](https://github.com/23004027/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138956447/b7999346-73cf-4cee-803f-e72ddecf7f05)

# JK FlipFlop:
![WhatsApp Image 2023-12-29 at 23 17 06_deee468c](https://github.com/23004027/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138956447/bcc24143-219d-47f6-9d11-30ddadeb0dcf)

# D FlipFlop:
![WhatsApp Image 2023-12-29 at 23 17 07_90866cca](https://github.com/23004027/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138956447/0dd302c2-3653-46e9-94e9-312c8b69e0d4)

# T FlipFlop:
![WhatsApp Image 2023-12-29 at 23 17 07_1abf3e4e](https://github.com/23004027/Experiment--05-Implementation-of-flipflops-using-verilog/assets/138956447/dfd659ee-21f3-4ca0-b242-393457dde136)

### RESULTS :
Thus, the implementation of SR,JK,D and T flipflops using nand gates are done sucessfully.


















### RESULTS 
