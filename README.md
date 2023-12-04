# dementia_factors
## Objective
This study aims to explore previously unidentified risk factors in dementia. Leveraging various machine learning algorithms, the researcher seeks to discern the relative importance of variables contributing to dementia and, ultimately, predict an individual's likelihood of developing this condition. Through this research, we aim to provide valuable insights that inform individuals about the choices they can make to safeguard their cognitive health.
Data Sources
The investigation utilized data derived from the Behavioral Risk Factor Surveillance System (BRFSS), a nationally representative survey designed for U.S. residents. The surveys encompassed inquiries about health-related risk behaviors, chronic health conditions, and utilization of preventive services. The dataset under consideration spans 2015 to 2022, with an annual compilation of over 400,000 interviews (BRFSS Archived, 2022). While the BRFSS survey's inception dates back to 1984, the specific question related to dementia was introduced in 2015. Notably, the BRFSS dataset is publicly accessible, facilitating direct download by researchers from official websites.
The dependent variable in this study was extracted from the query, "What is the main health problem, long-term illness, or disability that the person you care for has?" A caregiver reported this information, and the response options included "Dementia or other Cognitive Impairment Disorder," serving as the dependent variable denoting dementia. Other health problems were categorized as non-dementia. The independent variables in the study encompassed various risk factors, such as obesity, physical activity, smoking, alcohol use, stroke, depression, kidney disease, diabetes, and heart disease. Obesity was dichotomously recorded, with 1 indicating the presence of obesity and 2 denoting its absence.
Additionally, demographic variables were considered independent factors, including age, sex, race, employment status, education level, income, marital status, urban and rural residency, and healthcare access. For the race variable, six options were provided, with four races analyzed due to limited representation in other categories: White, Black, American Indian or Alaska Native, and Asian. The healthcare access variable gauged whether respondents identified one person or a group of doctors as their designated personal healthcare provider.
Data Preparation
Before modeling, the dataset underwent meticulous preparation involving feature selection, addressing missing values, mitigating class imbalance, and executing feature transformations. This preparatory phase was executed using Python and R programming languages, with the latter utilized for transferring the SAS dataset to CSV files. Key libraries and packages, notably scikit-learn, were employed in the data analysis.
Optimal feature selection was accomplished by leveraging both the Lancet and Libra index features (Bin-Hezam & Ward, 2019) and discerning relevant features within the context of the available BRFSS dataset.
Addressing missing values was a crucial facet of the data preprocessing, particularly given the presence of numerous missing entries in the outcome variables. The strategy employed involved the exclusion of instances with missing values. For other missing data within the independent variables, the SimpleImputer method was applied to impute the most frequently occurring data instead of the missing values.
In the context of handling imbalanced class distributions, the NeighbourhoodCleaningRule was implemented to rectify the ratio disparity between the majority and minority classes, thereby enhancing the robustness of the classification model.
After the aforementioned preprocessing steps, the dataset underwent a stratified split, partitioning into a 70% training set and a 30% testing set. This partitioning ensured the representative distribution of classes in both subsets. The classification models employed in this study were deliberately chosen for their interpretability. Logistic regression, random forest, and decision tree classifiers were selected because they facilitate a more transparent understanding of the underlying relationships within the data.
