# 🕸️ Ethereum Token Transfer Network Analysis and ML Account Classification

## Overview
This project applies **network science and machine learning techniques** to analyze Ethereum blockchain token transfer data.  
The goal is to build a clean token flow network, identify key actors, and predict account types (CEX, DEX, MEV Bots) based on network features.

---

## 🎯 Objectives
* Construct a directed weighted graph from ERC20 token transfer data.
* Perform exploratory analysis to uncover global and local network structures.
* Investigate key actors such as Binance, Uniswap, and MEV bots using centrality and ego graphs.
* Develop a machine learning model to classify accounts based on graph metrics and neighbor composition.

---

## 🛠 Methodologies Implemented

**Network Construction:**
* Clean ERC20 token transfer dataset (spam filtering, verified tokens, decimals).
* Build directed graph with weighted edges (token transfer volumes).

**Exploratory Network Analysis:**
* Degree distributions (In-degree, Out-degree)
* Strongly Connected Components (SCC) and Weakly Connected Components (WCC)
* PageRank centrality
* Ego graph analysis of Binance, Coinbase, and Uniswap

**Machine Learning Classification:**
* Feature engineering (degree, PageRank, neighbor composition ratios)
* Random Forest Classifier to predict account categories (CEX, DEX, MEV, Other)
* Performance evaluation and feature importance analysis

---

## 📚 Data

**Datasets:**
* Token transfers (`transfers_20080000.parquet`)
* Transaction metadata (`txs_20080000.parquet`)
* Verified token labels (`token_labels.csv`)
* Account labels and categories (`account_labels.csv`)

**Sources:**
* Ethereum blockchain data and Alchemy API

---

## 📈 Key Results

**Network Insights:**
* +300k addresses and 500k edges → Sparse but highly structured network.
* Core-periphery structure with centralized exchanges and DeFi routers as hubs.
* Uniswap Universal Router dominates DeFi flows, MEV bots form peripheral yet strategic connections.

**Machine Learning Results:**
* Random Forest model achieved strong classification performance.
* PageRank and neighbor composition were key predictors.
* Application to full network → automatic labeling of unclassified addresses.

---

## 🛠 Tools and Libraries
* Python 3.11
* pandas, numpy, matplotlib, networkx
* scikit-learn
* pyvis (for interactive network visualization)

---

## 🚀 How to Run
1. Clone the repository.
2. Install dependencies:
```bash
pip install -r requirements.txt
```
---

## 🔮 Future Improvements
* Extend ML model to predict activity types (DeFi, NFT, MEV, OTC).
* Integrate ERC721/ERC1155 tokens to build multi-token ecosystem view.
* Apply Graph Neural Networks (GNN) for improved account classification.



---

## 📖 References
* Ethereum Whitepaper (Vitalik Buterin, 2013)
* Newman, M. (2018). Networks: An Introduction. Oxford University Press.
* Alchemy Developer Docs: Token Transfer API
* scikit-learn documentation


---

## 📑 License
This project is for educational purposes only.
