# Hierarchical Clustering Data Corpus

## Overview

This repository contains a dataset designed to support research and development in the area of 
**hierarchical clustering**. The hierarchy is maintained on the intent labels over two levels: L1 & L2.
L1 represents the high-level (or a broader) intent, while L2 represents the low-level (granular) intent.
The data corpora shared in this repository (Banking-7 and Clinc-15) are outcomes of some modifications 
done over the existing intent datasets, namely Clinc150 and Banking77.

Here is the label distribution over the two levels:

**Banking-7**: \
L1 - 7\
L2 - 77

**Clinc-15**: \
L1 - 15\
L2 - 150

The datasets are stored in the **JSON Lines (jsonl)** format, which allows for efficient storage and processing 
of large datasets.

## Usage

To use the dataset, clone this repository and load the data.
```bash
git clone https://github.com/Observeai-Research/hierarchical-clustering-data-corpus.git
````

Use the following code snippet to load the data using the `json` library in Python:
```python
import json
final_data = []
with open(file_path, 'r', encoding='utf-8') as f:
    for line in f:
        # Parse the line into a Python dictionary
        data = json.loads(line)
        final_data.append(data)

print(final_data)
```

## Acknowledgement

We acknowledge and give credit to the authors of Clinc-150 for their valuable
contribution to the research community:

    Original Authors: Stefan Larson, Anish Mahendran, Joseph J. Peper, Christopher Clarke, Andrew Lee, Parker Hill,
    Jonathan K. Kummerfeld, Kevin Leach, Michael A. Laurenzano, Lingjia Tang, Jason Mars
    Original Dataset Name: Clinc150
    Link to Original Dataset: https://github.com/clinc/oos-eval/tree/master
#####

    Original Authors: Inigo Casanueva, Tadas Temcinas, Daniela Gerz, Matthew Henderson, Ivan Vulic
    Original Dataset Name: Banking77
    Link to Original Dataset: https://github.com/PolyAI-LDN/task-specific-datasets/tree/master/banking_data