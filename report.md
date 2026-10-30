# Code Rules
--- 

## 1. Tidy Names
### Description
All names are cleaned up by trimming whitespace before and after the recipe titles, diet names, and cuisine names. All of the above names are also converted to lowercase for better consistency.

### Rule Evaluation
This is an excellent and very necessary rule that insures a basic level of input validation is present in the data, keeping starting data and any future user-added data from double counting recipies or wrongly separating recipes that are supposed to belong to the same diet.

This rule could be improved somewhat by adding some basic spell-checking or sorting the diets into pre-existing categories based on how closely they match the expected diet categories to ensure spelling errors don't cause recipes to be categorized incorrectly.

## 2. Ignore Unusable Rows
### Description
All rows are checked to ensure the row includes all the expected values for the data analysis/visualization. It checks for missing names, diets, or macro-measurements in grams. It also checks to make sure there are no negative numbers or other disqualifying issues.

### Rule Evaluation
This rule is definitely necessary, as it insures all data used by the web app contains the information needed to be analyzed as the program is intented. Anything that is missing information needed to be useful for the app's intended purpose is excluded, keeping all the information presented to the user relevant and constructive.

## 3. Ignore Duplicates
### Description
All rows are checked by name to ensure recipes are not added/counted multiple times

### Rule Evaluation
This rule is very important for ensuring the data is not skewed by double counting identical recipes. Without using this rule, it is possible for the end user to accidentally come to an incorrect or inaccurate conclusion as some recipes would essentially be unknowingly weighted much higher than others within the dataset.

## 4. Ignore Extreme Values
## Description
Some values may contain numbers that are implausible or impossible within the context of macro measurements in recipes. To address this, extremely large values that are not realistic for the fields in question will not be counted by the system.

### Rule Evaluation
This rule helps filter out both intentional and unintentional errors entered in to the dataset. All rows that are counted and used by the system will be plausible enough to be useful for analysing within the context of this application.

## 5. Allow Zeroes
### Description
The application will include values of 0 for the macros. It is not unreasonable to assume some dishes will not include macros like fat, so values of 0 will still be inclueded in the data analysis and visualization.

### Rule Evaluation
This rule makes sure that viable data is not removed just because a macro has 0 grams of a macro. Many vegitarian or vegan options may not include things like fat, and this rule ensures that all the relevant information is still used by the application.

With that considered, this rule has more use as a business rule rather than a software process. Since a row affected by this rule would already be ingested to be used by the web application, it doens't provide any real purpose and therefore is unecessary to include.

## Summary
Almost all of the rules are fairly well thought out and provide an important purpose to the program, with the exception of rule 5. The first rule could be somewhat expanded to improve input validation, but the rule 5 is completely redundant and doesn't provide any noticable impact or improvement to the program as a whole.