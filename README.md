Download Link: https://assignmentchef.com/product/solved-nctu-cs-assignment-2-decision-tree-random-forest-knn
<br>
<span style="font-size: 2em;">Objective</span>

<ol>

 <li>Data Input –</li>

 <li>Data Preprocessing

  <ul>

   <li>Transform data format and shape so your model can process them.</li>

   <li><strong>Shuffle the data</strong>.</li>

   <li>Transform label format so you can do the required two tasks described below Data section.</li>

  </ul></li>

 <li>Model Construction</li>

</ol>

For all the models, you need to do two tasks described below in the data section.

<ol>

 <li style="list-style-type: none;">

  <ul>

   <li>The data consists of both <strong>categorical</strong> and <strong>numerical</strong> features, and you have to treat them differently.</li>

   <li>Three models must be constructed, <strong>Decision Tree</strong>, <strong>Random Forest</strong>, and <strong>K-Nearest Neighbor</strong>.

    <ol>

     <li>For the Decision Tree model, you may use the following ID3 algorithm pseudocode. – 10%</li>

    </ol></li>

  </ul></li>

</ol>

<ol start="2">

 <li>ID3 (Examples, Target_Attribute, Attributes)     Create a root node for the tree4.      If all examples are positive, Return the single-node tree Root, with label = +.5.      If all examples are negative, Return the single-node tree Root, with label = -.6.      If the number of predicting attributes is empty, then Return the single node tree Root,7.      with label = most common value of the target attribute in the examples.8.      Otherwise Begin9.          A ← The Attribute that best classifies examples.10.         Decision Tree attribute for Root = A.11.         For each possible value, vi, of A,12.             Add a new tree branch below Root, corresponding to the test A = vi.13.             Let Examples(vi) be the subset of examples that have the value vi for A14.             If Examples(vi) is empty15.                 Then below this new branch add a leaf node with label = most common target value in the examples16.             Else below this new branch add the subtree ID3 (Examples(vi), Target_Attribute, Attributes – {A})17.     End18. Return Root</li>

</ol>

Note that you could implement any decision tree algorithm, not restrict to ID3. But you need to clarify which algorithm you used.

<ol>

 <li style="list-style-type: none;">

  <ul>

   <li style="list-style-type: none;">

    <ol>

     <li>For the Random Forest model, you must construct multiple Decision Tree models from randomly selected data (from the training subset) and perform voting for prediction. – 10%

      <ul>

       <li>For the data selection, the following methods are all acceptable. You could choose one to implement.

        <ul>

         <li>Randomly select features</li>

         <li>Randomly select samples</li>

         <li>Both</li>

        </ul></li>

       <li>The number of trees must be greater than or equal to 3. You need to try at least 3 different numbers of trees and compare the result.</li>

       <li>Understand the difference between K-fold cross-validation and Random Forest. <strong>Confuse one with another, and you won’t get this part of the score.</strong></li>

      </ul></li>

     <li>For the KNN model, you need to modify categorical features to calculate distance. And you may need to normalize every feature to let your KNN model work as expected. – 10%

      <ul>

       <li>You need to try at least 3 different K values and compare their results.</li>

      </ul></li>

    </ol></li>

  </ul></li>

 <li>Validation – 5%

  <ul>

   <li>Two validation methods need to be implemented.

    <ol>

     <li><a href="https://en.wikipedia.org/wiki/Cross-validation_(statistics)#Holdout_method">Holdout validation</a> with the ratio <span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mn>7</mn><mo>:</mo><mn>3</mn></math>">7:37:3</span></li>

     <li><a href="https://en.wikipedia.org/wiki/Cross-validation_(statistics)#k-fold_cross-validation">K-fold cross-validation</a> with <span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>K</mi><mo>=</mo><mn>3</mn></math>">K=3K=3</span>

      <ul>

       <li>Obtain the final performance by <strong>averaging</strong> all folds’ performance.</li>

      </ul></li>

    </ol></li>

  </ul></li>

 <li>Results – 10%

  <ul>

   <li>Obtain the performances of all experiment settings <strong>in tables</strong> by the following metrics:

    <ol>

     <li>Confusion matrix</li>

     <li>Accuracy</li>

     <li>Sensitivity(Recall)</li>

     <li>Precision</li>

    </ol></li>

  </ul></li>

 <li>Comparison &amp; Conclusion – 5%

  <ul>

   <li>Also some feedback, anything you want to tell me.</li>

  </ul></li>

 <li>Questions – 40%

  <ul>

   <li>Decision Tree</li>

  </ul></li>

