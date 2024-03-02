# MSc (resources)

My MSc duration was **(Jan, 2020 to Jan, 2023) exactly 3 years**. By the grace of almighty Allah I have completed my course work and 1 thesis publication.
During my MSc I have taken 7 course though could not participate in the final exam of **Deep Learning for Natural Language Processing** Course. However, I have completed all it's assignment,
project and Presentation.

## MSc Course List (18 credits)

### Semester-1

**1.  Advanced Algorithm Design and Analysis**

**Projects:**
1.  Solve a KNAPSACK problem using Genetic Algorithm
2.  Reduce the number of nodes in n-Queen probelm (4*4)

**2.  Advanced Image Processing**

**Projects:**
1.  Skin Cancer detection using Convolutional Neural Network

**3.  Deep Learning for Natural Language Processing**

**Projects:**
1.  Natural Language processing usind Deep Learning (Sentiment Analysis)
2.  Presentation 

### Semester-2

**4.  Machine Learning**

**Projects:**
1. Project on Principal Component Analysis (PCA) and Singular Value Decomposition (SVD)
2. Code in SCADI dataset to analysis the effectiveness of PCA and SVD
3. Presentation

**5.  Medical Image Processing**

**Projects:**
1.  Brain Tumor Detection using Deep Learning
2.  Decoding Spatial Memory Retrieval in Cubical space using fMRI data
3.  Image Super resolution using SRGAN

### Semester-3

**6.  Cloud Computing**

**Projects:**
1. Reports on "Signnificance of cloud computing to ensure Road Safety"

### Semester-4

**7.  Neural Network**

**Projects:**
1.  An Intelligent Diagnostic System to analyze early-stage Chronic Kidney Disease for Clinical Application
2.  Code using python machine learning techniques
3.  Presentation

### Thesis (8 credits)

Topic: ***SKIN CANCER DETECTION UTILIZING INTENSITY VALUE ESTIMATION MODEL WITH A DEEP NEURAL NETWORK***

#### Thesis book (pdf) modification src:

1.  https://pdfresizer.com/crop
2.  https://smallpdf.com/
3.  https://www.img2go.com/

#### Image enhancer

1.  https://picwish.com/
2.  https://www.media.io/
3.  https://pinetools.com/sharpen-image

#### Image/ photo Edit

