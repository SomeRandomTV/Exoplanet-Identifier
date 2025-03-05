# **Exoplanet Identifier**  
## **A Machine Learning Project to Classify Exoplanets**  

### **Why am I doing this?**  
I say I understand machine learning (**which I do**), but I haven't really **gotten my hands dirty**.  

I have **almost no experience** with tools like **pandas, scikit-learn, numpy, etc.**, but **here’s how we learn**: by doing! 🚀  

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

## **Let's do this. 🚀✨**  
