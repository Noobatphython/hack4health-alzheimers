
Quick Start (Google Colab - Easiest!)
Step 1: Open the notebook
Click this Link (or paste in browser): https://drive.google.com/file/d/13JmIn0gpnyJetr7S4K9n-HMDCilWIKFS/view?usp=sharing
Then press open with olab on top right 
 
Dowload the data mentioned below 
 Data You Need
1. MRI Brain Scans (Required)
Get train.parquet5,120 brain MRI scans for trainingHack4Health competition and test.parquet1,280 brain MRI scans for testingHack4Health competition

2. Clinical Data (Auto-downloaded)
The notebook automatically downloads clinical data from Kaggle - no action needed!

If you prefer to run on your own computer:
bash# 1. Clone this repository
git clone https://github.com/YOUR_USERNAME/hack4health-alzheimers.git
cd hack4health-alzheimers

# 2. Install Python packages
pip install -r requirements.txt

# 3. Add your data files to the data/ folder

# 4. Open and run the notebook
jupyter notebook Hack4Health_Final_Submission.ipynb


How It Works
MRI Model (ResNet50)
Brain Scan Image → ResNet50 Neural Network → Diagnosis
                   (pretrained on 14M images)

Output: One of 4 classes
├── 0: Non-Demented
├── 1: Mild Demented  
├── 2: Moderate Demented
└── 3: Very Mild Demented
Clinical Model (MLP)
32 Patient Features → Neural Network → Diagnosis
│
├── Age, Gender, Education
├── BMI, Smoking, Exercise
├── Family History, Diabetes
├── MMSE Score, Memory Complaints
└── ... and more

Output: Alzheimer's Yes/No


 Limitations

Small sample for Mild Demented class (only 49 images)
Clinical data is synthetic (for educational purposes)
MRI and Clinical data are from different patients (not true multimodal)

Citations
Clinical Dataset:
Rabie El Kharoua (2024). Alzheimer's Disease Dataset. Kaggle.
DOI: 10.34740/KAGGLE/DSV/8668279
Methods:

He et al. (2016). Deep Residual Learning. CVPR.
Selvaraju et al. (2017). Grad-CAM. ICCV.
