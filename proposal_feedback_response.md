Can you describe in a bit more detail what you plan to do for the CNN + RNN or CNN + LSTM architecture? In general, RNN and LSTM models are used for variable-length inputs, e.g., if you have a text document that might have 100 or 1000 words, but you want the model to be able to adapt to either one. In your dataset, are there any variable-length inputs? Or are there sequences of images per patient/scan?


        The primary motivation for the  CNN + RNN or CNN + LSTM architecture comes from this paper: https://www.sciencedirect.com/science/article/pii/S2352914820305621. Our dataset does not contain variable length inputs or sequences, however in the aforementioned paper this was also the case. And yet using a CNN +LSTM architecture, the authors were able to achieve a better accuracy using the combined model and so we wanted to adapt that methodology for our project.


You mention using pretrained models in your first Desired Goal. Do you know of models that were pre-trained on some sort of medical images? While a model trained on generic images (e.g., ImageNet) might have some benefit on this task, a model trained on medical images will likely be more effective.

        The model we found is https://github.com/Tencent/MedicalNet. However, it is pre-trained on 3D medical images which are different from our dataset which consists of 2D images.

        In the realm of pre trained Residual Neural Nets of 2D datasets, the one we want to look at is RESNET50 (https://pytorch.org/vision/main/models/generated/torchvision.models.resnet18.html) it is a model within pytorch that was trained on ImageNet and that is properly documented. While it has not been trained on medical data, it seems like the best choice due to the model being offered by a reputable organization and it is of the right architecture (ResCNN). 


Can you make your first Stretch Goal more specific? This is a very reasonable approach for running experiments to determine the importance of different hyperparameters, but it’s not necessarily a “stretch.” You could spend anywhere between a few hours and a few months depending on how many experiments you choose to run; that’s going to make it hard to evaluate how much progress you’ve made towards your goals.

        We will focus on varying the following hyperparameters: the number of hidden layers and nodes, learning rate, the kernel sizes and also include Batch normalization and evaluate how those specific changes/combinations of changes impact our performance in order to find the best-performing combination of architectures. We will then work on optimizing those specific hyperparameters in order to further improve our performance.


Do you have a specific multiclass dataset in mind for your second Stretch Goal?

        Yes
        https://huggingface.co/datasets/alkzar90/NIH-Chest-X-ray-dataset
        This dataset contains 15 possible classes and would thus make a perfect multiclass dataset.
