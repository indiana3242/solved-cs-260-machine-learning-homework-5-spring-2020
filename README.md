Download Link: https://assignmentchef.com/product/solved-cs-260-machine-learning-homework-5-spring-2020
<br>
The following questions are from <em>Understanding Machine Learning: From Theory to Algorithms </em>by Shai Shalev-Shwartz and Shai Ben-David. It can be found here http://www.cs.huji.ac.il/ shais/UnderstandingMachineLearning/ by courtesy of the authors.




In the following two problems, you will implement linear and kernel support vector machine using stochastic gradient descent. Please report your answer of the following questions to Gradescope, and submit your source code to CCLE. Your answer will NOT be graded if we do not see your source code submission on CCLE. Note that, you are allowed to use other programming languages. If so, you need to create an csv data loader and read the data from ./data/*.csv.

<ol start="7">

 <li>(15 Points) Implement the SGD algorithm for solving the optimization problem of Soft-SVM with the objective function</li>

</ol>

(1)

<ul>

 <li>Run the skeleton code, report the training and testing error obtained by the Linear SVM model implemented in scikit-learn.</li>

 <li>Implement SGD algorithm for solving Soft-SVM. Replace line 119-121 of the skeleton code with your implementation.</li>

</ul>

The objective function (Eq. (1)) has been implemented in the function LinearSVM.objective. In this problem, we will keep a running average of updated weights, namely

Plot the objective value <em>J</em>(<strong>w</strong>¯<sup>(<em>t</em>)</sup>) with respect to the number of iterations <em>t </em>during training. Note that, optimal hyperparameter <em>λ </em>(in Eq. 1) and <em>T </em>(SGD maximum number of iterations) may vary with the implementation. Thus, you may need to tune the hyperparameter to reach good performance.

<ul>

 <li>Report the training error and testing error on the dataset with the hyperparameter <em>λ </em>and <em>T </em>you used.</li>

</ul>

<ol start="8">

 <li>(15 Points) Implement the SGD algorithm for solving the Soft-SVM optimization problem with RBF kernel. In this problem, we focus on the objective function of the dual Soft-SVM problem,</li>

</ol>

(2)

where the RBF kernel is defined as

<ul>

 <li>Run the skeleton code, report the training and testing error obtained by the Soft-SVM model with RBF kernel implemented in scikit-learn.</li>

 <li>Implement RBF kernel. That is, given two sets of samples <strong>X </strong>∈ R<em><sup>m</sup></em><sup>1×<em>d </em></sup>and</li>

</ul>

<strong>Y </strong>∈ R<em><sup>m</sup></em><sup>2×<em>d</em></sup>, where <em>d </em>number of dimensions and <em>m</em><sub>1</sub>, <em>m</em><sub>2 </sub>number of samples of <strong>X </strong>and <strong>Y </strong>respectively, the function RBF.__call__ returns a matrix <strong>K </strong>∈ R<em><sup>m</sup></em><sup>1×<em>m</em></sup><sup>2 </sup>with each element). Replace line 49-51 in the skeleton code with your implementation.

<ul>

 <li>Implement SGD algorithm for solving Soft-SVM. Replace line 230-232 of the skeleton code with your implementation.</li>

</ul>

The objective function of dual SVM (Eq. (2)) has been implemented in the function RBFSVM.dual_objective. In this problem, we will keep a running average of the updated alphas,

Plot the objective function of dual SVM Θ(<em>α</em>¯<sup>(<em>t</em>)</sup>) with respect to the number of iterations <em>t </em>during training. Note that, optimal hyperparameter <em>γ</em>(for RBF kernel), <em>T </em>(SGD maximum number of iterations) and <em>λ </em>(in Eq. 1) may vary with the implementation. Thus, you may need to tune the hyperparameter to reach good performance.

<ul>

 <li>Report the training and testing error on the dataset with the hyperparameter <em>γ</em>, <em>T </em>and <em>λ </em>you used.</li>

</ul>