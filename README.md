# DeepStruct
Protein Secondary Structure Prediction Using Recurrent Neural Networks

## 
Knowing the structure of a protein is essential in understanding
its biological function. However, current methods such as
x-ray diffraction can take many years and cost tens of
thousands of dollars to analyze one single protein. Fortunately,
we have analyzed the state of the art models for problems in
sequence analysis and time series prediction. In this paper we
propose the application of a Bidirectional Recurrent Neural
Network (BRNN) to predict a proteins secondary structure
using only it’s residue sequence. BRNNs capture future
information through forward and backward states, which is
useful in secondary structure prediction, where context is
important. Recently, recurrent neural networks have been
shown to produce good results for natural language processing.
We aim to leverage this technology to push the state of the art
closer to the theoretical accuracy limit of 88-90%.


Recurrent Neural Networks (RNN) have been successfully
used for text classification in recent years. Since protein
sequences tend to have many dependencies on the previous
values, we believe that using an RNN might yield significant
improvements over using one dimensional convolutional net-
works, such as the ones used in DeepCNF. Protein sequences
may also have dependencies on previous values too, thus we
use a two layer Bidirectional Recurrent Neural Network, each
with 128 hidden units. The BRNNs are followed by multiple
dense layers, with 32, 64, 16, and 8 units each respectively.
With this configuration we noticed some overfitting in the later
epochs, so we added a dropout of 0.1 after each of the dense
layers, except the final output.

