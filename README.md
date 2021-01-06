# JSS Tool:
Waikato Environment for Knowledge Analysis (WEKA) is a popular, open source toolkit implemented in Java for machine learning and data mining. We used WEKA 3.8 for our study. We used the ClassBalancer filter in WEKA for balancing our dataset. We used two machine-learning algorithms (Support Vector Machine and Logistic Regression) to classify the vulnerable and neutral methods for all systems. We applied 10-fold cross validation to evaluate our predictive model to ensure that the trained model works accurately for an unknown dataset. The default parameter setting for two ML algorithms in WEKA 3.8 was considered for the study.

# JSS-Dataset
An ARFF (Attribute-Relation File Format) file is an ASCII text file that describes a list of instances sharing a set of attributes. 
ARFF files have two distinct sections. The first section is the Header information, which is followed the Data information.
The relation name is defined as the first line in the ARFF file. The format is: @relation <relation-name>
Each attribute in the data set has its own @attribute statement which uniquely defines the name of that attribute and it's data type. The order the attributes are declared indicates the column position in the data section of the file. For example, if an attribute is the third one declared then Weka expects that all that attributes values will be found in the third comma delimited column. The format for the @attribute statement is: @attribute <attribute-name> <datatype>
The @data declaration is a single line denoting the start of the data segment in the file. The format is: @data
Each instance is represented on a single line, with carriage returns denoting the end of the instance. Attribute values for each instance are delimited by commas. They must appear in the order that they were declared in the header section (i.e. the data corresponding to the nth @attribute declaration is always the nth field of the attribute).
  
# Example File:
@RELATION iris

@ATTRIBUTE sepallength  NUMERIC

@ATTRIBUTE sepalwidth   NUMERIC

@ATTRIBUTE petallength  NUMERIC

@ATTRIBUTE petalwidth   NUMERIC
@ATTRIBUTE class        {Iris-setosa,Iris-versicolor,Iris-virginica}
@DATA
5.1,3.5,1.4,0.2,Iris-setosa
4.9,3.0,1.4,0.2,Iris-setosa
4.7,3.2,1.3,0.2,Iris-setosa

Reference: https://www.cs.waikato.ac.nz/ml/weka/arff.html


