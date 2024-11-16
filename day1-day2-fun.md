Day 1 Fun:
- __High Creativity Mode__: Set temperature to around 0.8–1.0, raise top_k (e.g., 100–500), and increase top_p close to 1.0 to encourage novel and varied responses.

- __Conservative Mode__: Lower top_p (e.g., 0.8) or reduce top_k to around 20 for tighter, more on-topic responses—ideal for precision-focused tasks.

- __Extreme Outputs__: Push boundaries by maxing out temperature and top_k, combining with top_p=1.0, to explore the "edges" of the model's response space, which can produce fun, unpredictable results.

Day 2 Fun:
- High-Dimensional Embeddings + High Dropout Rate + t-SNE Visualization
Parameters:
Embedding Dimension: 256
Dropout Rate: 0.7
Learning Rate: 0.01
Expected Easter Egg: High-dimensional embeddings with heavy dropout create unique patterns in the embedding space. Visualize using t-SNE to find unexpected clusters or “hidden” class relationships, revealing how the model groups seemingly unrelated features.

- Low-Dimensional Embeddings + Early Stopping + High Batch Size
Parameters:
Embedding Dimension: 5
Batch Size: 512
Early Stopping: Patience of 1 or 2 epochs
Expected Easter Egg: The model might classify most items into a few broad categories due to limited embedding dimensions. This can yield quirky results as early stopping kicks in before the model converges, creating partial or humorous misclassifications.

- Extreme Regularization + Small Batch Size + Learning Rate Decay
Parameters:
L2 Regularization on Embedding Layer: 0.01
Batch Size: 4
Learning Rate Decay: From 0.01 to 0.0001 over epochs
Expected Easter Egg: Extreme regularization limits the flexibility of the embedding layer, while small batch sizes make learning noisy. This might cause the model to “forget” details over time, leading to unique, fluctuating predictions as learning rate decay kicks in.

- Random Embedding Initialization + High Learning Rate + High Dropout Rate
Parameters:
Embedding Initialization: Random Normal
Learning Rate: 0.1
Dropout Rate: 0.5
Expected Easter Egg: This combination can make the model behave erratically in early epochs, producing strange classification patterns. Watching the training loss in early epochs might show zigzag patterns or unexpected spikes.

- Tiny Embedding Dimension + Low Learning Rate + Batch Normalization
Parameters:
Embedding Dimension: 2
Learning Rate: 0.001
Batch Normalization: Applied after the embedding layer
Expected Easter Egg: With only two dimensions, the embedding space is heavily constrained, and batch normalization might amplify minor differences. The model could produce extreme or binary-like classifications, treating slight input changes as major category shifts.

- Swish Activation + High Regularization + Early Stopping
Parameters:
Activation: Swish (a unique, smooth activation function)
L1 + L2 Regularization: 0.005 each
Early Stopping Patience: 3 epochs
Expected Easter Egg: Swish activation adds a non-linear twist that can create surprising embeddings when combined with regularization. Early stopping may cause it to halt with partially formed clusters, revealing quirky or incomplete representations.

- Very High Batch Size + Low-Dimensional Embedding + PCA Visualization
Parameters:
Embedding Dimension: 3
Batch Size: 1024
PCA for Visualization: Reduced to 2D space
Expected Easter Egg: High batch size on a limited embedding space may lead to overlapping clusters. Visualizing with PCA could reveal patterns where different classes overlap or form unexpected “bubbles” in the embedding space.

- Extreme Dropout + Low Embedding Dimension + Sigmoid Activation on Final Layer
Parameters:
Embedding Dimension: 5
Dropout Rate: 0.9
Activation on Final Layer: Sigmoid (suitable for binary or extreme classification)
Expected Easter Egg: High dropout and low embedding dimension force the model to operate with minimal information, leading to random or highly simplified classifications. This setup can yield extreme output values, potentially misclassifying items in humorous or unexpected ways.

- High Embedding Dimension + Cyclical Learning Rate Schedule + Intermediate Output Visualizations
Parameters:
Embedding Dimension: 128
Learning Rate: Cycles between 0.001 and 0.1 every few epochs
Intermediate Layer Outputs: Visualize after each learning rate cycle
Expected Easter Egg: Cyclical learning rates can reveal “waves” in training behavior, where the model oscillates between converging and diverging. Intermediate visualizations show the embeddings reshaping in real time, potentially creating dynamic patterns.
Residual Connections in Embedding Layers + Dense Layer Visualizations + t-SNE
Parameters:
Embedding Dimension: 64
Residual Connections: Shortcuts between embedding layers
t-SNE Visualization: Visualize dense layer outputs after embeddings
Expected Easter Egg: Residual connections within embedding layers create interactions that may lead to unexpected embeddings. Using t-SNE on the dense layers could reveal “loops” or circular clusters, hinting at unique patterns in how data points relate.
