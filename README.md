# Stroke-Prediction-with-COREL-classifier-Using-Synthetic-Data
Stroke Prediction with COREL classifier Using Synthetic Data
<h1>Stroke Prediction with COREL classifier Using
Synthetic Data</h1>


Heart disease and stroke are significant causes of mortality in both men and women in the United
States, with a heart attack occurring approximately every 90 seconds and a stroke claiming a life
every 4 minutes. Swift medical intervention plays a crucial role in preventing many of these deaths
and minimizing permanent bodily damage. Both conditions result from disruptions in blood flow to
the heart or brain, leading to cellular dysfunction and subsequent harmful effects throughout the body.
This research paper aims to address the need for early detection of stroke risk by developing a
Certifiable Optimal Rule ListS (COREL) based classifier. While existing models have demonstrated
high accuracy rates, they suffer from prolonged prediction times. The study will explore the efficacy
of the COREL classifier in constructing an optimal rule list capable of efficiently predicting strokes.
The dataset used for this research exhibits a high level of imbalance, with 209 instances of stroke and
4700 instances of non-stroke cases. Such an imbalance can lead to biased model performance,
reducing predictive accuracy for the minority class. To mitigate this issue, the paper employs
synthetic data generation through the GaussianCopulaSynthesizer, a cutting-edge generative model
that learns the underlying data distribution and creates synthetic samples closely resembling the
original data. Combined with the Coral Classifier, a robust algorithm designed to predict the outcomes
with optimal rule lists, this approach seeks to improve stroke prediction accuracy.

<b>Methods</b>
Due to the significant imbalance in the dataset, we conducted two separate predictions. In the first
approach, we balanced the data by generating synthetic data for the minority class from the original
dataset, using the GaussianCouplaSynthesizer. This synthesizer leverages a combination of classic
statistical methods and GAN-based deep learning techniques to effectively create synthetic data
points.
The second prediction was performed on the balanced dataset. This two-step approach allowed us to
address the challenges posed by imbalanced data and enhance the model's performance, leading to
more accurate predictions in our research study.
The results of synthetic data generation can be seen from the following figure:

</br>

![image](https://github.com/acmax406/Stroke-Prediction-with-COREL-classifier-Using-Synthetic-Data/assets/79563144/2f435381-95ae-47bd-a215-d9e1a8dc90ec)

<br>
Also, the frequency of different variables (synthetic vs Real) can be seen from the following
figure:
</br>

![image](https://github.com/acmax406/Stroke-Prediction-with-COREL-classifier-Using-Synthetic-Data/assets/79563144/0f92f20d-f1a2-4dd7-b26f-899ededc4eb9)
<br>
**Model Used:**
For the data prediction we have use the Certifiable Optimal Rule ListS (COREL) based classifier.
This Model creates rules to predict outcomes, like a decision tree. It uses a tree-like structure to
explore all possible combinations of rules efficiently. It removes rules that don't help much and keeps
track of the best ones. It also avoids redundant rules by using a special trick. This helps CORELS find
accurate rules with fewer calculations, making it faster and better at predicting.

**Results**
For balanced original data points the model predicted approx. 68% accuracy. With the
following rule lists:
</br>
![image](https://github.com/acmax406/Stroke-Prediction-with-COREL-classifier-Using-Synthetic-Data/assets/79563144/77e20ffe-7334-4a3f-a769-9ff9025e851b)
</br>
For the balanced synthetic+original data points model predicted approx. 77.4% accuracy. With
following rule lists.
</br>
![image](https://github.com/acmax406/Stroke-Prediction-with-COREL-classifier-Using-Synthetic-Data/assets/79563144/9aa6df94-08c4-4b27-9fd7-0f3f52d7a888)
</br>
![image](https://github.com/acmax406/Stroke-Prediction-with-COREL-classifier-Using-Synthetic-Data/assets/79563144/6a544624-3f97-49e8-a499-d963df61d3bc)
</br>
**Conclusion**
</br>
The dataset used in this research exhibited a high level of imbalance, not only in terms of the
prediction values but also in various variables, such as gender, work_type, and
smoking_status. To address this issue, we employed a synthesizer to balance the data points.
However, the impact of data balancing on the model's accuracy was not significant. Several
limitations were identified in the model we created. Firstly, the data points were still
imbalanced with respect to gender, work_type, and smoking_status even after applying the
Figure :Real Data Figure :Real data+synthetic data

synthesizer. Additionally, the synthesizer used had an accuracy of only 90% in generating
synthetic data points, leading to the incorporation of some inaccurate information in the
COREL model.

The COREL model itself possesses several limitations that need to be considered. Firstly, its
branch-and-bound nature makes it computationally intensive, particularly with larger datasets
or complex rule antecedents, making the search for the optimal rule list impractical in some
cases. Secondly, the process of transforming continuous data into categorical data might
result in significant information loss, potentially affecting the model's performance.
Moreover, although the COREL model may generate a good rule list based on the training
dataset, its ability to generalize and perform well on unseen data points remains a concern.

Overall, due to the combination of data imbalance and the limitations of the COREL model,
it was not deemed efficient enough for deployment in this research. Further investigations
and improvements are necessary to address these challenges and enhance the model's
performance for real-world applications.




