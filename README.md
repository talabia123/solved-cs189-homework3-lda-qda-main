Download Link: https://assignmentchef.com/product/solved-cs189-homework3-lda-qda-main
<br>
<h1></h1>

This homework consists of coding assignments and math problems. Begin early; you can submit models to Kaggle only twice a day!

DELIVERABLES:

<ol>

 <li>Submit your predictions for the test sets to Kaggle as early as possible. Include your Kaggle scores in your write-up. The Kaggle competition for this assignment can be found at

  <ul>

   <li>MNIST: https://www.kaggle.com/c/spring21-cs189-hw3-mnist</li>

   <li>SPAM: https://www.kaggle.com/c/spring21-cs189-hw3-spam</li>

  </ul></li>

 <li>Write-up: Submit your solution in PDF format to “Homework 3 Write-Up” in Gradescope.

  <ul>

   <li>On the first page of your write-up, please list students with whom you collaborated</li>

   <li>Start each question on a new page. If there are graphs, include those graphs on the same pages as the question write-up. DO NOT put them in an appendix. We need each solution to be self-contained on pages of its own.</li>

   <li>Only PDF uploads to Gradescope will be accepted. You are encouraged use L<sup>A</sup>T<sub>E</sub>X or Word to typeset your solution. You may also scan a neatly handwritten solution to produce the PDF.</li>

   <li>Replicate all your code in an appendix. Begin code for each coding question in a fresh page. Do not put code from multiple questions in the same page. When you upload this PDF on Gradescope, <em>make sure </em>that you assign the relevant pages of your code from appendix to correct questions.</li>

   <li>While collaboration is encouraged, <em>everything </em>in your solution must be your (and only your) creation. Copying the answers or code of another student is strictly forbidden. Furthermore, all external material (i.e., <em>anything </em>outside lectures and assigned readings, including figures and pictures) should be cited properly. We wish to remind you that consequences of academic misconduct are <em>particularly severe</em>!</li>

  </ul></li>

 <li><u>Code</u>: Submit your code as a .zip file to “Homework 3 Code”.

  <ul>

   <li>Set a seed for all pseudo-random numbers generated in your code. This ensures your results are replicated when readers run your code.</li>

   <li>Include a README with your name, student ID, the values of random seed (above) you used, and any instructions for compilation.</li>

   <li>Do NOT provide any data files. Supply instructions on how to add data to your code.</li>

   <li>Code requiring exorbitant memory or execution time might not be considered.</li>

   <li>Code submitted here must match that in the PDF Write-up. The Kaggle score will not be accepted if the code provided a) does not compile or b) compiles but does not produce the file submitted to Kaggle.</li>

  </ul></li>

 <li>The assignment covers concepts on Gaussian distributions and classifiers. Some of the material may not have been covered in lecture; you are responsible for finding resources to understand it.</li>

</ol>

<h1>1          Honor Code</h1>

Declare and sign the following statement (Mac Preview and FoxIt PDF Reader, among others, have tools to let you sign a PDF file):

<em>“I certify that all solutions are entirely my own and that I have not looked at anyone else’s solution. I have given credit to all external sources I consulted.” </em>Signature:

<h1>2          Gaussian Classification</h1>

Let <em>f</em>(<em>x </em>| <em>C<sub>i</sub></em>) ∼ N(µ<em><sub>i</sub></em>,σ<sup>2</sup>) for a two-class, one-dimensional classification problem with classes <em>C</em><sub>1 </sub>and <em>C</em><sub>2</sub>, <em>P</em>(<em>C</em><sub>1</sub>) = <em>P</em>(<em>C</em><sub>2</sub>) = 1/2, and µ<sub>2 </sub>&gt; µ<sub>1</sub>.

<ol>

 <li>Find the Bayes optimal decision boundary and the corresponding Bayes decision rule by finding the point(s) at which the posterior probabilities are equal.</li>

 <li>Suppose the decision boundary for your classifier is <em>x </em>= <em>b</em>. The Bayes error is the probability of misclassification, namely,</li>

</ol>

<em>P<sub>e </sub></em>= <em>P</em>((<em>C</em><sub>1 </sub>misclassified as <em>C</em><sub>2</sub>) ∪ (<em>C</em><sub>2 </sub>misclassified as <em>C</em><sub>1</sub>)).

Show that the Bayes error associated with this decision rule, in terms of <em>b</em>, is

