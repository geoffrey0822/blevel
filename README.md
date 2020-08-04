# Bi-level Neural Network

### 1. Descriptions
Bi-level Neural Network is designed for hierarchy classification problem, therefore we developed a layer which could support bi-level label, and the neural network could solve different objectives for different branches.
___


### 2. Experimental Results

| Models    | Pretrained | Grouped by    | Top-1 for single branch | Top-1 for Top branch | Top-1 for Bottom branch | Top-1 for fused |
|-----------|------------|---------------|-------------------------|----------------------|-------------------------|-----------------|
| AlexNet   | No         | Less Confused | 59.87%                  | 62.6%                | 58.7%                   | 58.7%           |
| AlexNet   | No         | Most Confused | 59.87%                  | 78.9%                | 60.01%                  | 60.01%           |
| AlexNet   | Yes        | Most Confused | 78.35%                  | 89.76%               | 85.91%                  | 86.7%           |
| GoogLeNet | No         | Less Confused | 62.06%                  | 70.1%                | 61.9%                   | 61.9%           |
| GoogLeNet | No         | Most Confused | 62.06%                  | 82.3%                | 65.8%                   | 65.8%           |

*Table 1. Test result for VOC2012 Dataset*

| Models     | Pretrained | Grouped by | Top-1 for single branch | Top-1 for Top branch | Top-1 for Bottom branch | Top-1 for fused |
|------------|------------|------------|-------------------------|----------------------|-------------------------|-----------------|
| AlexNet    | No         | Given      | 56.2%                   | 62.1%                | 56.3%                   | 60.9%           |
| AlexNet    | Yes        | Given      | 66.71%                  | 80.5%                | 71.1%                   | 75.91%          |
| ResNet-110 | No         | Given      | 72.3%                   | 90.8%                | 78.4%                   | 78.4%           |
| DenseNet   | No         | Given      | 76.21%                  | 95.7%                | 80.36%                  | 80.36%          |

*Table 2. Test result for CiFar-100 Dataset*

___

### 3. Step to execute the program
1. Download & Install our modified Caffe [git clone https://github.com/geoffrey0822/caffe_dev.git]
2. Clone the repository
3. Run bash script "./runTrain_reg.sh" for duo-hand gesture recongition to reproducing the experiment result. Run python script "python addon/create_mlabel_dataset.py SRC_DIR DST_DIR OUTPUT_DB_NAME OUTPUT_INDEX_FILENAME ratio 1.0" and then import into DIGITS, therefore you can train the bilevel model in DIGITS instead of command mode.
___
### 4. Publications
___

### Pytorch Implimentation 
1. Please refer to https://github.com/geoffrey0822/HTNN
