# Question Paraphrases Dataset For Turkish Language
This data set contains 1377 question paraphrases for Turkish Languages. 
The original questions are taken from Istanbul Bilgi Universitiy Frequently Asking Questions resource 
https://www.bilgi.edu.tr/tr/yasam/ogrenci/sss/. Later,we manually added two additional truly semantically equivalent additional questions. These quesitons pairs are considered postivie example of the quesiton paraphrasing.  2187 

We also supplemented the dataset with 2187 negative examples labeled as 0. The source of negative examples are be pairs of "related questions" which, although pertaining to similar topics, are not truly semantically equivalent. It would be very much like Quora Question Pairs
https://www.quora.com/q/quoradata/First-Quora-Dataset-Release-Question-Pairs


## Paraphrasing Detection
To do classify wheter two questions are duplicate, we can train a simple classification algorithm.
We plan to implement a ML-based paraphrase question detection model for Turkish language. It would be very helpfull especially for ChatBot framework in Turkish Language.


