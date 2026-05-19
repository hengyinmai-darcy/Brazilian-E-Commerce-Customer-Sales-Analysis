Brazilian E-Commerce Business Analysis
巴西电商商业分析项目

SQL + Python + Customer Segmentation + Sales Analytics + Business Insights
SQL + Python + 用户分层 + 销售分析 + 商业洞察

Project Overview ｜ 项目简介

This project analyzes the Brazilian E-Commerce Public Dataset by Olist using Python, SQL, and data visualization techniques.
本项目基于 Olist 巴西电商公开数据集，使用 Python、SQL 与数据可视化技术进行商业数据分析。

The goal of this project is to explore customer behavior, sales performance, logistics efficiency, and customer value segmentation to generate actionable business insights.
项目目标是分析用户行为、销售表现、物流效率以及用户价值分层，并输出具有商业价值的数据洞察。

The analysis covers:
项目主要包括：

Sales trend analysis ｜ 销售趋势分析
Product category analysis ｜ 商品类别分析
Regional customer analysis ｜ 用户地区分析
Delivery delay impact analysis ｜ 物流延迟影响分析
Customer segmentation ｜ 用户分层分析
Repeat purchase analysis ｜ 复购率分析
Customer activity analysis ｜ 用户活跃度分析
RFM customer value analysis ｜ RFM用户价值分析

This project demonstrates practical business analysis skills commonly used in real-world e-commerce companies.
本项目展示了真实电商行业中常见的数据分析与商业分析能力。

Tools & Technologies ｜ 使用工具
Python
SQL (SQLite)
Pandas
Matplotlib
Seaborn
Kaggle Notebook
Dataset ｜ 数据集

Dataset used:
使用数据集：

Brazilian E-Commerce Public Dataset by Olist

The dataset contains multiple business-related tables such as customers, orders, payments, products, and logistics data.
该数据集包含多个与电商业务相关的数据表，包括用户、订单、支付、商品以及物流数据。

Business Questions ｜ 商业问题

This project aims to answer several key business questions:
本项目主要解决以下商业问题：

How are sales changing over time?
销售额如何随时间变化？
Which product categories generate the highest revenue?
哪些商品类别贡献了最高销售额？
Which regions contribute the most customers and revenue?
哪些地区贡献了最多用户与销售额？
How does delivery delay affect customer experience?
物流延迟如何影响用户体验？
Who are the high-value customers?
谁是高价值用户？
What is the repeat purchase rate?
平台复购率如何？
Which customers are at risk of churn?
哪些用户存在流失风险？
Data Processing ｜ 数据处理

The analysis started with loading multiple CSV files into Pandas DataFrames.
项目首先将多个 CSV 文件读取到 Pandas DataFrame 中。

customers = pd.read_csv('olist_customers_dataset.csv')
orders = pd.read_csv('olist_orders_dataset.csv')
payments = pd.read_csv('olist_order_payments_dataset.csv')
items = pd.read_csv('olist_order_items_dataset.csv')
products = pd.read_csv('olist_products_dataset.csv')

Main data preparation tasks included:
主要数据处理步骤包括：

Handling missing values ｜ 处理缺失值
Datetime conversion ｜ 时间格式转换
SQL table joins ｜ SQL多表关联
Aggregating sales metrics ｜ 销售指标聚合分析
SQL Analysis ｜ SQL分析

SQLite was used to simulate a real business database environment.
项目使用 SQLite 模拟真实商业数据库环境。

Key SQL operations included:
主要 SQL 操作包括：

JOIN multiple tables ｜ 多表关联
GROUP BY aggregation ｜ 分组聚合
Revenue analysis ｜ 销售额分析
Customer analysis ｜ 用户分析

Example SQL query:
SQL 示例：

SELECT
    customer_state,
    COUNT(DISTINCT order_id) AS total_orders,
    SUM(payment_value) AS total_sales
FROM merged_table
GROUP BY customer_state
ORDER BY total_sales DESC;
Key Analysis & Insights ｜ 核心分析与商业洞察
1. Monthly Sales Trend Analysis ｜ 月度销售趋势分析

The platform showed an overall growth trend in both order volume and revenue.
平台订单量与销售额整体呈增长趋势。

Certain months experienced significant growth spikes, likely influenced by seasonal demand and promotional campaigns.
部分月份出现明显增长高峰，可能受到季节性消费需求与营销活动影响。

