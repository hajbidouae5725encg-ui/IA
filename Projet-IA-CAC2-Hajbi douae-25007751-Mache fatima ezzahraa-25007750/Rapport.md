# 🎓 ENCG Settat — Intelligence Artificielle

## 📊 Compte Rendu de Projet

### Analyse Machine Learning — Dataset Adult

**Filière :** CAC 2 — Semestre 8

**Réalisé par :** Hajbi Douae 25007751 - fatima ezzahraa mache 25007750

**Année universitaire :** 2025–2026

<img src="douae.jpeg" style="height:300px;margin-right:300px; float:left; border-radius:10px;"/> <img src="mache photo.jpeg" style="height:300px;margin-right:300px; float:left; border-radius:10px;"/>
---

# 📑 Table des Matières

1. Introduction et Contexte
2. Présentation du jeu de données
3. Algorithme 1 — Régression Logistique
4. Algorithme 2 — Random Forest
5. Algorithme 3 — Isolation Forest
6. Comparaison et Évaluation Globale
7. Synthèse et Recommandation
8. Annexe — Code Source

---

# 1. 📌 Introduction et Contexte

## 1.1 Présentation de l’étude

Ce projet vise à analyser et comparer les performances de trois algorithmes de Machine Learning appliqués à un problème de classification : la prédiction du niveau de revenu (>50K) à partir de caractéristiques socio-économiques.

Les algorithmes étudiés sont :

* Régression Logistique (modèle supervisé linéaire)
* Random Forest (ensemble learning supervisé)
* Isolation Forest (détection d’anomalies non supervisée)

---

## 1.2 Objectif

L’objectif principal est :

* d’évaluer la performance des modèles
* d’identifier le meilleur algorithme
* de comprendre les limites de chaque approche

---

# 2. 📊 Présentation du jeu de données

Le dataset utilisé est le **Adult Dataset**, largement utilisé en Machine Learning.

### 🔹 Variables principales :

* âge
* niveau d’éducation
* profession
* statut marital
* heures de travail
* capital gain / loss
* revenu (variable cible)

### 🔹 Caractéristiques :

* Dataset réel
* Problème de classification binaire
* Présence de variables catégorielles
* Déséquilibre modéré des classes

---

# 3. 🤖 Algorithme 1 — Régression Logistique

## 3.1 Principe

La régression logistique permet d’estimer la probabilité d’appartenance à une classe à l’aide d’une fonction sigmoïde.

## 3.2 Avantages

✔ Simple et rapide
✔ Interprétable

## 3.3 Limites

✘ Ne capture pas les relations non linéaires
✘ Performance limitée sur données complexes

## 3.4 Analyse

Ce modèle sert de **baseline**.
Il permet d’évaluer si les relations dans les données sont linéaires.

---

# 4. 🌲 Algorithme 2 — Random Forest

## 4.1 Principe

Le Random Forest est un ensemble d’arbres de décision utilisant le principe du bagging.

## 4.2 Avantages

✔ Très performant
✔ Capture les interactions complexes
✔ Robuste au bruit

## 4.3 Limites

✘ Moins interprétable
✘ Plus coûteux en calcul

## 4.4 Analyse

C’est généralement le modèle le plus performant dans ce type de problème grâce à sa capacité à modéliser des relations complexes.

---

# 5. ⚠️ Algorithme 3 — Isolation Forest

## 5.1 Principe

L’Isolation Forest est utilisé pour détecter des anomalies sans utiliser de labels.

## 5.2 Avantages

✔ Pas besoin de données labellisées
✔ Détection rapide d’anomalies

## 5.3 Limites

✘ Beaucoup de faux positifs
✘ Moins adapté à la classification classique

## 5.4 Analyse

Ce modèle est utile dans des contextes exploratoires mais moins performant pour une classification supervisée.

---

# 6. 📈 Comparaison et Évaluation Globale

| Algorithme            | Performance | Interprétabilité | Type          |
| --------------------- | ----------- | ---------------- | ------------- |
| Régression Logistique | Moyenne     | Élevée           | Supervisé     |
| Random Forest         | Élevée      | Moyenne          | Supervisé     |
| Isolation Forest      | Faible      | Faible           | Non supervisé |

---

## 🔍 Analyse globale

* Le Random Forest domine en performance
* La régression logistique est utile comme référence
* L’Isolation Forest est intéressant sans labels

---

# 7. ✅ Synthèse et Recommandation

### 🎯 Résultat final

Le **Random Forest** est le modèle recommandé car :

* il offre la meilleure précision
* il gère les interactions complexes
* il est robuste aux données réelles

---

### ⚠️ Remarque

Le choix du modèle dépend :

* de la disponibilité des données
* du besoin d’interprétabilité
* du contexte métier

---

# 8. 💻 Annexe — Code Source

```python
from sklearn.ensemble import RandomForestClassifier
from sklearn.linear_model import LogisticRegression
from sklearn.ensemble import IsolationForest

# Exemple de modèle Random Forest
rf = RandomForestClassifier(n_estimators=100)
rf.fit(X_train, y_train)

# Prédictions
y_pred = rf.predict(X_test)
```

---

# 📚 Conclusion Générale

Ce projet met en évidence l’importance du choix du modèle en Machine Learning.
Il montre que les méthodes d’ensemble comme le Random Forest sont souvent les plus performantes dans des contextes réels.

---

