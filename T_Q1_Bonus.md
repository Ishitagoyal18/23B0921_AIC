## Vision-Based Transformers

In the research paper titled **'AN IMAGE IS WORTH 16X16 WORDS:
TRANSFORMERS FOR IMAGE RECOGNITION AT SCALE'**, the authors present an innovative application of transformer models to image recognition. This model has been highly succesful in Natural Language Processing(NLP).
But it can be used for image classification as well. Images can be broken down in smaller patches and each patch can be treated as a word in a sentence. These transformers can be processed through transformers to understand the whole image and finally the model predicts the class of the image.

![image](https://github.com/Ishitagoyal18/23B0921_AIC/assets/154070968/d0fcc334-a7ae-4129-81dd-877e68fd9c65)
<br>
<br>

### Steps

* First step to divide the image into patches, typically 16*!6 pixels. Its very much similar to dividing text sequences in tokens in NLP tasks.
* These patches are then transformed into fixed size vectors through trainable linear projection. Basically position embeddings are added to patch embeddings.
* These vectors are then passed through transformer encode layers. Eah layer consist of various other layers. Self-attention layer is included to focus on relevant parts of the image by computing attention scores between patches. A feed-forward neural network is used to capture complex patterns.
* The output of the transformer encoder is a sequence of vectors, each representing information from a different patch in the image. To obtain a single prediction for the entire image, a classification head is attached to the model. This head typically consists of a simple linear layer followed by a softmax function to produce class probabilities
* Finally, the predicted class probabilities from the softmax function are used to determine the class label for the input image. This label represents the model's prediction of what the image contains based on the learned features and patterns.
* During training, the weights of the linear projection, transformer encoder layers, and classification head are adjusted to minimize the difference between the predicted probabilities and the ground truth labels.
* Then comes the evaluation part where model is evaluated on test dataset.
* Pre trained model can be further fine tuned on specific datasets.


### Differentiation points

* The major difference in this is self attention mechanism. self-attention lets it understand how all parts of the image relate to each other, capturing distant relationships better than CNNs.
* Its more flexible and generalisable that CNN and can handle input images of arbitrary sizes.

### Acknowledgements

1. https://medium.com/@weiwen21/an-image-is-worth-16x16-words-transformers-for-image-recognition-at-scale-957f88e53726
2. https://medium.com/@faheemrustamy/vision-transformers-vs-convolutional-neural-networks-5fe8f9e18efc

Both of these sites were of great help me to understand this.




