***<span style="font-size: 3em;">:warning:</span>You must agree to the [license](https://github.com/Sinhala-NLP/NSINA?tab=License-1-ov-file#readme) and terms of use before using the dataset in this repo.***

# Sinhala News Category Prediction
This is a text classification task created with the [NSINA dataset](https://github.com/Sinhala-NLP/NSINA). This dataset is also released with the same license as NSINA. Given the news content, the ML models should predict a pre-defined category for the news. 


## Data
First, for this task, we dropped all the news articles in NSINA 1.0 without a category as some news sources prefer not to categorise them. Next, we identified the top 100 news categories from the available news instances. We grouped possible categories into four main categories: local news, international news, sports news, and business news.
Data can be loaded into pandas dataframes using the following code. 

```python
from datasets import Dataset
from datasets import load_dataset

train = Dataset.to_pandas(load_dataset('sinhala-nlp/NSINA-Categories', split='train'))
test = Dataset.to_pandas(load_dataset('sinhala-nlp/NSINA-Categories', split='test'))
```

## Citation
If you are using the dataset or the models, please cite the following paper.

~~~
@inproceedings{Nsina2024,
author={Hettiarachchi, Hansi and Premasiri, Damith and Uyangodage, Lasitha and Ranasinghe, Tharindu},
title={{NSINA: A News Corpus for Sinhala}},
booktitle={The 2024 Joint International Conference on Computational Linguistics, Language Resources and Evaluation (LREC-COLING 2024)},
year={2024},
month={May},
}
~~~
