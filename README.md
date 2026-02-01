<h1>📊 Multiple Linear Regression (MLR) in Machine Learning</h1>

<h2>1️⃣ What is Multiple Linear Regression?</h2>
<p>
<strong>Multiple Linear Regression</strong> is a <strong>supervised machine learning algorithm</strong>
used to predict a <strong>continuous numeric value</strong> using <strong>more than one input feature</strong>.
</p>

<p>It is an extension of <strong>Simple Linear Regression</strong>.</p>

<ul>
  <li><strong>Simple Linear Regression</strong>: One input feature → One output</li>
  <li><strong>Multiple Linear Regression</strong>: Multiple input features → One output</li>
</ul>

<hr>

<h2>2️⃣ Real-Life Example</h2>
<p>Predicting <strong>house price</strong> based on multiple factors:</p>

<ul>
  <li>Area (sq ft)</li>
  <li>Number of bedrooms</li>
  <li>Number of bathrooms</li>
  <li>Location</li>
  <li>Age of the house</li>
</ul>

<p>
<strong>Input (X)</strong>: Area, Bedrooms, Bathrooms, Location, Age<br>
<strong>Output (Y)</strong>: House Price
</p>

<hr>

<h2>3️⃣ Mathematical Equation</h2>

<h3>Simple Linear Regression</h3>
<p><code>y = mx + c</code></p>

<h3>Multiple Linear Regression</h3>
<p><code>y = b₀ + b₁x₁ + b₂x₂ + b₃x₃ + ... + bₙxₙ</code></p>

<table border="1" cellpadding="8">
  <tr>
    <th>Symbol</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>y</td>
    <td>Predicted output</td>
  </tr>
  <tr>
    <td>b₀</td>
    <td>Intercept</td>
  </tr>
  <tr>
    <td>b₁, b₂, b₃</td>
    <td>Coefficients (weights)</td>
  </tr>
  <tr>
    <td>x₁, x₂, x₃</td>
    <td>Input features</td>
  </tr>
</table>

<hr>

<h2>4️⃣ How Multiple Linear Regression Works</h2>
<ol>
  <li>Initialize coefficients randomly</li>
  <li>Make predictions</li>
  <li>Calculate error (actual − predicted)</li>
  <li>Update coefficients to reduce error</li>
  <li>Repeat until error is minimized</li>
</ol>

<p>Optimization is done using <strong>Gradient Descent</strong> or the <strong>Normal Equation</strong>.</p>

<hr>

<h2>5️⃣ Assumptions of Multiple Linear Regression</h2>
<ul>
  <li>Linearity between input and output</li>
  <li>No multicollinearity among features</li>
  <li>Homoscedasticity (constant variance of errors)</li>
  <li>Errors are normally distributed</li>
  <li>Errors are independent</li>
</ul>

<hr>

<h2>6️⃣ Example Dataset</h2>

<table border="1" cellpadding="8">
  <tr>
    <th>Area</th>
    <th>Bedrooms</th>
    <th>Age</th>
    <th>Price</th>
  </tr>
  <tr>
    <td>1000</td>
    <td>2</td>
    <td>10</td>
    <td>50</td>
  </tr>
  <tr>
    <td>1500</td>
    <td>3</td>
    <td>5</td>
    <td>80</td>
  </tr>
  <tr>
    <td>2000</td>
    <td>4</td>
    <td>2</td>
    <td>120</td>
  </tr>
</table>

<p>
<strong>X</strong>: Area, Bedrooms, Age<br>
<strong>Y</strong>: Price
</p>

<hr>

<h2>7️⃣ Python Implementation</h2>

<h3>Import Libraries</h3>
<pre><code>
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error, r2_score
</code></pre>

<h3>Train the Model</h3>
<pre><code>
model = LinearRegression()
model.fit(X_train, y_train)
</code></pre>

<h3>Evaluate the Model</h3>
<pre><code>
y_pred = model.predict(X_test)
print("MSE:", mean_squared_error(y_test, y_pred))
print("R2 Score:", r2_score(y_test, y_pred))
</code></pre>

<hr>

<h2>8️⃣ Understanding Coefficients</h2>
<pre><code>
print(model.coef_)
print(model.intercept_)
</code></pre>

<p>
Each coefficient shows how much the output changes when that feature increases by one unit.
</p>

<hr>

<h2>9️⃣ Advantages of Multiple Linear Regression</h2>
<ul>
  <li>Simple and fast</li>
  <li>Easy to interpret</li>
  <li>Works well for linear relationships</li>
  <li>Good baseline regression model</li>
</ul>

<hr>

<h2>🔟 Disadvantages of Multiple Linear Regression</h2>
<ul>
  <li>Cannot model non-linear relationships</li>
  <li>Sensitive to outliers</li>
  <li>Affected by multicollinearity</li>
  <li>Strong assumptions must be satisfied</li>
</ul>

<hr>

<h2>1️⃣1️⃣ Simple vs Multiple Linear Regression</h2>

<table border="1" cellpadding="8">
  <tr>
    <th>Feature</th>
    <th>SLR</th>
    <th>MLR</th>
  </tr>
  <tr>
    <td>Number of Inputs</td>
    <td>One</td>
    <td>Multiple</td>
  </tr>
  <tr>
    <td>Complexity</td>
    <td>Low</td>
    <td>Medium</td>
  </tr>
  <tr>
    <td>Accuracy</td>
    <td>Lower</td>
    <td>Higher</td>
  </tr>
</table>

<hr>

<h2>1️⃣2️⃣ When to Use Multiple Linear Regression?</h2>
<ul>
  <li>Output variable is continuous</li>
  <li>Relationship is approximately linear</li>
  <li>Interpretability is important</li>
  <li>Dataset is not highly complex</li>
</ul>

<hr>

