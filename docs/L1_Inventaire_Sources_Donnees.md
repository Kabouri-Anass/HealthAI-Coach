# Livrable 1 : Rapport d'inventaire des sources de données

## 1. Introduction et Contexte
Ce document recense l'ensemble des sources de données, internes et externes, utilisées pour le projet **HealthAI Coach**. [cite_start]L'objectif est de constituer un référentiel de données hétérogènes fiable pour alimenter les algorithmes de recommandation et les tableaux de bord analytiques[cite: 73, 76].

## 2. Inventaire des sources sélectionnées
[cite_start]Conformément au cahier des charges, nous utilisons au minimum deux sources de données distinctes[cite: 129]:

### A. Base Nutritionnelle (Kaggle)
* [cite_start]**Source** : Daily Food & Nutrition Dataset [cite: 184]
* [cite_start]**Format** : CSV / JSON [cite: 182]
* [cite_start]**Données** : Apports énergétiques, macronutriments et tracking santé [cite: 183, 186]
* [cite_start]**Justification** : Permet de fournir un suivi nutritionnel précis pour les comptes Freemium et Premium[cite: 41, 42].

### B. Catalogue d'exercices (GitHub)
* [cite_start]**Source** : ExerciseDB API Repository [cite: 191]
* [cite_start]**Format** : JSON (API) [cite: 182]
* [cite_start]**Données** : 1300+ exercices avec groupes musculaires et instructions [cite: 191, 194]
* [cite_start]**Justification** : Base indispensable pour l'accompagnement sportif personnalisé[cite: 37].

### C. Profils Utilisateurs & Biométrie (Simulés)
* [cite_start]**Source** : Gym Members Exercise Dataset [cite: 196]
* [cite_start]**Données** : Âge, poids, BPM, calories brûlées [cite: 198]
* [cite_start]**Justification** : Utilisé pour tester la progression des utilisateurs et les indicateurs de santé connectée[cite: 37].

graph TD
    subgraph "Sources Externes"
        A[Kaggle: Nutrition] 
        B[GitHub: ExerciseDB]
        C[Kaggle: Biométrie]
    end

    subgraph "Traitement & Nettoyage (P2)"
        D{Pipeline ETL Python}
        E[Validation & Nettoyage]
    end

    subgraph "Stockage (P1)"
        F[(Base PostgreSQL)]
    end

    subgraph "Exposition & Visualisation (P3/P4)"
        G[API REST Flask]
        H[Dashboard React]
    end

    A & B & C --> D
    D --> E
    E --> F
    F --> G
    G --> H