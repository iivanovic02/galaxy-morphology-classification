\# Galaxy Morphology Classification

This is an image classifier that uses the ResNet-18 model to identify the morphological class of a galaxy.



\## Hardware and Support:

\- The notebook was configured for NVIDIA GPU machines that run CUDA.

\- \*\*AMD/Mac Users:\*\* The notebook will default to CPU but for GPU utilisation, check the links below for command line installation prompts:

&#x20;- \[ROCm (AMD)](https://pytorch.org/get-started/locally/)

&#x20;- \[MPS (Mac)] (https://developer.apple.com/metal/pytorch/)



\## Evaluation \& Results:

The model managed to achieve a test accuracy score of \*\*90.1%\*\* after 10 epochs of training. Below is the confusion matrix which shows the performance across each galaxy class. We see that it performs very well in identifying \*\*spiral\*\* and \*\*completely round smooth\*\* galaxies but gets confused with \*\*cigar-shaped\*\* and \*\*edge-on\*\* galaxies.



!\[Confusion Matrix](CM.png)



\*\*Model Inference:\*\*

Below is an example prediction of M82, otherwise known as the cigar galaxy, with confidence levels.



!\[M82 Example](predict\_galaxy\_example.png)



\*\*Batch Visualisation:\*\*

A random sample of images plotted with their corresponding true and predicted labels.



!\[Subplot Images](subplots\_example\_image.png)



\## How to run:

1. Install dependencies with: `pip install -r requirements.txt`
2. Download the images dataset from \[Galaxy Zoo classification](https://www.kaggle.com/datasets/anjosut/galaxy-zoo-classification) and place them in the `Train\_images` folder in the same directory as the notebook.
3. Open `classifier.ipynb` and run the whole notebook from top to bottom (restart and run all). From here, the `predict\_galaxy` function at the bottom can be run as many times as desired, so long as there are images in `demo\_images` (a few are included).

