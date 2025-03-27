# Machine Learning II - Reinforcement Learning

**Université** : Mohamed Premier Oujda  
**École** : Nationale de l'Intelligence Artificielle et du Digital Berkane  
**Année universitaire** : 2024 / 2025  
**Professeur** : [Mohamed Khalifa BOUTAHIR](mailto:email@example.com) 
________________________________________
📖 Introduction
Ce repository contient une série de Travaux Pratiques (TP) sur l'apprentissage par renforcement ( Reinforcement Learning - RL). Il couvre les bases des algorithmes tabulaires comme le Q-Learning et SARSA, jusqu'aux méthodes plus avancées comme Proximal Policy Optimization (PPO).
Les TP sont conçus pour aider les étudiants à comprendre et implémenter ces algorithmes dans des environnements simulés.
________________________________________

# Table des Matières
1. [TP1 - Découverte d'OpenAI Gym](#tp1---découverte-dopenai-gym)  
2. [TP2 - Q-Learning avec FrozenLake](#tp2---q-learning-avec-frozenlake)  
3. [TP3 - Optimisation des Feux de Circulation](#tp3---optimisation-des-feux-de-circulation)  
4. [TP4 - PPO avec Taxi-v3](#tp4---ppo-avec-taxi-v3)  
5. [Structure du Repository](#structure-du-repository)  
6. [Installation](#installation)  
7. [Ressources](#ressources)  
________________________________________
# TP1 - Découverte d'OpenAI Gym
Objectifs
•	Se familiariser avec les environnements de Reinforcement Learning
•	Explorer l'environnement CartPole-v1
•	Implémenter des politiques aléatoires
Résultats Clés
•	Compréhension des espaces d'états et d'actions
•	Performance des actions aléatoires : ~20 pas avant échec
•	Visualisation des états et récompenses
________________________________________
 # TP2 - Q-Learning avec FrozenLake
Objectifs
•	Implémenter l'algorithme Q-Learning
•	Comprendre l'exploration vs exploitation
•	Analyser la convergence de la Q-table
Algorithmes Clés
Q(s,a) ← Q(s,a) + α[r + γ max Q(s',a') - Q(s,a)]
Résultats
Métrique	Valeur
Taux de réussite (aléatoire)	1.5%
Taux de réussite (après Q-Learning)	75%
Épisodes d'entraînement	5000
________________________________________
# TP3 - Optimisation des Feux de Circulation
Comparaison Q-Learning vs SARSA
# Q-Learning (off-policy)
Q(s,a) ← Q(s,a) + α[r + γ max Q(s',a') - Q(s,a)]

# SARSA (on-policy)
Q(s,a) ← Q(s,a) + α[r + γ Q(s',a') - Q(s,a)]
Performances
Algorithme	Réduction Temps d'Attente
Q-Learning	82%
SARSA	78%
________________________________________
# TP4 - PPO avec Taxi-v3
Proximal Policy Optimization
Fonction objectif avec clipping :
L(θ) = ᵜ[min(r_t(θ)A_t, clip(r_t(θ), 1-ε, 1+ε)A_t)]
Résultats
Phase	Taux de Réussite	Steps Moyens
Avant entraînement	0%	200+
Après 1000 épisodes	92%	15.2
________________________________________
📂 Structure du Repository
ML2/
├── TP1/                  # Découverte OpenAI Gym
├── TP2/                  # Q-Learning FrozenLake
├── TP3/                  # Feux de Circulation
├── TP4/                  # PPO Taxi-v3
├── requirements.txt       # Dépendances
└── README.md             # Ce fichier
________________________________________
🛠️ Installation
Prérequis
•	Python 3.x
•	pip installé
Installation
1.	Cloner le repository :
git clone https://github.com/votre-utilisateur/ML2.git
2.	Créer un environnement virtuel et installer les dépendances :
cd ML2
python -m venv venv
source venv/bin/activate  # (ou venv\Scripts\activate sous Windows)
pip install -r requirements.txt
3.	Exécuter un TP :
python tp1.py
________________________________________
# Contributions
Les contributions sont les bienvenues ! Pour proposer une modification :
1.	Forker le repository
2.	Créer une branche avec un nom explicite :
git checkout -b feature-nouvelle-fonctionnalite
3.	Faire un commit et push :
git commit -m "Ajout d'une nouvelle fonctionnalité"
git push origin feature-nouvelle-fonctionnalite
4.	Ouvrir une Pull Request sur GitHub.
________________________________________
# Ressources
Documentation :
•	OpenAI Gymnasium
•	Stable Baselines3
Livres :
•	"Reinforcement Learning: An Introduction" - Sutton & Barto
•	"Deep Reinforcement Learning Hands-On" - Maxim Lapan
Articles :
•	Proximal Policy Optimization (PPO) - Schulman et al. 2017
•	Q-Learning Convergence - Watkins & Dayan 1992
________________________________________
📝 Remarques Finales
Ce repository couvre les fondamentaux du Reinforcement Learning :
•	Des algorithmes tabulaires (Q-Learning, SARSA)
•	Aux méthodes de politique avancées (PPO)
•	Avec applications sur des problèmes concrets
•	Les visualisations et comparaisons permettent de bien comprendre les forces/faiblesses de chaque approche.


