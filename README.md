<h1 align="center"> Understanding Cognitive Skills Development in Large Language Models: A Comparative Analysis of Errors in Complex Language Tasks </h1>
<h3 align="center">Adi Sharfaizen, Tomer Klaiman, Matan Abudy</h3>
This is the code for "Understanding Cognitive Skills Development in Large Language Models: A Comparative Analysis of Errors in Complex Language Tasks," a final project in the Natural Language Processing course at Tel-Aviv University. The course was taught by Maor Ivgi, and the project was supervised by Samuel Amouyal.

# Data

The data comprises two experiments conducted at Tel Aviv University. In these experiments, participants were presented with various sentences, followed by two options for completion that gauged their comprehension of the given sentence. For instance:

Sentence: "The banker that you praised climbed the mountain just outside of town before it snowed."
True completion: "You praised the banker."
False completion: "The banker praised you."

It is important to note that prior to conducting our experiment and testing, we had to preprocess the data in order to construct the two completions and to appropriately tag them as either True or False.


# Usage

This repository includes two Colab notebooks. One notebook is for the evaluation of data using the MultiBERTs family of
models, and the other is for the evaluation of data using the Pythia family of models.

## MultiBERTs
In MultiBERTs, we evaluate the models using 3 seeds - 0, 1, and 2. This can be configured in the notebook by setting
the `SEEDS_TO_TEST` variable. One can also set the different training steps to evaluate by adjusting the `STEPS_TO_TEST`
variable, currently set to 0, 40, 100, 140, and 200.

## Pythia
In Pythia, we evaluate all model sizes - 70M, 410M, and 1B (defined in `model_size_list`). We also test on steps 1,
35000, 75000, 110000, and 143000, defined in the `checkpoint_step_list`.