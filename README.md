# MIMO
semi-supervised MIMO, a construction of Scientific Knowledge  Graph 

## ENV

torch/0.4.0, python/2.7.14

The versions of python in training and predicting shoud be the same!!! (the pre-trained model was in python2, so please run extractor with python2, or you will get wrong prediction.) 

## Quick Start: RUN Extractor



## TRAIN MODEL

mkdir models
mkdie results

### Supervised MIMO (single featrue with multi-input gates):
 
python train.py --cuda --config 000111000 --language_model ./models/LM/model.pt --wordembed ./models/WE/pubmed-vectors=50.bin

### Supervised MIMO (multi-input gates, multi-input ensembles):

python train_ensemble.py --cuda --config 111 --language_model ./models/LM/model.pt --wordembed ./models/WE/pubmed-vectors=50.bin

### Semi-supervised MIMO (single featrue with multi-input gates)

python main_self_training.py --cuda --language_model ./models/LM/model.pt --wordembed ./models/WE/pubmed-vectors=50.bin --check_point ../models/supervised_model_011000000.torch --AR --TC --SH --DEL

## DOWNLOAD
DropBox link: 
