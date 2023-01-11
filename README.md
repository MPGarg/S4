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
1. a_o1 = σ(o1) = 1/(1 + exp(-o1))
2. a_o2 = σ(o2) = 1/(1 + exp(-o2))

Error Calculations:
1. E1 = (1/2) \* (t1 - a_o1)^2
2. E2 = (1/2) \* (t2 - a_o2)^2
3. E_Total = E1 + E2

Backpropagation calcualtions start once we have output and error is calculated.
1. Calculation of derivative for error with respect to w5
       -∂E_total/∂w5 = ∂(E1+E2)/∂w5	
       -As E2 is constant wrt w5 thus only E1 remains
  -∂E_total/∂w5 = ∂E1/∂w5			
  -Simplyfying equation further
∂E_total/∂w5 = ∂E1/∂w5 = ∂E1/∂a_o1\*∂a_o1/∂o1\*∂o1/∂w5			
∂E1/∂a01 = ∂((1/2) * (t1 - a_o1)^2)/∂a_o1 = (a_o1 - t1)			
∂a_o1/∂o1 = ∂(σ(o1))/∂o1 = a_o1 * (1 - a_o1)			
∂o1/∂w5 = a_h1			

