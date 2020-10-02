# Question Paraphrases Dataset For Turkish Language
This data set contains 1377 positive question paraphrases for Turkish Languages and 2187 negative examples. 
The original questions are taken from Istanbul Bilgi Universitiy Frequently Asking Questions resource 
https://www.bilgi.edu.tr/tr/yasam/ogrenci/sss/. Later,we manually created two additional truly semantically equivalent questions. These quesitons pairs are considered postivie example of the quesiton paraphrasing. 

## Negative Sampling:
We also supplemented 2187 negative examples labeled as 0. The source of negative examples are be pairs of "related questions" which, although pertaining to similar topics, are not truly semantically equivalent. It would be very much like Quora Question Pairs
https://www.quora.com/q/quoradata/First-Quora-Dataset-Release-Question-Pairs


## Paraphrasing Detection
To do classify wheter two questions are duplicate, we trained a simple classification algorithm based on BERT. It would be very helpfull especially for ChatBot framework in Turkish Language.

Following code shows how to run the detection model 


```
from transformers import *
import torch
from transformers import AutoTokenizer, AutoModelForSequenceClassification
tokenizer = AutoTokenizer.from_pretrained("savasy/TurkQP")
model = AutoModelForSequenceClassification.from_pretrained("savasy/TurkQP")


s0="Bugün yağmur yağacak mı ?"
s1="Yağmur yağabilir mi bugün ?"
inputs= tokenizer(s0, s1, add_special_tokens=True, return_tensors='pt')
output= pytorch_model(inputs['input_ids'], token_type_ids=inputs['token_type_ids'])[0]
pred = output.argmax().item()

pred==1

```

