# Privacy-Preserving Multimodal Sentiment Analysis
This project includes the codes and some results of our paper.
We follow the framework for the [ACM MM 2020] paper [MISA: Modality-Invariant and -Specific Representations for Multimodal Sentiment Analysis].
<font color='red'>However, we modify the codes of models in "models.py" using a new autoencoding architecture.</font>

### Setup the environment

We work with a conda environment.

```
conda env create -f environment.yml
conda activate DPCRL
```

### Data Download

- Install [CMU Multimodal SDK](https://github.com/A2Zadeh/CMU-MultimodalSDK). Ensure, you can perform ```from mmsdk import mmdatasdk```.    
- Option 1: Download [pre-computed splits](https://drive.google.com/drive/folders/1IBwWNH0XjPnZWaAlP1U2tIJH6Rb3noMI?usp=sharing) and place the contents inside ```datasets``` folder.     
- Option 2: Re-create splits by downloading data from MMSDK. For this, simply run the code as detailed next.

### Running the code

1. ```cd src```
2. Set ```word_emb_path``` in ```config.py``` to [glove file](http://nlp.stanford.edu/data/glove.840B.300d.zip).
3. Set ```sdk_dir``` to the path of CMU-MultimodalSDK.
2. ```python train.py --data mosi```. Replace ```mosi``` with ```mosei``` or ```ur_funny``` for other datasets.
