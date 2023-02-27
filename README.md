# UniDL4BioPep_ASL_PyTorch

## Welcome
Here, you will see a simple piece of code applies the methodology proposed in the research paper **UniDL4BioPep: A universal deep learning architecture for binary classification in peptide bioactivity** with the [ASL function](https://github.com/Alibaba-MIIL/ASL) aiming for better performances on imbalanced datasets.

You may be curious about our main [Github repository](https://github.com/dzjxzyd/UniDL4BioPep), in which you will see more playable datasets and experimental details.

## System requirements
To play with this piece of code, simply, ```cd``` to the working directory;<br>
```
conda env create -f environment.yml
```
And you will have all the requirements set.

## Usage
At the very beginning of ```apply.ipynb```, you will be able to see marked-up comments 'changeable.'
```
train_l_file = os.path.join(os.getcwd(), "alternative_ACP_train.xlsx")  # changeable
train_d_file = os.path.join(os.getcwd(), "train_embedded.csv")
test_l_file = os.path.join(os.getcwd(), "alternative_ACP_test.xlsx")  # changeable
test_d_file = os.path.join(os.getcwd(), "test_embedded.csv")
```
You can leave ```d_file```s as they are and change ```l_file```s to any other excel documents.

**Hyparameters for tunning in your own dataset**
Go to the ```class AsymmetricLoss(nn.Module); class ASLSingleLabel(nn.Module); class AsymmetricLossOptimized(nn.Module)```, then you can find two parameters ```gamma_neg=4, gamma_pos=1```
The Spirit of ASL function is to adjust the two parameters to obtain a better performance. The detailed information about the three ASL function, please refer to [ASL function](https://github.com/Alibaba-MIIL/ASL).

## 
Here we present an template of the usage of UniDL4BioPep_ASL_PyTorch on one of our benchamrk datasets (anticancer peptide dataset).
**The default parameter is gamma_neg=4, gamma_pos=1**

