# Language translation Model README

This README file provides instructions on how to run the model and evaluate its performance.

NOTE: Use google collaboratory

## Setup

To run the model, you need to install the required packages. Run the following command in your terminal: 

!pip install datasets transformers[sentencepiece] sacrebleu -q

## Dataset

The model uses the IITB English-Hindi dataset, which can be loaded using the `load_dataset` function from the `datasets` library. The dataset can be accessed using the `raw_datasets` variable.

## Preprocessing

The data is preprocessed using the Helsinki-NLP/opus-mt-en-hi model. The `AutoTokenizer` class from the `transformers` library is used to tokenize the input sentences. The maximum input and target lengths are set to 128.

## Training

The model is trained using the `TFAutoModelForSeq2SeqLM` class from the `transformers` library. The training data is prepared using the `prepare_tf_dataset` function, and the `DataCollatorForSeq2Seq` class is used for data collation. The model is compiled and trained using the `fit` function.

## Saving the Model

After training, the model is saved using the `save_pretrained` function.

## Model Testing

To test the model, you need to load the saved model and tokenizer. The `AutoTokenizer` and `TFAutoModelForSeq2SeqLM` classes are used for this purpose. You can then provide an input text to the model and generate the translated output.

Please refer to the code for more details on how to run the model 