Business Impact ｜ 商业价值：

Evaluate business growth trends ｜ 评估业务增长趋势
Support marketing planning ｜ 支持营销策略制定
2. Product Category Analysis ｜ 商品类别分析

Sales were concentrated in several high-performing product categories.
平台销售额主要集中于部分高表现商品类别。

Some categories generated significantly higher revenue than others.
部分商品类别贡献了明显更高的销售收入。

Business Impact ｜ 商业价值：

Optimize inventory allocation ｜ 优化库存管理
Improve category marketing strategy ｜ 优化品类营销策略
3. Regional Analysis ｜ 地区分析

Customers were mainly concentrated in economically developed regions.
用户主要集中于经济较发达地区。

Some regions showed low customer penetration and growth potential.
部分地区用户覆盖率较低，存在市场增长空间。

Business Impact ｜ 商业价值：

Improve regional marketing strategy ｜ 优化区域营销
Support market expansion decisions ｜ 支持市场扩张决策
4. Delivery Delay Impact Analysis ｜ 物流延迟影响分析

Some orders experienced significant delivery delays.
部分订单存在明显物流延迟问题。

Long delivery times may negatively affect customer satisfaction and repeat purchases.
物流时效过长可能降低用户满意度与复购率。

Business Impact ｜ 商业价值：

Improve logistics performance ｜ 优化物流效率
Reduce churn risk ｜ 降低用户流失风险
5. Customer Segmentation Analysis ｜ 用户分层分析

Customers were segmented based on spending behavior.
项目基于消费行为对用户进行了分层分析。

A small group of high-value customers contributed a large percentage of total revenue.
少部分高价值用户贡献了平台大量销售额。

Business Impact ｜ 商业价值：

Improve VIP customer retention ｜ 提升高价值用户留存
Support personalized marketing ｜ 支持精准营销
6. Repeat Purchase Analysis ｜ 复购率分析

Only a portion of customers returned for repeat purchases.
仅部分用户存在复购行为。

Repeat customers generally contributed higher customer lifetime value.
复购用户通常具有更高生命周期价值。

Business Impact ｜ 商业价值：

Evaluate customer loyalty ｜ 评估用户忠诚度
Improve retention strategy ｜ 优化用户留存策略
7. Customer Activity Analysis ｜ 用户活跃度分析

Customer activity was analyzed using recency metrics.
项目使用 Recency 指标分析用户活跃度。

Some customers remained highly active, while others showed strong churn risk.
部分用户保持较高活跃度，而部分用户存在明显流失风险。

Business Impact ｜ 商业价值：

Identify inactive users ｜ 识别沉睡用户
Support re-engagement campaigns ｜ 支持用户召回活动
RFM Analysis ｜ RFM用户价值分析

RFM analysis was used to evaluate customer value based on:
项目使用 RFM 模型评估用户价值：

Recency ｜ 最近消费时间
Frequency ｜ 消费频率
Monetary ｜ 消费金额

Example scoring process:
评分代码示例：

rfm['R_score'] = pd.qcut(
    rfm['recency'],
    4,
    labels=[4,3,2,1]
)

rfm['F_score'] = pd.qcut(
    rfm['frequency'].rank(method='first'),
    4,
    labels=[1,2,3,4]
)

rfm['M_score'] = pd.qcut(
    rfm['monetary'],
    4,
    labels=[1,2,3,4]
)

RFM helps businesses identify:
RFM 模型可以帮助企业识别：

VIP customers ｜ 高价值用户
Churn-risk customers ｜ 流失风险用户
Loyal customers ｜ 忠诚用户
Conclusion ｜ 项目总结

This project demonstrates how SQL and Python can be combined to solve real-world business problems in e-commerce.
本项目展示了如何结合 SQL 与 Python 解决真实电商业务中的数据分析问题。

The analysis provided insights into customer behavior, sales growth, logistics efficiency, and customer value segmentation.
项目从用户行为、销售增长、物流效率以及用户价值分层等多个角度进行了深入分析。

Future improvements may include:
未来可扩展方向包括：

Churn prediction ｜ 用户流失预测
Recommendation systems ｜ 推荐系统
Customer lifetime value prediction ｜ 用户生命周期价值预测
Power BI / Tableau dashboards ｜ BI可视化仪表盘
Author ｜ 作者
麦恒铟 Hengyin Mai

Data Analysis Portfolio Project
数据分析作品集项目
