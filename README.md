# Pretrained Protein Language model-based Network

Python implementation of Pretrained Protein Language model-based Network (PPLN).
CCS value prediction using pretrained deep protein language model as a feature extractor from peptide sequences 
and estimation neural network (NN) requiring training.

<img width="407" alt="ppln" src="https://github.com/user-attachments/assets/344eb457-9125-43f3-b07b-6e4b7aee6b89">




## Requirements
- Pytorch
- numpy

## Data
The MS raw data used for obtaining trained model (trainedmodel.pt) and analysis files have been deposited with the ProteomeXchange
Consortium (http://proteomecentral.proteomexchange.org) via the jPOST partner
repository (https:// jpostdb.org) with the data set identifier PXD046201.

The file "trainedmodel.pt" is the model trained using the above data.
ESM-1b (Rives et al., 2021) was used as the pretrained deep protein language model.


## CCS prediction with trained model (trainedmodel.pt)
1. Prepare csv file for test: with amino-acid sequence, charge, and mass data
2. Run preprocessing.py for the csv file
3. Run main_trained.py (Output: out_test_predictCCS.csv)

## CCS prediction with training on your data
1. Prepare 2 csv files, one for training and one for test
   - for training of estimation NN: with amino-acid sequence, CCS value, charge, and mass data
   - for test: with amino-acid sequence, (CCS value,) charge, and mass data 
3. Run preprocessing.py for each csv file
4. Run main.py (Output: out_test_predictCCS.csv)


## License
This project is licensed under the MIT License, see the LICENSE file for details.

## Author
[Ayano NAKAI-KASAI](https://sites.google.com/view/ayano-nakai/home/english)

Graduate School of Engineering, Nagoya Institute of Technology

nakai.ayano@nitech.ac.jp

## References
- Alexander Rives, Joshua Meier, Tom Sercu, Siddharth Goyal, Zeming Lin, Jason Liu, Demi Guo,
Myle Ott, C. Lawrence Zitnick, Jerry Ma, and Rob Fergus. Biological structure and function emerge
from scaling unsupervised learning to 250 million protein sequences. Proceedings of the National
Academy of Sciences, 118(15):e2016239118, 2021. [github](https://github.com/facebookresearch/esm)
