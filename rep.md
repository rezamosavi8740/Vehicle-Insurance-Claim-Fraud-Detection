**VEHICLE INSURANCE CLAIM FRAUD DETECTION**

Reza Mosavi ,400222100

*Abstract*

Insurance companies have many problems today. One of the big problems of these companies today is detecting the fraud of insurance holders. In this dataset, the aim is to detectfraudincarinsurancethathashadanaccident.Vehicle insurancefraudinvolvesconspiringtomakefalseorexagger- ated claims involving property damage or personal injuries following an accident. Some common examples include staged accidents where fraudsters deliberately “arrange” for accidents to occur; the use of phantom passengers where people who were not even at the scene of the accident claim to have sufferedgrievous injury, and make false personal in- jury claims where personal injuries are grossly exaggerated. In this exercise, we tried to identify fraudsters with the help of machine learning methods and classificationalgorithms.

*Introduction*

We work with 33 features when working with this dataset. To implement machine learning models for data classifica- tion based on the FraudFoundP feature, we use the sklearn library in the Python programming language. The problems we face before implementing the algorithms

- Data imbalance
- Existence of incorrect values in the data

After examining these challenges, we have to encode cat- egorical data. After the finalpreparation, we start training these models:

- Logistic Regression
- Support Vector Machine
- Decision Tree
- Random Forest
- KNN
- GradientBoosting

Aftertrainingthesemodels,westarttoimprovetheresults of some models For example, we use the GridSearchCV algorithm or I create over-fittingmodels. .

Table 1: Margin Specifications



|**Margin A4 Paper US Letter Paper**|
| - |
|Top 37mm (1.46in) 0.75in (19mm) Bottom 19mm (0.75in) 0.75in (19mm) Left 20mm (0.79in) 0.79in (20mm) Right 20mm (0.79in) 1.02in (26mm)|

**METHODOLOGIES**

*Data Analysis*

first,fordataanalysisweshouldreaddescriptionofdataset and know features and target of dataset in detail.

**Checking Numerical Features :**  We have 9 numerical features in our dataset First, we draw the histogram of these data.

![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.001.png)

Figure 1: numerical features , It is quickly visible that there are incorrect values in Age.

It can be seen that the Age column has an incorrect value of 0. PolicyNumber has no effectbecause it is like an index and is just a number. The value in different DriverRating classes is almost the same. In the year column, we generally work with 3 differentyears. Most of the accidents occurred in the middle of the month. Most of the age signs are about 30 years old.

Now, in particular, we check the age chart and its distri- bution chart based on the value whose ages are recorded as zero before drawing the chart.

![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.002.png)

Figure2: Itcan beseenthat mostofthe accidentsare around the age of 30 and FraudFoundP is more positive around the age of 30.

Now we are going to check the Fraud Found P feature. This feature is the feature based on which we want to do the classification.

![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.003.png)

Figure 3: It can be seen quickly that the data is not balanced

In the following, I will try to balance the data in different ways. Finally, since the Policy Number feature has no effect, we will remove this feature and then correct the incorrect values of some values.

**Examining the features of categorical :**  Now to check thefeaturecategoricalForthispurpose,wedrawtheirgraphs based on FraudFoundP.

Features examined in this chart(These features are related to time):

- Month
- WeekOfMonth
- DayOfWeek
- DayOfWeekClaimed
- MonthClaimed
- WeekOfMonthClaimed

![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.004.png)

Figure4: Itcanbeseenthatthenumberofaccidentsthrough- out the year in differentmonths is almost constant

It can be seen that the number of accidents throughout the year in different months is almost constant. Every month, most accidents occur in the middle of the month. Every week, most accidents happen in the middle of the week. It

is quite visible that the number of accidents claimed during Hatfa all occur in an average week. It is quite visible that the number of accidents claimed during the month is almost the same.

Now let’s check some other features.

- Sex

![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.005.png)

Figure 5: The dominant gender of the society is men and they have more positive FraudFoundP than women.

- DriveRate

![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.006.png)

Figure6: Theaccidentrateofvehiclesthathaveaninsurance policy is higher and they have more positive FraudFoundP.

- VehicleCategory

![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.007.png)

Figure 7: Most of the available vehicles are sedans and they have the highest FraudFoundP rates.

- AgentType

![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.008.png)

Figure 8: In general, in the agent section, most of our data is external, and all FraudFoundP is linked to external.

- Year

![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.009.png)

Figure 9: In general, we are dealing with 3 differentyears.

*PreProcessing*

In this section, we have to check two things. The first case is to encode categorical features. The second is data balancing.

- encoding In this section, we encode the data using the label encoding method
- Data balancing
- Oversampling
- Undersampling

After doing these tasks, the data is ready to train the model.

*Models Results*

- Logistic Regression
- Undersampling

f1 score : 0.23269513991163474 roc score: 0.6709242370532693

![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.010.png)

Figure 10

- Oversampling

f1 score : 0.22107728337236532 rocauc score: 0.6231125679586829

![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.011.png)

Figure 11

- svm
- Undersampling

f1 score : 0.23667820069204157 roc score: 0.6851261641584222

![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.012.png)

Figure 12

- Oversampling

f1 score : 0.23804463336875661 rocauc score: 0.6332465921175598

![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.012.png)

Figure 13

- svm polynomial kernel
- Undersampling

f1 score : 0.16927899686520378 roc score: 0.5600737971705714

![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.013.png)

Figure 14

- Oversampling

f1 score : 0.23169398907103822 rocauc score: 0.6250612290934872

![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.014.png)

Figure 15

- Grid Search

f1 score : 0.23847841989758592 rocauc score: 0.6792046663014405

![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.015.png)

Figure 16

WeuseGridSearchtofindthebestinputvaluesof the model function. We know that this algorithm from cross validation Uses

- svm kernel RBF
- Grid Search

f1 score : 0.22517911975435007

roc score: 0.6253722084367245

![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.016.png)

Figure 17

- Oversampling

f1 score : 0.2130937098844673 rocauc score: 0.5978698720634205

![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.017.png)

Figure 18

- Decision Tree This model is more suitable in its initial state. We will try to improve the results with pruning.

![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.018.png)

Figure 19

- Undersampling

f1 score : 0.22461331540013452 roc score: 0.6728336179949084

![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.019.png)

Figure 20

- Oversampling

f1 score : 0.2316275490573297 rocauc score: 0.6544894156650753

![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.020.png)

Figure 21

The result did not improve with pruning.

- GradientBoostingClassifier
- Undersampling

f1 score : 0.2306525037936267 roc score: 0.664351777255003

![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.021.png)

Figure 22

- GridSearch

f1 score : 0.2788671023965142 rocauc score: 0.7468826958783634

![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.022.png)

Figure 23

- RandomForestClassifier
- Undersampling

f1 score : 0.2543933054393306 roc score: 0.6785222841674454

*conclusion![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.023.png)*

Figure 24

- Oversampling

f1 score : 0.18287937743190658 rocauc score: 0.5613152976056202

The best model resulting from Grid Search is based on ![](Aspose.Words.c3b77f22-149b-4055-a286-3cc72261093e.024.png)Gradient Boosting. Almost the results of all models are at

the same level. Note that the selected metric is proportional to the imbalance of the dataset. The roc plots shown all

Figure 25 represent model results.
