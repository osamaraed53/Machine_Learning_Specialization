# Multiple linear regression
## Muiltable features (variables)
![alt text](./assets/image11.png)

previously : $f_{w,b}(x) = wx+b$  
now : $f_{w,b}(x) = w_{1}x_{1} + w_{2}x_{2} +w_{3}x_{3} +w_{4}x_{4} +b$   
example :$f_{w,b}(x) = 0.1x_{1} + 4x_{2} + 10x_{3} + -2x_{4} + 80$   
$x_{1} \rArr$ feature 1  
$x_{2}\rArr$ feature 2   
$x_{3}\rArr$ feature 3   
$x_{4}\rArr$ feature 4   
80 is b $\rArr$ base price



Multiple linear regression Notations 
---
$f_{\vec {w},b}(\vec {x}) = w_{1}x_{1} + w_{2}x_{2} + ... +w_{n}x_{n} +b$  
$\vec {w} = [w_{1} w_{2} w_{3} ... w_{n}]$ parameters of the model   
b is a number   
$\vec {x} = [x_{1} x_{2} x_{3} ... x_{n}]$    
  
$f_{\vec {w},b}(\vec {x}) = \vec{w} \cdot \vec{x} + b =  w_{1}x_{1} + w_{2}x_{2} + ... +w_{n}x_{n} +b$    
$\cdot \rArr$ dot product 

>[!Note]
we add arrow up on top(vector) of x and w to signify these list of numbers (vectors)

## Vectorization  
> when you implementing a learning algorithm, using vectorization will both
> 1. make code shorter and also make it run much more efficiently.  
> 2. Take advanttage of modern numerical algebra libraries
> 3. can use GPU when write vesctorized code to help execute code more much quikly
>
> ![alt text](./assets/image12.png)

Previos notaion & Vector notaion 
![alt text](./assets/image13.png)

Gradient descent : One feature & N feature
![alt text](image.png)

## An alternative to gradient descent
### Normal equation 
> it turns out to be possible to use an advanced linear algebra library to just solve for e and b all in one go without iterations.
- only for liner regression   
- Solve for w,b without it iterations
**Disadvantages**
- Doesn't generalize to other learning algorithm.
- Slow when number of features is larger ($> 10,000$)   
**What we need to know** 
- Normal equation method may be used in machine learning libraries that implement linear regression. 
- Gradient descnt is the recommended method for finding parameters w,b.  
**Extra note by Osama**
The **Normal Equation** is a direct mathmematical formula used in linear regression to find the best parameters without using gradient descent. 

Instead of iterating step by step, it gives you the answer in one shot.

we need to find parameters
$$
\theta =
\begin{bmatrix}
b \\
w_1 \\
w_2 \\
\vdots \\
w_n
\end{bmatrix}
$$ 
so that : 
$$
h_\theta(x) = X\theta
$$
Where : 
- X = feature matrix (with a column of 1s for bias)
- $\theta$ (theta) = parameters (weights + bias)
- y = target values
  

  
## Feature scaling

