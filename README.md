# Small Molecular Generation for Drug Discovery


 <div align="center">
    <a href="https://colab.research.google.com/github/reshalfahsi/molecular-generation-drug-discovery/blob/master/Small_Molecular_Graph_Generation_for_Drug_Discovery.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="colab"></a>
    <br />
 </div>


With the advent of deep learning, [drug development](https://en.wikipedia.org/wiki/Drug_development) can be sped up just by learning the patterns within the molecules regarding their chemical properties and composition. The pursuit of good candidates for drugs can be achieved using the generative model which can extrapolate the unseen molecular structure. In this project, one of the most popular generative models, ``Generative Adversarial Network`` or ``GAN``, is utilized. The generator of GAN consists of MLP, and the discriminator of GAN consists of R-GCN + MLP. Nowadays, there are plenty of open-sourced datasets that can be used for this purpose such as the ``QM9 (Quantum Machines 9) dataset``. The GAN model is trained on QM9 dataset and its performances are assessed by means of [molecular metrics](https://github.com/nicola-decao/MolGAN/blob/master/utils/molecular_metrics.py), i.e., quantitative estimate of druglikeness (QED), solubility (defined as the log octanol-water partition coefficient or logP), synthetizability, natural product, drug candidate, valid, unique, novel, and diversity.


## Experiment


All of the experiments are summed up in this [notebook](https://github.com/reshalfahsi/molecular-generation-drug-discovery/blob/master/Small_Molecular_Graph_Generation_for_Drug_Discovery.ipynb).


## Result

## Quantitative Result

The performance of the model through a normally distributed latent vector sample in ``6561`` runs against the ``QM9 dataset`` is presented below.

Metrics | Score |
------------ | ------------- |
QED |  0.406 |
Solubility | 0.317 |
Synthetizability | 0.344 |
Natural Product | 0.758 |
Drug Candidate | 0.478 |
Valid | 0.797 |
Unique | 0.033 |
Novel | 0.790 |
Diversity | 0.567 |


## Loss Curve

<p align="center"> <img src="https://github.com/reshalfahsi/molecular-generation-drug-discovery/blob/master/assets/loss_curve.png" alt="loss_curve" > <br /> GAN's generator and discriminator loss curve in the training process. </p>


## Qualitative Result

Here are some samples of the qualitative results of the model.

<p align="center"> <img src="https://github.com/reshalfahsi/molecular-generation-drug-discovery/blob/master/assets/qualitative_result.png" alt="qualitative_result" > <br /> The qualitative results of the generated molecules. The chemical structure, the SMILES representation, and the QED scores are provided. </p>


## Credit

- [Drug Molecule Generation with VAE](https://keras.io/examples/generative/molecule_generation/)
- [WGAN-GP with R-GCN for the generation of small molecular graphs](https://keras.io/examples/generative/wgan-graphs/)
- [Modeling Relational Data with Graph Convolutional Networks](https://arxiv.org/abs/1703.06103)
- [(Paper) MolGAN: An implicit generative model for small molecular graphs](https://arxiv.org/abs/1805.11973)
- [(Code) MolGAN: An implicit generative model for small molecular graphs](https://github.com/nicola-decao/MolGAN)
- [PyTorch-GAN](https://github.com/eriklindernoren/PyTorch-GAN)
- [RDKit](https://github.com/rdkit/rdkit)
- [PyTorch Lightning](https://lightning.ai/docs/pytorch/latest/)
