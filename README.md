# Inferring Alcohol Consumption from Liver Disease Biomarkers

> *Abstract:*  
> This is the abstract

## Motivation

Liver disease affects millions of people worldwide and is one of leading causes of premature death. According to CDC, 1.8% of adults older than 18 have liver disease and it is more prominent among populations living in poverty. ([source](https://ftp.cdc.gov/pub/Health_Statistics/NCHS/NHIS/SHS/2018_SHS_Table_A-4.pdf)). Although liver disease may be caused by genetic factors or viral infections, alcohol consumption is associated with the disease's most common manifestation ([source](https://pmc.ncbi.nlm.nih.gov/articles/PMC9599689/)). Alcohol-related cirrhosis affects a younger population more and has a lower life expectancy, comapred to other causes of the disease ([source](https://pubmed.ncbi.nlm.nih.gov/7648984/)). 

At the same time, not only is alcohol-related liver disease is preventable, in its eearly stages, the disease is also *reversable* [source](https://britishlivertrust.org.uk/information-and-support/liver-health-2/stages-of-liver-disease/). Thus reducing intake among healthy individuals and abstaining completely for individuals that suffer from liver disease can increase longevity among vulnerable populations and improve health outcomes. 

![Stages of liver disease, image sourced from the British Liver Trust](https://17xpvwx1p0y4h.cdn.shift8web.com/wp-content/uploads/stages-of-liver-disease-for-cirrhosis.png)

*Stages of liver disease. Image sourced from [British Liver Trust](https://britishlivertrust.org.uk/information-and-support/liver-health-2/stages-of-liver-disease/).*

Liver performs several key functions in a mammal body. This organ is responsible for filtration and storage of blood, metabolizing proteins into amino acids, and forming bile. Excess amino acids in the body are sent to the liver for processing and metabolism, where liver releases amonia (which will turn into uric acid), glutamate, glutamine, aspartate. 

![Liver functions, image sourced from the British Liver Trust](https://britishlivertrust.org.uk/wp-content/uploads/AdobeStock_94365261-Converted-1024x951.png)

*Liver fuctions. Image sourced from [British Liver Trust](https://britishlivertrust.org.uk/information-and-support/liver-health-2/stages-of-liver-disease/).*

While patients may choose to not disclose their alcohol consumption levels to the attending phisician, inferring consumption from liver disease biomarkers could provide insights to the medical staff and allow them to deliver necessary counceling and resources to the patient. Especially, detecing alcohol-induced liver damage has the potential to save lives. 

The goal of this project is to assess if measures of serum enzymes and size of red blood cells are good indicators of high alcohol consumption and can be utilized in clinical settings to provide guidance to physicians in diagnosing alcohol-induced liver disorders.

## Dataset

Liver Disorders dataset used in this study comes from the BUPA Medical Research Ltd and was obtained from UCI Machine Learning Repository [source](https://doi.org/10.24432/C54G67). BUPA provides medical coverage to patients worldwide.  The dataset was donated by Richard S. Forsyth and contains 5 features describing results of blood tests performed on male subjects in the 1980s. The dataset contains "drinks" columns which is used as a target variable in this analysis. `selector` column is included for the purpose of splitting training and testing subsets. Typically, this dataset is used in order to benchmark machine learning algorithms. 

The target variable counts the number of drinks that the study participant consumes daily and is measured in half-pints. The target variable can be modeled as Poisson random variable, since it counts discrete events happening within a fixed period of time. This metric is self-reported and may not be a truthful representation of the actual amount of alcohol consumed. Alcohol consumption may be variable for each individual and each participant might metabolize alcohol differently.

Nontheless, it would be interesting to know how much of the variance in alcohol consumption can be explained by the liver function test results.

Enzymes are released by the liver due to hepatocellular (specific to liver cells) injury include:
* AST (`sgot` in the dataset) - Aspartate Aminotransferase - an enzyme also found in muscles, found primarily in a mitochondrium of the liver lobule.
* ALT (`sgpt` in the dataset) - Alanine Aminotransferase - an enzyme primary to liver, found mostly in cytoplasm.

Generally, these two enzymes are found in 1-to-1 ratio. AST is more indicative of alcohol damage because ethanol found in alcohol may be causing damage to the mitochondria. Significantly large values of the ratio (ten times larger then the baseline) indicate an acute and severe disease due to alcohol damage. If the values are five times greater than the baseline, the values can indicate chronic conditions like fatty liver, chonic hepatatis, or prolonged use of liver-damaging medication instead. 

Enzymes which are associated to liver disease due to cholestasis (impairment of flow of bile from the liver to the small intestive) include:
* ALP (`alkphos`) - Alkaline Phosphotase - not specific to the liver and can be found in a number of organs.
* GGT (`gammagt`) - Gamma-Glutamil Transpeptidase - if this enzyme is up and ALP is up, it will point to cholestasis.

Albumin, PT, and Billirubin are frequently tested for liver disease and damage but are not included in this dataset. Instead, the dataset includes Mean Corpuscular Volume (MCV, `mcv`) which measures the average red blood cell size. Size of red blood cells could increase due to increased deposition of cholesterol and phospholipids on the membranes of the cells. A healthy liver is able to remove red blood cells during maturation (typically 120 days) but a damaged liver may not be as effective [source](https://www.youtube.com/watch?v=tY-1eOoDHSU). 

Liver damage can result from many factors. Viral hepatitis, genetic conditions, illicit drug use, and use of medication can cause liver damage as well. Age, demographics, diet, and environmental factors can alter bloodwork results. Longevity and pattern of alcohol consumption play a confounding role. Therefore, we should expect that the proportion of alcohol consumption variance explained by the model of liver function tests is fairly small.

A human body is not an islated system so it is likely that some of our feautres are not indepent of each other. However, it would still be helpful to assess their relationship with our target variable in order to assess their contribution to inferring alcohol consumption. 

## Methods



## Results

## Code

## Requirements

