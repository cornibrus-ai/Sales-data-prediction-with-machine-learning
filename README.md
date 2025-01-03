# Sales-data-prediction-with-machine-learning
Conception d'un système qui analyse des données de ventes, les stocke dans une base de données SQL, les affiche sous forme de rapports et graphiques interactifs, et utilise des algorithmes de machine learning pour prédire les tendances futures.

### Fonctionnalités
1. **Gestion des données avec Excel/VBA** :
   - Importation et exportation des données entre Excel et une base SQL.
   - Modification et consultation rapide des données.

2. **Interface Web en PHP** :
   - Consultation des données stockées dans la base SQL sous forme de tableau.
   - Visualisation des tendances à l’aide de graphiques interactifs (Chart.js).

3. **Prédiction avec TensorFlow** :
   - Analyse des ventes passées et prédictions des ventes futures grâce à un modèle de machine learning.
   - Génération de graphiques des données historiques et des prédictions.

---

### Technologies utilisées
- **Bases de données** : MySQL ou SQLite.
- **Automatisation Excel** : VBA.
- **Développement web** : PHP, HTML, CSS, JavaScript.
- **Data Science** : Python, pandas, NumPy, TensorFlow, matplotlib.
- **Graphiques interactifs** : Chart.js.

---

### Installation et Configuration

##### Pré-requis
**Outils nécessaires** :
  - MySQL (ou SQLite) pour la base de données.
  - Microsoft Excel (avec support VBA).
  - Serveur local comme XAMPP ou WAMP.
  - Python 3.0 avec les bibliothèques suivantes :
    - pandas
    - numpy
    - tensorflow
    - matplotlib
  - Navigateur web pour l’interface utilisateur.

---

### Structure du code

data/ : *Contient toutes les données utilisées dans le projet.*
   raw/ *pour les données initiales non modifiées*
   processed/ *pour les données nettoyées, prêtes à être analysées.*

database/ : *Contient les scripts SQL pour créer la base de données*
   schema.sql *Création des tables SQL*
   seed.sql *Données simulées pour tests*
   config.py *pour centraliser les paramètres d’accès (e.g., mot de passe, host).*

excel_vba/ : *Contient les fichiers Excel et les macros VBA pour gérer les données.*
   data_management.xlsm *Fichier Excel avec macros*
   macros/ : *Scripts VBA organisés par fonction*
      connect.vba *Script de connexion SQL*
      export.vba *Exportation des données vers SQL*
      import.vba *Importation des données depuis SQL*

web_app/ : *Organisation claire entre backend (app.php), frontend (templates et static), et API.*
   templates/ : *Fichiers HTML*
      index.html *Page principale*
      charts.html *Graphiques interactifs*
   static/ : *Fichiers statiques (CSS, JS)*
      styles.css *Feuille de styles*
      script.js *Logique frontend*
   app.php *Fichier principal pour le backend PHP*
   api/ : *Points d'API pour les données*
      get_daya.php *Récupérer les données depuis SQL*
      post_data.php *Ajouter des données à la base SQL*

machine_learning/ : *Scripts pour entraîner et déployer le modèle TensorFlow*
   models/: *Modèles d'IA sauvegardés*
      sales_models.h5 *Modèle TensorFlow entraîné*
   scripts/ : *Scripts Python pour l'entraînement et l'inférence*
      train_model.py *Script d'entraînement du modèle*
      predict.py *Prédictions des ventes futures*
   notebooks/ : *Jupyter notebooks pour la documentation et la traçabilité des analyses exploratoires*
      data_analysis.ipynb
      ml_training.ipynb

tests/ : *Contient les scripts de tests unitaires et d’intégration.*
   database_tests.py *Tests pour les opérations SQL*
   web_app_tests.py *Tests pour les routes PHP*
   ml_tests.py *Tests pour le modèle TensorFlow*

.gitignore : *Fichiers à ignorer par Git*

main.py : *Point d’entrée pour la partie Python. Par exemple, il pourrait coordonner l’analyse des données et appeler les prédictions.*

README.md : *Documentation du projet*

requirements.txt : *Liste des dépendances Python à installer via le terminal* 

---

### Commandes utiles

Installation des dépendances Python :
'''pip install -r requirements.txt'''

Lancer les tests unitaires
'''python -m unittest discover tests/'''

Démarrer le serveur local pour PHP
'''php -S localhost:8000 -t web_app/'''