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

Task 3 进阶baseline讲解     
1. 这部分把baseline进阶，参考价值更大。
2. package部分：rdkit处理化学结构。
3. 预处理方法相似：drop掉缺失值多的列，这里用的notnull>10。改良的话，可以drop掉行，缺失多了也不行。
4. 特征处理：重点是这个SMILES的化学信息处理，是为了确保所有SMILES都是以相同的方式处理信息的。之后用了TF-IDF，但是这个也有自身问题，可以考虑替换升级（自己跑的话）。
5. TF-IDF（Term Frequency-Inverse Document Frequency）：是一种用于信息检索与文本挖掘的常用加权技术。它是一种【统计方法】，用以评估一个词语对于一个文件集或一个语料库中的其中一份文件的重要程度。主要思想是：如果某个词语在一篇文章中出现的频率高（Term Frequency，TF），并且在其他文章中很少出现（Inverse Document Frequency，IDF），则认为这个词语具有很好的类别区分能力，对这篇文章的内容有很好的指示作用。注意有自身bug。
6. 交叉验证：（1）K-折交叉验证（K-Fold Cross-Validation）：比较常规，一般5和10。（2）留一交叉验证（Leave-One-Out Cross-Validation, LOOCV）：用于小样本机器学习。（3）分层交叉验证（Stratified Cross-Validation）：确保每个折中类别的比例与整个数据集保持一致。（4）时间序列交叉验证（Time Series Cross-Validation）：确保测试集总是来自时间序列的末端。
7. CatBoost：自动处理，宝藏package。
8. 整体上机器学习思路清晰，甚至感觉可以在此基础上直接搞。     
   


