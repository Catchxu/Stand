STANDS is a powerful documentation framework to detect, align and subtyping anomalous tissue domains across multiple samples. In the subsequent sections, we will introduce the preparatory tasks before utilizing STANDS for your research, including the installation of Python packages, downloading of datasets, and other related procedures.




## Installation
STANDS is developed as a Python package. You will need to install Python, and the recommended version is Python 3.9.5.

You can download the package from GitHub and install it locally:

```commandline
git clone https://github.com/Catchxu/STANDS.git
cd STANDS/
python3 setup.py install
```




## Datasets
All experimental datasets involved in this paper are available from their respective original sources: the 10x-Visium datasets of healthy human breast tissues (10x-hNB datasets) are available at [CELLxGENE](https://cellxgene.cziscience.com/collections/4195ab4c-20bd-4cd3-8b3d-65601277e731); The 10x-Visium datasets of human breast cancer tissues (10x-hBC datasets) are available at [github](https://github.com/almaan/her2st/tree/master); The 10x-Visium datasets of human primary sclerosing cholangitis tissue (10x-hPSC datasets) and human liver caudate lobe tissue are available at [CELLxGENE](https://cellxgene.cziscience.com/collections/0c8a364b-97b5-4cc8-a593-23c38c6f0ac5); The 10x-Visium datasets of human renal cell cancer tissue (10x-hRCC datasets) are available at [Gene Expression Omnibus](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE175540); The scRNA-seq dataset of human pancreatic ductal (sc-hPD) and 10x-Visium datasets of the human pancreatic ductal adenocarcinomas (10x-hPDAC) are available at [Gene Expression Omnibus](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE111672); The slide-seqV2 datasets of mouse embryo tissues (ssq-mEmb datasets) are available at [CELLxGENE](https://cellxgene.cziscience.com/collections/d74b6979-efba-47cd-990a-9d80ccf29055); The Stereo-seq datasets of mouse embryo tissue (Stereo-mEmb datasets) are available at [STOmicsDB](https://db.cngb.org/stomics/mosta/). 

Additionally, if you have trouble with preprocessing data, we have prepared organized and processed small datasets for your reference. In addition, these demo datasets are also used in the tutorials. You can download the demo datasets from [Google Drive](https://drive.google.com/file/d/17SUwJp0q2UwAMiVfQn4gSRJwef1hkG0G/view?usp=sharing). Here, V05-V07 (as reference datasets) and G2, H1 (as target datasets) have been zipped.


## Pretrained weights
Considering that STANDS uses a pretrained visual extractor, we also provide pretrained weights, which you can download from [Google Drive](https://drive.google.com/file/d/1uhwaoSdTZ0ihqkEeW4IuH0DbyQpce8kh/view?usp=sharing). The model here is pre-trained on human breast tissue. If it needs to be applied to other tissues, it may be necessary to re-pretrain to obtain the best results, even though it may not be necessary in many cases.

Additionally, we also provide trained weights, including generator and discriminator, for the processed demo dataset (also human breast tissue). You can download them from [Google Drive](https://drive.google.com/file/d/1N_He2EpjNhqsRpFXx6-4Mnb4h81r1H3V/view?usp=sharing). The weights here can be directly loaded into the model for anomaly detection. At the same time, if you only need batch alignment, these weights can also help you skip the anomaly detection step.


## Getting help
Please see the tutorial for more complete documentation of all the functions of STANDS. For any questions or comments, please use the [GitHub issues](https://github.com/Catchxu/STANDS/issues) or directly contact Kaichen Xu at the email: kaichenxu358@gmail.com.




## Tested environment
### Environment 1
- CPU: Intel(R) Xeon(R) Platinum 8255C CPU @ 2.50GHz
- Memory: 256 GB
- System: Ubuntu 20.04.5 LTS
- Python: 3.9.15

### Environment 2
- CPU: Intel(R) Xeon(R) Gold 6240R CPU @ 2.40GHz
- Memory: 256 GB
- System: Ubuntu 22.04.3 LTS
- Python: 3.9.18




## Dependencies
- anndata>=0.10.7
- dgl>=2.1.0
- networkx>=3.2.1
- numpy>=1.22.4
- pandas>=1.5.1
- Pillow>=9.4.0
- PuLP>=2.7.0
- pyemd>=1.0.0
- rpy2>=3.5.13
- scanpy>=1.10.1
- scikit_learn>=1.2.0
- scipy>=1.11.4
- torch>=2.0.0
- torchvision>=0.15.1
- tqdm>=4.64.1