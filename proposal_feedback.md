### Proposal Feedback

8/10

This looks great, but please answer a few clarifying questions for full points.

Can you describe in a bit more detail what you plan to do for the CNN + RNN or CNN + LSTM architecture? In general, RNN and LSTM models are used for variable-length inputs, e.g., if you have a text document that might have 100 or 1000 words, but you want the model to be able to adapt to either one. In your dataset, are there any variable-length inputs? Or are there sequences of images per patient/scan?

You mention using pretrained models in your first Desired Goal. Do you know of models that were pretrained on some sort of medical images? While a model trained on generic images (e.g., ImageNet) might have some benefit on this task, a model trained on medical images will likely be more effective.

Can you make your first Stretch Goal more specific? This is a very reasonable approach for running experiments to determine the importance of different hyperparameters, but it’s not necessarily a “stretch.” You could spend anywhere between a few hours and a few months depending on how many experiments you choose to run; that’s going to make it hard to evaluate how much progress you’ve made towards your goals.

Do you have a specific multiclass dataset in mind for your second Stretch Goal?
