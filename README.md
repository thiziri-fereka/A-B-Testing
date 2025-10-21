# A-B-Testing
# 📊 A/B Testing – Analyse de performance et test statistique

## 🧠 Contexte du projet  
Ce projet a pour objectif d’évaluer l’impact d’une nouvelle version d’un produit (ou d’une page web) par rapport à une version existante via des méthodes d’**A/B testing**.  
Le jeu de données utilisé est le **“A/B Testing Dataset”** disponible sur Kaggle. :contentReference[oaicite:4]{index=4}

---

## 🎯 Objectifs  
- Vérifier et nettoyer les données (gestion des valeurs manquantes, des doublons, des incohérences).  
- Formuler les **hypothèses nulle et alternative** pour le test.  
- Comparer les taux de conversion entre les deux groupes (contrôle vs traitement).  
- Réaliser un **z-test de différence de proportions**, et calculer un **intervalle de confiance à 95 %**.  
- Interpréter les résultats pour en tirer des conclusions opérationnelles.

---

## 🧩 Données utilisées  
Le dataset contient les colonnes principales :  
- `user_id` : identifiant unique de la session ou du visiteur  
- `timestamp` : moment de la visite  
- `group` : groupe d’appartenance (contrôle ou traitement)  
- `landing_page` : version de la page assignée (ancienne ou nouvelle)  
- `converted` : indicateur binaire de conversion (0 = non, 1 = oui) :contentReference[oaicite:5]{index=5}  
Avant l’analyse :  
- Suppression des doublons  
- Gestion des valeurs manquantes et des incohérences  
- Structuration des groupes A et B pour l’analyse statistique

---

## ⚙️ Outils et technologies  
- **Python 3**  
- **Pandas**, **NumPy** – pour le nettoyage et la manipulation des données  
- **SciPy**, **Statsmodels** – pour les tests statistiques (z-test, intervalles de confiance)  
- **Matplotlib**, **Seaborn** – pour la visualisation des résultats  
- **Jupyter Notebook**

---

## 🧪 Méthodologie  
1. **Préparation des données**  
   - Identifié et supprimé les doublons  
   - Vérifié et imputé/éliminé les valeurs manquantes  
   - Corrigé les incohérences éventuelles dans les valeurs (ex. pages, groupes)  
   - Créé les groupes « contrôle » vs « traitement » et calculé les taux de conversion  
2. **Définition des hypothèses**  
   - H₀ : *Le taux de conversion du groupe traitement est égal à celui du groupe contrôle*  
   - H₁ : *Le taux de conversion du groupe traitement est différent (ou supérieur) à celui du groupe contrôle*  
3. **Analyse statistique**  
   - Calcul des taux de conversion pour chaque groupe  
   - Utilisation d’un **z-test** de différence de proportions  
   - Calcul d’un **intervalle de confiance à 95 %** pour la différence de conversion  
4. **Interprétation des résultats**  
   - Vérification du p-value par rapport à un seuil α (ex. 0,05)  
   - Conclusion sur le rejet (ou non) de l’hypothèse nulle  
   - Implications business : recommandation quant à l’adoption de la version « nouvelle »

---

## 📈 Résultats  
- Le test statistique a permis d’évaluer si la différence de conversion entre les deux versions était **statistiquement significative**.  
- L’intervalle de confiance a fourni une estimation robuste de la marge d’erreur autour de cette différence.  
- En fonction des résultats, des recommandations opérationnelles ont été formulées pour orienter la décision d’implémentation.

*(Les visualisations détaillées et les étapes sont disponibles dans le fichier `A_B_TESTING.ipynb`.)*
