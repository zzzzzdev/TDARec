# TDARec

Code for submission  #4665: Semantic-guided Data Augmentation and Filtering for Sequential Recommendation



# Steps for Reproducing 

### Step 1: Download Datasets

You can download the datasets used in this paper thorugh following links:

Toys: https://drive.google.com/file/d/1De099aEeHZ-8rKcscElYnO1Mo3pCZ-oO/view?usp=drive_link

Sports: https://drive.google.com/file/d/1VJ2qx8mHi2nhyEVkoEv-3YQ5ZraG7cNs/view?usp=drive_link

Clothing: https://drive.google.com/file/d/1YkWVgFKkB_XYuBU9JCr9uLs2A32aat04/view?usp=drive_link



And put the files in `<data_path>` like the following.

```
$ tree data_path
<data_path>
├── Amazon_Toys
│   ├── Amazon_Toys.inter
│   └── Amazon_Toys.item
├── Amazon_Sports
│   ├── Amazon_Sports.inter
│   └── Amazon_Sports.item
└── Amazon_Clothing
    ├── Amazon_Clothing.inter
    └── Amazon_Clothing.item
```



### Step 2: Create Conda Environment

```shell
conda create --name <env_name> --file requirements.txt
```



### Step 3： Train and Predict

```shell
$project_path='xx'
$data_path='xx'
$dataset='Amazon_Clothing' # you could change it to "Amazon_Sports" or "Amazon_Toys"
sh TDARec.sh <project_path> <data_path> <dataset>
```

For example:

```shell
$project_path='/opt/data/private/interactive4388/Documents/TDARec/'
$data_path='/opt/data/private/interactive4388/Documents/All_Dataset/'
$dataset='Amazon_Clothing'

sh TDARec.sh \
/opt/data/private/interactive4388/Documents/TDARec/ \
/opt/data/private/interactive4388/Documents/All_Dataset/
```



You can change the dataset for training by uncommenting the related part in the `TDARec.sh`



You can change the config in the `seq.yaml`

