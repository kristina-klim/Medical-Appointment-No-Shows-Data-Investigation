# Medical-Appointment-No-Shows-Data-Investigation
## Intro

This dataset collects information from 100k medical appointments in Brazil and focuses on whether or not patients show up for their appointment. Several characteristics of the patient are included in each row.

Investigation project for Udacity Nanodegree Program. I have taken a Medical Appointment No Shows data set for that work. This dataset contains information from 100k medical appointments in Brazil and focuses on whether or not patients show up at the doctor's office after the patient made an appointment. The main goal is to analyze the dataset to determine what factors are essential to know to predict if a patient will show up or not?

__To accomplish this goal, I will answer the following questions:__
- Q 1: What is the ratio of appointment showed-up versus not showed-up?
- Q 2: Male or female showed up at the doctor most often?
- Q 3: What is the distribution of the age for the showed-up and not showed-up appointment?
- Q 4: What is the average age for each gender in the showed-up and not showed-up scenarios?
- Q 5: Is there a relationship between diseases and appointments show up?
- Q 6 : Is there a difference between who receives SMS reminders or not?
- Q 7 : What hospitals are the most popular?

## Methods Used
- Pandas, Numpy: clean, manipulation and transform data
- Matplotlib and Seaborn: visualization

## Needs of this project:
- Explore, validate and clean data
-	Merging three datasets into one.
-	Exploratory Data Analysis

## Files specifications

__Data Set__
The data is contained one file: noshowappointments-kagglev2-may-2016.csv

- PatientId (float)- identification number of a patient
- AppointmentID (int) - identification number of each appointment
-	Gender(object) - male or female
- AppointmentDay (object) - the day of the actuall appointment, when they have to visit the doctor.
-	ScheduledDay (object) - the day someone called or registered the appointment, this is before appointment of course.
-	Age (int) - how old is the patient.
-	Neighbourhood (object) - where the appointment takes place.
-	Scholarship (int) - 0 or 1, indicates whether or not the patient is enrolled in Brasilian welfare program Bolsa Família
-	Hipertension (int) - 0 or 1
-	Diabetes (int) - 0 or 1
-	Alcoholism (int) - 0 or 1
-	Handcap (int) - 0 or 1
- SMS_received (int) - 1 or more messages sent to the patient. 
- No-show (object) - "Yes" or "No", it says ‘No’ if the patient showed up to their appointment, and ‘Yes’ if they did not show up. 

## Conclusions
Data shows that 80% of all appointments ended up with actual visiting, but when the patient scheduled an appointment, it is still a 20% chance that the patient will not show up. If it is female, the possibility of a visit is almost 53% more than if it is a male. A significant part of patients are children under ten years old. 
76% patient don't have "hipertension", "diabetes", "alcoholism", "handcap" diseases. We also saw that sending SMS does not guarantee a visit.
For building a prediction model of showing up at the doctor's office or not, I would use the following features: gender, age, difference days between scheduled and actual appointments, neighborhood (location of hospitals). I would not use the "hipertension", "diabetes" due high correlation between them, and sms_received features due to many conditions.

## Limitations
We have used the Medical Appointment No Shows dataset for analysis and worked with popularity, diseases, and DateTime. The investigation is limited to only the provided dataset. There are limited kinds of conditions, and data sets show that 76% of patients don't have a particular illness like: "hipertension","diabetes", "alcoholism", "handcap". But what about other diseases, like a heart condition or cancer - that information might be helpful for analysis. 
Information about the patient's income and marital status could reveal more patterns in a patient's behavior and increase prediction probability.

## References

-	https://towardsdatascience.com/clearing-the-confusion-once-and-for-all-fig-ax-plt-subplots-b122bb7783ca
-	https://stackoverflow.com/questions/22591174/pandas-multiple-conditions-while-indexing-data-frame-unexpected-behavior
-	https://matplotlib.org/stable/api/_as_gen/matplotlib.axes.Axes.set_xlim.html
-	https://stackoverflow.com/questions/60637257/how-to-plot-multiple-columns-side-by-side-with-seaborn-countplot
-	https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.apply.html
-	https://www.w3schools.com/python/python_lambda.asp
-	https://stackoverflow.com/questions/41622054/stacked-histogram-of-grouped-values-in-pandas
-	https://www.kite.com/python/answers/how-to-delete-rows-from-a-pandas-%60dataframe%60-based-on-a-conditional-expression-in-python
-	https://www.kaggle.com/joniarroba/noshowappointments









