# Chemprop-BP

This repository is forked from [Chemprop](https://github.com/chemprop/chemprop), a repository containing message passing neural networks for molecular property prediction.

In this repository we update and build upon the Chemprop codebase with certain desired features that are not provided by Chemprop (or did not provide at the time of our updates).

**References**: Chemprop was initially described in the paper [Analyzing Learned Molecular Representations for Property Prediction](https://pubs.acs.org/doi/abs/10.1021/acs.jcim.9b00237) for molecules and [Machine Learning of Reaction Properties via Learned Representations of the Condensed Graph of Reaction](https://doi.org/10.1021/acs.jcim.1c00975) for reactions. It now has its own dedicated manuscript: [Chemprop: A Machine Learning Package for Chemical Property Prediction](https://doi.org/10.1021/acs.jcim.3c01250).

[Installation](#installations) <br>
(0) clone repo <br>
(1) Create and activate conda env
```
conda create -n chemprop-bp python=3.9 pip
```
```
conda activate chemprop-bp
```
(2) Check for GPU on machine
```
nvidia-smi
```
(3) Install (GPU compatible) PyTorch
```bash
python -m pip install torch torchvision torchaudio
```
(4) Install dependencies
```bash
conda install -c conda-forge \
  flask>=1.1.2 \
  gunicorn>=20.0.4 \
  hyperopt>=0.2.3 \
  matplotlib>=3.1.3 \
  numpy>=1.18.1 \
  pandas>=1.0.3 \
  pandas-flavor>=0.2.0 \
  pip>=20.0.2 \
  rdkit>=2020.03.1.0 \
  scikit-learn>=0.22.2.post1 \
  scipy>=1.4.1 \
  tensorboardX>=2.0 \
  tqdm>=4.45.0 
```
(5) Setup & Install chemprop-BP package (editable)
```
  python -m pip install -e .
```
(6) Check chemprop-BP installation
```
python -m pip show chemprop-BP
```



[Modifications](#modifications) <br>

(0a) Binary Classification - flag: --dataset_type classification <br>
Example: ```chemprop_train --data_path <data_path> --dataset_type classification```

(0b) Binary Classification + class weighted loss: <br>
Example: ```chemprop_train --data_path <data_path> --dataset_type classification --class_weighted_loss```

(1) Class weighted loss (cross entropy) - flag: --class_weighted_loss <br>
Example: ```chemprop_train --data_path <data_path> --dataset_type multiclass --multiclass_num_classes 3 --class_weighted_loss```

(2) Task specific layers/towers - flag: --task_specific_ffn <br>
Example: ```chemprop_train --data_path <data_path> --dataset_type classification --task_specific_ffn```

(3) Multi-layer FFN - arguments
