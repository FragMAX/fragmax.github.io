---
layout: default
title: FragMAXapp
description: Quick tutorial for FragMAXapp
---

# Login Credentials

Username and password are provided by the hosting site. 

At MAX IV Laboratory, this is provided by the [User Office](https://duo.maxiv.lu.se/duo/) and it is the same across the facility

![FragMAXapp](https://raw.githubusercontent.com/FragMAX/fragmax.github.io/master/assets/img/login-pic.png)

# Project Setup

If you don't have any projects yet, this will be your landing page
![Project-setup](https://raw.githubusercontent.com/FragMAX/fragmax.github.io/master/assets/img/project-setup.png)

| Field             | Expected input    |
|:------------------|:---------------------------------------------------------------------------------|
| **Protein**           | Protein name as declared in ISPyB/EXI                                            |
| **Library Name**      | Fragment library name as declared in ISPyB/EXI                                   |
| **Library fragments** | CSV file containing fragments definitions. See how to create this file [HERE](#library-definitions)      |
| **Proposal number**   | FragMAX project proposal number |
| **Shifts**            | If the site you are using FragMAXapp supports it, input the visits according to local format (e.g.: MAX IV -> 20201022)      |
| **Data Processing**   | Enable/Disable encryption mode for data processing |


## Library definitions

mylibrary.csv
```
A01a,O=C1N[C@@H](CO1)C1=CC=CC=C1
A01b,CN1CCCCS1(=O)=O
A02a,CC1=CC=C(S1)C1=CC(=NN1)C(O)=O
A02b,CC1=CC(C)=NC=N1
```

### Standard fragment libraries definitions
**FragMAXlib**

FragMAXlib is formulated via in-house fragment collection of FragMAX. FragMAXlib is an XFS-focused library, specifically designed for FragMAX operations. The library is in a constant refinement cycle and is periodically updated, depending on the fragment performance in screening experiments, new chemotypes in a commercial chemical space and platform updates. FragMAXlib compounds are selected on the basis of their fragment-likeness and synthetic tractability. Currently, the library has 110 entries.

| Descriptor        | min               | max               | mean              |
|:------------------|:------------------|-------------------|-------------------|
| Mw                |108                | 269               | 158               |
| Num heavy atoms   |8                  | 18                | 11.2              |
| SlogP             |-0.7               | 2.6               | 1                 |
| Num. H-bonds acc. | 1                 | 5                 | 2.5               |
| Num. H-bonds don. | 0                 | 2                 | 0.9               |
| Num. rot. bonds   | 0                 | 3                 | 1                 |

Library definitions CSV. ![Download here](https://raw.githubusercontent.com/FragMAX/fragmax.github.io/master/assets/lib/FragMAXlib.csv)
_yay_

[back](./)
