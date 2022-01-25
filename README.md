# UIT-ViSD4SA PACLIC 35
## General Introduction
This repository contains the data of the paper: Span Detection for Vietnamese Aspect-Based Sentiment Analysis. 

UIT-ViSD4SA is a benchmark Vietnamese smartphone feedback dataset for ABSA and span detection. UIT-ViSD4SA consisting of 35,396 human-annotated spans on 11,122 feedback comments, and each is manually annotated according to its spans towards ten fine-grained aspect categories with sentiment polarities. We split the dataset into a training set (7,784), a development set (1,113) and a test set (2,225) randomly.
## Data Example
![examle](https://github.com/kimkim00/UIT-ViSD4SA/blob/main/example.png)
## Read File
```python
!pip install jsonlines

import jsonlines

data = []

with jsonlines.open('train.jsonl') as f:

    for line in f.iter():
       
        data.append((line['text'], {'labels': line['labels']}))
```
## Citation
Please cite the following paper if you found it useful in your work.

````
@inproceedings{thanh-etal-2021-span,
    title = "Span Detection for {V}ietnamese Aspect-Based Sentiment Analysis",
    author = "Thanh, Kim Nguyen Thi  and
      Khai, Sieu Huynh  and
      Huynh, Phuc Pham  and
      Luc, Luong Phan  and
      Nguyen, Duc-Vu  and
      Van, Kiet Nguyen",
    booktitle = "Proceedings of the 35th Pacific Asia Conference on Language, Information and Computation",
    month = "11",
    year = "2021",
    address = "Shanghai, China",
    publisher = "Association for Computational Lingustics",
    url = "https://aclanthology.org/2021.paclic-1.34",
    pages = "322--332",
}
````

## Contact
