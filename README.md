# Machine Learning with KNIME · Traffic Accidents and Garment Productivity

End-to-end data mining project built in **KNIME Analytics Platform**, from data exploration and cleaning to training and evaluating regression and classification models on two real datasets.

Built for the *Aprendizagem e Decisão Inteligentes* (Intelligent Learning and Decision) course at the University of Minho, 2023.

📄 **Full report (Portuguese):** [Relatório_ADI.pdf](Relatório_ADI.pdf) · **Assignment:** [Enunciado TPG.pdf](Enunciado%20TPG.pdf)

## Task A · Traffic accidents in Porto Alegre

**Dataset:** more than 60,000 traffic accident records from Porto Alegre, Brazil, between 2018 and 2022.

**Goal:** predict how many people are injured or killed in an accident. It was predicted directly with regression and, for classification, binned into three ranges: no victims, 1–2 victims and 3 or more.

**Data preparation:** removed irrelevant columns, created and transformed features (for example, filling in missing hours from the day/night column), handled missing values and explored the data by time, vehicle type and location.

**Models:** linear regression, polynomial regression and neural networks for regression; decision trees, logistic regression and neural networks for classification.

**Results:** the neural network performed best, with about **97.7% accuracy**. The confusion matrix showed that the models still struggle with the rare high-casualty accidents, which the report identifies as the main thing to improve.

## Task B · Garment factory productivity

**Dataset:** daily production records from a garment factory.

**Goal:** predict the team's `actual_productivity`.

**Data preparation:** removed impossible values in the target and handled missing values, then explored the data again after cleaning.

**Models:** the same regression and classification families as in Task A.

**Results:** linear regression reached an RMSE of **0.151**. For classification, decision trees performed best, with about **73.8% accuracy**.

## Evaluation

- **Regression:** MAE, MSE, RMSE and R²
- **Classification:** confusion matrix, accuracy, sensitivity and specificity

## Repository structure

```
Tarefa_A/
├── TP_TarefaA.knwf        # KNIME workflow
└── cat_acidentes2.csv     # Dataset
Tarefa_B/
├── TP_TarefaB.knwf        # KNIME workflow
└── producao_vestuario.csv # Dataset
Relatório_ADI.pdf          # Report (Portuguese)
Enunciado TPG.pdf          # Assignment brief
```

## How to open

1. Install [KNIME Analytics Platform](https://www.knime.com/downloads).
2. Go to **File → Import KNIME Workflow** and choose `Tarefa_A/TP_TarefaA.knwf` or `Tarefa_B/TP_TarefaB.knwf`.
3. If needed, point the CSV Reader node to the dataset in the same folder, then run the workflow.

## Team

- [Gonçalo Santos](https://github.com/goncalosantos3) (a95354)
- [Telmo Maciel](https://github.com/telmomaciel9) (a96569)
- João Neves (a89604)
- Guilherme Pereira (a89479)
