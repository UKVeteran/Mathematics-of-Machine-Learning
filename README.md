<div align="center">
  <h1>Mathematics of Machine Learning</h1>
  <p><strong>Author:</strong> Johar M. Ashfaque</p>
</div>

<br>

<h2>📌 Overview</h2>
<p>This repository provides foundational notes on the mathematics of machine learning. It focuses on statistical learning theory, empirical risk minimization, and several popular algorithms, including decision trees, random forests, and neural networks.</p>
<p>For the complete, detailed notes and equations, please refer to the primary document: <strong>Mathematics_of_Machine_Learning.pdf</strong>.</p>

<hr>

<h2>🗂️ Table of Contents</h2>
<ul>
  <li><strong>1. Introduction</strong></li>
  <li><strong>2. Popular Machine Learning Methods I</strong></li>
  <li><strong>3. Statistical Learning Theory</strong></li>
  <li><strong>4. Computation for Empirical Risk Minimisation</strong></li>
  <li><strong>5. Popular Machine Learning Methods II</strong></li>
</ul>

<hr>

<h2>📖 Section Summaries</h2>

<h3>1. Introduction</h3>
<ul>
  <li>The notes introduce a pair of random variables $(X,Y)\in\mathcal{X}\times\mathcal{Y}$ with a joint distribution $P_{0}$, where $X$ acts as a vector of predictors and $Y$ as an output.</li>
  <li>A measurable function $h:\mathcal{X}\rightarrow\mathcal{Y}$ is used to predict $Y$ from $X$ and is known as a hypothesis.</li>
  <li>In a classification setting, the misclassification error loss function is defined as $l(h(x),y)=\begin{cases}0&if~h(x)=y\\ 1&otherwise.\end{cases}$.</li>
  <li>The Bayes classifier $h_{0}$ minimizes misclassification risk and operates using the condition $\eta(x):=\mathbb{P}(Y=1|X=x)$.</li>
  <li>Empirical risk minimisation seeks to minimize the training error over a hypothesis class using the objective $\hat{R}(h):=\frac{1}{n}\sum_{i=1}^{n}l(h(X_{i}),Y_{i})$.</li>
  <li>The bias-variance tradeoff involves evaluating the conditional risk of an empirical risk minimiser, which breaks down into squared bias, the variance of $\hat{h}$, and irreducible variance.</li>
</ul>

<h3>2. Popular Machine Learning Methods I</h3>
<ul>
  <li><strong>Decision Trees:</strong> Regression trees utilize a set of basis functions made up of indicator functions on rectangular regions. They are computed using a recursive binary partitioning algorithm to minimize the residual sum of squares (RSS).</li>
  <li><strong>Random Forests:</strong> This method attempts to improve the variance of a single tree by sampling the training data with replacement. It constructs new datasets $D_{1}^{*},...,D_{B}^{*}$ and grows a decision tree for each while randomly sampling $m_{try}$ predictors for splits.</li>
</ul>

<h3>3. Statistical Learning Theory</h3>
<ul>
  <li><strong>Hoeffding's Inequality:</strong> Explores sub-Gaussian random variables and provides probability bounds for the sum of independent variables.</li>
  <li><strong>Rademacher Complexity:</strong> The empirical Rademacher complexity for a class of functions $\mathcal{F}$ is defined using i.i.d. Rademacher random variables $\epsilon_{i}$.</li>
  <li><strong>VC Dimension:</strong> The VC dimension for a class of functions $\mathcal{H}$ is defined as the largest integer $n$ such that a set of points is shattered by $\mathcal{H}$. The Sauer-Shelah lemma demonstrates that beyond the VC dimension $d$, the growth of the shattering coefficient becomes polynomial.</li>
</ul>

<h3>4. Computation for Empirical Risk Minimisation</h3>
<ul>
  <li><strong>Convex Surrogates:</strong> Because misclassification loss optimization can be intractable, convex surrogate loss functions like Hinge loss, Exponential loss, and Logistic loss are used.</li>
  <li><strong>Constraint Classes:</strong> Norm constraints, such as $l_{2}$ and $l_{1}$ constraints, are applied to keep Rademacher complexity finite in vector spaces.</li>
  <li><strong>Gradient Descent:</strong> Stochastic Gradient Descent (SGD) evaluates the gradient on a single data point at each step, making it computationally efficient while minimizing a convex function.</li>
</ul>

<h3>5. Popular Machine Learning Methods II</h3>
<ul>
  <li><strong>Adaboost:</strong> This algorithm performs greedy empirical risk minimization over a weighted combination of base classifiers using exponential loss.</li>
  <li><strong>Gradient Boosting:</strong> This method minimizes an empirical risk version by using regression to approximate conditional expectations, updating models by regressing negative residuals.</li>
  <li><strong>Feedforward Neural Networks:</strong> These networks use a specific class of hypotheses with depth $d$ and intermediate layers formulated as $A^{(k)}(v)=\beta^{(k)}v+\mu^{(k)}$. Nonlinear activation functions, such as the rectified linear unit (ReLU) and the sigmoid function, are applied elementwise. Parameters are fitted using stochastic gradient descent and backpropagation.</li>
</ul>
