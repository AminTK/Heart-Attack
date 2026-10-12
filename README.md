# Heart-Attack

# Heart Attack and Factors Affecting Heart Health

The heart is one of the human body's most vital organs; through the continuous pumping of blood, it delivers the oxygen and nutrients required by cells to the body's various tissues. Proper heart function depends on numerous factors, including the health of blood vessels, blood pressure, metabolic status, physical activity, and lifestyle. Any disruption in heart function or the blood supply to the heart can have serious consequences for human health.

One of the most significant cardiovascular conditions is a heart attack, or myocardial infarction. A heart attack typically occurs when blood flow to a portion of the heart muscle is suddenly reduced or blocked. This condition often arises from the formation of a blood clot in one of the coronary arteries—the vessels responsible for supplying oxygen and nutrients to the heart muscle. If the disruption to blood flow persists, a portion of the heart tissue may become damaged or die. Consequently, rapid diagnosis and immediate medical care play a crucial role in minimizing complications and increasing the likelihood of recovery.

Blood pressure is a key factor associated with heart health. When blood pressure remains above the optimal range for an extended period, the heart encounters greater resistance while pumping blood. This condition can lead to thickening of the heart muscle, damage to blood vessel walls, and an increased risk of cardiovascular disease. However, blood pressure is merely one risk factor, and a heart attack cannot be predicted based solely on its level. Furthermore, a normal blood pressure reading at a single point in time does not guarantee the absence of cardiac risk. Numerous factors contribute to an increased risk of heart attack. Key factors include age, a family history of heart disease, tobacco use, high blood pressure, elevated LDL cholesterol, diabetes, excess weight, physical inactivity, and certain unhealthy dietary patterns. These factors can affect vascular health and cardiac function either individually or through their interaction with one another. For instance, elevated LDL cholesterol can contribute to the formation of fatty plaques on arterial walls, while diabetes can damage blood vessels. The cumulative effect of these conditions over time can heighten the risk of developing cardiovascular disease.

Various clinical and laboratory indicators are used to assess heart health and evaluate risk factors. Variables such as blood pressure, age, levels of total cholesterol, LDL, HDL, and triglycerides, blood sugar, Body Mass Index (BMI), and a history of underlying medical conditions are considered when evaluating cardiovascular risk. Some of these variables provide information on the body's current state, while others help identify long-term risk factors. However, no single indicator is sufficient on its own to definitively diagnose a heart attack.

With advancements in data science and machine learning, the analysis of medical datasets has emerged as a prominent approach for studying cardiovascular disease. By examining patient data, it is possible to identify statistical patterns linking demographic characteristics, clinical indicators, and disease status. Furthermore, statistical and machine-learning models can be employed to estimate risk or classify individuals based on available data. However, the performance of these models depends on data quality, sample selection, the definition of the target variable, and the evaluation method; their results do not necessarily imply a proven cause-and-effect relationship.

In this project, by examining and analyzing indicators related to heart health and heart attacks, we aim to better understand the relationship between various factors and the recorded status of patients. The objective is to identify patterns within the data, investigate differences between various groups, and assess the role of clinical variables in analyzing cardiac status. Such an analysis can contribute to a better understanding of risk factors as well as the capabilities and limitations of data-driven methods in healthcare, although the findings will not replace a physician's diagnosis or an individual clinical assessment.

# The features of the dataset

1. Age : Patient **age** in years. The age of participants in the dataset ranges from 29 to 77 years.

2. Sex : Gender of the patient (0 = male, 1 = female).

3. cp (chest pain type) : This feature represents the type of chest pain experienced by the patient. Chest pain is a key clinical symptom used in diagnosing heart disease, and different types of chest pain are associated with different levels of cardiac risk.

> - 0 : Typical angina
This is the classic form of angina caused by reduced blood flow to the heart muscle. It usually occurs during physical activity or emotional stress and is relieved by rest or medication. This type of pain is strongly associated with coronary artery disease.

> - 1 : Atypical angina
Chest pain does not follow the classic pattern of angina. It may differ in location, duration, or triggering factors and is less clearly related to physical exertion. Although it can be cardiac-related, its diagnostic certainty is lower than typical angina.

> - 2 : Non-angina pain
Chest pain that is not related to heart disease. It may originate from non-cardiac causes such as muscular issues, gastrointestinal problems, or respiratory conditions. This type of pain generally has a low association with coronary heart disease.

> - 3 : Asymptomatic
The patient does not experience any chest pain. Despite the absence of symptoms, heart disease may still be present and detected through other clinical indicators.

4. trestbps (Resting systolic blood pressure (measured in mm Hg)) : **Resting blood pressure** refers to the systolic blood pressure measured when an individual is at rest, typically in a seated position and without recent physical activity.

> Systolic Blood Pressure Ranges
> | Value (mm Hg) | Category |
> |---------------|----------|
> | Less than 120 | Normal |
> | 120–129 | Elevated |
> | 130–139 | Hypertension (Stage 1) |
> | 140 or higher | Hypertension (Stage 2) |

