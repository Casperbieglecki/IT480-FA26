# Lab 0: GitHub Setup & Python Foundations for Deep Learning

**Estimated time:** 60–75 minutes (mostly in-class, finish remaining "Try it yourself" prompts as homework)
**Submission:** Two links on Canvas — your GitHub repo URL, and your completed notebook URL
**Due:** Before Session 2

## Learning Objectives

By the end of this lab, you will be able to:
- Use GitHub's fork → edit → commit workflow (used for every lab this semester)
- Perform vectorized array operations and matrix multiplication in NumPy
- Load, inspect, and filter tabular data with Pandas
- Create basic plots with Matplotlib
- Explain what matrix multiplication has to do with a neural network

## Part A — GitHub Setup (do this first)

1. If you don't already have one, create a free GitHub account at [github.com](https://github.com).
2. Go to the main course repository (link posted in today's Canvas announcement).
3. Click **Fork** (top right) to create your own copy under your GitHub account.
4. Open Google Colab (`colab.research.google.com`) → **File → Open notebook → GitHub tab** → paste your forked repo's URL → open `Lab0/hello_deep_learning.ipynb`.
5. Run the first cell (environment check):
```python
   import numpy, pandas, matplotlib, sklearn, tensorflow
   print("Environment OK — all libraries loaded")
   print("TensorFlow version:", tensorflow.__version__)
```
6. Add a markdown cell with your name, then go to **File → Save a copy in GitHub**, select your fork, and commit with a message like `"Lab 0: initial commit"`.
7. Check your GitHub repo in the browser — confirm your commit shows up.

*(Working locally in VS Code instead of Colab? Clone your fork with `git clone <your-fork-url>`, make the same edit, then `git add . && git commit -m "Lab 0: initial commit" && git push`.)*

## Part B — NumPy: Vectors and Matrix Multiplication

In a new cell, import NumPy. Then:
1. Create two vectors of your choosing (at least 3 elements each) and compute their dot product.
2. Create two 2×2 matrices and compute their matrix product.
3. Simulate a simple neuron: create an `inputs` array, a `weights` array (same length), and a `bias` value. Compute `output = dot(inputs, weights) + bias`.

**Try it yourself:** Change your weights and inputs and observe how the output changes. Add one more input and matching weight — does it still work? Why or why not?

## Part C — Pandas: Working with Tabular Data

1. Load the Iris dataset (`sklearn.datasets.load_iris`, `as_frame=True`).
2. Print the first 5 rows and summary statistics.
3. Filter the dataframe to rows where petal length is greater than 5 cm. How many rows match?
4. Group the data by species (`target`) and compute the average of each measurement.

**Try it yourself:** Filter the dataframe on a different condition of your choosing, and print how many rows match.

## Part D — Matplotlib: Basic Plotting

1. Create a scatter plot of petal length vs. petal width, colored by species.
2. Label your axes and give the plot a title.

**Try it yourself:** Make a second plot comparing two different columns from the dataset.

## Part E — Bonus (optional): See a Real Model Run

Using `tensorflow.keras.applications.MobileNetV2` (pretrained, `weights='imagenet'`), load one of the sample images in `Lab0/sample_images/`, preprocess it to 224×224, and run inference. Print the top 3 predicted classes using `decode_predictions`.

This loads a model already trained on 1.4 million images and asks it to classify a photo it's never seen — the same basic pattern (load a pretrained model, run inference) you'll use later this semester on the Jetson.

## What Gets Done in Class vs. at Home

Parts A–D are walked through live in class. If you don't finish every "Try it yourself" prompt during class, finish them at home — the pattern will already be familiar from following along.

## Deliverables Checklist

- [ ] Forked repo with at least one commit visible in GitHub history
- [ ] Parts A–D completed and run successfully, with your own answers to each "Try it yourself" prompt
- [ ] Part E attempted (optional, for extra practice)

## Grading Rubric (20 points)

| Criterion | Points |
|---|---|
| GitHub fork created with at least one commit | 5 |
| NumPy exercises completed correctly | 4 |
| Pandas exercises completed correctly | 4 |
| Matplotlib plots produced correctly | 4 |
| "Try it yourself" prompts answered thoughtfully | 3 |
