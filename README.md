# -binary-classifier-using-logistic-regression
The sigmoid function is the core of logistic regression, used to convert raw input (a linear combination of features) into a probability between 0 and 1.

📐 Sigmoid Function Formula:
𝜎(𝑧)=1/1+𝑒−𝑧
σ(z)= 1+e−z 1
Where:
𝑧=𝑤0+𝑤1𝑥1+𝑤2𝑥2+⋯+𝑤𝑛𝑥𝑛
z=w0+w1x1+w2x2+⋯+wnxn
e is Euler’s number (~2.718)

🧠 What It Does:
Takes any real number 
𝑧∈(−∞,∞)
Compresses it into a value 
∈(0,1)

This value represents the probability of belonging to class 1.
📈 Sigmoid Curve
The curve is S-shaped, and:

For large negative 
z,𝜎(𝑧)→0

For large positive 
z, 𝜎(𝑧)→1
At 𝑧=0
z=0, 
𝜎(0)=0.5
This is why:
If output ≥ 0.5 → class 1
If output < 0.5 → class 0
Example:
Suppose:
𝑧=2
Then:
𝜎(2)=1/1+𝑒−2≈1/1+0.1353≈0.88
σ(2)=1+e−2
1≈ 1+0.1353
1≈0.88
That means there's an 88% probability of the instance belonging to class 1.

In Logistic Regression:
z = np.dot(weights, inputs) + bias
prob = sigmoid(z)
