# Quarter 1 Project
Instructed by Dr. Yilmaz in Room 202

The Audubon Society Field Guide provides a classification of mushrooms based on a variety of characteristics that help determine whether a mushroom is edible or poisonous. These traits span across 22 features, which describe physical properties of the mushroom.

Based on these features, mushrooms are classified as either edible or poisonous. This classification is important for ensuring public safety, as some mushrooms that appear edible may actually be poisonous. Each mushroom is labeled based on its edibility, but the process of determining this label based on the various physical features is not always straightforward and well defined. Unlike other plants, there is no simple rule to classify mushrooms as edible or poisonous, such as the “leaflets three, let it be” rule for identifying Poison Ivy or Poison Oak. For this project, we will explore the features provided in the dataset and use them to train and test a binary classification model that predicts the edibility of a mushroom. After determining which classification models perform best, we can identify characteristics which contribute most to the model's predictions and determine which attributes are the most statistically significant in identifying mushroom edibility.

Steps to Reproduce Our Most Effective Model (SVC with Correlation Attribute Selection):

1.   Download the mushrooms.csv from the official UCI repository
2.   Place the mushrooms.csv file in a new directory named “Q1 Project”
3.   Open Weka and load the mushrooms.csv file
4.   Go to the “Select Attributes” tab and ensure the class variable is set to class
5.   Select CorrelationAttributeEval as Attribute Evaluator and Ranker as Search Method
6.   Begin the attribute selection and take inventory of features in the output that have a ratio not greater than or equal to 0.25 (our cutoff)
7.   Open a Python IDE (Jetbrains DataSpell was used for this paper) with CWD as “Q1 Project”. If the Python environment is not in the “Q1 Project” directory, type `cd [Path of Q1 Project directory]`
9.   Copy the split.py, model.py, and load.py programs from the paper’s source to the directory
10.   Install required dependencies using the shell terminal:
`pip install numpy pandas scikit-learn`
11. Open the split.py program in the IDE
12. Configure the attributes_to_remove list in the split.py program to contain the names of the features in the earlier inventory as strings
13. Change the contents of the folder_name string to “correlation”
14. Run the split.py program to remove irrelevant attributes, encode data, perform KNN imputation, and test-train-split into separate directories

For personal use only.
