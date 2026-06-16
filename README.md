# DecodeLabs — Data Science Project 1  
## Advanced EDA & Feature Engineering — Titanic Dataset  

### 🎯 Objectifs
- Nettoyer et préparer le dataset Titanic.  
- Créer de nouvelles features pertinentes.  
- Entraîner un modèle de classification (Logistic Regression, Random Forest).  
- Évaluer la performance avec des métriques standards.  

### 📂 Dataset
- Source : `sns.load_dataset("titanic")` (Seaborn).  
- Taille : 891 lignes, 15 colonnes.  
- Variables principales : `survived`, `pclass`, `sex`, `age`, `sibsp`, `parch`, `fare`, `embarked`.  

### ⚙️ Pipeline IPO
1. **[EDA & Cleaning](ca://s?q=Exploratory_data_analysis_steps)**  
   - Gestion des valeurs manquantes (drop, imputation, suppression colonnes).  
   - Traitement des outliers (Winsorization IQR).  
2. **[Feature Engineering](ca://s?q=Feature_engineering_examples)**  
   - `family_size = sibsp + parch + 1`  
   - `is_alone = 1 si family_size == 1`  
   - `age_fare_ratio = age / (fare + 1)`  
3. **[Validation](ca://s?q=Data_validation_in_projects)**  
   - Vérification dataset non vide, pas de missing values.  
   - Suppression collinéarité > 0.80.  
4. **[Model Training](ca://s?q=Titanic_survival_prediction_model)**  
   - Logistic Regression.  
   - Random Forest (comparaison).  
5. **[Evaluation](ca://s?q=Model_evaluation_metrics_in_ML)**  
   - Accuracy, Confusion Matrix.  
   - ROC Curve + AUC.  
   - Cross-validation (CV scores).  

### ✅ Conclusion
Le pipeline IPO a permis de transformer le dataset Titanic en données propres et enrichies.  
Les modèles montrent une bonne capacité prédictive, avec Random Forest légèrement meilleur.  
Améliorations possibles : hyperparameter tuning, ajout d’autres features (titre du passager, cabine).  

---
 
