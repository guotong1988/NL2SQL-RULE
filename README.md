# NL2SQL-BERT

[![LICENSE](https://img.shields.io/badge/license-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE)

Content Enhanced BERT-based Text-to-SQL Generation https://arxiv.org/abs/1910.07179

# Requirements

python 3.6

records 0.5.3   

torch 1.1.0   

# Run

1, Data prepare:

`data_and_model/output_entity.py`

2, Train and eval:

`train.py`

# Results on BERT-Base-Uncased without EG
| **Model**   | Dev <br />logical form <br />accuracy | Dev<br />execution<br/> accuracy | Test<br /> logical form<br /> accuracy | Test<br /> execution<br /> accuracy |
| ----------- | ------------------------------------- | -------------------------------- | -------------------------------------- | ----------------------------------- |
| SQLova    | 80.6                      | 86.5                  | 80.0                        | 85.5                   |
| Our Methods | 84.3                      | 90.3                | 83.7                      | 89.2 |

# Data
One data look:
```
{
	"table_id": "1-1000181-1",
	"phase": 1,
	"question": "Tell me what the notes are for South Australia ",
	"question_tok": ["Tell", "me", "what", "the", "notes", "are", "for", "South", "Australia"],
	"sql": {
		"sel": 5,
		"conds": [
			[3, 0, "SOUTH AUSTRALIA"]
		],
		"agg": 0
	},
	"query": {
		"sel": 5,
		"conds": [
			[3, 0, "SOUTH AUSTRALIA"]
		],
		"agg": 0
	},
	"wvi_corenlp": [
		[7, 8]
	],
	"bertindex_knowledge": [0, 0, 0, 0, 4, 0, 0, 1, 3],
	"header_knowledge": [2, 0, 0, 2, 0, 1]
}
```

All origin data:

https://drive.google.com/file/d/1iJvsf38f16el58H4NPINQ7uzal5-V4v4

# Trained model

https://drive.google.com/open?id=18MBm9qzobTBgWPZlpA2EErCQtsMhlTN2

# Reference 

https://github.com/naver/sqlova
