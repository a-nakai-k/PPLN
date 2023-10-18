# Pretrained Protein Language model-based Network

Python implementation of Pretrained Protein Language model-based Network (PPLN).
CCS value prediction using pretrained deep protein language model (ESM-1b) as a feature extractor from peptide sequences 
and estimation neural network (NN) requiring training.
<img width="407" alt="ppln" src="https://github.com/a-nakai-k/PPLN/assets/40450686/da500608-4224-4884-8ca9-74e5cdb739ec">



## Requirements
- Pytorch
- numpy

## Run
1. Prepare csv files for training and test
   - for training of estimation NN: with amino-acid sequence, CCS value, charge, and mass data
   - for test: with amino-acid sequence, (CCS value,) charge, and mass data 
3. Run preprocessing.py
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
