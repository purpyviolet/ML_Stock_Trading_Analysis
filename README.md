# ML_Stock_Trading_Analysis
机器学习大作业——股票交易以及分析，使用LSTM为主要预测模型

## 运行顺序

代码运行顺序为：

1. `data_processing_日线.ipynb`、`data_processing_分钟线.ipynb`
2. `add_factor_日线.ipynb`、``add_factor_日线.ipynb`
3. `日线LSTM预测.ipynb`、`分钟线LSTM预测.ipynb`
4. `股票策略与评估.ipynb`





两个data_processing对应txt数据到xls或者xlsx数据格式的转换，方便后续添加因子

add_factor对应两个线的添加因子

在确保有HSI_5分钟线+factor.xlsx和HSI_日线数据+factor.xls两个数据后，再运行日线和分钟线LSTM预测



则**5分钟线**数据可以更改的部分：

1. 训练集的个数，投资期有3年，可以分别选不同的投资期，以月或者季来预测，查看效果，再将预测结果运用到后面投资策略上
2. epochs数（大概200-300）



后期策略评估的文件读取是通过读取 HSI_日线数据_with_predict.xlsx和HSI_5分钟线_with_predict.xlsx两个文件，读取部分分别在两个股票策略评估代码中

后期融合这两个数据进行策略投资



最后股票策略与评估存在一个小bug，关于参数初始化的问题，重新添加后删除再次运行即可
