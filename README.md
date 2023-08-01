# Transformer-From-Scratch

![image](https://github.com/dikshank/Transformer-From-Scratch/assets/65603832/ebd680f7-209a-4e39-8013-e812f85f46d6)

The above image is complete transformer architecture

Transformer models, first introduced in the paper "Attention is All You Need" by Vaswani et al., are a type of model architecture used in the field of deep learning, particularly for handling sequential data in tasks such as language translation, text summarization, sentiment analysis, etc. The key innovation of transformer models is the self-attention mechanism, which allows the model to weigh the relevance of each part of the input sequence when producing an output.

Here's a simplified description of how to implement a transformer model from scratch:

Embedding Layer: First, the input data (usually text) is converted into vectors using an embedding layer. This could be a simple learned embedding or a pre-trained embedding like Word2Vec or GloVe.

Positional Encoding: Transformers do not inherently capture the order of the data (since they are not recurrent like RNNs or LSTMs), so positional encoding is added to the input embeddings to incorporate the sequence order.

Self-Attention Mechanism: This is the key innovation of the transformer model. Self-attention allows the model to look at an input sequence and determine which parts are relevant to each other. The output of this layer is a weighted sum of the inputs, where the weights are determined by the attention scores.

Feed-Forward Neural Networks: After the self-attention layer, the data is passed through a couple of feed-forward neural networks. The output of these networks is then normalized and added to the input of the layer (this is called a residual connection).

Encoder and Decoder: The architecture mentioned above constitutes an encoder. In a full transformer model, there are multiple such encoders stacked together. Similarly, the model has a set of decoders which are also stacked together. The final output of the model is passed through a linear layer and a softmax function to produce the predictions.

Training: Like other deep learning models, transformer models are trained using stochastic gradient descent (or a variant thereof). The models are usually trained in a supervised manner, i.e., with a large dataset of inputs and corresponding target outputs.

Fine-tuning: Once a transformer model has been pre-trained, it can be fine-tuned on a specific task using a smaller amount of task-specific data.

Implementing transformers from scratch requires a good understanding of machine learning and deep learning principles, linear algebra, calculus. Most commonly, high-level APIs such as TensorFlow and PyTorch are used to implement Transformers (I have used Tensorflow), which simplify the implementation but still require understanding the underlying principles. It's also important to note that training transformer models typically requires significant computational resources (often GPUs).



