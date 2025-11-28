# 🎯 Анализ продаж растений (Florist Shop Dataset, Kaggle)

**Junior Data Analyst проект**: полный цикл анализа данных — от EDA до машинного обучения и интерпретируемости моделей (LIME/SHAP/PDP).

[![Python](https://img.shields.io/badge/Python-3.10-blue)](https://python.org)
[![Pandas](https://img.shields.io/badge/Pandas-2.1-green)](https://pandas.pydata.org)
[![Scikit-learn](https://img.shields.io/badge/Scikit-learn-1.5.2-orange)](https://github.com/scikit-learn/scikit-learn)
[![XGBoost](https://img.shields.io/badge/XGBoost-2.0-yellow)](https://xgboost.readthedocs.io)
[![SHAP](https://img.shields.io/badge/SHAP-0.46-red)](https://shap.readthedocs.io)

## 📊 Описание данных
- **Источник**: [Kaggle Florist Shop Dataset](https://www.kaggle.com/datasets/xavierberge/florist-shop-dataset)
- **Объем**: 25k+ транзакций продаж растений (2022-2024)
- **Ключевые метрики**: SalesUSD, Quantity, PriceUSD, CountryCode, ProductFamily
- **Задача**: выявить факторы продаж + построить модель прогнозирования

## 🔍 Основные инсайты на основе EDA
- **Топ-страна**: China (44.66% выручки)
- **Топ-семейство**: Asteraceae, Fabaceae, Poaceae
- **Сезонность**: пик продаж весна-лето
- **ABC-XYZ**: 80% выручки — AZ сегмент
- **RFM**: Champions (высокая ценность)

![Продажи по странам](Images/sales_by_country.png)
![RFM сегменты](Images/rfm_segments.png)

## 🤖 Машинное обучение
| Модель | RMSE ↓ | R² ↑ |
|--------|--------|------|
| Extra Trees | **385.66** | **0.992** |
| Random Forest | 411.31 | 0.991 |
| Bagging | 405.50 | 0.992 |
| XGBoost | 540.13 | 0.985 |
| Linear Regression | 5599.79 | -0.593 |

**Лучшая модель**: Extra Trees (RMSE=385 USD)

## 🔬 Интерпретируемость (XAI)
- **LIME**: quantity, PriceUSD, countrycode — топ-3 фактора
- **SHAP**: ProductFamily влияет на 25% предсказаний
- **PDP**: линейная зависимость SalesUSD от quantity

## 📈 Бизнес-рекомендации
1. **Фокус на China + Asteraceae** — 45% выручки
2. **AZ сегмент** — 80% прибыли, оптимизировать логистику
3. **RFM Champions** — персональные скидки (+15% LTV)
4. **Модель Extra Trees** — внедрить в продакшн (точность 99%)

## 👩‍💻 Навыки проекта
Python • Pandas • Seaborn • Matplotlib • Scikit-learn • XGBoost
EDA • RFM • ABC-XYZ • Feature Engineering • Model Selection
LIME • SHAP • PDP • Business Insights

## 🚀 Быстрый запуск