5. chol : Serum Cholesterol (mg/dl) refers to the total cholesterol level measured in the blood serum. It is an important clinical indicator used to assess the risk of cardiovascular disease.

> This parameter is measured in mg/L or ppm.

> Cholesterol Level Ranges 
> | Value (mg/dl) | Category | 
> |---------------|----------| 
> | Less than 200 | Desirable | 
> | 200–239 | Borderline High | 
> | 240 or higher | High Risk |

6. Fasting Blood Sugar (fbs) : refers to the glucose level in the blood measured after at least 8 to 12 hours of fasting.
It is an important indicator for assessing diabetes and risk of cardiovascular disease.

> Medical Interpretation:
> - Values above 120 mg/dl may indicate impaired glucose regulation or diabetes
> - High fasting blood sugar is often associated with increased risk of heart disease
> - fbs = 1→ The individual's fasting blood sugar is **greater than 120 mg/dl** (indicating possible **prediabetes or diabetes**).
> - fbs = 0→ The individual's fasting blood sugar is within the **normal range**.

7. restecg (Resting Electrocardiographic Results) : records the electrical activity of the heart while the patient is at rest. It is used to detect heart problems such as **arrhythmia, ischemia, or left ventricular hypertrophy (LVH)**. In medical datasets, this variable is usually defined as:

> Resting ECG results :
> - 0 → Normal : heart activity with no apparent problem
> - 1 → Having ST-T wave abnormality : May indicate ischemia, previous heart damage, or other rhythm disturbances
> - 2 → Showing probable or definite left ventricular hypertrophy : Enlargement of the left ventricular muscle, often due to high blood pressure or chronic heart disease** .

8. thalach (Maximum Heart Rate Achieved) : **maximum heart rate** achieved by an individual during a **stress test**. This test is used to assess heart performance under physical stress and to detect potential cardiovascular problems.

> Normal Range
> - Typical maximum heart rate (bpm) formula: [ MaxHR = 208 - (0.7 * Age) ]
> - Values ≥85% of Max HR are generally considered a normal response
> - Values significantly below this range may indicate reduced cardiac fitness or heart disease risk

> Example Ranges (Approximate):

> |Age (years)|	Estimated Max HR (bpm)|	Normal Range (~85–100%)|
> |-------|-------|-------|
> |40	|180	|153–180 bpm|
> |50	|173	|147–173 bpm|
> |60	|166	|141–166 bpm|

> - Values below 70% are considered low, values between 70% and 85% are considered normal, and values above 85% are considered acceptable or above average.

9. exang(Exercise-induced angina) : ** indicates the **presence or absence of chest pain during physical activity or exercise**. It is an important indicator for detecting **myocardial ischemia or coronary artery problems**.

> - 1 → Yes → The individual experiences chest pain during exercise: a higher risk of heart disease
> - 0 → No → The individual does not experience chest pain : no exercise-induced chest pain

10. Oldpeak(ST Depression Induced by Exercise) : refers to the **ST segment depression observed on an ECG during exercise relative to rest**. This metric is used to assess **myocardial ischemia or reduced blood flow to the heart**.

> Typical Ranges (Approximate)
> |Oldpeak (mV)	|Interpretation|
> |0.0	|No ST depression (Normal)|
> |0.1 – 1.0	|Mild ST depression (Mild ischemia)|
> |1.1 – 2.0	|Moderate ST depression (Moderate ischemia)|
> |2.0	|Severe ST depression (Severe ischemia)|

11. slope : indicates the **slope of the ST segment on an ECG during peak exercise**. This feature is used to assess **myocardial ischemia and its severity**.

> Medical Interpretation
> - Upsloping (0): Generally normal or low risk (ST segment slopes upward)
> - Flat (1): May indicate mild to moderate ischemia (ST segment is flat)
> - Downsloping (2): Suggests severe ischemia or impaired blood flow to the heart (ST segment slopes downward)

12. ca(Number of Major Vessels Colored by Fluoroscopy) : represents the **number of major coronary vessels** that are visualized (colored) during **fluoroscopy**. This test helps identify **blockages or narrowing in the coronary arteries**.

> Medical Interpretation
> - 0 vessels: No major vessels visible → may indicate significant blockage
> - 1–2 vessels: Partial visualization → moderate coronary artery disease
> - 3–4 vessels: More vessels visible → better coronary blood flow

13. thal(Thalium Stress Test Result) : it represents the result of the **thalium stress test**, a nuclear imaging test used to evaluate **blood flow to the heart muscle** and to detect **ischemia or permanent cardiac damage**

> Variable Definition and Medical Interpretation
> - 0 → Normal(** Normal blood flow to the heart muscle)
> - 1 → Fixed defect( Area of permanent damage** to the heart muscle, usually due to a previous heart attack)
> - 2 → Reversible defect( Reduced blood flow during exercise that improves at rest, indicating myocardial ischemia**

> Not described (3): Result is missing or cannot be clearly interpreted)
> - 3 → Not described / Unknown(** Result is missing or cannot be clearly interpreted )

14. target : Heart disease status

> - 0 → No heart disease
> - 1 → Presence of heart disease </span>
