# Formation au métabarcoding avec BARQUE
*De l'assurance qualité à l'assignation taxonomique*

## Plan de la présentation

### 1. Introduction
- Objectifs de la formation
- Vue d'ensemble du métabarcoding
- Comment fonctionne le séquençage Illumina

### 2. Les fichiers FASTQ
- Structure des fichiers de sortie du séquenceur
- Format FASTQ et interprétation des scores de qualité
- Causes de dégradation de la qualité

### 3. Manipuler des fichiers FASTQ avec R
- Installation des packages Bioconductor requis
- Lecture et extraction d'informations des fichiers FASTQ
- Analyses statistiques et graphiques de qualité
- Exercice pratique avec vos propres données

### 4. BARQUE - Pipeline de métabarcoding
- Présentation du pipeline développé par Éric Normandeau
- Les 6 grandes étapes :
  1. Validation du projet
  2. Nettoyage des données (Trimmomatic)
  3. Appariement des lectures (FLASH)
  4. Séparation des amplicons (reconnaissance d'amorces)
  5. Retrait des chimères (VSEARCH)
  6. Assignement taxonomique (BOLD, MitoFish, etc.)

### 5. Utilisation pratique de BARQUE
- Téléchargement et installation
- Configuration des amorces et paramètres
- Workflow utilisateur complet
- Utilisation avec Docker

## Ressources

- **Données d'exemple** : [Dataset de test BARQUE](https://github.com/enormandeau/barque_test_dataset)
- **Code source BARQUE** : [GitHub - enormandeau/barque](https://github.com/enormandeau/barque)
- **Packages R requis** : ShortRead, Biostrings, Rqc

## Post formation

- Fixer l'application BARQUE enbarqué dans Shiny sur la selection des primers
- Montrer le rapport et demander du feedback
