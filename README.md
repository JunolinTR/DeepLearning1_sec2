**Deep Learning -1**

Byte Club

Blog generation project using fine-tuned Language models

Summary of Project Report

The objective of this project is to fine-tune a language model in order to produce an appropriate heading for paragraphs using a Google Colab environment with acceleration using the T4 GPU. We started with the work of preparing the dataset. In our case, a CSV file containing the results of data scraping was uploaded to Google Drive. Further, access via Colab was performed by mounting the drive. The preprocessing started with the importing of the required libraries, loading the CSV file into a pandas DataFrame, and cleaning by handling duplicates, null values, and outliers. Further, paragraphs with word counts over 200 were removed.

Our fine-tuning approach followed the LED model-Longformer Encoder Decoder. Preprocessing steps involved tokenization, setting up batch sizes, and splitting into training, validation, and test sets. The validation set was small to allow for rapid iteration; in a practical case, it would need to be larger. After an hour, the fine-tuned model ran approximately 100 steps and saved checkpoints.

We also did some configuration for the training setup, and monitored performance with the ROUGE metric. We stored checkpoints in the "files" section of Colab. At the end, we made a few tests about the model efficiency using the checkpoint-100 and observing how well the model was capable of generating an appropriate heading of paragraphs given to the system.
