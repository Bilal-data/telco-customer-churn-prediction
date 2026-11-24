# telco-customer-churn-prediction
Predicting customer churn using logistic regression on the Telco Customer Churn dataset
# Telco Customer Churn Prediction

Analyzing a telecom company's customer data (7,011 customers, 21 features) to understand why customers leave (churn) and build a model that predicts it.

Dataset: [Telco Customer Churn (IBM sample)](https://github.com/easonlai/telco_customer_churn), public sample data, no license restriction on use.

## Key findings
- Overall churn rate: 26.6% of customers.
- Customers who churn have much shorter tenure on average (18 months vs 38 months for those who stay).
- Month-to-month contracts have by far the highest churn rate (42.7%) vs one-year (11.2%) and two-year contracts (2.9%).
- Customers who churn pay higher monthly charges on average (74.5 vs 61.3).

## Predictive model
Built a Logistic Regression model using 19 customer features (80/20 train/test split).
- Test accuracy: 80.4% on 1,403 customers never seen during training.
- Strongest factors reducing churn risk: longer tenure, longer contract commitment.
- Strongest factors increasing churn risk: internet service type, total charges, streaming add-ons.
- The first model run produced a convergence warning due to unscaled features; fixed by applying `StandardScaler` before retraining, with no loss in accuracy.

## Limitations
- Single logistic regression model with default settings; accuracy could likely improve with other models or hyperparameter tuning.
- Dataset is a public sample, not necessarily representative of all telecom markets.
- No date information in the dataset, so churn timing patterns (e.g. seasonality) could not be analyzed.

---

## بالعربي

# التنبؤ بترك العملاء (Customer Churn) لشركة اتصالات

تحليل بيانات 7,011 عميل لشركة اتصالات (21 عمود) لفهم ليه العملاء بيسيبوا الخدمة (churn)، وبناء نموذج يتوقع ده.

مصدر البيانات: [Telco Customer Churn (عينة IBM)](https://github.com/easonlai/telco_customer_churn)، بيانات عامة متاحة للاستخدام.

## أهم النتائج
- نسبة ترك العملاء الإجمالية: 26.6%.
- العملاء اللي سابوا متوسط مدة بقائهم أقصر بكتير (18 شهر مقابل 38 شهر للي فضلوا).
- العقد الشهري عنده أعلى نسبة ترك بفارق كبير (42.7%) مقارنة بعقد سنة (11.2%) وعقد سنتين (2.9%).
- العملاء اللي سابوا بيدفعوا فاتورة شهرية أعلى في المتوسط (74.5 مقابل 61.3).

## نموذج التنبؤ
بنيت نموذج Logistic Regression باستخدام 19 عامل (تقسيم 80/20 تدريب/اختبار).
- دقة النموذج على الاختبار: 80.4% على 1,403 عميل ماشافهمش النموذج قبل كده.
- أقوى العوامل اللي بتقلل احتمال الترك: مدة البقاء الأطول، الالتزام بعقد أطول.
- أقوى العوامل اللي بتزود احتمال الترك: نوع خدمة الإنترنت، إجمالي المدفوع، خدمات البث الإضافية.
- أول تشغيل للنموذج ظهر فيه تحذير (convergence warning) بسبب اختلاف مقاييس الأعمدة؛ اتحل باستخدام `StandardScaler` قبل إعادة التدريب، من غير خسارة في الدقة.

## الحدود
- النموذج عبارة عن Logistic Regression واحد بإعدادات افتراضية؛ الدقة ممكن تتحسن مع نماذج تانية أو ضبط المعاملات.
- البيانات عينة عامة، مش بالضرورة ممثلة لكل أسواق الاتصالات.
- مفيش معلومات تاريخ في البيانات، فمقدرناش نحلل أنماط زمنية (موسمية) لترك العملاء.
