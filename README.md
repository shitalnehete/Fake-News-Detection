## Abstract:
The spread of fake news remains a critical issue that threatens the integrity of commerce, journalism, and democracy worldwide, often
with disastrous consequences. In our project, we leveraged the LIAR dataset, which contains real-life political statements, to identify instances of fake news. Our approach not only takes into account the statement itself but also incorporates crucial information about the speaker, subject, context, affiliation, and occupation to develop both binary and six-class classification models that categorize statements according to varying levels of falsity, ranging from true to pants on fire. Our model yielded impressive results, achieving an accuracy rate of 0.75 for binary classification and 0.34 for six-class classification. By taking a more comprehensive approach to detecting fake news, we hope to contribute to the fight against the spread of misinformation and disinformation in today’s world.

## How to run
To conduct experiments using the provided code, you can run the main.py file. If you want to train a model, set the mode variable to "train". If you want to evaluate a saved model, set mode to "test" and provide the path to the saved model in the pathModel variable. The code supports two datasets: LIAR and LIAR-PLUS, which can be selected by setting the dataset_name variable accordingly. The current implementation produces binary results.

If you want to use the BERT model, you can use the BERT_DAPT_LIAR.py file for training and the test.py file for testing. When running the test.py file, you need to provide the path to the checkpoint file to be used for testing. We have tested the code using the bert_model_test_roberta_binary.pth checkpoint file, which corresponds to the RoBERTa model with domain adaptive pretraining.


## Results

| Model         | Accuracy      | metric|
| ------------- |:-------------:|:-----:|
| Baseline for CNN with attention & BiLSTM  | 0.63    | 0.24 |
| Baseline with BERT| 0.75      |   0.32 |
|CNN with attention & GRU | 0.61	| 0.25 |
| BERT with domain adaptive  pre-fine tuning | 0.75 | 0.34 |