<em>P</em><em>e </em> <em>b </em>exp − µ 2  <em>dx </em>+ Z ∞ exp (<em>x </em>− µ1)2      .



−              

                 <em>dx</em>

<em>b                         </em>2σ2     

<ol start="3">

 <li>Using the expression above for the Bayes error, calculate the optimal decision boundary <em>b</em><sup>∗ </sup>that minimizes <em>P<sub>e</sub></em>(<em>b</em>). How does this value compare to that found in part 1? <em>Hint: P<sub>e</sub></em>(<em>b</em>) <em>is convex for </em>µ<sub>1 </sub>&lt; <em>b </em>&lt; µ<sub>2</sub><em>.</em></li>

</ol>

<h1>3          Isocontours of Normal Distributions</h1>

Let <em>f</em>(µ,Σ) be the probability density function of a normally distributed random variable in R<sup>2</sup>. Write code to plot the isocontours of the following functions, each on its own separate figure. Make sure it is clear which figure belongs to which part. You’re free to use any plotting libraries or stats utilities available in your programming language; for instance, in Python you can use Matplotlib and SciPy.

                11 and Σ = 10 20.

<ol>

 <li><em>f</em>(µ,Σ), where µ =</li>

</ol>

                            −21 and Σ = 21      41.

<ol start="2">

 <li><em>f</em>(µ,Σ), where µ =</li>

</ol>



      0, µ2 = 20 and Σ1 = Σ2 = 21 11.

<ol start="3">

 <li><em>f</em>(µ1,Σ1) − <em>f</em>(µ2,Σ2), where µ1 = </li>

</ol>

2

                                                  0, µ2 = 20, Σ1 = 21    11 and Σ2 = 12   14.

<ol start="4">

 <li><em>f</em>(µ1,Σ1) − <em>f</em>(µ2,Σ2), where µ1 =</li>

</ol>

2

                                                       

1              −1              2   0                   2   1

<ol start="5">

 <li><em>f</em>(µ<sub>1</sub>,Σ<sub>1</sub>) − <em>f</em>(µ<sub>2</sub>,Σ<sub>2</sub>), where µ<sub>1 </sub>= 1, µ2 = −1, Σ1 = 0 1 and Σ2 = 1 2.  </li>

</ol>

<h1>4          Eigenvectors of the Gaussian Covariance Matrix</h1>

Consider two one-dimensional random variables <em>X</em><sub>1 </sub>∼ N(3,9) and <em>X</em> 4), where N(µ,σ<sup>2</sup>) is a Gaussian distribution with mean µ and variance σ<sup>2</sup>. Write a program that draws <em>n </em>= 100 random two-dimensional sample points from (<em>X</em><sub>1</sub>, <em>X</em><sub>2</sub>) such that the <em>i</em>th value sampled from <em>X</em><sub>2 </sub>is calculated based on the <em>i</em>th value sampled from <em>X</em><sub>1</sub>. In your code, make sure to choose and set a fixed random number seed for whatever random number generator you use, so your simulation is reproducible, and document your choice of random number seed and random number generator in your write-up. For each of the following parts, include the corresponding output of your program.

<ul>

 <li>Compute the mean (in R<sup>2</sup>) of the sample.</li>

 <li>Compute the 2 × 2 covariance matrix of the sample.</li>

 <li>Compute the eigenvectors and eigenvalues of this covariance matrix.</li>

 <li>On a two-dimensional grid with a horizonal axis for <em>X</em><sub>1 </sub>with range [−15,15] and a vertical axis for <em>X</em><sub>2 </sub>with range [−15,15], plot

  <ul>

   <li>all <em>n </em>= 100 data points, and</li>

   <li>arrows representing both covariance eigenvectors. The eigenvector arrows should originate at the mean and have magnitudes equal to their corresponding eigenvalues.</li>

  </ul></li>

 <li>Let <em>U </em>= [<em>v</em><sub>1 </sub><em>v</em><sub>2</sub>] be a 2 × 2 matrix whose columns are the eigenvectors of the covariance matrix, where <em>v</em><sub>1 </sub>is the eigenvector with the larger eigenvalue. We use <em>U</em><sup>&gt; </sup>as a rotation matrix to rotate each sample point from the (<em>X</em><sub>1</sub>, <em>X</em><sub>2</sub>) coordinate system to a coordinate system aligned with the eigenvectors. (As <em>U</em><sup>&gt; </sup>= <em>U</em><sup>−1</sup>, the matrix <em>U </em>reverses this rotation, moving back from the eigenvector coordinate system to the original coordinate system). <em>Center </em>your sample points by subtracting the mean µ from each point; then rotate each point by <em>U</em><sup>&gt;</sup>, giving <em>x</em><sub>rotated </sub>= <em>U</em><sup>&gt;</sup>(<em>x </em>− µ). Plot these rotated points on a new two dimensional-grid, again with both axes having range [−15,15].</li>

