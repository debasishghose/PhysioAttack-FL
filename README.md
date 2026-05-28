# PhysioAttack-FL Dataset

## Description

PhysioAttack-FL is a benchmark dataset for adversarial robustness evaluation in Federated Learning (FL) systems for Internet of Medical Things (IoMT) applications. The dataset contains feature-level representations of federated client model updates collected under both benign and adversarial conditions.

The benchmark was generated from federated learning experiments conducted on heterogeneous Raspberry Pi edge devices using physiological stress monitoring datasets. The dataset supports research on malicious client detection, robust aggregation, Byzantine resilience, and secure federated learning.

## Source Data

The dataset is derived from the following publicly available physiological datasets:

* SWELL-KW
* WESAD

Raw physiological signals are not redistributed. The dataset only contains derived statistical and geometric features extracted from federated model updates.

## Dataset Contents

Each row in the dataset represents a federated client update generated during a communication round in the federated learning process.

The dataset contains:

* Feature-engineered representations of model updates
* Benign and malicious client behaviors
* Multiple adversarial attack categories
* Model metadata and temporal information

## Features

The dataset includes the following engineered features:

* `l2_norm`
* `l1_norm`
* `max_weight`
* `mean`
* `std_deviation`
* `skewness`
* `kurtosis`
* `cosine_similarity`
* `euclidean_dist`
* `norm_growth`
* `temporal_similarity`

Additional metadata fields include:

* `timestamp`
* `client_id`
* `model`

## Labels

### Binary Attack Label

`attack`

* `0` = Benign
* `1` = Malicious

### Attack Type Label

`type`

* `0` = Benign
* `1` = Sign-Flip
* `2` = Scaling
* `3` = Label-Flipping
* `4` = Byzantine

## Federated Learning Setup

The dataset was generated using a physical cross-device federated learning testbed consisting of:

* 7 Raspberry Pi 4 devices
* 3 Raspberry Pi 5 devices
* 1 centralized federated server

## Applications

This dataset can be used for:

* Federated learning security research
* Malicious client detection
* Byzantine attack detection
* Robust aggregation evaluation
* IoMT security benchmarking
* Adversarial machine learning
* Privacy-preserving healthcare AI

## Citation

If you use this dataset in your research, please cite:

Ystebø, K. A., Johnsen, C.-E. D., Andersen, L.-E., Banik, B., & Ghose, D. (2026). Adversarially Robust Federated Learning for IoMT-based Physiological Condition Monitoring: A Benchmark Dataset and ML-Aided Aggregation Framework. Proceedings of the ACM Conference on Bioinformatics, Computational Biology, and Health Informatics (ACM-BCB), Rende, Italy. - Accepted 


## License

This dataset is provided for academic and non-commercial research purposes only.

Users are responsible for complying with the licenses and citation requirements of the original SWELL-KW and WESAD datasets.
