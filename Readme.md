# **Exoplanet Identifier**  
## **A Machine Learning Project to Classify Exoplanets**  

### **Why am I doing this?**  
I say I understand machine learning (**which I do**), but I haven't really **gotten my hands dirty**.  

I have **almost no experience** with tools like **pandas, scikit-learn, numpy, etc.**, but **here’s how we learn** by jumping into the deep end 🚀 \
I want to see where I struggle the most, this is also really going to help with ARA

---

### **What is the Goal Here?**  
I want to analyze **planetary properties** to determine if a planet is:  

> - **0 → "Candidate"** → A potential exoplanet  
> - **1 → "Confirmed"** → A verified exoplanet  
> - **2 → "False Positive"** → Not actually an exoplanet  

I also want to **build a solid ML foundation** before diving into **Deep Learning** (Neural Networks and all that fun stuff) while working on the **virtual assistant for ARA**.  

---

### **What’s in the Data?**  
The dataset comes from **Kaggle's Kepler Exoplanet Dataset**, which includes the following key features:  

| Feature        | Description |
|---------------|------------|
| **kepid** | Unique Identifier for the host star |
| **kepoi_name** | Unique Identifier for the planetary candidate |
| **koi_disposition** | Status of the planetary candidate (0,1,2) |
| **koi_score** | Confidence score for classification (higher = stronger confidence) |
| **koi_period** | Orbital period (in days) |
| **koi_prad** | Estimated planetary radius (in Earth radii) |
| **koi_teq** | Estimated equilibrium temperature (Kelvin) |
| **koi_insol** | Insolation flux received (relative to Earth) |
| **koi_steff** | Effective temperature of the host star (Kelvin) |
| **koi_srad** | Stellar radius (in solar radii) |
| **koi_slogg** | Surface gravity of the host star (cm/s²) |
| **koi_kepmag** | Kepler-band magnitude (brightness of the star) |

---

### **What’s Next?**  
1. **Load and explore the dataset** using **pandas** 📊  
2. **Apply feature engineering & preprocessing** 🛠  
3. **Train a machine learning model** to classify exoplanets 🤖  
4. **Evaluate performance and optimize the model** 📈  

---

### **Project Roadmap**  
✅ **Step 1:** Load the data and check for missing values  
✅ **Step 2:** Perform exploratory data analysis (EDA)  
✅ **Step 3:** Preprocess data (handle missing values, normalize features)  
✅ **Step 4:** Train an initial ML model (Random Forest / XGBoost)  
✅ **Step 5:** Tune hyperparameters and optimize performance  
✅ **Step 6:** Interpret results & visualize feature importance  

---

## **Loading Project Data**
I loaded the Exoplanet data from the csv to a dataframe object using pandas read_csv() function 
I printed the head(top 10 rows of dataframe) to verify the correct data and labeling 
Now it is time to preprocess the data

## Visualize the data

I want to do this before I preprocess. \
This can answer these questions:
**How is the data distributed?**
**How many outliers are there?**
**How skewed is the data?**

I also want to see any correlation between the data features

Doing this will help select the normalization technique\
### Identify the independent and dependent variables

This requires a good understanding of the dataset which at the moment I thought I did\
Granted I took it for face value instead of looking into it which I will once I get home or should I pay attention to my assembly class?\

What kind of correlation do all these features have? What makes a planets an exoplanet according to these features?
Ok here is what I found: \



## Data Preprocessing
Now it is time to prepare/clean the data\
This consists of:
**1. Handling missing data**
**2. Removing Redundant Data**
**3. Normalizing data**

### Handling Missing data
After checking for any missing values is used **exoplanet_df.is_null().any()** to see if and where I am missing data\
Doing this revealed that there is no missing data which is great \

### Removing Redundant Data
Now it is time to remove redundant data\
This is data that has no importance but can affect the models performance\
That data in this case is:
**kepid** 
**kepoi_name**
\
These labels and data provide no useful insight and can affect my models performance 

### Data Normalizing 

Now I have to normalize the data\
What is **Data Normalization**?\
Data Normalization is transforming data features to a standard scale between **0 and 1**\
This is done by adjusting features based on **maximum and minimum** values\
You do this to ensure not one feature dominates the others\
\
There are several ways to normalize data\
One way I found that is very common is the **Min-Max** formula\
Looks like this: 
> 
X<sub>norm</sub> = (x - x<sub>min</sub>) / (x<sub>max</sub> - X<sub>min</sub>)
>
Where: \
**X** is the individual data\
**X<sub>min</sub>** is the smallest value in the dataset\
**X<sub>max</sub>** is the largest value in the dataset\
**X<sub>norm</sub>** is the normalized value(Usually between 0 and 1)\

\
There are other ways such as 
**Max-Abs Normalization**
where:\
X<sub>norm</sub> = X / |X<sub>max</sub>|

or 

**Mean Normalization** or **Z-Score Normalization**
But I want to check out **Log**


## The Machine Learning Model
At this point in time I am beginning to think about the model I want to use \
First I should probably graph the points or something \
For now though I am thinking of using Linear Regression(assuming this data is pretty linear)\
Otherwise I will have to look at the data and see where it is going\

