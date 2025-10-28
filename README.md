# 💳 Sistema de Detecção de Fraudes em Transações Financeiras

## 🧩 Definição do Problema

### **Contexto do Negócio**
Instituições financeiras enfrentam perdas significativas devido a transações fraudulentas, que totalizam bilhões de dólares anualmente.  
A detecção manual de fraudes torna-se inviável devido ao volume massivo de transações, exigindo soluções automatizadas que possam identificar padrões suspeitos em tempo real.

### **Problema Principal**
Como desenvolver um sistema de classificação preciso que possa distinguir entre transações legítimas e fraudulentas em um conjunto de dados **altamente desbalanceado**, onde as transações fraudulentas representam **menos de 0.2%** do total.

---

## ⚠️ Desafios Específicos

- **Desequilíbrio Extremo de Classes:** A minoria fraudulenta.
- **Qualidade de Dados:** Necessidade de pré-processamento robusto para lidar com colunas categoricas e normalização  

---

## 🎯 Objetivos do Projeto

### **Objetivo Primário**
Desenvolver um modelo de *machine learning* que **maximize a detecção de transações fraudulentas** enquanto mantém um **baixo índice de falsos positivos**.

### **Objetivos Secundários**
- Identificar as *features* mais relevantes para detecção de fraudes  
- Criar um sistema que possa ser adaptado para uso em tempo real  

---

## 🧮 Critérios de Sucesso

- **Recall alto** para a classe fraudulenta (> 85%)  
- **Precisão balanceada** que considere ambas as classes  
- **AUC-ROC superior a 0.95**  
- **F1-Score otimizado** para a classe minoritária  

---

## 🔍 Abordagem Proposta

1. **Análise Exploratória:** Compreender distribuições e correlações  
2. **Pré-processamento:** Normalização e tratamento de *outliers*  
3. **Balanceamento:** Aplicação de StandardScaler  
4. **Modelagem:** Testar *Logistic Regression*  
6. **Avaliação:** Métricas focadas no problema desbalanceado  
---

## 📊 Resultados Obtidos

O modelo foi avaliado utilizando um *pipeline* de classificação.  
A métrica de **acurácia total** obtida foi de aproximadamente **94.65%**.

### **Relatório de Classificação**
| Classe | Precision | Recall | F1-Score | Suporte |
|:-------|:----------:|:-------:|:---------:|--------:|
| **0 (Legítimas)** | 1.00 | 0.95 | 0.97 | 1,906,322 |
| **1 (Fraudulentas)** | 0.02 | 0.94 | 0.04 | 2,464 |

**Acurácia Geral:** `94.65%`  
**Média Macro:** Precision = 0.51 | Recall = 0.94 | F1 = 0.51  
**Média Ponderada:** Precision = 1.00 | Recall = 0.95 | F1 = 0.97  

### **Análise dos Resultados**
- O modelo atingiu **excelente recall (0.94)** para a classe de fraudes, indicando alta capacidade de detectar transações fraudulentas.  
- Entretanto, a **precisão para a classe fraudulenta (0.02)** foi baixa, o que sugere **muitos falsos positivos**.  
- Esse comportamento é comum em conjuntos de dados **altamente desbalanceados**, onde o modelo tende a priorizar a classe majoritária.  
- Ajustes futuros podem incluir:
  - Rebalanceamento com **SMOTE** ou **undersampling**;  
  - Ajuste de **limiar de decisão (threshold)**;  
  - Uso de **modelos mais sensíveis a classes minoritárias**, como *XGBoost* com `scale_pos_weight`.  

---

## 💡 Impacto Esperado

Redução de perdas financeiras através da **detecção precoce de atividades fraudulentas**, aumentando a **segurança para instituições financeiras e seus clientes**.
