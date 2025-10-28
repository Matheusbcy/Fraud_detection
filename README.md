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

## 💡 Impacto Esperado

Redução de perdas financeiras através da **detecção precoce de atividades fraudulentas**, aumentando a **segurança para instituições financeiras e seus clientes**.
