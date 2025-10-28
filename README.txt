-----------------------------------------------------------------
商务智能大作业文件整合
小组成员：吴越、张铭轩、卜方婧
2024.10.28
--------code----------
data_preprocessing.ipynb：数据预处理文件
model_alltogether_mlp.ipynb：all-together mlp的代码文件
model_user_product_mlp.ipynb：user-product mlp的代码文件
model_user_product_mlp_BERT.ipynb：user-product mlp BERT的代码文件
model_user_product_rnn_mlp.ipynb：user-product rnn mlp的代码文件
Matrix_Frac.ipynb：BiasSVD的代码文件
evaluation.ipynb：对比上述model在测试集上的MSE,MAE,RMSE，并给定用户进行推荐预测
--------model----------
alltogether_mlp.h5
user_product_mlp.h5
user_product_mlp_BERT.h5
user_product_rnn_mlp.h5
tokenizer_title.pkl（在训练集数据上得到的title tokenizer，用于user-product rnn mlp模型）
tokenizer_summary.pkl（在训练集数据上得到的summary tokenizer，用于user-product rnn mlp模型）
---------data--------
data_train.parquet：训练集数据（不包含summary信息）
data_test.parquet：测试集数据（不包含summary信息）
long_summary.parquet：所有评论数据的summary列（需根据productId和训练集与测试集进行合并）
title_embeded_df.parquet：经过BERT训练出的title变量（需根据productId和训练集与测试集进行合并）
summary_embeded_df.parquet：经过BERT训练出的summary变量（需根据productId和训练集与测试集进行合并）