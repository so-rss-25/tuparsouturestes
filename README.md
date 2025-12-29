# Tu pars ou tu restes ? 
Projet sur l'attrition en entreprise

## Contexte
L’attrition (le départ volontaire des employés) est un enjeu majeur pour les entreprises : perte de compétences, baisse de productivité, coûts élevés de recrutement et d’intégration…
Dans ce projet, nous avons étudié l’attrition à partir du dataset IBM HR Analytics Attrition Dataset (Kaggle) afin de :
* Comprendre pourquoi les employés quittent leur entreprise
* Prédire qui pourrait potentiellement partir dans les mois à venir

## Objectifs du projet
* Objectif 1 : Explication
Analyser les facteurs clés influençant l’attrition grâce à plus de 30 variables RH (âge, ancienneté, service, satisfaction, heures supplémentaires…).

* Objectif 2 : Prédiction
Construire un modèle capable de prédire le risque de départ pour chaque employé : AttriScan.

* Objectif 3 : Action RH
Mettre en place un système simple d’utilisation pour les équipes RH :
  * Tableau de bord Looker Studio
  * Alertes email automatiques via Zapier
  * Interprétation claire et visuelle des risques
 
## Données
* Source : https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset
* Nombre de lignes : 1470
* Variables : ~35
* Type : Informations RH internes (poste, salaire, satisfaction, déplacements, heures sup, ancienneté…)

## Datastack
* E&L : Google Colab, Python
* Data Platform : GoogleSheets
* Transform : Google Colab, Python, Gradio
* BI : Looker Studio
* Documentation : Notion
* Automation : Zapier

## Méthodologie
* Préparation & Nettoyage
  * Vérification des doublons & données nulles
  * Gestion des variables catégorielles : traduction, correspondance et segmentation des colonnes
  * Génération de prénoms, noms & emails fictifs

* Analyse Exploratoire
  * Analyse univariée
  * Analyse de la variable attrition : vs toutes les autres variables + recherche de profils type (personne qui part, personne qui reste)
  * Analyse bi-variée après identification des premiers facteurs clés : salaire, âge, niveau hiérarchique, genre
  * Analyse multi-variée : heatmaps pour repérer les corrélations et analyses complémentaires pour vérifier ou réfuter des hypothèses

* Modélisation (AttriScan)
  * Sélection des features et de la target
  * Entraînement de plusieurs modèles : Logistic Regression, Random Forest, XGBoost, EDABoost
  * Dataset non équilibré donc utilisation d'un SMOTE
  * Évaluation : accuracy, recall, r2-score, f1-score, optimisation du recall dans notre cas
  * Modèle final sélectionné : Logisitic Regression avec un SMOTE
  * Interprétabilité : SHAP

* Intégration & Outils
  * Dashboard Looker Studio
  * Mise en place d’un scoring pour chaque employé
  * Création d'un outil interactif sur Google Colab via Gradio
  * Système d’alertes automatisées sur Zapier

## Résultats
* Identification claire des populations à risque
* Mise en lumière des leviers RH prioritaires
* Dashboard interactif et exploitable immédiatement
* Prédiction automatisée et notification proactive
* Outil explicable et orienté décision

## Conclusion
Prévenir l’attrition coûte beaucoup moins cher que remplacer un employé. Avec AttriScan, les entreprises peuvent :
* anticiper les départs
* ajuster leurs politiques RH
* accompagner les jeunes talents
* réduire les coûts de recrutement

## Équipe
Sophie Reiss / Louise Euriat / Guillaume Gaglio / Clément Monteil
