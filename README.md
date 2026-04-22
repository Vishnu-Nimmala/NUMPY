<h1>NumPy Notes</h1>

<h2>What is NumPy?</h2>
<p>
NumPy stands for <b>Numerical Python</b>. It is a core Python library used for working with numerical data.
It helps to create data in the form of dimensions like 1D, 2D, and 3D arrays and also works with already existing dimensional data.
</p>

<h2>Why Use NumPy?</h2>
<ul>
    <li>Handles large data quickly and with less code</li>
    <li>Provides multidimensional arrays and mathematical functions</li>
    <li>Normal Python is slow for heavy calculations</li>
    <li>NumPy is faster and more efficient for large datasets</li>
    <li>Easy to perform mathematical operations</li>
</ul>

<h2>Where is NumPy Used in Real Life?</h2>
<ul>
    <li><b>ML and AI:</b> Handling data and calculations using arrays</li>
    <li><b>Image & Signal Processing:</b> Face recognition, filters, medical imaging</li>
    <li><b>Scientific Computing:</b> Physics simulations, weather forecasting, engineering calculations</li>
    <li><b>Finance:</b> Stock market analysis, risk calculation, algorithmic trading</li>
</ul>

<h2>Built-in Functions (Important 32 Functions)</h2>

<ol>

<li>
<h3>1. array()</h3>
<p>Used to create data in dimensions like 1D, 2D, and 3D.</p>
<pre>
a = np.array([10,20,30,40])
</pre>
</li>

<li>
<h3>2. ndim</h3>
<p>Used to find the number of dimensions in an array.</p>
<pre>
a = np.array([10,11,12,13])
print(a.ndim)
</pre>
</li>

<li>
<h3>3. shape</h3>
<p>Used to find the number of rows and columns.</p>
<pre>
print(a.shape)
</pre>
</li>

<li>
<h3>4. size</h3>
<p>Used to find the total number of elements.</p>
<pre>
print(a.size)
</pre>
</li>

<li>
<h3>5. index</h3>
<p>Used to find the position of an element.</p>
<pre>
print(a[1][2])
</pre>
</li>

<li>
<h3>6. arange()</h3>
<p>Works like range() in loops.</p>
<pre>
a = np.arange(1,81)
</pre>
</li>

<li>
<h3>7. reshape()</h3>
<p>Used to convert 1D to 2D or higher dimensions.</p>
<pre>
a = np.arange(1,81)
b = a.reshape(2,2,2,2,5)
</pre>
</li>

<li>
<h3>8. reshape(-1,1) and reshape(1,-1)</h3>
<p>Used to change 1D to 2D.</p>
<pre>
a = np.arange(1,81)
b = a.reshape(-1,1)
b = a.reshape(1,-1)
</pre>
</li>

<li>
<h3>9. zeros()</h3>
<p>Creates matrix with all zeros.</p>
<pre>
a = np.zeros((5,6), dtype=np.int64)
</pre>
</li>

<li>
<h3>10. ones()</h3>
<p>Creates matrix with all ones.</p>
<pre>
a = np.ones((5,6), dtype=np.int64)
</pre>
</li>

<li>
<h3>11. full()</h3>
<p>Creates matrix with a constant value.</p>
<pre>
a = np.full((5,6), 8)
</pre>
</li>

<li>
<h3>12. ravel()</h3>
<p>Converts any dimension to 1D.</p>
<pre>
b = a.ravel()
</pre>
</li>

<li>
<h3>13. random.randint()</h3>
<p>Generates random integer values.</p>
<pre>
a = np.random.randint(10,50,5)
</pre>
</li>

<li>
<h3>14. random.randn()</h3>
<p>Generates random numbers from normal distribution (-3 to 3 approx).</p>
<pre>
a = np.random.randn(4,4)
</pre>
</li>

<li>
<h3>15. random.rand()</h3>
<p>Generates random values from 0 to 1.</p>
<pre>
a = np.random.rand(4,4,2)
</pre>
</li>

<li>
<h3>16. random.random()</h3>
<p>Same as rand(), gives values from 0 to 1.</p>
<pre>
a = np.random.random((4,4))
</pre>
</li>

<li>
<h3>17. transpose()</h3>
<p>Converts rows into columns and columns into rows.</p>
<pre>
a = np.array([[10,9,8],[7,4,11],[13,1,6]])
b = np.transpose(a)
print(b)
</pre>
</li>

<li>
<h3>18. diagonal()</h3>
<p>Extracts diagonal elements from matrix.</p>
<pre>
arr = np.array([[1,2,3],
                [4,5,6],
                [7,8,9]])

diag = np.diagonal(arr)
print(diag)
</pre>
</li>

<li>
<h3>19. concatenate()</h3>
<p>Joins two or more arrays.</p>
<pre>
a = np.array([[1,2],[3,4]])
b = np.array([[5,6]])

result = np.concatenate((a,b), axis=0)
print(result)
</pre>
</li>

<li>
<h3>20. axis = 0 and axis = 1</h3>
<p>
axis=0 → Column-wise<br>
axis=1 → Row-wise
</p>
</li>

<li>
<h3>21. max()</h3>
<p>Finds highest value in matrix.</p>
<pre>
print(np.max(arr))
</pre>
</li>

<li>
<h3>22. min()</h3>
<p>Finds lowest value in matrix.</p>
<pre>
print(np.min(arr))
</pre>
</li>

<li>
<h3>23. argmax()</h3>
<p>Finds index of highest value.</p>
<pre>
print(np.argmax(arr))
</pre>
</li>

<li>
<h3>24. argmin()</h3>
<p>Finds index of lowest value.</p>
<pre>
print(np.argmin(arr))
</pre>
</li>

<li>
<h3>25. sum()</h3>
<p>Adds all elements or row-wise/column-wise sum.</p>
<pre>
arr = np.array([[1,2],
                [3,4]])

print(np.sum(arr))
print(np.sum(arr, axis=1))
print(np.sum(arr, axis=0))
</pre>
</li>

<li>
<h3>26. Math Functions</h3>
<p>Addition, subtraction, multiplication, division, etc.</p>
<pre>
c = np.add(a,b)
c = np.subtract(a,b)
</pre>
</li>

<li>
<h3>27. matmul()</h3>
<p>Used for matrix multiplication.</p>
<pre>
c = np.matmul(a,b)
</pre>
</li>

<li>
<h3>28. repeat()</h3>
<p>Repeats matrix elements multiple times.</p>
<pre>
a = np.array([[10,9,8],[7,4,11],[13,1,6]])
a = np.repeat(a, 5, axis=1)
</pre>
</li>

<li>
<h3>29. restart function</h3>
<p>Used to run the program again from the beginning.</p>
</li>

<li>
<h3>30. linspace()</h3>
<p>Creates evenly spaced values between two numbers.</p>
<pre>
a = np.linspace(1, 10, 5)
print(a)
</pre>
</li>

<li>
<h3>31. vstack()</h3>
<p>Vertical stack (row-wise joining).</p>
<pre>
a = np.array([1,2,3])
b = np.array([4,5,6])

print(np.vstack((a,b)))
</pre>
</li>

<li>
<h3>32. hstack()</h3>
<p>Horizontal stack (column-wise joining).</p>
<pre>
a = np.array([1,2,3])
b = np.array([4,5,6])

print(np.hstack((a,b)))
</pre>
</li>

</ol>

<h2>Conclusion</h2>
<p>
These are the most important NumPy functions mainly used in Data Science, Machine Learning, and AI development.
Learning these functions makes working with arrays and mathematical operations much easier and faster.
</p>
