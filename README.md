| [Autoencoders Keras implementation](#beta-and-gamma-model-in-keras) | [Autoencoders PyTorch implementation](#beta-and-gamma-model-in-pytorch) | [Pix2Pix](#pix2pix-model) |
| :---: | :---: | :---: |
|[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/guilbera/colorizing/blob/main/notebooks/keras_implementation/put_together_keras.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/guilbera/colorizing/blob/main/notebooks/pytorch_implementation/put_together_pytorch.ipynb) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/guilbera/colorizing/blob/main/notebooks/pytorch_implementation/put_together_pix2pix.ipynb) |

# colorizing
![Alt text](B&W_color.png?raw=true)

This is a project about colorizing black and white images using deep learning. The results are summarised in the medium blog post ["Black and White Image Colorization with Deep Learning"][1]. 3 models are implemented:
* [beta model][2], which consists of an autoencoder
* [gamma model][2], which consists of the same autoencoder with a classifier used in parallel of the encoder
* [Pix2Pix model][3], which is a GAN
The beta and gamma models are implemented in both Keras and PyTorch while the Pix2Pix model is implemented only in PyTorch. 

The dataset used for the training of the model can be downloaded [here][4] and originates from [here][5].

## Utilities
All the models use the pix utility (/notebooks/utilities/pix.ipynb) to copy the dataset from Google Drive to Google Colab and to convert RGB images to Lab images and vice versa. 

## Beta and Gamma model in Keras
The jupyter notebooks can be found in /notebooks/keras_implementation/. pix_keras.ipynb contains the dataloader. autoencoder_keras.ipynb contains the beta and gamma model implementation. put_together_keras.ipynb enables training the models in Google Colab.

## Beta and Gamma model in PyTorch
The jupyter notebooks can be found in /notebooks/pytorch_implementation/. pix_pytorch.ipynb contains the dataloader. autoencoder_pytorch.ipynb contains the beta and gamma model implementation. put_together_pytorch.ipynb enables training the models in Google Colab.

## Pix2Pix model
The jupyter notebooks can be found in /notebooks/pytorch_implementation/. It uses the same dataloader as the beta and gamma model (pix_pytorch.ipynb). pix2pix_model.ipynb contains the Pix2Pix implementation, it can output either 2 channels (Lab implementation) or 3 channels (RGB implementation). put_together_pix2pix.ipynb enables training the models in Google Colab.

All the Jupyter Notebooks can be opened directly from GitHub in Google Colab by clicking on the Google Colab badges. However, some notebooks open other notebooks as modules using the [Kora library][6]. Thus, it is recommended to copy first the repository in your Google Drive.

## Results
![Alt text](results.png?raw=true)

## Copyright
See [LICENSE](LICENSE) for details.

[1]: https://anne-guilbert.medium.com/black-and-white-image-colorization-with-deep-learning-53855922cda6 "Black and White Image Colorization with Deep Learning"
[2]: https://emilwallner.medium.com/colorize-b-w-photos-with-a-100-line-neural-network-53d9b4449f8d "How to colorize black & white photos with just 100 lines of neural network code"
[3]: https://arxiv.org/abs/1611.07004v3 "Image-to-Image Translation with Conditional Adversarial Networks"
[4]: https://drive.google.com/file/d/1hNXR_qPwNKS-z3xNQJ4fWlEWe-zES_nX/view?usp=sharing
[5]: https://www.floydhub.com/emilwallner/projects/color/43/data
[6]: https://medium.com/r/?url=https%3A%2F%2Fpypi.org%2Fproject%2Fkora%2F
