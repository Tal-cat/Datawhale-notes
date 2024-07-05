# AI summer camp ML      
Task 1 五分钟跑通baseline     
打怪兽证明很用心~点赞o(￣▽￣)ｄ     

Task 2 赛题深入分析    
1. 整体来看是对feature的具体说明，可以说相当有帮助。    
2. 表示允许选手通过【数据增强】或【自行搜集数据】来扩充数据集，并自行划分数据集用于训练和验证模
型。自行扩充相当于根据row补充强力column，可能对背景要求较高，小白（本人）先放一放。     
3. y就是Label，降解能力的标签，0表示降解能力差，1表示降解能力好。所以说是一个Classification Task。
4. Lable依据：根据DC50和Dmax值来判断降解能力的好坏：如果DC50 大于100nM且Dmax 小于
80%，则Label 为0；如果DC50 小于等于100nM或Dmax 大于等于80%，则Label为1。  
5. 学习之：【Smiles】是一种用于描述化学结构的文本字符串，它能够被用于【输入化学信息学软件】。下图：
   <img width="645" alt="截屏2024-07-05 18 29 07" src="https://github.com/Tal-cat/Datawhale-notes/assets/60603537/d3d5edb1-ce57-4258-8fd0-3d5cc8f663f5">
6. Assay (DC50/Dmax)比较贴近实验描述，有结构的文本串。
7. 学习之：【InChI（国际化学标识符）】:是一种用于唯一标识化学化合物的标准化字符串。它由一系列部分组成，提
供了关于分子结构的详细信息。下图：
   <img width="400" alt="截屏2024-07-05 18 31 49" src="https://github.com/Tal-cat/Datawhale-notes/assets/60603537/a1aa7a2e-e779-4df0-9e98-00b7930bc31d">
   


