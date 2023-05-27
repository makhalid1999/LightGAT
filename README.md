# LightGAT

Graphical models have been used extensively for recommendation systems. With deep learning revolutionising the world from data science to healthcare, it was natural that graphical models would adapt to this field by introducing new paradigms like Graph Neural Networks (GNNs). Graph Convolutional Networks, a class of GNNs have been used to mimic the use of Convolutional Neural Networks (CNN) on images for applications in graph classification and node labelling. He et al. have used such an approach to link items to users. They have simplified the GCN for optimization, including only the aggregation part. 

## Proposed Network

In our proposed layer, named LightGAT layer, we utilize the attention mechanism employed in the GAT layer. The attention mechanism is defined by equation (1), where W represents the transformation matrix, and X denotes the embedding of the subscripted node.
eAB = linear(concat(W XA, W Xb)) (1)
However, we deviate from the traditional approach by excluding the transformation matrix W and allowing all the learning to be conducted within the linear layer, as shown in equation (2).
eAB = linear(concat(XA, Xb)) (2)
Similar to the approach in [1], we also omit the use of nonlinear activation functions during the embedding generation process. Consequently, our message passing step can be described by equation (3), where a represents the softmax of the corresponding e values. XA[l + 1] = X u auAXu[l], u ∈ N(A) (3)
