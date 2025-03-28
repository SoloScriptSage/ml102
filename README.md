# NN101

This repo contains a basic introduction to how neural networks work, written in a straightforward and digestible way. We'll also use the MNIST dataset to teach a neural network to recognize handwritten digits.

## 🧠 How a Neuron Works

- A neuron receives inputs, each with a **weight**.
- It computes a **weighted sum** of those inputs, adds a **bias**, and produces an output.
- Mathematically, this is just a **linear function**.

## 📚 Learning Process

- Neurons **learn** by adjusting their weights and biases to minimize errors.
- The **dot product** from linear algebra is used to efficiently compute the outputs of neurons across layers.
- Since the world isn't entirely linear, we use **ReLU (Rectified Linear Unit)** to introduce **non-linearity**.

## 🔢 Making Predictions

- At the output layer, we use **Softmax** to convert raw numbers (logits) into a **probability distribution**—basically, what the network "thinks" is the right answer.

## 🎯 Measuring Error

- To determine how wrong the predictions are, we use **Categorical Cross-Entropy Loss**.
- This gives us a number that tells us how far the prediction is from the actual label.

## 🔁 Training with Backpropagation

- The network learns through **backpropagation**, which uses **partial derivatives** to figure out how much each weight contributed to the error.
- It then adjusts the weights and biases layer by layer, moving backward from the output to the input.

## ⚙️ Learning Rate & Optimization

- The **learning rate** controls how much the network changes with each update.
  - Too high? The network jumps around and never settles.
  - Too low? Learning becomes painfully slow.

- To make learning efficient, we use **optimizers**:
  - They adjust the learning rate dynamically.
  - Start with big steps, then refine gradually.
  - Common optimizers include:
    - **SGD (Stochastic Gradient Descent)** – simple and effective
    - **Momentum**
    - **Adaptive Gradients (AdaGrad)**
    - **RMSProp**

## 🧪 Dataset: MNIST

We'll use the classic **MNIST dataset** to train our neural network to recognize handwritten digits (0–9).

---

> This guide is meant to simplify complex concepts. Math can get wild under the hood, but the core ideas remain intuitive.
