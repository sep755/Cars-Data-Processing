# Car Performance Analysis

## 项目简介

本项目基于汽车数据集（Cars Dataset），使用 Python 对汽车性能数据进行清洗、预处理、统计分析与可视化探索。

通过分析汽车价格、马力、最高速度、加速性能、座位数以及能源类型等指标，研究不同类型汽车之间的性能差异及其相互关系。

---

## 使用技术

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## 项目结构

```text
Car_Analysis/
│
├── Cars Datasets.csv
│
├── analysis.ipynb
│
├── output
│   ├── fig1_Vehicle Parameter Correlation.png
│   ├── fig2_Distribution of Car Prices.png
│   ├── fig3_Relationship Between Car Price and Horse Power.png
│   ├── fig4_Fuel Type Distribution.png
│   └── fig5_Performance Comparison of Different Vehicle Types.png
│
├── README.md
└── requirements.txt
```

---

## 数据预处理

在正式分析前，对原始数据进行了清洗和转换：

### 1. 列名标准化

* 修正编码导致的异常列名
* 统一字段命名格式

### 2. 数据类型转换

将字段转换为适当的数据类型：

* Category

  * Company Names
  * Cars Names
  * Engines
  * CC/Battery Capacity
  * Fuel Types

* Numeric

  * Horse Power (hp)
  * Total Speed (km/h)
  * Seats
  * Torque (Nm)
  * Cars Prices ($)

### 3. 价格数据清洗

处理价格字段中的：

* 美元符号（$）
* 千位分隔符（,）
* 非标准格式

并转换为数值类型。

### 4. 缺失值处理

对数值型变量采用中位数填充缺失值。

### 5. 重复值处理

删除重复记录。

### 6. 异常值处理

采用 IQR（四分位距）方法检测并移除异常值。

---

## 数据分析与可视化

### 1. 特征相关性分析

绘制相关性热力图，分析以下指标之间的关系：

* Cars Prices ($)
* Horse Power (hp)
* Total Speed (km/h)
* Performance(0 - 100 )KM/H (sec)
* Seats
* Torque (Nm)

目的：

* 发现变量之间的相关程度
* 探索影响汽车价格的重要因素

---

### 2. 汽车价格分布

使用：

* Histogram
* KDE（核密度估计）

分析汽车价格的整体分布情况。

观察：

* 价格是否呈偏态分布
* 高价车辆占比情况

---

### 3. 马力与价格关系

使用散点图分析：

* Horse Power (hp)
* Cars Prices ($)

之间的关系。

目的：

* 研究高马力车型是否具有更高价格
* 观察变量之间的趋势关系

---

### 4. 能源类型占比分析

统计并绘制不同 Fuel Types 的占比饼图。

分析：

* Petrol
* Diesel
* Hybrid
* Electric

等车型在数据集中的分布情况。

---

### 5. 不同能源类型性能对比

按 Fuel Types 分组统计并可视化：

* 平均马力（Horse Power）
* 平均最高速度（Total Speed）
* 平均百公里加速时间（0-100 km/h）
* 平均价格（Cars Prices）

通过柱状图比较不同能源类型汽车的整体性能表现。

---

## 运行方法

### 安装依赖

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

或

```bash
pip install -r requirements.txt
```

### 启动 Notebook

```bash
jupyter notebook
```

打开：

```text
analysis.ipynb
```

依次运行所有单元格即可完成分析。

---

## 项目成果

本项目实现了：

* 数据读取
* 数据清洗
* 缺失值处理
* 重复值处理
* 异常值处理
* 统计分析
* 数据可视化

符合数据分析项目的基本流程，并能够实现完整的数据分析与结果展示。

---

## 作者

Name: sep755

Date: 2026
