# LightGAT

Graphical models have been used extensively for recommendation systems. With deep learning revolutionising the world from data science to healthcare, it was natural that graphical models would adapt to this field by introducing new paradigms like Graph Neural Networks (GNNs). Graph Convolutional Networks, a class of GNNs have been used to mimic the use of Convolutional Neural Networks (CNN) on images for applications in graph classification and node labelling. He et al. have used such an approach to link items to users. They have simplified the GCN for optimization, including only the aggregation part. 

## Proposed Network

In our proposed layer, named LightGAT layer, we utilize the attention mechanism employed in the GAT layer. The attention mechanism is defined by equation (1), where W represents the transformation matrix, and X denotes the embedding of the subscripted node.

eAB = linear(concat(W XA, W Xb)) (1)

However, we deviate from the traditional approach by excluding the transformation matrix W and allowing all the learning to be conducted within the linear layer, as shown in equation (2).

eAB = linear(concat(XA, Xb)) (2)

Similar to the approach in [1], we also omit the use of nonlinear activation functions during the embedding generation process. Consequently, our message passing step can be described by equation (3), where a represents the softmax of the corresponding e values. 

XA[l + 1] = X u auAXu[l], u ∈ N(A) (3)

## Conclusion

Throughout this project, we discovered that by tinkering with the underlying mechanisms of the Graph Neural Network, we can achieve varying outcomes, which may or may not meet our expectations. Such adjustments can serve to expedite the algorithm or reduce processing time, enhancing overall efficiency. Furthermore, this exploration allows us to devise unique algorithms that may not be universally applicable but prove effective for our specific objectives. In this study, we conducted our tests using the Karate Club dataset. However, this approach can be expanded to incorporate additional and larger datasets, such as the AmazonBlock and Gowalla datasets employed in [1]. By incorporating these diverse datasets, we can further validate the effectiveness and scalability of our strategies. Additionally, this strategy of exploration and modification can be extended to different types of networks, including GraphSAGE, to evaluate their performance in similar tasks. Furthermore, this approach holds promise for compressing heterogeneous graphs, presenting opportunities for experimentation and refinement. The potential benefits of these techniques extend beyond graph-related tasks and can be leveraged in various domains such as natural language processing and computer vision.
