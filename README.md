# INFO 527 — Neural Networks  
## Assignment 4: Convolution and Recurrent Networks

### Objectives
The objectives of this assignment are to:
1. Implement **Convolutional Neural Networks (CNNs)** and **Recurrent Neural Networks (RNNs)** using TensorFlow Keras.  
2. Understand how these architectures handle sequential and spatial data.  
3. Train, test, and evaluate deep learning models on image and text datasets.  
4. Experiment with dropout, regularization, and early stopping to improve generalization.

This assignment extends the previous work on feedforward networks by introducing architectures suited for **sequence modeling** and **image classification**.

---

### Files in This Repository
| File | Description |
|------|--------------|
| `notebooks/nn.ipynb` | Main notebook containing implementations of convolutional and recurrent neural networks. |
| `notebooks/nn.py` | Exported Python version of the notebook used for pytest testing. |
| `notebooks/convolution_and_recurrent_networks.ipynb` | Notebook for running tests and recording pytest results. |
| `results/nn.html` | Exported HTML version of the notebook for grading and readability. |
| `tests/test_nn.py` | Provided test file used to validate correctness using pytest. |
| `README.md` | This file, describing objectives, setup, and submission workflow. |
| `requirements.txt` | Python dependencies for reproducibility. |
| `.gitignore` | Specifies intentionally untracked files to keep the repository clean. |

---

### Functions to Implement (in `nn.py`)
You will complete the following four TensorFlow Keras model creation functions:

| Function | Description | Marks |
|-----------|--------------|-------|
| `create_toy_rnn(input_shape, n_outputs)` | Creates a simple **Recurrent Neural Network** that learns to predict \(x_{t-3} - y_t\) from sequential input pairs. | 3 |
| `create_mnist_cnn(input_shape, n_outputs)` | Builds a **Convolutional Neural Network (CNN)** for digit classification using the **MNIST** dataset. | 4 |
| `create_youtube_comment_rnn(vocabulary, n_outputs)` | Constructs an **RNN** for **YouTube Spam Comment classification**, processing tokenized text sequences. | 4 |
| `create_youtube_comment_cnn(vocabulary, n_outputs)` | Builds a **CNN** for the same YouTube spam detection task using 1D convolutions. | 4 |
| **Total Marks** |  | **15 marks** |

---

### Environment Setup
This project reuses the shared environment created for previous assignments.

```bash
# Activate your existing environment
source ~/venvs/ml-env/bin/activate

# Navigate to the assignment directory
cd ~/projects/info527-neural-networks-assignment4

# Install dependencies
pip install -r requirements.txt
````

**requirements.txt**

```
tensorflow>=2.13
keras>=2.13
numpy>=1.24
pytest>=7.0
jupyter>=1.0
ipykernel>=6.0
```

---

### Testing Instructions

1. Run all cells in `nn.ipynb` to complete your implementations.
2. Export your work as:

   * `nn.ipynb`
   * `nn.html`
   * `nn.py`
3. Place the exported `nn.py` file in the same directory as `test_nn.py`.
4. In Google Colab, upload the required dataset files into a `data/` folder:

   * `mnist.hdf5`
   * `Youtube01-Psy`, `Youtube02-KatyPerry`, `Youtube03-LMFAO`, `Youtube04-Eminem`, `Youtube05-Shakira`
   * `youtube-comments.hdf5`
5. Run the provided testing notebook `convolution_and_recurrent_networks.ipynb` and execute:

```bash
pytest tests/test_nn.py
```

**Expected Output:**

```
============================= test session starts ==============================
collected 4 items

test_nn.py ....                                                        [100%]

============================== 4 passed in XX.XXs ===============================
```

---

### Submission Files

Submit the following files for grading:

* `nn.ipynb`
* `nn.html`
* `nn.py`
* `convolution_and_recurrent_networks.ipynb` (with pytest results)

---

### Repository Information

**Repository name:** `info527-neural-networks-assignment4`
**Description:** Implementation of convolutional and recurrent neural networks using TensorFlow Keras. Includes CNNs for image and text classification, RNNs for sequence modeling, and experiments with dropout and early stopping. Part of the Master’s in MIS/ML program at the University of Arizona.

---

### Author

This repository was completed as part of INFO 527: Neural Networks, under the M.S. in Information Science and Machine Learning program (2023–2025).
