# My First Project

This project was created using Google Colab.

## Files
- my_project.ipynb – Main notebook file

## Author
Satyam

# Student Examination Score Improvement Analysis

# -----------------------------
# Step 1: Import required libraries
# -----------------------------
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

# -----------------------------
# Step 2: Create sample dataset
# (You can later replace this with CSV file)
# -----------------------------
data = {
    "Student_ID": [1, 2, 3, 4, 5],
    "Pre_Test_Score": [45, 50, 60, 55, 48],
    "Post_Test_Score": [65, 70, 78, 72, 68]
}

df = pd.DataFrame(data)

# -----------------------------
# Step 3: Calculate improvement
# -----------------------------
df["Improvement"] = df["Post_Test_Score"] - df["Pre_Test_Score"]

# -----------------------------
# Step 4: Statistical Analysis
# -----------------------------
pre_mean = df["Pre_Test_Score"].mean()
post_mean = df["Post_Test_Score"].mean()

pre_std = df["Pre_Test_Score"].std()
post_std = df["Post_Test_Score"].std()

print("Pre-test Mean:", pre_mean)
print("Post-test Mean:", post_mean)
print("Pre-test Std Dev:", pre_std)
print("Post-test Std Dev:", post_std)

# -----------------------------
# Step 5: Visualization (Histograms)
# -----------------------------
plt.hist(df["Pre_Test_Score"], alpha=0.6)
plt.hist(df["Post_Test_Score"], alpha=0.6)
plt.xlabel("Scores")
plt.ylabel("Number of Students")
plt.title("Pre-test vs Post-test Score Distribution")
plt.legend(["Pre-test", "Post-test"])
plt.show()

