---
license: mit
task_categories:
- graph-ml
language:
- en
tags:
- graph
- knowledge
- citation
- network
- scholar
pretty_name: AceMap Academic Graph Dataset
size_categories:
- 1B<n<10B
---

# AceMap Citation Network Dataset

## Dataset Description
The AceMap Academic Graph Dataset 20250228 is a large-scale academic citation network, containing **2,624,498,906 edges** and **264,675,127 nodes**. Each node represents an academic paper, and each edge indicates that one paper cites another. Each node can be linked to the [AceMap](https://acemap.info/) website for more detailed information.

## Dataset Source
This dataset is provided by:
- Wang, Xinbing, et al. "AceMap: Knowledge discovery through academic graph." arXiv preprint arXiv:2403.02576 (2024).

## Data Format
The dataset is provided in CSV file format, containing two columns:
- `id`: The unique identifier of the paper, in the form of `ZEJBRUdDQUdBRUI`.
- `referenced_works`: The unique identifier of the cited paper, in the form of `ZDlHREE5QjhCRkQ`.

## Data Examples
Here are some examples from the dataset:

| id                     | referenced_works               |
|------------------------|--------------------------------|
| ZEJBRkNDRTg3RDk        | ZDlHREE5QjhCRkQ                |
| ZEJBRkNDRTg3RDk        | ZDlHRTk4REVHN0E                |
...


## Usage Instructions

### 0. Download from Huggingface

[https://huggingface.co/datasets/Reacubeth/acemap_citation_network](https://huggingface.co/datasets/Reacubeth/acemap_citation_network)

### 1. Unzip the `.tar.gz` Files
Use the `tar` command to extract the contents of each `.tar.gz` file. For example, to extract all files to a directory named `data`, you can run the following commands:

```bash
tar -xzvf filelist_part_aa.tar.gz -C data/
tar -xzvf filelist_part_ab.tar.gz -C data/
tar -xzvf filelist_part_ac.tar.gz -C data/
tar -xzvf filelist_part_ad.tar.gz -C data/
tar -xzvf filelist_part_ae.tar.gz -C data/
```

This will extract the CSV files to the `data/` directory.

### 2. Load the CSV Files
Use Pandas or other data processing tools to load the CSV files. Here is an example of how to load and concatenate all CSV files into a single DataFrame:


3. **Access AceMap Website**: For more detailed information about each paper, visit the [AceMap](https://acemap.info/) website by concatenating the following example strings:
```python
url = 'https://acemap.info/papers/' + 'ZEJBRkNDRTg3RDk'
```

## Citation
If you use this dataset, please cite the following publication:
```
@article{wang2024acemap,
  title={AceMap: Knowledge discovery through academic graph},
  author={Wang, Xinbing and Fu, Luoyi and Gan, Xiaoying and Wen, Ying and Zheng, Guanjie and Ding, Jiaxin and Xiang, Liyao and Ye, Nanyang and Jin, Meng and Liang, Shiyu and others},
  journal={arXiv preprint arXiv:2403.02576},
  year={2024}
}
```

## Contact
For any questions or further assistance, please contact email yixu98@sjtu.edu.cn.
