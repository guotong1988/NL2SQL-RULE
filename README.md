# NL2SQL-BERT

Content Enhanced BERT-based Text-to-SQL Generation https://arxiv.org/abs/1910.07179

# Run

1, Data prepare:

`data_and_model/output_entity.py`

2, Train and eval:

`train.py`

# Results on BERT-Base-Uncased without EG
| **Model**   | Dev <br />logical form <br />accuracy | Dev<br />execution<br/> accuracy | Test<br /> logical form<br /> accuracy | Test<br /> execution<br /> accuracy |
| ----------- | ------------------------------------- | -------------------------------- | -------------------------------------- | ----------------------------------- |
| SQLova    | 80.6                      | 86.5                  | 80.0                        | 85.5                   |
| Our Methods | 84.3                      | 90.0                | 83.7                      | 89.2 |

# Reference 

https://github.com/naver/sqlova