1.  https://www.cutout.pro/
2.  https://imageresizer.com/resize/
3.  [DeepAi-Image generator and super resolution](https://deepai.org/machine-learning-model/torch-srgan)

#### [Publication] Convert Image to High Resolution Vector Image

1.  https://vectormagic.com/

#### Draw figs

1.  https://app.diagrams.net/

#### Tpis and Tricks

1.  Use ``pdf version`` or ``EPS`` i.e. vector of every image to get the best quality
2.  Use ``Latex`` for easy and better organization
3.  Import ``pdf`` figs
4.  Use python ``matplot`` lib for ``pdf`` format image extraction
5.  Notice that no overlapping happens in ``curve and legend``
6.  Save the best ``ML models`` for future use, otherwise you will regret like me 🙄

#### Image modifications and working
1.  [Inkscape](https://inkscape.org/), Open source powerful vector editor that uses SVG as its native format. It can read and write SVG flawlessly and can export EPS.
2.  [Ghostview](https://ghostscript.com/releases/) is a free PS/EPS viewer based on Ghostscript. Ghostscript is a very complete and high-quality (PS/ EPS) parser that is capable of rasterizing most PS/EPS files.
3.  Python code (font size big (24/30), check font family, image size (w:12, h: 8) (300dpi), Ratio same, check label, X,Y ticks)
curves: desktop -> vector magic (pick color, enhance)-> save pdf, eps -> edit
[Super Resolution](https://bigjpg.com/) 20 img/month, [Image format converter](https://onlineconvertfree.com/convert/pdf/)

# Draw and Save confusion matrix as EPS

```
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.metrics import confusion_matrix

cm = [[1102, 4],
      [3, 713]]

# Set font size and font family
# plt.rcParams.update({'font.size': 30, 'font.family': 'Times New Roman'})
# plt.rcParams['font.family'] = 'sans-serif'  # Set default font to sans-serif
# plt.rcParams['font.sans-serif'] = ['Arial']  # Specify the specific sans-serif font to use
plt.rcParams.update({'font.size': 30})

# Plot confusion matrix
plt.figure(figsize=(8, 10))
sns.heatmap(cm, annot=True, fmt='d', cmap='Blues', 
            xticklabels=['0', '1'], 
            yticklabels=['0', '1'])
plt.xlabel('Predicted label')
plt.ylabel('True label')
plt.title('Confusion Matrix')

plt.savefig('confusion_matrix.eps', format='eps', dpi=300, bbox_inches='tight')
```

# Update the image with large size like 300 dpi and EPS format

```
import os
import matplotlib.pyplot as plt
import matplotlib.image as mpimg

directory = '/content/drive/MyDrive/CODE/Brain Tumor/curves/'

# Iterate over files in the directory
for filename in os.listdir(directory):
    if filename.endswith('.png'):
        # Load the PNG image
        img = mpimg.imread(os.path.join(directory, filename))
        
        width = 10  # Width in inches
        height = 8  # Height in inches
        
        fig = plt.figure(figsize=(width, height), dpi=300)
        plt.imshow(img)
        
        # Add any labels, legends, or annotations to the plot if needed
        
        eps_filename = os.path.splitext(filename)[0] + '.eps'  # Change file extension to .eps
        fig.savefig(os.path.join(directory, eps_filename), format='eps', bbox_inches='tight')
        plt.close(fig)
```

# Visualize EPS image in colab

```
from PIL import Image
eps_image = Image.open('your_eps_image.eps')
eps_image.show()
```

# Publications (4)

1.  (2022), <ins>Published in *Computer Science*</ins>, **Melanoma Skin Cancer and Nevus Mole Classification using Intensity Value Estimation with Convolutional Neural Network**, authors: **N. I. Md. Ashafuddula and Rafiqul Islam**
[Read full text here](https://journals.agh.edu.pl/csci/article/view/4844) Please cite our paper,

```
@article{Ashafuddula2022MelanomaSC, 
title={Melanoma Skin Cancer and Nevus Mole Classification using Intensity Value Estimation with Convolutional Neural Network}, 
volume={24}, 
url={https://journals.agh.edu.pl/csci/article/view/4844}, 
DOI={10.7494/csci.2023.24.3.4844}, 
number={3}, 
journal={Computer Science}, 
author={Ashafuddula, N. I. Md. and Islam, Rafiqul}, 
year={2023}, 
month={Oct.} }
```

2.  (2023), <ins>Published in *Applied Computational Intelligence and Soft Computing*</ins>, **An Intelligent Diagnostic System to analyze early-stage Chronic Kidney Disease for Clinical Application**, authors: **N. I. Md. Ashafuddula, Bayezid Islam and Rafiqul Islam**
[Read full text here](https://www.hindawi.com/journals/acisc/2023/3140270/), Please cite our paper,

```
@article{Ashafuddula2023ckd, 
title={An Intelligent Diagnostic System to Analyze Early-Stage Chronic Kidney Disease for Clinical Application}, 
volume={2023}, 
url={https://www.hindawi.com/journals/acisc/2023/3140270/}, 
DOI={10.1155/2023/3140270},  
journal={Applied Computational Intelligence and Soft Computing},
pages={17},
author={Md. Ashafuddula, N. I. and Islam, Bayezid and Islam, Rafiqul},
month={Nov.},
year={2023},
publisher={Hindawi}}
```

3.  (2023-24), <ins>*In Submission*</ins>,**IVE-MDNet: Intensity value estimation model combined with a transfer learning approach for melanoma skin cancer diagnosis**, authors: **N. I. Md. Ashafuddula and Rafiqul Islam**
   
4.  (2022-24), <ins>*Accepted with Revision*</ins> **ContourTL-Net: Contour-based Transfer Learning Algorithm for Early-stage Brain Tumor Detection**, authors: **N. I. Md. Ashafuddula and Rafiqul Islam**

# Paper writing Guideline

```
we show, the section, this paper, present/ present perfect tense
In the experiment (past,)
```

Guidelines to use of tenses in different sections of a journal/ conference/ article paper:

** Abstract:****

1. Use the ``past tense`` to summarize the ``main objectives, methods, and results`` of the study.
2. Use the ``present tense`` sparingly for ``general statements or conclusions`` that are still considered relevant.

**Introduction:**

1. Use the ``present tense`` to describe ``established facts or general truths``.
2. Use the ``past tense`` to describe previous ``research findings or studies that have already been conducted``.

**Literature Review:**

1. Use the ``present tense`` when discussing ``current theories, concepts, or findings that are still considered relevant``.
2. Use the ``past tense`` when ``referring to studies or research that has already been published``.

**Methodology:**

1. Use the ``past tense`` to describe the ``methods and procedures that were used in the study``.
2. Use the ``present tense`` to ``describe materials or instruments that are still in use or relevant.``

**Results:**

1. Use the ``past tense`` to describe the ``results obtained from the study``.
2. Use the ``present tense`` to discuss or interpret the ``findings, especially when stating general principles or conclusions``.

**Discussion:**

1. Use the ``present tense`` to discuss the ``implications of the study and its relevance to current knowledge``.
2. Use the ``past tense`` to refer to ``specific results or findings discussed ``earlier in the paper.

**Conclusion:**

1. Use the ``present tense`` to ``summarize the main findings`` of the study and to ``make recommendations`` for ``future research``.
2. Use the ``past tense`` to briefly ``recap the key points discussed in the paper``.
