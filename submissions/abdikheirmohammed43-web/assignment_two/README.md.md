# Research Paper: Social Media Impact Dataset

## Title & Collection Method
* **Title:** The Impact of Social Media on Individuals and Behaviour.
* **Collection Method:** I designed a survey questionnaire using Google Forms and collected responses from 50 individuals. The dataset contains a mix of text and numerical answers, intentionally left unstructured so that I can clean and preprocess it later.

---

## Description of Features & Labels
* **Features (X):**
  1. `Age` (Categorical/Text ranges)
  2. `Time_Wastage_Opinion` (Categorical: haa / maya / macquul wye)
  3. `Social_Media_Hours` (Categorical/Text ranges)
  4. `Primary_Reason` (Categorical: wax barasho, daawasho, bashaal kaliye, jw.)
  5. `Sleep_Hours` (Categorical/Text ranges)

* **Label (y):**
  * `Overall_Impact` -> haa inta badan / maya kuma qabo / faaido yar
  * *This makes the problem a multi-class classification task (predicting one of three possible impact categories based on user behavior).*

---

## Dataset Structure
* **Rows:** 50 respondents (samples)
* **Columns:** 6 (5 features + 1 label)

### Sample Table (5 rows of actual uncleaned data)
| Age | Time_Wastage_Opinion | Social_Media_Hours | Primary_Reason | Sleep_Hours | Overall_Impact |
| :--- | :--- | :--- | :--- | :--- | :--- |
| under 18 | haa | 4-6 | wax barasho iyo daawasho | 4-6 | haa inta badan |
| 25-30 | macquul wye | 4-6 | bashaal kaliye | 6-8 | maya kuma qabo |
| 25-30 | haa | 4-6 | wax barasho iyo daawasho | 6-8 | faaido yar |
| under 18 | haa | 6-8 | bashaal kaliye | 6-8 | faaido yar |
| 25-30 | maya | 2-4 | bashaal kaliye | 6-8 | haa inta badan |

---

## Quality Issues
* **Missing values:** A few respondents skipped some optional questions, leaving blank fields (Missing Values).
* **Categorical text:** Text ranges like `Age` ("under 18", "25-30") and categories like `Primary_Reason` and `Overall_Impact` must be encoded (Label/One-Hot Encoding) into numerical data for Machine Learning.
* **Inconsistent reporting & Complex Strings:** Columns like `Primary_Reason` contain mixed entries joined together (e.g., "wax barasho iyo daawasho") which require parsing and preprocessing.

---

## Use Case
* This dataset can be used to train a classification model to predict and categorize the overall impact of social media on an individual based on their habits.
* **Possible algorithms:** Logistic Regression, Decision Tree, Random Forest.
* **Data Science Lifecycle:** It fits perfectly into the **Data Collection and Data Preparation** phase, which is the foundation of the lifecycle.
*