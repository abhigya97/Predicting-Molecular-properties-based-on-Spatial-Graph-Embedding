# Predicting-Molecular-properties-based-on-Spatial-Graph-Embedding

This project was done as part of the course Graph Analytics at IU Bloomington. 

## Abstract 
Predicting the molecular properties of molecules is an essential step during drug discovery. Traditionally, a lot of time-consuming biochemical experiments needed to be performed to obtain these properties. Nowadays, computers are used to predict molecular properties. The speed for predicting molecular properties has increased, but the accuracy of prediction is still not satisfactory. Various machine learning and deep learning models have been introduced to address the issue of accuracy of prediction. This project is an attempt to recreate the deep learning graph convolution model proposed by Wang, Li, Jiang, Wang, Zhang, and Wei [1] to predict molecular properties using spatial graph embedding.

## Results and Conclusions

<img width="460" alt="Screen Shot 2021-01-31 at 3 56 02 PM" src="https://user-images.githubusercontent.com/69980927/106397736-d906f980-63dc-11eb-9445-12d8fa3b08f6.png">

<img width="434" alt="Screen Shot 2021-01-31 at 3 55 05 PM" src="https://user-images.githubusercontent.com/69980927/106397711-b5dc4a00-63dc-11eb-8905-7e04112dabb8.png">

Table 1 shows the experimental results on the three data-sets for the model defined in this project. These results are being compared to the results obtained by using only the atomic features of the molecule and the predefined graph convolution model given by DeepChem [3]. Table 2 shows the results for the DeepChem model.

During training, the loss is continuously decreasing for each data-set. This means that the model is working. However, the inconsistency be- tween the training and testing accuracy shows that since the model is very complex, it is over-fitting to the training data. It can be seen from the results that the model defined in this project is working better for ESOL than the DeepChem model. It is interesting to note that since the hyper-parameters of the model were tuned for ESOL data-set, this im- provement in result specifically for the ESOL data-set proves two things: (1) The algorithm defined by Wang, Li, Jiang, Wang, Zhang, and Wei [1] is working, (2)The hyper-parameters including the number of convolution layers need to be tuned for each data-set.

The result for the FreeSolv data-set is very close for both the models. This may be because this data-set is the smallest among the three and is very similar to ESOL data-set. Hence, the parameters defined for the ESOL data-set seem to be working for FreeSolv data-set too. However, it can be seen from the results of both the models that lipophilicity data-set is hard to train because of both its complexity and size. But, the perfor- mance of the model defined in this project is way worse for lipophilicity data-set than the performance of the DeepChem model. One of the rea- sons for this is the difference in the nature of lipophilicity data-set to that of ESOL data-set. Lipophilicity data-set has an atom size of 115 while the ESOL data-set has an atom size of 55. Also, lipophilicity data-set has 4200 compounds, while ESOL only has 1128 compounds. The training accu- racy for lipophilicity data-set converges at 92% if the model is trained for more extended periods. However, the testing accuracy only converges at 44% when the model is trained for a shorter time. When testing accuracy increases, the corresponding training accuracy decreases. This shows that the model is over-fitting to the training data because of both the complexity of the model and the size and complexity of the data-set. Also, the model defined in this project is much more complex than the predefined DeepChem model.


## References
1. Xiaofeng Wang, Zhen Li, Mingjian Jiang, Shuang Wang, Shugang Zhang, and Zhiqiang Wei. Molecule property prediction based on spatial graph embedding. Journal of Chemical Information and Modeling, 59, 08 2019.
2. Molecular fingerprints and similarity searching.
3. The deepchem project works to democratize deep learning for science.
4. Greg Landrum. Open-source cheminformatics software.
