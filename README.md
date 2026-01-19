📊 Prodigy Infotech – Data Science Internship
Task 05: Accident Data Visualization & Pattern Analysis
👤 Intern

Aarti Singh

📌 Task Description

The objective of this task is to analyze and visualize accident data to identify meaningful patterns related to time, weather, severity, visibility, and geographical locations using Exploratory Data Analysis (EDA) techniques.

🎯 Objectives

Load and inspect the dataset

Extract time-based features

Perform exploratory data analysis (EDA)

Visualize trends and patterns

Identify accident hotspots

Analyze the impact of weather and visibility

📂 Dataset

Dataset Used: US Accidents Dataset (Small Version)

Contains information about accidents such as time, location, weather condition, severity, visibility, and state.

🛠️ Tools & Technologies

Python

Pandas

NumPy

Matplotlib

Seaborn

Google Colab / Jupyter Notebook

🔍 Exploratory Data Analysis Performed
1. Accidents by Hour of the Day
df['Start_Time'] = pd.to_datetime(df['Start_Time'])
df['Hour'] = df['Start_Time'].dt.hour

plt.figure(figsize=(10,5))
sns.histplot(df['Hour'], bins=24)
plt.title("Accidents by Hour of Day")
plt.show()

2. Accidents by Weather Condition
plt.figure(figsize=(10,5))
sns.countplot(x="Weather_Condition", data=df)
plt.xticks(rotation=45)
plt.show()

3. Severity vs Weather
plt.figure(figsize=(10,5))
sns.countplot(x="Weather_Condition", hue="Severity", data=df)
plt.xticks(rotation=45)
plt.show()

4. Day vs Night Accidents
plt.figure(figsize=(6,4))
sns.countplot(x="Sunrise_Sunset", data=df)
plt.show()

5. Visibility Distribution
plt.figure(figsize=(8,4))
sns.histplot(df['Visibility(mi)'], bins=20)
plt.show()

6. Precipitation Distribution
plt.figure(figsize=(8,4))
sns.histplot(df['Precipitation(in)'], bins=20)
plt.show()

7. Accident Hotspots (Geographical KDE Plot)
plt.figure(figsize=(8,6))
sns.kdeplot(
    x=df['Start_Lng'],
    y=df['Start_Lat'],
    cmap="Reds",
    fill=True
)
plt.title("Accident Hotspots")
plt.show()

8. Accidents by State
plt.figure(figsize=(10,5))
df['State'].value_counts().plot(kind='bar')
plt.title("Accidents by State")
plt.show()

✅ Conclusion

This task helped in understanding how visualization techniques can be used to identify hidden patterns in real-world data. The analysis revealed insights related to accident frequency based on time, weather conditions, severity, and geographic distribution.
