# MNIST with PyTorch

> Author: Pablo Blanco

Created a CNN for MNIST competition in [Kaggle](https://www.kaggle.com/competitions/digit-recognizer) as I am learning the framework of PyTorch.


# Architecture
The architecture I used for my CNN was inspired in the one that you can read [here](https://www.kaggle.com/code/cdeotte/how-to-choose-cnn-architecture-mnist/notebook) by [@cdeotte](https://www.kaggle.com/cdeotte).

It is the next one:
```
Model(
  (conv1): Sequential(
    (0): Conv2d(1, 32, kernel_size=(3, 3), stride=(1, 1))
    (1): ReLU()
    (2): Conv2d(32, 32, kernel_size=(3, 3), stride=(1, 1))
    (3): ReLU()
    (4): Conv2dSame(32, 32, kernel_size=(5, 5), stride=(2, 2))
    (5): ReLU()
    (6): Dropout2d(p=0.4, inplace=False)
  )
  (conv2): Sequential(
    (0): Conv2d(32, 32, kernel_size=(3, 3), stride=(1, 1))
    (1): ReLU()
    (2): Conv2d(32, 64, kernel_size=(3, 3), stride=(1, 1))
    (3): ReLU()
    (4): Conv2dSame(64, 64, kernel_size=(5, 5), stride=(2, 2))
    (5): ReLU()
    (6): Dropout2d(p=0.4, inplace=False)
  )
  (out): Sequential(
    (0): Flatten(start_dim=1, end_dim=-1)
    (1): Linear(in_features=1024, out_features=128, bias=True)
    (2): ReLU()
    (3): Dropout(p=0.4, inplace=False)
    (4): Linear(in_features=128, out_features=10, bias=True)
  )
)
```

# Results
I got a Score of **0.97014** in the submission I uploaded. Getting me to rank as 1543 position in the leaderboard. You can find it.

