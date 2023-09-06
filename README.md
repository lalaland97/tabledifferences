# tabledifferences
A Python code to check the differences between two tables

import pandas as pd
import random

# Set a random seed for reproducibility
random.seed(42)

# Number of rows for each class (AVP Yes and AVP No)
num_samples = 50

# Initialize empty lists to store data
employee_ids = []
apprenticeship_types = []
graduate_programs = []
promotions = []
age_ranges = []
avp_labels = []

# Generate data for AVP Yes
for i in range(1, num_samples + 1):
    employee_ids.append(f'AVPY{i}')
    apprenticeship_types.append(random.choice(['Foundation', 'Higher', 'Other']))
    graduate_programs.append(random.choice(['Yes', 'No']))
    promotions.append(random.randint(0, 5))
    age_ranges.append(random.choice(['20-25', '25-30', '30-35', '35-40']))
    avp_labels.append('Yes')

# Generate data for AVP No
for i in range(1, num_samples + 1):
    employee_ids.append(f'AVPN{i}')
    apprenticeship_types.append(random.choice(['Foundation', 'Higher', 'Other']))
    graduate_programs.append(random.choice(['Yes', 'No']))
    promotions.append(random.randint(0, 5))
    age_ranges.append(random.choice(['20-25', '25-30', '30-35', '35-40']))
    avp_labels.append('No')

# Create a DataFrame from the generated data
sample_data = pd.DataFrame({
    'Employee_ID': employee_ids,
    'Apprenticeship_Type': apprenticeship_types,
    'Graduate_Program': graduate_programs,
    'Promotions': promotions,
    'Age_Range': age_ranges,
    'AVP': avp_labels
})

# Shuffle the dataset to randomize the order
sample_data = sample_data.sample(frac=1, random_state=42).reset_index(drop=True)

# Save the dataset to a CSV file (optional)
sample_data.to_csv('sample_avp_dataset.csv', index=False)

# Display the first few rows of the dataset
print(sample_data.head())
