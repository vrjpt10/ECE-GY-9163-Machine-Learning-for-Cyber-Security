
# Backdoor Detector
This is a project to design a backdoor detector for BadNets trained on the YouTube Face dataset using the pruning defense.

#### Methodology

As stated in the instructions, the pruning was performed on the `conv_3` layer. It was intended to be done in accordance with the decreasing order of average activation values throughout the validation dataset.
The validation accuracy of the new pruned badnet was measured and recorded everytime a channel was pruned.

The models were saved when accuracy dropped by at least 2%, 4%, and 10% and were recorded under the names, `B_prime0.h5`, `B_prime1.h5`, and `B_prime2.h5` respectively. You can find them in the `Models` folder. Their weights are in `Weights` folder.

#### Deployment

Requirements for running the code:

- Access to enough execution memory (Google Colab Pro is preferable).
- Google drive link for accessing [clean dataset](https://drive.google.com/file/d/1HK1nkl22TNJUxm41bfhhIoU0XexlGqnl/view?usp=sharing) and [poisoned dataset](https://drive.google.com/file/d/1LcOWje2yRguY1CJd61xetIliQ0tUXJ2g/view?usp=sharing). You can also access it from [here](https://drive.google.com/drive/folders/1Rs68uH8Xqa4j6UxG53wzD0uyI8347dSq).

The program is available in the `Homework_2.ipynb` file.

#### Observations

The following changes were observed in the accuracy on clean test data and the attack success rate (on backdoored test data) as a function of the fraction of channels pruned (X).

![](https://github.com/vrjpt10/Machine-Learning-for-Cyber-Security/blob/main/Lab-2/Screenshot/accuracy-asr-x.jpg)
### Author

- [Vaishnavi Rajput](https://www.github.com/vaishnavirjpt10/)

