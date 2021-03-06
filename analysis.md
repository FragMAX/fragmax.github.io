---
layout: default
title: FragMAXapp
description: Project Management and Data Analysis
---

***

* [Data analysis](#data-analysis) 
    * [Custom paramteres](#custom-parameters)
    * [Pipedream](#pipedream)

# Data analysis

FragMAXapp offers a variety of pipelines for data analysis. The options are presented in the _Data analysis_ tab. 

![HOME](https://raw.githubusercontent.com/FragMAX/fragmax.github.io/master/assets/img/analysis1.png)

On the _top left_ corner, checkboxes gives a quick selection of datasets as follow:

|Option|Selection|
|-|-|
|Process all datasets|All datasets available in the provided shifts |
|Process new datasets|Selects all datasets that is marked in **yellow** in the home page (A.K.A. datasets that was not analysed previously|
|Select ALL datasets|This option will mark all checkboxes in the _Selected datasets_ tab |
|No checkbox checked|The datasets selected in the _Selected datasets_ will be used|


![HOME](https://raw.githubusercontent.com/FragMAX/fragmax.github.io/master/assets/img/analysis2.png)
*Dataset selection tab*

Once the minimum information is provided to a give step, the referred button will be enabled. 

| Step                      | Option                | Expected input                         | Effect                                                    | Remarks                                                                                                                           | Required |
|----------------------     |-----------------      |----------------------------------------|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|----------|
|**Data processing**        |**_Software_**         | Select the checkboxes                  | Uses the method on all selected datasets                  | Every new analysis will replace previous results                                                                                  | Yes      |
|                           |**_Space group_**      | e.g.: P43 21 2                         | The SPG provided will be used during data processing      | XDSAPP requires Space group number instead, e.g.: 96                                                                              | No       |
|                           |**_Cell parameters_**  | e.g.: (66,66,100,90,90,90)             | The Cell parameters will be used during data proessing    | Please check if the selected software supports only SPG or Cell Param. Example: XDSAPP will required both, XIA2 can take only one | No       |
|**Structure refinement**   |**_Software_**         | Select the checkboxes                  | Uses the method on all selected datasets                  | Every new analysis will replace previous results                                                                                  | Yes      |
|                           |**_PDB model_**        | Select one of the project's PDB models | Selected model will be used for structure refinement      | PDB models should be added through [Project definitions](https://fragmax.github.io/loginsetup.html#pdb-upload)                    | Yes      |
|                           |**_Space group_**      | e.g.: P43 21 2                         | The SPG provided will be used during structure refinement |                                                                                                                                   | Yes      |
|                           |**_Run aimless_**      | Select the checkboxes                  | Run aimless prior to structure refinement                 | Fixes some issues regarding alternative SPG during data processing                                                                | No       |
| **Ligand fitting**        |**_Software_**         | Select the checkboxes                  | Uses the method on all selected datasets                  | Every new analysis will replace previous results                                                                                  | Yes      |
|                           |**_SMILES to CIF_**    | Select the option                      | Convert fragment SMILES to CIF using selected method      | Fragments can be updated through [Library view](https://fragmax.github.io/loginsetup.html#library-definitions)                    | Yes      |

This options can be parsed in the screen below

![HOME](https://raw.githubusercontent.com/FragMAX/fragmax.github.io/master/assets/img/analysis4.png)

## Custom parameters

For each method, custom paramters are available. 

The tabs on the bottom of the page will provide some extra pre-selected customisations and one extra field, **Custom parameters**. 

In the Custom Parameters, it is possible to pass anything supported by the method.

```
Example:

DIMPLE 
* -M0 
    * will be used to do Molecular replacement always
* -M0 --slow 
    * will do MR and extra cycles of refinement
```

NOTE: The custom paramteres should be passed as they would in the command line version of the method. Links for the method documentation is provided below the input box.


## Pipedream 

Selecting GlobalPhasing Pipedream will open the referred tab for extra inputs. 

Please not that information passed to Pipedream will **ONLY** come from the tab. Dataset selection works as usual, from the top checkboxes selection. 





