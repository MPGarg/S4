## Assignment Session-3 Part-1

Backpropagation for 3 layer Neural Network is explained in detail below.

Neural network is under consideration as shown below & is assigned with initial weights.
![image](https://user-images.githubusercontent.com/120099863/211860337-40ddc717-28f0-4ae7-8094-5c371e8c1652.png)

Input Nodes:
1. i1
2. i2

Hidden Layer Nodes:
1. h1 = w1\*i1 + w2\*i2
2. h2 = w3\*i1 + w4\*i2

Activation values for Hidden Layer:
1. a_h1 = σ(h1) = 1/(1 + exp(-h1))
2. a_h2 = σ(h2) = 1/(1 + exp(-h2))

Output Layer Nodes:
1. o1 = w5\*a_h1 + w6\*a_h2
2. o2 = w7\*a_h1 + w8\*a_h2

Activation values for Output Layer:
1. a_o1 = σ(o1)
2. a_o2 = σ(o2)

Errors:
1. E1 = (1/2) \* (t1 - a_o1)^2
2. E2 = (1/2) \* (t2 - a_o2)^2
3. E_Total = E1 + E2
