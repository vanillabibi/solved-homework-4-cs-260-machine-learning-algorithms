Download Link: https://assignmentchef.com/product/solved-homework-4-cs-260-machine-learning-algorithms
<br>
<h1>1           Linear Regression with Heterogenous Noise</h1>

In the standard linear regression model, we consider the model that the observed response variable <em>y </em>is the prediction perturbed by noise, namely

<em>y </em>= <strong>x</strong><sup>&gt; </sup>+ <em>“</em>

where <em>” </em>is a Gaussian random variable with mean 0 and variance <sup>2</sup>. Notably, we are assuming that for all observations in the training data, the corresponding noises are identically and independently distributed. In other words, for the <em>n</em>-th observation <strong>x</strong><em><sub>n</sub></em>, the observed response is

where <em>“<sub>n </sub></em>⇠N(0<em>, </em><sup>2</sup>).

This assumption is not applicable in some cases. For example, in the example of predicting the sale prices of houses, the variances for larger houses (e.g., houses with larger <strong>x</strong><em><sub>n </sub></em>which is the square footage) tend to be bigger, as the sale prices for larger houses seem to be more variable. In this case, we can model the data in the following way:

where <em>“<sub>n </sub></em>are independently distributed but <strong>do not have to be identically distributed</strong>. In particular, each one could have a di↵erent variance, namely, <em>“<sub>n </sub></em>⇠N(0<em>, <sub>n</sub></em><sup>2</sup>).

<ul>

 <li>Suppose our training dataset contains {(<strong>x</strong><em><sub>n</sub>,y<sub>n</sub></em>)<em>,n </em>= 1<em>,</em>2<em>,…,N</em>} such observations. Write down the log-likelihood function of the data. This function should be a function of the data as well as and all <em>n</em>.</li>

 <li>Derive the maximum likelihood estimate of , and express it in terms of the data as well as all the              <em><sub>n</sub></em>.</li>

</ul>

You should assume        <em><sub>n </sub></em>is known to you — you do not need to estimate them from the data.

<h1>2           Linear Regression with Smooth Coe          cients</h1>

Consider a dataset with <em>n </em>data points (<strong>x</strong><em><sub>i</sub>,y<sub>i</sub></em>), <strong>x</strong><em><sub>i </sub></em>2R<em><sup>p</sup></em><sup>⇥1</sup>, drawn from the following linear model:

<em>y </em>= <strong>x</strong><sup>&gt; </sup>+ <em>“,</em>

where <em>” </em>is a Gaussian noise. Suppose the features <em>x<sub>i</sub></em><sub>1</sub><em>,…,x<sub>ip </sub></em>for all <em>i </em>= 1<em>,…,n </em>have a natural ordering. Several examples have this ordering property; for example in the study of the impact of proteins on certain types of cancer, the proteins are ordered sequentially on a line. Intuitively, we can encode the natural ordering information by introducing a condition that requires the di↵erence ( <em><sub>i i</sub></em><sub>+1</sub>)<sup>2 </sup>cannot be large, for <em>i </em>= 1<em>,…,p </em>1.

1

<ul>

 <li>State the condition as a regularizer. Write the new optimization problem for finding by combining both this regularization and <em>L</em><sub>2 </sub> (10 points)</li>

 <li>Find the optimal by solving the problem in part (a). (5 points)</li>

</ul>

<h1>3           Linearly Constrained Linear Regression</h1>

Consider a dataset with <em>n </em>data points (<strong>x</strong><em><sub>i</sub>,y<sub>i</sub></em>), <strong>x</strong><em><sub>i </sub></em>2R<em><sup>p</sup></em><sup>⇥1</sup>, drawn from the following linear model:

<em>y </em>= <strong>x</strong><sup>&gt; </sup>+ <em>“,</em>

where <em>” </em>is Gaussian noise. Suppose we have additional information about that requires <em>A </em>= <strong>b </strong>where <em>A </em>2 R<em><sup>q</sup></em><sup>⇥<em>p </em></sup>and <strong>b </strong>2 R<em><sup>q</sup></em><sup>⇥1</sup>. Suppose the constraint <em>A </em>= <strong>b </strong>has a non-empty set of solutions; thus the optimization has feasible solutions. Find the maximum likelihood estimation of under this constraint.

<h1>4           Online Learning</h1>

The perceptron algorithm often makes harsh updates, as it is strongly biased towards the current mistakenlylabeled sample. Suppose at the <em>i</em>th step, the classifier is <strong>w</strong><em><sub>i </sub></em>and we want to make a more conservative update based on observation of (<strong>x</strong><em><sub>i</sub>,y<sub>i</sub></em>) to a new classifier <strong>w</strong><em><sub>i</sub></em><sub>+1</sub>. Derive a new update method for the perceptron such that it makes the smallest di↵erence from the previous model, that is, it minimizes k<strong>w</strong><em><sub>i</sub></em><sub>+1 </sub><strong>w</strong><em><sub>i</sub></em>k2 while ensuring that <strong>w</strong><em><sub>i</sub></em><sub>+1 </sub>classifies the current sample correctly. You need to provide the closed form analytical equation for the update rule.


