# **Abstractive Text Summarization with BART**

### Bidirectional Autoregressive Transformer (BART) is a Transformer-based encoder-decoder model, often used for sequence-to-sequence tasks like summarization and neural machine translation. BART is pre-trained in a self-supervised fashion on a large text corpus. During pre-training, the text is corrupted and BART is trained to reconstruct the original text (hence called a "denoising autoencoder"). Some pre-training tasks include token masking, token deletion, sentence permutation (shuffle sentences and train BART to fix the order), etc.


## **Dataset**
###  SAMSum dataset, This dataset contains around 15,000 pairs of conversations/dialogues and summaries. It was available on [This link](https://huggingface.co/datasets/Samsung/samsum). The dataset has two fields:
* dialogue
* summary 

## **Fine-tune BART**
### <p style="text-align: justify"'>The choice of the BART model in the provided code example is just one of many possibilities. BART (Bidirectional and Auto-Regressive Transformers) is a transformer-based model that has shown strong performance in various natural language processing tasks, including abstractive text summarization. It was pre-trained on a denoising autoencoder objective, which makes it proficient at generating coherent and contextually relevant summaries. **We use sequence lengths of 512 and 128 for the encoder and decoder, respectively, instead of 1024 (which is the default sequence length). This will allow us to run this example quickly on Colab.**</p>

## Hyperparameters
```python
BATCH_SIZE = 8
NUM_BATCHES = 600
EPOCHS = 10  # Can be set to a higher value for better results
MAX_ENCODER_SEQUENCE_LENGTH = 512
MAX_DECODER_SEQUENCE_LENGTH = 128
MAX_GENERATION_LENGTH = 40
```

## **Model Summary**
![image](https://github.com/mrjoneidi/Abstractive-Text-Summarization-with-BART/assets/132068610/13c2f8dc-ed82-4a31-82e4-1f8eaaee2356)

## **I reached Losss = 0.049 and Accuracy = 0.93 in 10 epochs**