</ol>

<ol>

 <li style="list-style-type: none;">

  <ul>

   <li style="list-style-type: none;">

    <ul>

     <li>Show the <strong>prediction</strong> and <strong>reasoning</strong> of 1-samples in the <strong>validation set</strong>. – 10%</li>

    </ul></li>

   <li>Random Forest

    <ul>

     <li>Describe the difference between <strong>boosting</strong> and <strong>bagging</strong>. – 10%</li>

    </ul></li>

   <li>KNN

    <ul>

     <li>Pick 2 features, draw and describe the <strong>KNN decision boundaries</strong>. – 10%

      <ul>

       <li>You can pick 2 features to re-train the model, or just fix every other feature values.</li>

      </ul></li>

     <li>Show the <strong>prediction</strong> and <strong>reasoning</strong> of 1-samples in the <strong>validation set</strong>. – 10%</li>

    </ul></li>

  </ul></li>

 <li>Finish during class – 20%

  <ul>

   <li>Submit your report and source codes to the newE3 system before class ends.</li>

   <li>Finish time will be determined by the submission time.</li>

  </ul></li>

</ol>

<h2 data-id="Data---Student-Performance-Data-Set">Data – Student Performance Data Set</h2>

<ul>

 <li>Data can be downloaded here:

  <ul>

   <li><a href="https://archive.ics.uci.edu/ml/datasets/Student+Performance">http://archive.ics.uci.edu/ml/datasets/Student+Performance</a></li>

  </ul></li>

 <li>Please <strong>NOTE</strong> that the last column is the label (G3)</li>

 <li>Two datasets provided (Mathematics, Portuguese language) are both acceptable. You could choose one to analyze.</li>

 <li>Followed by <a href="http://www3.dsi.uminho.pt/pcortez/student.pdf">this paper</a>, You will <strong>have to</strong> do 2 classification tasks:

  <ul>

   <li>Binary classification – pass if <span data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mi>G</mi><mn>3</mn><mo>&amp;#x2265;</mo><mn>10</mn></math>">G3≥10G3≥10</span>, else fail</li>

   <li>5-Level classification – based on the Erasmus grad conversion system.</li>

  </ul></li>

</ul>

<table>

 <thead>

  <tr>

   <td><strong>Country</strong></td>

   <td><strong>I (excellent/very good)</strong></td>

   <td><strong>II (good)</strong></td>

   <td><strong>III (satisfactory)</strong></td>

   <td><strong>IV (sufficient)</strong></td>

   <td><strong>V (fail)</strong></td>

  </tr>

 </thead>

 <tbody>

  <tr>

   <td>Portugal/France</td>

   <td>16-20</td>

   <td>14-15</td>

   <td>12-13</td>

   <td>10-11</td>

   <td>0-9</td>

  </tr>

  <tr>

   <td>Ireland</td>

   <td>A</td>

   <td>B</td>

   <td>C</td>

   <td>D</td>

   <td>F</td>

  </tr>

 </tbody>

</table>

<ul>

 <li>Data Set Information

  <ul>

   <li>This data approach student achievement in secondary education of two Portuguese schools. The data attributes include student grades, demographic, social and school related features) and it was collected by using school reports and questionnaires. Two datasets are provided regarding the performance in two distinct subjects: Mathematics (mat) and Portuguese language (por). In [Cortez and Silva, 2008], the two datasets were modeled under binary/five-level classification and regression tasks. Important note: the target attribute G3 has a strong correlation with attributes G2 and G1. This occurs because G3 is the final year grade (issued at the 3rd period), while G1 and G2 correspond to the 1st and 2nd period grades. It is more difficult to predict G3 without G2 and G1, but such prediction is much more useful (see paper source for more details).</li>

  </ul></li>

 <li>Attribute Information</li>

