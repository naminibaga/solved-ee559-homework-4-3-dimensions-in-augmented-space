Download Link: https://assignmentchef.com/product/solved-ee559-homework-4-3-dimensions-in-augmented-space
<br>
<ol>

 <li>Code up a 2-class perceptron classifier, for the case of 2 features (3 dimensions in augmented space). As in the previous homework problems, you are expected to code this up yourself rather than use a library or toolbox, so the same guidelines apply.</li>

</ol>

Use basic sequential gradient descent.

<strong>Hint</strong>:  One way to randomly shuffle the data points, is to generate random permutations of numbers from 1 to <em>N</em>, where <em>N</em> = number of training samples.  The result can be used as indices for the data points and their labels.

It is recommended (but not required) that you use augmented space, and reflect the training data.  Do not reflect the test data.

Because the data you will use might not be linearly separable, you will need two halting conditions:

<ul>

 <li>The usual perceptron halting condition: if there have been no updates to <em><u>w</u></em>  in 1 epoch, then halt;</li>

 <li>An ad hoc one in case condition (1) is not satisfied. A reasonable one is to set a maximum number of iterations or epochs (1000 epochs should be high enough), and during the last full epoch, at each iteration <em>i</em>, evaluate <em>J</em>(<em><u>w</u></em>(<em>i</em>)) over all training data</li>

</ul>

<em> </em>

points, and store each <em>J</em>(<em><u>w</u></em>(<em>i</em>)).  Then, after the last iteration, choose the <em><u>w</u></em>(<em>i</em>) that had

<em>       </em>

the smallest criterion value <em>J</em>(<em><u>w</u></em>(<em>i</em>)) .

<em> </em>

For your initial weight vector, use <em><u>w</u></em>(0)= 0.1(<u>1</u>)  (vector of 0.1 in each component).

<em> </em>

For your learning rate parameter, use η(<em>i</em>)=1.

<em> </em>

Run your classifier on 3 datasets:  Synthetic1 (get from HW1 folder), Synthetic2 (also from HW1 folder), and Synthetic3 (from the current HW folder).

<ul>

 <li>For each dataset, report on the final weight vector, the classification error rate on the training set, and the classification error rate on the test set.</li>

 <li>Also for each dataset, give a 2D plot showing decision boundary and regions, as well as training data points (similar to plots of HW1). You may find it convenient to use the PlotDecBoundaries function from HW1 folder.</li>

 <li>For Synthetic1 and Synthetic2 datasets, compare your error rates of part (a) with the error rates obtained in HW1(a); you can compare with the posted solutions if your HW1 answer wasn’t correct. Explain any significant differences between perceptron result and nearest means result.</li>

</ul>




<em>Problem 2 on next page… </em>




<ol>

 <li>1 of 2</li>

 <li>In a gradient descent procedure, let the “weight update” be defined as</li>

</ol>

Δ<em><u>w</u></em>(<em>i</em>)= <em><u>w</u></em>(<em>i</em>+1)− <em><u>w</u></em>(<em>i</em>).

<em> </em>

Consider a given weight vector <em><u>w</u></em><sub>0</sub> which is the weight vector at (given) iteration<em> i</em> , so that <em><u>w</u></em>(<em>i</em>)= <em><u>w</u></em><sub>0</sub>.

<em>N</em>

Let the criterion function take the form <em>J</em>(<em><u>w</u></em>)<sup>=</sup><sup>∑ </sup><em>J </em>(<em><u>w</u></em>) , in which <em><sub> </sub>J<sub>n</sub></em>(<em><u>w</u></em>) is the criterion <em>            <sub>n</sub></em>

function for one data point.  In this problem, do not plug in for the perceptron criterion function; please solve the problem for the general case of <em> J </em>and <em>J<sub>n </sub></em>.  Assume

η(<em>i</em>)=η= constant.

<em> </em>

<ul>

 <li>For stochastic gradient descent, variant 2, find E{Δ<em><u>w</u></em>(<em>i</em>)} , in which E{ } denotes expected value, and for each probabilistic experiment, <em>n</em> is randomly chosen from <sub> </sub><em><sub> </sub></em>{1,2,!,<em>N</em>} with uniform probability.  Try to express your answer in terms of ∇<em><u><sub>w</sub></u>J</em>(<em><u>w</u></em><sub>0</sub>) .</li>

 <li>Compare your result of (a) with Δ<em><u>w</u></em>(<em>i</em>) for batch gradient descent. Describe in words</li>

</ul>

<em> </em>

how the batch GD update compares with the expected value of the stochastic GD  variant 2 update.

Explain why the comparison between these two expressions makes sense, or does not make sense.


