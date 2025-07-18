# 处理 CheXpert Plus 数据

## 数据集来源
https://stanfordaimi.azurewebsites.net/datasets/5158c524-d3ab-4e02-96e9-6ee9efc110a1

## 处理数据
[process.ipynb](process.ipynb) : 

1. 合并了csv和report_fixed.json当作dataframe  
2. 删除了section_finding为空和长度小于2的数据  
3. 查看frontal和lateral的比例，并过滤掉lateral，只保留frontal  
4. 删除了section_impression为空和长度小于2的数据  
5. 把.jpg改为.png
6. 统计全阴性占比  
7. 去掉没用的标签，打包到[chexpert_dataset_filtered.json](chexpert_dataset_filtered.json)  
8. 统计疾病阴性阳性占比