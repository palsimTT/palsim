#### **Table 1: Performance comparison of models for predicting $p_t^s$ and $p_t^b$ with different players**

| **Model** | **Player** | **KLD ST ↓** | **KLD BP ↓** | **TVD ST ↓** | **TVD BP ↓** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **TG (Ours)** | Ito | **0.1049** | **0.1246** | **0.1260** | *0.1640* |
| | Sun | **0.0263** | 0.0762 | **0.0458** | 0.1351 |
| | Fan | **0.0298** | *0.1363* | *0.0475* | **0.1500** |
| LSTM | Ito | *0.1127* | *0.1286* | 0.1439 | 0.1676 |
| | Sun | 0.0324 | *0.0753* | 0.0532 | 0.1488 |
| | Fan | 0.0534 | 0.1632 | 0.0738 | 0.1901 |
| SASRec | Ito | 0.1188 | 0.1329 | 0.1452 | 0.1690 |
| | Sun | 0.0307 | 0.0783 | *0.0495* | 0.1415 |
| | Fan | 0.0362 | 0.1423 | 0.0625 | 0.1604 |
| TabR | Ito | 0.1304 | 0.1369 | 0.1446 | 0.1724 |
| | Sun | *0.0298* | **0.0746** | 0.0505 | *0.1253* |
| | Fan | 0.0388 | 0.1371 | 0.0594 | *0.1547* |
| FT-Transformer| Ito | 0.1745 | 0.1374 | 0.1811 | **0.1528** |
| | Sun | 0.1142 | 0.1250 | 0.1257 | 0.1924 |
| | Fan | 0.0802 | 0.1549 | 0.0972 | 0.1898 |
| XGBoost | Ito | 0.1285 | 0.1815 | *0.1320* | 0.2096 |
| | Sun | 0.0515 | 0.0811 | 0.0793 | **0.1230** |
| | Fan | *0.0351* | **0.1362** | **0.0454** | 0.1862 |
| LR | Ito | 0.1573 | 0.1331 | 0.1876 | 0.1847 |
| | Sun | 0.0572 | 0.1180 | 0.0808 | 0.1833 |
| | Fan | 0.0440| 0.1654 | 0.0669 | 0.1869 |
| *Historical* | Ito | *0.8916* | *0.4245* | *0.5400* | *0.2661* |
| | Sun | *0.6790* | *0.2822* | *0.4181* | *0.2575* |
| | Fan | *0.8011* | *0.4082* | *0.4916* | *0.2946* |

#### **Table 2: Performance evaluation of the joint distribution inferred via IPF with different players**

| **Method** | **Player** | **JSD ↓** | **TVD ↓** |
| :--- | :--- | :--- | :--- |
| **TG + IPF (Ours)** | Ito | 0.1050 | 0.2974 |
| | Sun | 0.0433 | 0.1793 |
| | Fan | 0.0583 | 0.1924 |
| Prior Baseline | Ito | 0.2983 | 0.5893 |
| | Sun | 0.2369 | 0.5088 |
| | Fan | 0.2638 | 0.5417 |
| *Improvement (%)* | Ito | *64.81%* | *49.54%* |
| | Sun | *81.74%* | *64.76%* |
| | Fan | *77.90%* | *64.48%* |

The results demonstrate consistent performance across players with different tactical styles, confirming PaLSim's generalizability. In the revision, we will report averaged results across these three players in the **MODEL EVALUATION** section and **ABLATION**.

#### **Table 3: Comparative evaluation of win rate prediction models with different players**

| **Model** | **Player** | **ECE ↓** | **BSS (%) ↑** | **SAS ↑** |
| :--- | :--- | :--- | :--- | :--- |
| **WRP (Ours)** | Ito | **0.0165** | **4.64** | **0.7497** |
| | Sun | **0.0144** | 1.39 | **0.5940** |
| | Fan | **0.0264** | 4.12 | **0.5807** |
| XGBoost | Ito | 0.0432 | *4.52* | 0.5167 |
| | Sun | 0.0451 | 0.69 | 0.4270 |
| | Fan | 0.0371 | 2.43 | 0.4906 |
| FT-Transformer| Ito | 0.0316 | 2.39 | *0.6073* |
| | Sun | 0.0332 | *1.99* | 0.4655 |
| | Fan | 0.0432 | **4.56** | 0.4533 |
| LSTM | Ito | *0.0282* | 1.74 | 0.6022 |
| | Sun | 0.0361 | **2.17** | 0.4526 |
| | Fan | *0.0369* | *4.29* | *0.5125* |
| TabR | Ito | 0.0292 | 1.57 | 0.5943 |
| | Sun | *0.0314* | 1.67 | *0.5762* |
| | Fan | 0.0380 | 4.22 | 0.4491 |
| *Bayesian* | Ito | *0.0074* | *1.18* | *0.8621* |
| | Sun | *0.0146* | *0.72* | *0.6086* |
| | Fan | *0.0436* | *1.53* | *0.3167* |