</ul>

In your plots, clearly label the axes and include a title. Moreover, make sure the horizontal and vertical axis have the same scale! The aspect ratio should be one.

<h1>5          Classification and Risk</h1>

Suppose we have a classification problem with classes labeled 1,…,<em>c </em>and an additional “doubt” category labeled <em>c </em>+ 1. Let <em>r </em>: R<em><sup>d </sup></em>→ {1,…,<em>c </em>+ 1} be a decision rule. Define the loss function

<table width="324">

 <tbody>

  <tr>

   <td width="165">0λ<em>r</em><em>L</em>(<em>r</em>(<em>x</em>) = <em>i</em>,<em>y </em>= <em>j</em>) =λ<em>s</em></td>

   <td width="159">if <em>i </em>= <em>j i</em>, <em>j </em>∈ {1,…,<em>c</em>}, if <em>i </em>= <em>c </em>+ 1,otherwise,</td>

  </tr>

 </tbody>

</table>

where λ<em><sub>r </sub></em>≥ 0 is the loss incurred for choosing doubt and λ<em><sub>s </sub></em>≥ 0 is the loss incurred for making a misclassification. Hence the risk of classifying a new data point <em>x </em>as class <em>i </em>∈ {1,2,…,<em>c </em>+ 1} is

<em>c</em>

X

<em>R</em>(<em>r</em>(<em>x</em>) = <em>i</em>|<em>x</em>) =            <em>L</em>(<em>r</em>(<em>x</em>) = <em>i</em>,<em>y </em>= <em>j</em>) <em>P</em>(<em>Y </em>= <em>j</em>|<em>x</em>).

<em>j</em>=1

<ol>

 <li>Show that the following policy obtains the minimum risk when λ<em><sub>r </sub></em>≤ λ<em><sub>s</sub></em>.</li>

</ol>

(a) Choose class <em>i </em>if <em>P</em>(<em>Y </em>= <em>i</em>|<em>x</em>) ≥ <em>P</em>(<em>Y </em>= <em>j</em>|<em>x</em>) for all <em>j </em>and <em>P</em>(<em>Y </em>= <em>i</em>|<em>x</em>) ≥ 1 − λ<em><sub>r</sub></em>/λ<em><sub>s</sub></em>; (b) Choose doubt otherwise.

<ol start="2">

 <li>What happens if λ<em><sub>r </sub></em>= 0? What happens if λ<em><sub>r </sub></em>&gt; λ<em><sub>s</sub></em>? Explain why this is consistent with what one would expect intuitively.</li>

</ol>

<h1>6          Maximum Likelihood Estimation and Bias</h1>

Let <em>X</em><sub>1</sub>,…, <em>X<sub>n </sub></em>∈ R be <em>n </em>sample points drawn independently from normal distributions such that<sub>√</sub>

<em>X<sub>i </sub></em>∼ N(µ,σ<sup>2</sup><em><sub>i </sub></em>), where σ<em><sub>i </sub></em>= σ/                   <em>i </em>for some parameter σ. (Every sample point comes from a

distribution with a different variance.)

<ul>

 <li>Derive the maximum likelihood estimates, denoted ˆµ and ˆσ, for the mean µ and the parameter σ. You may write an expression for ˆσ<sup>2 </sup>rather than ˆσ if you wish—it’s probably simpler that way. Show all your work.</li>

 <li>Given the true value of a statistic θ and an estimator θˆ of that statistic, we define the <em>bias </em>of the estimator to be the the expected difference from the true value. That is,</li>

</ul>

<em>bias</em>(θˆ) = E[θˆ] − θ.

We say that an estimator is <em>unbiased </em>if its bias is 0.

Either prove or disprove the following statement: <em>The MLE sample estimator </em>µˆ <em>is unbiased</em>. <em>Hint: Neither the true </em>µ <em>nor true </em>σ<sup>2 </sup><em>are known when estimating sample statistics, thus we need to plug in appropriate estimators.</em>