</ul>

<ul>

 <li style="list-style-type: none;">

  <ol>

   <li>school – student’s school (binary: ‘GP’ – Gabriel Pereira or ‘MS’ – Mousinho da Silveira)</li>

   <li>sex – student’s sex (binary: ‘F’ – female or ‘M’ – male)</li>

   <li>age – student’s age (numeric: from 15 to 22)</li>

   <li>address – student’s home address type (binary: ‘U’ – urban or ‘R’ – rural)</li>

   <li>famsize – family size (binary: ‘LE3’ – less or equal to 3 or ‘GT3’ – greater than 3)</li>

   <li>Pstatus – parent’s cohabitation status (binary: ‘T’ – living together or ‘A’ – apart)</li>

   <li>Medu – mother’s education (numeric: 0 – none, 1 – primary education (4th grade), 2 â€“ 5th to 9th grade, 3 â€“ secondary education or 4 â€“ higher education)</li>

   <li>Fedu – father’s education (numeric: 0 – none, 1 – primary education (4th grade), 2 â€“ 5th to 9th grade, 3 â€“ secondary education or 4 â€“ higher education)</li>

   <li>Mjob – mother’s job (nominal: ‘teacher’, ‘health’ care related, civil ‘services’ (e.g. administrative or police), ‘at_home’ or ‘other’)</li>

   <li>Fjob – father’s job (nominal: ‘teacher’, ‘health’ care related, civil ‘services’ (e.g. administrative or police), ‘at_home’ or ‘other’)</li>

   <li>reason – reason to choose this school (nominal: close to ‘home’, school ‘reputation’, ‘course’ preference or ‘other’)</li>

   <li>guardian – student’s guardian (nominal: ‘mother’, ‘father’ or ‘other’)</li>

   <li>traveltime – home to school travel time (numeric: 1 – &lt;15 min., 2 – 15 to 30 min., 3 – 30 min. to 1 hour, or 4 – &gt;1 hour)</li>

   <li>studytime – weekly study time (numeric: 1 – &lt;2 hours, 2 – 2 to 5 hours, 3 – 5 to 10 hours, or 4 – &gt;10 hours)</li>

   <li>failures – number of past class failures (numeric: n if 1&lt;=n&lt;3, else 4)</li>

   <li>schoolsup – extra educational support (binary: yes or no)</li>

   <li>famsup – family educational support (binary: yes or no)</li>

   <li>paid – extra paid classes within the course subject (Math or Portuguese) (binary: yes or no)</li>

   <li>activities – extra-curricular activities (binary: yes or no)</li>

   <li>nursery – attended nursery school (binary: yes or no)</li>

   <li>higher – wants to take higher education (binary: yes or no)</li>

   <li>internet – Internet access at home (binary: yes or no)</li>

   <li>romantic – with a romantic relationship (binary: yes or no)</li>

   <li>famrel – quality of family relationships (numeric: from 1 – very bad to 5 – excellent)</li>

   <li>freetime – free time after school (numeric: from 1 – very low to 5 – very high)</li>

   <li>goout – going out with friends (numeric: from 1 – very low to 5 – very high)</li>

   <li>Dalc – workday alcohol consumption (numeric: from 1 – very low to 5 – very high)</li>

   <li>Walc – weekend alcohol consumption (numeric: from 1 – very low to 5 – very high)</li>

   <li>health – current health status (numeric: from 1 – very bad to 5 – very good)</li>

   <li>absences – number of school absences (numeric: from 0 to 93)</li>

   <li>G1 – first period grade (numeric: from 0 to 20)</li>

   <li>G2 – second period grade (numeric: from 0 to 20)</li>

   <li>G3 – final grade (numeric: from 0 to 20, output target)</li>

  </ol></li>

</ul>