# Enhanced Image Description Model

---

<p align="center">
  <img src="https://miro.medium.com/v2/resize:fit:685/1*UDOnzqoTnWUQoPP8pZUXgQ.png" alt="Project Overview Concept" width="600">
  <br>
  <small>Sample Model</small>
</p>
<br>

### **University:** Queen Mary University of London
### **Course:** Computational Creativity
### **Professor:** Simon Colton
### **Student:** Erfan Rafieioskouei
<br>

---
<br>

## Project Overview

This project focuses on **Image Captioning**, a multi-modal task at the intersection of Computer Vision and Natural Language Processing. The goal is to generate relevant and descriptive text captions for given input images.

This notebook implements an enhanced image captioning system that goes beyond basic pre-trained models by training a significant component and incorporating additional features for interaction and creativity.

<p align="center">
  <img src="https://placehold.co/600x300/E8E8E8/777777?text=Image+Captioning+Concept%5Cn(Image+In+%E2%86%92+Text+Out)" alt="Image Captioning Concept Diagram">
  <br>
  <small>Conceptual Diagram of Image Captioning</small>
</p>

---

## Technical Approach

The system utilizes a deep learning architecture combining:

1.  **Image Encoding:** A pre-trained **CLIP (ViT-B/32)** model extracts rich, semantically meaningful features from the input image. The CLIP encoder itself is kept frozen to leverage its powerful pre-trained knowledge.
2.  **Caption Decoding:** A **Transformer Decoder** model generates the caption word by word, conditioned on the image features provided by the CLIP encoder.
3.  **Training:** While the CLIP encoder is pre-trained, the Transformer decoder and the interface layers between the encoder and decoder are **trained** within this notebook on the Flickr8k dataset. This allows the model to learn the specific task of generating captions relevant to the dataset's style and content.

<p align="center">
  <img src="https://placehold.co/600x350/E8E8E8/777777?text=Model+Architecture%5Cn(CLIP+Encoder+%E2%86%92+Transformer+Decoder)" alt="Model Architecture Diagram">
  <br>
  <small>Simplified Model Architecture</small>
</p>

---

## Implemented Features & Added Value

This project incorporates several features based on the course requirements and added value criteria:

* **Generative System:** The core functionality is generative – producing novel text (captions) based on image input.
* **Deep Learning:** Leverages state-of-the-art deep learning models (CLIP and Transformer).
* **Training Models:** A key component (the Transformer Decoder) is **trained** as part of the project, demonstrating the ability to adapt and train deep learning architectures rather than solely relying on pre-existing end-to-end models.
* **Multi-modal Capabilities:** Directly addresses a multi-modal task by bridging vision (images) and language (text captions).
* **User Interface:** Implements an interactive **`ipywidgets` interface** within the Colab notebook. This allows users ("casual creators") to easily upload their own images and receive generated captions directly in the notebook environment.
* **Additional Non-Deep Learning Generative Technique:** Includes a **synonym replacement** function using NLTK's WordNet. This post-processes the DL-generated caption to create simple variations, demonstrating an additional, non-DL generative approach.
* **Runs in Colab:** The entire system, including data loading, training, evaluation, and the interactive UI, is designed to run within a Google Colab notebook environment.

*(Note: Addressing higher-level philosophical issues in computational creativity is typically part of the analysis or report accompanying the technical implementation and is not directly coded within the generative system itself.)*

---

## Colab Notebook

You can find the project's Colab notebook here: [Image Description Project](https://colab.research.google.com/drive/186hpWKj7mgshIG7PhJGD76oM6X1PxccY?usp=sharing)

---
