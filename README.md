# Grading-the-Graders
This Python project analyzes how UBC professors' contract statuses affect class averages. It includes large amounts of data cleaning (PDF>WORD>CSV), visualization, and fixed effects regression analysis, aligning financial and teaching data to explore grading patterns.

**Data Collection:**
Manual financial data extraction from UBC reports, formatted with professor names and financial details.
Word Document Processing:
Loaded financial data into a Word document.
Used Python's re (regex) module to identify and format relevant data.
Excel Data Preparation:

I transferred data to Excel, using text-to-column features for initial cleaning.
Data Aggregation with Pandas:

Performed aggregation and pivoting operations in Python using the pandas library.
Calculated wage increases to identify potential contract renewals.
Handling Duplicates and Contract Status:

Removed duplicate entries for data accuracy.
A dummy variable was assigned to indicate the final year of contracts based on salary hikes.
Professor Name Reformatting:

Standardized professor names for consistency with class data.
Grades Data Cleaning:

Processed grade data for compatibility with financial data.
Merging Financial and Grades Data:

Merged datasets by year, aligning fiscal and academic information.
The combined dataset was refined to eliminate missing or irrelevant data.
Final Dataset Creation:

I compiled a clean, comprehensive dataset for regression analysis and saved it in CSV format.

**Regression Analysis Steps:**
Simple Ordinary Least Squares (OLS) Regression:

Ran a basic OLS regression to examine the relationship between average grades (Avg) and contract ending status (ContractEnded).
OLS Controlling for Enrolled Students:

Extended the OLS model to include the number of enrolled students as a control variable (Enrolled), refining the analysis.
Regression with Professor Fixed Effects:

Incorporated fixed effects for individual professors to control for their specific grading tendencies and characteristics.
Regression with Professor and Course Fixed Effects:

Further refined the model by adding fixed effects for courses (C(Course)), capturing the unique aspects of different classes.
Final Comprehensive Regression Model:

Compiled a comprehensive regression model that includes professor fixed effects, course fixed effects, and controls for the number of students enrolled.
This final model offers a robust analysis of how contract status impacts grading, accounting for multiple influencing factors.

**Visualization Steps:**
Average Treatment Effect (ATE) Visualization:

Plotted the distribution of grades for professors based on their contract status.
Used seaborn and matplotlib libraries for histograms, comparing groups where contract ended and where it did not.
Controlled Visualization for Professors (ATT):

Visualized the average grades for professors who experienced both contract statuses.
Illustrated the change in grading patterns pre- and post-contract ending.
Comparison of Average Grade Changes:

Analyzed the change in average grades for each professor over different contract statuses.
Generated histograms to depict these variations in grading.
ATT Visualization Including Class Changes:

Extended the analysis to professors teaching the same courses under different contract statuses.
Compared average grades in identical courses across different contract years.
Graph Visualization of Analysis Flow:

Employed graphviz to create a Directed Acyclic Graph (DAG) illustrating the analytical framework.
The DAG visually represented the relationships and potential confounding factors in the study.


**Abstract of the paper**
This study investigates the causal relationship between professors’ contract status
and their class averages at the University of British Columbia (ubc, 2023b) over
the academic years 2020, 2021, and 2022. It utilizes a dataset with 20,639 classes
taught by 2,546 different professors; this paper uses a fixed effects regression to control
for variables such as individual professors and specific courses. The aim is to
determine whether professors in the final year of their contracts have an incentive
to inflate grades, potentially influenced by tenure reviews or contract renewals. The
findings show a statistically significant increase in class averages during the last year
of a professor’s contract, indicating a potential moral hazard with grading practices.
While the study gives insights into university grading practices, its scope is limited
by the available data spanning only three years. Future research could explore
different datasets and alternative methodologies.
