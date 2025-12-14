# Exploring Diffusion Models' Corruption Stage in Few-Shot Fine-tuning and Mitigating with Bayesian Neural Networks (KDD 2026)

[![arXiv](https://img.shields.io/badge/arXiv-2405.19931-b31b1b.svg)](https://arxiv.org/abs/2405.19931)

Few-shot fine-tuning enables efficient personalization of diffusion models, but its training dynamics remain poorly understood.  
This work identifies a previously underexplored **corruption stage** during few-shot fine-tuning, where generation quality temporarily degrades and exhibits structured noisy artifacts before eventually recovering through overfitting. We provide a theoretical explanation showing that this phenomenon arises from a **narrowed learning distribution** intrinsic to few-shot regimes. To mitigate corruption, we introduce a Bayesian treatment of diffusion models via variational inference, which implicitly broadens the learned distribution and yields a training objective interpretable as an expectation of the diffusion loss regularized toward the pretrained model. The proposed approach is fully compatible with existing few-shot fine-tuning methods (e.g., DreamBooth, LoRA, OFT) and introduces no additional inference cost, while consistently improving fidelity, quality, and diversity across personalization tasks.

## Requirements

To install the required libraries, execute the following command:

```
pip install -r requirements.txt
```




## Usage

### Baseline Models
To fine-tune a model using the DreamBooth, LoRA, or OFT methods without BNNs, run the appropriate script:

```
bash run_scripts_baseline_dreambooth/lora/oft.sh.

```


### Models with BNNs
To fine-tune a model using the DreamBooth, LoRA, or OFT methods with BNNs, execute the following script:


```
bash run_scripts_bayes_dreambooth/lora/oft.sh.

```



## Results
The generated images can be found in the `logs` directory. Results are evaluated using the following metrics: Clip-I, Clip-T, Dino, Lpips, and Clip-IQA.

## License
This project is licensed under the Apache License 2.0.