#### **Table 1: Performance comparison of models for predicting $p_t^s$ and $p_t^b$**
| **Model** | **KLD ST ↓** | **KLD BP ↓** | **TVD ST ↓** | **TVD BP ↓** | **Rank ↓** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **TG (Ours)** | **0.1049** | **0.1246** | **0.1260** | 0.1640 | **1.25** |
| LSTM | 0.1127 | 0.1286 | 0.1439 | 0.1676 | 2.50 |
| SASRec | 0.1188 | 0.1329 | 0.1452 | 0.1690 | 3.75 |
| TabR | 0.1304 | 0.1369 | 0.1446 | 0.1724 | 4.75 |
| FT-Transformer | 0.1745 | 0.1374 | 0.1811 | **0.1528** | 5.00 |
| XGBoost | 0.1285 | 0.1815 | 0.1320 | 0.2096 | 5.00 |
| LR | 0.1573 | 0.1331 | 0.1876 | 0.1847 | 5.75 |
| *Historical* | *0.8916* | *0.4245* | *0.5400* | *0.2661* | *8.00* |

#### **Table 2: Performance evaluation of the joint distribution inferred via IPF**
| **Method** | **JSD ↓** | **TVD ↓** |
| :--- | :--- | :--- |
| **TG + IPF (Ours)** | 0.1050 | 0.2974 |
| Prior Baseline | 0.2983 | 0.5893 |
| *Improvement (%)* | *64.80%* | *49.53%* |

#### **Table 3: Comparative evaluation of win rate prediction models**
| **Model** | **ECE ↓** | **BSS (%) ↑** | **SAS ↑** |
| :--- | :--- | :--- | :--- |
| **WRP (Ours)** | **0.0165** | **4.64** | **0.7497** |
| XGBoost | 0.0432 | 4.52 | 0.5167 |
| FT-Transformer | 0.0316 | 2.39 | 0.6073 |
| LSTM | 0.0282 | 1.74 | 0.6022 |
| TabR | 0.0292 | 1.57 | 0.5943 |
| *Bayesian* | *0.0074* | *1.18* | *0.8621* |

#### **Table 4: Ablation study of components of TG**
| **Variant** | **KLD ST ↓** | **KLD BP ↓** | **TVD ST ↓** | **TVD BP ↓** |
| :--- | :--- | :--- | :--- | :--- |
| **TG (full)** | **0.1049** | **0.1246** | 0.1260 | **0.1640** |
| w/o Hybrid Loss | 0.1049 | 0.1717 | **0.1220** | 0.1930 |
| w/o Pos + AttnGate | 0.1062 | 0.1288 | 0.1269 | 0.1652 |
| w/o AttnGate | 0.1073 | 0.1296 | 0.1269 | 0.1671 |
| w/o Pos | 0.1079 | 0.1313 | 0.1287 | 0.1664 |
| Baseline | 0.1112 | 0.1291 | 0.1306 | 0.1686 |
| Reverse Uni | 0.1137 | 0.1230 | 0.1291 | 0.1635 |
| w/o Uni + AttnGate | 0.1151 | 0.1297 | 0.1291 | 0.1662 |
| w/o Uni + Pos | 0.1160 | 0.1354 | 0.1330 | 0.1687 |

#### **Table 5: Ablation study of components of WRP**
| **Variant** | **ECE ↓** | **BSS (%) ↑** | **SAS ↑** |
| :--- | :--- | :--- | :--- |
| **WRP (full)** | **0.0165** | 4.64 | **0.7497** |
| GQA2MHA | 0.0179 | 4.60 | 0.7397 |
| w/o ortho | 0.0182 | 4.64 | 0.7308 |
| GQA2MLP | 0.0189 | 1.30 | 0.6966 |
| w/o GQA | 0.0242 | 3.53 | 0.6785 |
| Direct Pooling | 0.0418 | **4.74** | 0.4127 |
| w/o OOF | 0.0526 | 3.85 | 0.4871 |