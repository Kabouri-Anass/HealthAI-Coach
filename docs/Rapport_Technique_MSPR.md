# Rapport Technique : Plateforme HealthAI Coach

## 1. Introduction
### 1.1 Présentation du contexte
[cite_start]HealthAI Coach est une jeune startup française évoluant sur le marché de la santé connectée et du coaching personnalisé. [cite_start]Dans un secteur en pleine croissance (+20%/an), l'entreprise se distingue par une approche holistique intégrant la nutrition, le sport et le suivi biométrique[cite: 52, 56]. 

### 1.2 Enjeux et Business Model
[cite_start]La startup adopte un modèle économique hybride pour répondre aux besoins de cibles variées (Millennials, actifs urbains)[cite: 40, 46]:
* [cite_start]**Freemium** : Accès aux fonctionnalités de base (journal alimentaire, IMC)[cite: 41].
* [cite_start]**Premium (9,99€/mois)** : Recommandations personnalisées via IA[cite: 42].
* [cite_start]**Premium+ (19,99€/mois)** : Intégration de données biométriques et consultations[cite: 43].
* [cite_start]**B2B** : Offre en marque blanche pour les salles de sport et mutuelles[cite: 44].

### 1.3 Objectifs de la mission
[cite_start]Notre équipe a pour mission de concevoir et livrer le backend métier de cette plateforme[cite: 79]. Les objectifs principaux sont :
1. [cite_start]L'automatisation de la collecte de données hétérogènes[cite: 81].
2. [cite_start]Le nettoyage et la garantie de qualité des données pour les futurs modules IA[cite: 82].
3. [cite_start]La mise à disposition d'une API REST sécurisée et d'un dashboard analytique accessible (RGAA)[cite: 84, 85].
## 2. Organisation de l'équipe
### 2.1 Répartition des rôles et responsabilités
Pour garantir l'efficacité du projet HealthAI Coach, nous avons défini des rôles spécifiques basés sur les compétences de chacun :

* **P1 - Coordinateur Technique & BDD** : Responsable de la conception Merise (MCD/MLD) et de l'intégrité des données SQL.
* **P2 - Data Engineer ETL** : En charge du pipeline d'ingestion Python, du nettoyage et de la qualité des données.
* **P3 - Développeur Backend** : Développement de l'API REST Flask, de la sécurité JWT et intégration du module IA.
* **P4 - Développeur Frontend** : Création du dashboard interactif sous React avec un focus sur l'accessibilité RGAA.
* **P5 - DevOps & Tech Writer** (Moi) : Gestion du cycle de vie Git, conteneurisation Docker, déploiement et rédaction technique.

### 2.2 Outils de collaboration et Méthodologie
Nous avons adopté une méthodologie agile pour assurer la tenue des délais (Livrables L1 à L8) :
* **GitHub** : Centralisation du code source et gestion des versions.
* **Trello** : Suivi des tâches en temps réel (colonnes À faire, En cours, Terminé).
* **Discord** : Communication instantanée pour résoudre les blocages techniques.
* **Docker** : Garant de l'isomorphisme entre nos environnements de développement et de production.