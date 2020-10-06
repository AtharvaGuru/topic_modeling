# Topic Modeling, from EMR to underlying conditions
This project uses information from electronic medical record (EMR) to generate a prediction of the underlying conditions of the patients
Latent Dirichlet allocation (LDA) was used in the project to generate the topics

* Input: For every patient there is a text file (.txt) with fields extracted from EMR, as well as an annotation file (.ann) with name entities extracted from the text file.  
* Output: The program generates a csv file that listed the dominant topic and keywords from the topic for each patient.  

<table>
  <tr>
    <th>Files</th>
    <th>Notes</th>
  </tr>
  <tr>
    <td>main.py</td>
    <td>Generate topic modeling for a folder of files</td>
  </tr>
  <tr>
    <td>helpers.py</td>
    <td>support functions for main.py</td>
  </tr>
  <tr>
    <td>topic_modeling_explore.ipynb</td>
    <td>Stepwise exploritary analysis to discover the data, EDA, and find the best parameters</td>
  </tr>
</table>
<br>

The text file has a few fields that are good candidates for topic modeling. The following content have been tried for LDA modeling:
* The full text file
* Chief Complaint
* History of Present Illness
* Discharge Diagnosis

Observations: 
* Grid search generated the optimal number of topics being 10. It does not seem to be enough topics to cover the complexity of the data, even though it is algorithmically optimal. 
* In addition, when using the topic keywords are very unspecific. Probably due to the many non-relevant words in a large body of text
