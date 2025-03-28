# 📘 Machine Learning II - Reinforcement Learning

### **Université** : Mohamed Premier Oujda  
### **École** : Nationale de l'Intelligence Artificielle et du Digital Berkane  
### **Année universitaire** : 2024 / 2025  
### **Professeur** : [Mohamed Khalifa BOUTAHIR](email@example.com)   
### **Étudiant** : [Oualid Ghaffari](walid.ghiffario@gmail.com)  
---

## 📖 Introduction  
Ce repository contient une série de **Travaux Pratiques (TP)** sur l'**Apprentissage par Renforcement** (*Reinforcement Learning - RL*). Il couvre :  
✅ Les algorithmes tabulaires comme **Q-Learning** et **SARSA**.  
✅ Les méthodes avancées comme **Proximal Policy Optimization (PPO)**.  
✅ L’implémentation et l’expérimentation dans des **environnements simulés**.  

---

## 📚 Table des Matières  
1. [🔹 TP1 - Découverte d'OpenAI Gym](#[https://github.com/ghaffariOualid/Reinforcement-Learning_ENIAD/blob/main/TP01.ipynb])  
2. [❄️ TP2 - Q-Learning avec FrozenLake](#-tp2---q-learning-avec-frozenlake)  
3. [🚦 TP3 - Optimisation des Feux de Circulation](#-tp3---optimisation-des-feux-de-circulation)  
4. [🚖 TP4 - PPO avec Taxi-v3](#-tp4---ppo-avec-taxi-v3)  
5. [📂 Structure du Repository](#-structure-du-repository)  
6. [🛠️ Installation](#-installation)  
7. [🤝 Contributions](#-contributions)  
8. [📚 Ressources](#-ressources)  
---

## 🔹 TP1 - Découverte d'OpenAI Gym  

### 🎯 Objectifs  
✔ Se familiariser avec les environnements **Reinforcement Learning**.  
✔ Explorer l’environnement **CartPole-v1**.  
✔ Implémenter des **politiques aléatoires**.  

### 📊 Résultats clés  
- **Compréhension** des **espaces d'états** et **d'actions**.  
- **Performance des actions aléatoires** : ~20 pas avant échec.  
- **Visualisation** des **états et récompenses**.  

---

## ❄️ TP2 - Q-Learning avec FrozenLake  

### 🎯 Objectifs  
✔ Implémenter l'algorithme **Q-Learning**.  
✔ Comprendre **l’exploration vs exploitation**.  
✔ Analyser la **convergence de la Q-table**.  

### 🔢 Algorithme Q-Learning  
$$ Q(s,a) ← Q(s,a) + α[r + γ \max Q(s',a') - Q(s,a)] $$  

### 📊 Performances  

| Métrique                        | Valeur |
|---------------------------------|--------|
| Taux de réussite (aléatoire)    | 0 %   |
| Taux de réussite (après Q-Learning) | 100%   |
| Épisodes d'entraînement         | 5000   |

---

## 🚦 TP3 - Optimisation des Feux de Circulation  

### 🎯 Objectifs  
✔ Comparer **Q-Learning** (*off-policy*) et **SARSA** (*on-policy*).  
✔ Optimiser les feux de circulation en **réduisant le temps d’attente**.  
✔ Expérimenter avec un **environnement personnalisé** []simulant un réseau routier.    

### 🔢 Algorithmes  

#### **Q-Learning (off-policy)**  
$$ Q(s,a) ← Q(s,a) + α[r + γ \max Q(s',a') - Q(s,a)] $$  

#### **SARSA (on-policy)**  
$$ Q(s,a) ← Q(s,a) + α[r + γ Q(s',a') - Q(s,a)] $$  

### 📊 Performances  

| Algorithme  | Réduction Temps d'Attente |
|------------|--------------------------|
| Q-Learning | 82%                      |
| SARSA      | 78%                      |

---

## 🚖 TP4 - PPO avec Taxi-v3  

### 🎯 Objectifs  
✔ Implémenter **Proximal Policy Optimization (PPO)**.  
✔ Tester sur **Taxi-v3** avec **Stable Baselines3**.  

### 🔢 Fonction objectif avec Clipping  
$$ L(θ) = ᵜ[\min(r_t(θ)A_t, clip(r_t(θ), 1-ε, 1+ε)A_t)] $$  

### 📊 Résultats  

| Phase              | Taux de Réussite | Steps Moyens |
|-------------------|----------------|-------------|
| Avant entraînement | 0%             | 200+        |
| Après 1000 épisodes | 92%            | 15.2        |

---

## 📂 Structure du Repository  

- **ML2/**  
  - 📁 `TP1/` - Découverte OpenAI Gym  
  - 📁 `TP2/` - Q-Learning FrozenLake  
  - 📁 `TP3/` - Feux de Circulation  
  - 📁 `TP4/` - PPO Taxi-v3    
  - 📄 `README.md` - Ce fichier  


---
## ✅ Prérequis  
✔ **Python 3.x**  
✔ **pip install --upgrade gymnasium pygame numpy**  

---

## 📚 Ressources  

### 📖 Documentation Officielle  

- 📌 [**OpenAI Gymnasium**](https://gymnasium.farama.org/) - Environnements RL standardisés.  
- 📌 [**Stable Baselines3**](https://stable-baselines3.readthedocs.io/) - Implémentations avancées des algorithmes RL.  

### 📕 Livres Fondamentaux  

| 📘 Livre | 🔗 Lien | 🎯 Focus |
|----------|--------|---------|
| *Reinforcement Learning: An Introduction* (Sutton & Barto) | [📄 Lien PDF](http://incompleteideas.net/book/RLbook2020.pdf) | Théorie RL |
| *Deep Reinforcement Learning Hands-On* (Maxim Lapan) | [🔗 Packt](https://www.packtpub.com/product/deep-reinforcement-learning-hands-on-second-edition/9781838826994) | Pratique avec PyTorch |

---

## 📝 Remarques Finales  

📌 Ce repository couvre les **fondamentaux du Reinforcement Learning** à travers :  

✅ Des **algorithmes tabulaires** (**Q-Learning, SARSA**).  
✅ Des **méthodes avancées** (**PPO, policy gradient**).  
✅ Des **applications pratiques** sur des problèmes réels.  
✅ Des **visualisations et comparaisons** pour mieux comprendre chaque approche.  

Nous espérons que ces ressources vous aideront dans votre apprentissage du **Reinforcement Learning** ! 💡🔥
