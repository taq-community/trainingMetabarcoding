# Formation au métabarcoding avec BARQUE
*De l'assurance qualité à l'assignation taxonomique*

## Mettre à jour et publier la présentation

### Modifier la présentation

1. Éditer le fichier principal de la présentation : [index.qmd](index.qmd)
2. Prévisualiser les changements localement:

```bash
quarto preview index.qmd
```

### Publier la présentation

Pour publier la présentation mise à jour:

```bash
quarto publish
```

Cette commande va :
- Générer la présentation HTML
- Créer/mettre à jour la branche `gh-pages`
- Pousser les changements vers GitHub
- La présentation sera automatiquement déployée via GitHub Pages

**Note** : Assurez-vous d'avoir Quarto installé sur votre système. Pour l'installation, visitez : [https://quarto.org/docs/get-started/](https://quarto.org/docs/get-started/)

## Plan de la présentation

Durée: 2h30

### 1. Introduction
- Objectifs de la formation
- Installation des librairies R requises
- Vue d'ensemble du métabarcoding
- Fonctionnement du séquençage Illumina (fluorophores, chromatographes, scores de qualité)

### 2. Les fichiers FASTQ
- Fichiers de sortie du séquenceur Illumina (nomenclature, paired-end, lanes)
- Structure du fichier FASTQ (4 lignes par amplicon)
- Ligne d'identification (ID instrument, flowcell, coordonnées, barcodes)
- Interprétation des scores de qualité (encodage ASCII, scores Phred, précision)
- Causes de dégradation de la qualité

### 3. Manipuler des fichiers FASTQ avec R
- Lecture de fichiers FASTQ avec ShortRead
- Extraction des informations (séquences, identifiants, qualités)
- Résumés statistiques et composition en bases
- Assurance qualité avec la librairie Rqc
- Exercice pratique avec vos propres données

### 4. BARQUE - Pipeline de métabarcoding
- Présentation du pipeline développé par Éric Normandeau
- Les 6 grandes étapes :
  1. Validation du projet
  2. Nettoyage des données (Trimmomatic)
  3. Appariement des lectures (FLASH)
  4. Séparation des amplicons (reconnaissance d'amorces)
  5. Retrait des chimères (VSEARCH)
  6. Assignement taxonomique (BOLD, MitoFish, SILVA, etc.)

### 5. Utilisation pratique de BARQUE
- Téléchargement et installation
- Configuration des amorces (primers.csv)
- Ajustement des paramètres (barque_config.sh)
- Base de données par type d'amorces
- Comment VSEARCH assigne la taxonomie
- Gestion des correspondances multiples

### 6. Utiliser Docker pour exécuter BARQUE
- Pourquoi utiliser Docker
- Comment Docker fonctionne
- Télécharger l'image Docker
- Exécuter BARQUE dans un conteneur Docker

### 7. Extra
- Application Shiny embarquée pour exécuter BARQUE
- Génération de rapports de métabarcoding avec barqueReport

## Ressources

- **Données d'exemple** : [Dataset de test BARQUE](https://github.com/enormandeau/barque_test_dataset)
- **Code source BARQUE** : [GitHub - enormandeau/barque](https://github.com/enormandeau/barque)
- **Packages R requis** : ShortRead, Biostrings, Rqc
