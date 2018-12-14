# eslint-config-pop
Eslint configuration with the most popular configurations found in the npm registry.

## Contents
 1. [Procedure](#procedure)
 2. [Results](#results)
 3. [How To Use](#how-to-use)
 
## Procedure
We went ahead and download top projects from the npm registry that make use of EsLint. 
We ended up with a total of **388 individual repositories**.

Our goal is to find which are the most popular option done  by developers for the EsLint configuration fields.
The fields are:

- `extends`
- `env`
- `plugins`
- `parserOptions`
- `parser`
- `rules`
- `ecmaFeatures`
- `overrides`
- `settings`
- `globals`
    
A field may appear in the configuration or not. In the latter case, it means that the default configuration given by the EsLint 
Configuration is used.
We counted how many times each field appeared. We then found out all the possible configurations a field can take and counted their 
appearences as well.

You can check out all the configuration details in the [EsLint Configuration Page](https://eslint.org/docs/user-guide/configuring).

Finally, we were able to create out own configurations files (.eslintrc.json) with the most popular options between developers.

**_Note_**: In our choice we exluded fields that appeared in less than 80 out of 387 repositories (approximately 1/5). We made 
and exception for `globals`, and we excluded. The reason is that every developer uses his own global variables that are different 
from project to project. 


## Results
We created 2 configuration files for EsLint both in _.json_ and _.yaml_ format.
-`popEslintrcSimple.json popEslintrcSimple.yaml`
-`popEslintrc.json popEslintrc.yaml`

The two first ones are simple and contain just the most popular option for each field. 
In the two second ones the parameters for populrity weren't just the top choice. In order for an option to be included the following 
criteria should be met:

- the number of times this option is used must be higher than the mean of all options appearences
- the number of times this option is used must be higher than 10
- this option must not be contradictory or a redundancy to a more popular option that has alreaby been included

The first ones are great for a beginner to start working with EsList , because they consist of the simplest and most popular settings.
The second ones are better for more experienced developers that want for detailed and accurate results.

We also created two more _.json_ files with the statistics for all the fields.

- `popConfig.json`
  It contains all the fields except `rules`. For each field there is the property setting and the property timesUsed. Declaring what 
  is the option for that field and how many times it was used.
  
- `popRules.json`
   This is the exact equivalent but only for the field rules. The seperation has been made because of the huge amount of data in the rules 
   field. 
   
 **_Important Note:_** In the last two files every field has a setting called default. It means that this field hasn't appeared in a repo
 so its settings are set to default.
   
   
## How To Use
You can download our configuration files, save them as `.eslintrc.json` or `.eslintrc.yaml` add them to your project folder and start 
working with EsLint.

For more information/details visit the [EsLint Page](https://eslint.org/).