<ol>

 <li>Either prove or disprove the following statement: <em>The MLE sample estimator </em>σ<sup>ˆ2 </sup><em>is unbiased</em>. <em>Hint: Neither the true </em>µ <em>nor true </em>σ<sup>2 </sup><em>are known when estimating sample statistics, thus we need to plug in appropriate estimators.</em></li>

</ol>

<h1>7          Covariance Matrices and Decompositions</h1>

<table width="624">

 <tbody>

  <tr>

   <td colspan="3" width="624">As described in lecture, the covariance matrix Var(<em>R</em>) ∈ R<em><sup>d</sup></em><sup>×<em>d </em></sup>for a random variable <em>R </em>∈ R<em><sup>d </sup></em>with</td>

  </tr>

  <tr>

   <td width="487">mean µ is</td>

   <td width="28"></td>

   <td width="109"></td>

  </tr>

  <tr>

   <td width="487">Var(<em>R</em>) = Cov(<em>R</em>,<em>R</em>) = E[(<em>R </em>− µ)(<em>R </em>− µ)<sup>&gt;</sup>] =<sub></sub><sub></sub><sub></sub><sub> </sub>Cov(Cov(Var(<em>RR</em>…<em>R<sub>d</sub></em><sub>2</sub>,,1<em>RR</em>)<sub>11</sub>))                                                               Cov(Cov(Var(<em>RRR<sub>d</sub></em>1,,<sub>2</sub><em>RR</em>)2<sub>2</sub>))where Cov(<em>R<sub>i</sub></em>,<em>R<sub>j</sub></em>) = E[(<em>R<sub>i </sub></em>− µ<em><sub>i</sub></em>)(<em>R<sub>j </sub></em>− µ<em><sub>j</sub></em>)] and Var(<em>R<sub>i</sub></em>) = Cov(<em>R<sub>i</sub></em>,<em>R<sub>i</sub></em>).</td>

   <td width="28">………</td>

   <td width="109">Cov(<em>R</em><sub>2</sub>,<em>R<sub>d</sub></em>)Cov(<em>R</em>1,<em>R</em><em>d</em>) ,…Var(<em>R<sub>d</sub></em>)</td>

  </tr>

 </tbody>

</table>

If the random variable <em>R </em>is sampled from the multivariate normal distribution N(µ,Σ) with the

PDF

1           −((<em>x</em>−µ)<sup>&gt;</sup>Σ<sup>−1</sup>(<em>x</em>−µ))/2,

<em>f</em>(<em>x</em>) = <em>e</em>

p(2π)<em>d</em>|Σ|

then Var(<em>R</em>) = Σ.

Given <em>n </em>points <em>X</em><sub>1</sub>, <em>X</em><sub>2</sub>,…, <em>X<sub>n </sub></em>sampled from N(µ,Σ), we can estimate Σ with the maximum likelihood estimator

<em>n</em>

ˆ 1 X(<em>X<sub>i </sub></em>− µ)(<em>X<sub>i </sub></em>− µ)<sub>&gt;</sub>, Σ =

<em>n</em>

<em>i</em>=1

which is also known as the covariance matrix of the sample.

<ul>

 <li>The estimate Σˆ makes sense as an approximation of Σ only if Σˆ is invertible. Under what circumstances is Σˆ not invertible? Make sure your answer is complete; i.e., it includes all cases in which the covariance matrix of the sample is singular. Express your answer in terms of the geometric arrangement of the sample points <em>X<sub>i</sub></em>.</li>

 <li>Suggest a way to fix a singular covariance matrix estimator Σˆ by replacing it with a similar but invertible matrix. Your suggestion may be a kludge, but it should not change the covariance matrix too much. Note that infinitesimal numbers do not exist; if your solution uses a very small number, explain how to calculate a number that is sufficiently small for your purposes.</li>

 <li>Consider the normal distribution N(0,Σ) with mean µ = 0. Consider all vectors of length 1; i.e., any vector <em>x </em>for which k<em>x</em>k = 1. Which vector(s) <em>x </em>of length 1 maximizes the PDF <em>f</em>(<em>x</em>)? Which vector(s) <em>x </em>of length 1 minimizes <em>f</em>(<em>x</em>)? Your answers should depend on the properties of Σ. Explain your answer.</li>

</ul>

<h1>8          Gaussian Classifiers for Digits and Spam</h1>

