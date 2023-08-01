# Transformer-From-Scratch

![image](https://github.com/dikshank/Transformer-From-Scratch/assets/65603832/ebd680f7-209a-4e39-8013-e812f85f46d6)
The above image is complete transformer architecture

![image](https://github.com/dikshank/Transformer-From-Scratch/assets/65603832/b60b0ff0-0eba-4536-b6e7-ab4e93283c22)
This is the initial part of a transformer where it takes input and converts it into word embeddings and then adds the positional information in the created word embeddings.

The inputs here represent the numerical tokens of the source language. For example let's say you have a sentence ['It is a nice place'], then this will be preprocessed and we will finally convert it to a number vector like [2,3,4,5,6] where each number is just index of our word and this numbering is based on the tokenizer we use.

<font color='cyan'>THE LOGIC BEHIND POSITIONAL ENCODING</font>

Transformers are unable to get the sequence of a sentence because, unlike RNNs where we pass the sentence, in transformer we pass the complete sentence all at once so transformer have almost no understanding of the positions of these words inside sentence.

The Positional encoding are some number that we add in our word emebeddings. Let's say we have two word car and vechicle, when we have "perfect" word embeddings for both these words then we should definately see some similarity between these, because both of the words are obviously similar. And When we add positional encoding to our word embeddings then obviously these embeddings will change. So we must add positional encodings that are not too larger because we don't want to change the sementic similarity among different words by adding large numbers of position and irrespective of what word comes first, our positional encoding should remain the same. In other words, our positional encoding must not depend of the type of the word we have at any index. One possible solution what the the authors of 'Attention is all you need" applied, which is using sin and cosine function to get the positional embeddings.
