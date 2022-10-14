# Discriminative Visual Similarity Search with Semantically Cycle-consistent Hashing Networks
Here is the official codebase for `Discriminative Visual Similarity Search with Semantically Cycle-consistent Hashing Networks`. 
[MMAsia2022 Version](https://dl.acm.org/doi/abs/10.1145/3469877.3490583)  
[Extended TOMM Version](https://dl.acm.org/doi/abs/10.1145/3532519)  
This repo contains two versions of SCHN(the original SCHN on MMAsia2022 and the one with the discriminator TOMM). You can specify the variant by the `method_name` constant in `run.py`(Line 18).

## REQUIREMENTS
`requirements.txt` contains libraries used in my environments. Though other versions may also work, I have no time to test and can't guarantee any of that.

## DATASETS
1. [CIFAR-10](http://www.cs.toronto.edu/~kriz/cifar-10-python.tar.gz)

2. [NUS-WIDE](https://pan.baidu.com/s/1f9mKXE2T8XpIq8p7y8Fa6Q) Password: uhr3

3. [MIR-Flickr](https://press.liacs.nl/mirflickr/) 25K version

## Project Structure
The structure of the project files should go as follows.

```
.
├── data
│   ├── cifar10.py
│   ├── data_loader.py
│   ├── flickr25k.py
│   ├── imagenet.py
│   ├── __init__.py
│   ├── nus_wide.py
│   └── transform.py
├── dataset
│   ├── cifar-10-batches-py
│   │   ├── batches.meta
│   │   ├── data_batch_1
│   │   ├── data_batch_2
│   │   ├── data_batch_3
│   │   ├── data_batch_4
│   │   ├── data_batch_5
│   │   ├── readme.html
│   │   └── test_batch
│   ├── Flickr
│   │   ├── database_label.txt
│   │   ├── db_image.txt
│   │   ├── mirflickr
│   │   │   ├── im21110.jpg
│   │   │   └── ......
│   │   ├── test_image_m.txt
│   │   └── test_label.txt
│   └── NUS-WIDE
│       ├── database_img.txt
│       ├── database_label_onehot.txt
│       ├── database_label.txt
│       ├── images
│       │   ├── 0068_2569963337.jpg
│       │   └── ......
│       ├── img_tc10.txt
│       ├── README.md
│       ├── targets_onehot_tc10.txt
│       ├── targets_tc10.txt
│       ├── test_img.txt
│       ├── test_label_onehot.txt
│       ├── test_label.txt
│       └── t.txt
├── logs
├── main_mmasia.py
├── main_tomm.py
├── modules
│   ├── alexnet.py
│   ├── all_in_one.py
│   ├── gcn
│   │   ├── layers.py
│   │   ├── models.py
│   │   └── __pycache__
│   │       ├── layers.cpython-39.pyc
│   │       └── models.cpython-39.pyc
│   ├── __init__.py
│   └── mlp.py
├── README.md
├── requirements.txt
├── run.py
└── utils
    ├── evaluate.py
    └── __init__.py
```

#### Citation:

If you find our approach useful in your research, please cite our papers:
[1] Z. Zhang, J. Wang, G. Lu, Towards Discriminative Visual Search via Semantically Cycle-consistent Hashing Networks, in Proc. of The ACM Multimedia Asia, 2021.  
[2] Z. Zhang, J. Wang, L. Zhu, G. Lu, Discriminative Visual Similarity Search with Semantically Cycle-consistent Hashing Networks, ACM Transactions on Multimedia Computing, Communications, and Applications (TOMM), 18(2s): 1-21, 2022.

```
@incollection{zhang2021towards,
  title={Towards Discriminative Visual Search via Semantically Cycle-consistent Hashing Networks},
  author={Zhang, Zheng and Wang, Jianning and Lu, Guangming},
  booktitle={ACM Multimedia Asia},
  pages={1--7},
  year={2021}
}

@article{zhang2022discriminative,
  title={Discriminative Visual Similarity Search with Semantically Cycle-consistent Hashing Networks},
  author={Zhang, Zheng and Wang, Jianning and Zhu, Lei and Lu, Guangming},
  journal={ACM Transactions on Multimedia Computing, Communications, and Applications (TOMM)},
  volume={18},  
  number={2s},  
  pages={1--21},  
  year={2022},
  publisher={ACM New York, NY}
}
```