In this problem, you will build classifiers based on Gaussian discriminant analysis. Unlike Homework 1, you are NOT allowed to use any libraries for out-of-the-box classification (e.g. sklearn). You may use anything in numpy and scipy.

The training and test data can be found with this homework. Don’t use the training/test data from Homework 1, as they have changed for this homework. You can verify that your data files and python environment are setup properly by running sanity.py. Submit your predicted class labels for the test data on the Kaggle competition website and be sure to include your Kaggle display name and scores in your writeup. Also be sure to include an appendix of your code at the end of your writeup.

<ol>

 <li>Taking pixel values as features (no new features yet, please), fit a Gaussian distribution to each digit class using maximum likelihood estimation. This involves computing a mean and a covariance matrix for each digit class, as discussed in lecture.</li>

</ol>

<em>Hint: </em>You may, and probably should, contrast-normalize the images before using their pixel values. One way to normalize is to divide the pixel values of an image by the <em>l</em><sub>2</sub>-norm of its pixel values.

<ol start="2">

 <li>(Written answer + graph) Visualize the covariance matrix for a particular class (digit). How do the diagonal terms compare with the off-diagonal terms? What do you conclude from this?</li>

 <li>Classify the digits in the test set on the basis of posterior probabilities with two different approaches. Feel free to either use the starter code provided in starter.py or write your own implementation from scratch

  <ul>

   <li>(Graphs) Linear discriminant analysis (LDA). Model the class conditional probabilities as Gaussians N(µ<sub>C</sub>,Σ) with different means µ<sub>C </sub>(for class C) and the same covariance matrix Σ, which you compute by averaging the 10 covariance matrices from the 10 classes.</li>

  </ul></li>

</ol>

To implement LDA, you will sometimes need to compute a matrix-vector product of the form Σ<sup>−1</sup><em>x </em>for some vector <em>x</em>. You should not compute the inverse of Σ (nor the determinant of Σ) as it is not guaranteed to be invertable. Instead, you should find a way to solve the implied linear system without computing the inverse. <em>Hint: How do we solve OLS when the data matrix is singular?</em>

Hold out 10,000 randomly chosen training points for a validation set (You may reuse your homework 1 solution or an out-of-the-box library for dataset splitting <em>only</em>). Classify each image in the validation set into one of the 10 classes. Compute the error rate (1− # points correctly classified# total points ) on the validation set and plot it over the following numbers of randomly chosen training points: 100, 200, 500, 1,000, 2,000, 5,000, 10,000, 30,000, 50,000. (Expect some variation in your error rate when few training points are used.)

<ul>

 <li>(Graphs) Quadratic discriminant analysis (QDA). Model the class conditional probabilities as Gaussians N(µ<sub>C</sub>,Σ<sub>C</sub>), where Σ<sub>C </sub>is the estimated covariance matrix for class C.</li>

</ul>

(If any of these covariance matrices turn out singular, implement the trick you described in Q7(b). You are welcome to use <em>k</em>-fold cross validation to choose the right constant(s) for that trick.) Repeat the same tests and error rate calculations you did for LDA.

<ul>

 <li>(Written answer) Which of LDA and QDA performed better? Why?</li>

 <li>(Written answer + graph) Include a plot of validation error versus the number of training points for each digit. Plot all the 10 curves on the same graph as shown in Figure 1. Which digit is easiest to classify? Include written answers where indicated.</li>

</ul>

Figure 1: Sample graph with 10 plots

<ol start="4">

 <li>Using the mnistdata.mat, train your best classifier for the trainingdata and classify the images in the testdata. Submit your labels to the online Kaggle competition. Record your optimum prediction rate in your submission. You are welcome to compute extra features for the Kaggle competition, as long as they do not use an exterior learned model for their computation (no transer learning!). If you do so, please describe your implementation in your assignment. Please use extra features only for the Kaggle portion of the assignment.</li>

 <li>Next, apply LDA or QDA (your choice) to spam. Submit your test results to the online Kaggle competition. Record your optimum prediction rate in your submission. If you use additional features (or omit features), please describe them.</li>

</ol>

<em>Optional: </em>If you use the defaults, expect relatively low classification rates. We suggest using a Bag-Of-Words model. You are encouraged to explore alternative hand-crafted features, and are welcome to use any third-party library to implement them, as long as they do not use a separate model for their computation (no word-2-vec!).