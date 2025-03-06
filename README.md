Graph Convolutional Network for Writer-Independent Offline  Signature Verification(SigGCN)

Input- A pair of signature images
Output:  check whether it’s an original or an forged pair by implementing and using SigGCN model.

The signature image is passed through CNN to get N feature vectors of dimension D and the position encoding with the same shape. 
Then the K nearest neighbors algorithm finds the K nearest vectors and adds an undirected edge to form a graph with N vertices.

SigGCN first transforms the images into graph structure data using CNN networks separately then inputs them into a multilayer GCN for graph representation learning to obtain the two signature graph representations individually. 
Then it measures the distance between the two representations according to the defined metric function, and then compares it with the threshold value for verification.

