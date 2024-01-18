# Chemprop-BP

This repository is forked from [Chemprop](https://github.com/chemprop/chemprop), a repository containing message passing neural networks for molecular property prediction.

In this repository we update and build upon the Chemprop codebase with certain desired features that are not provided by Chemprop (or did not provide at the time of our updates).

**References**: Chemprop was initially described in the paper [Analyzing Learned Molecular Representations for Property Prediction](https://pubs.acs.org/doi/abs/10.1021/acs.jcim.9b00237) for molecules and [Machine Learning of Reaction Properties via Learned Representations of the Condensed Graph of Reaction](https://doi.org/10.1021/acs.jcim.1c00975) for reactions. It now has its own dedicated manuscript: [Chemprop: A Machine Learning Package for Chemical Property Prediction](https://doi.org/10.1021/acs.jcim.3c01250). Please cite these papers if Chemprop is helpful to your research.


[Modifications](#modifications) <br>

(1) Class weighted loss (cross entropy) - flag: --class_weighted_loss <br>
Example: ```chemprop_train --data_path <data_path> --dataset_type multiclass --multiclass_num_classes 3 --class_weighted_loss```
