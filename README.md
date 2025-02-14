# Business Card (Premiers pas sur GitHub)
![image](https://github.com/user-attachments/assets/7271109b-12a6-48f5-9566-5cc83480e4fa)


Projet simple de carte de visite : Mon objectif est de me familiariser avec les meilleures pratiques de développement, de documentation et de gestion de code source.
Dans ce fichier, je documente mes avancées dans ce projet avec notamment les problèmes rencontrés et leurs résolutions.

---
## Sommaire
- [Connexion du projet local à GitHub](#connexion-du-projet-local-à-github)
- [Hébergement du site sur GitHub Pages](#hébergement-du-site-sur-github-pages)
---

## Connexion du projet local à GitHub
26/10/24

### Contexte
J'ai commencé un simple projet de carte de visite, en utilisant Git pour le contrôle de version et GitHub pour l'hébergement de mon code. Cependant, j'ai rapidement rencontré des problèmes liés à la gestion des branches par défaut.

### Étapes suivies
#### 1. Création du dépôt sur GitHub :
Je me suis connecté à mon compte GitHub et ai créé un nouveau dépôt nommé business-card. J'ai veillé à initialiser le dépôt avec un README afin de m'assurer de documenter ce projet.

#### 2. Initialisation de Git :
Dans VSCode, j'ai ouvert le dossier où j'avais créé les fichiers de base "index.html" et "style.css" en amont. J'ai ouvert le terminal avec le raccourci `CTRL+J` et étant déjà dans le dossier de mon projet, j'ai exécuté `git init` pour initialiser un dépôt Git local. Cela a créé un fichier .git dans mon dossier.

![image](https://github.com/user-attachments/assets/5df1eed6-3ff1-4cfc-9ff0-e85d410e06d7)


#### 3. Ajout du dépôt distant :

J'ai associé mon dépôt local à celui de GitHub en utilisant la commande `git remote add origin https://github.com/sogomis/business-card.git`, ce qui m'a permis de configurer l'origine de mon dépôt distant.

#### 4. Premier commit :

J'ai ajouté mes fichiers avec `git add .` et effectué mon premier commit avec un message descriptif, `git commit -m "Initial commit"`.

##### ❌ Problèmes rencontrés : Branche par défaut
Lors de ma tentative de push de ma branche avec `git push -u origin main`, j'ai rencontré une erreur. Git crée par défaut une branche `master`, tandis que GitHub utilise `main` comme branche par défaut. Cela a causé des conflits et a rendu l'opération de push impossible.

##### 💡 Résolution du problème
Pour résoudre ce problème, j'ai pris les mesures suivantes :

1. Renommer la branche locale : J'ai utilisé la commande `git branch -m master main` pour renommer ma branche locale de master à main.

2. Changement de la configuration par défaut de Git : Pour éviter ce problème à l'avenir, j'ai configuré Git afin qu'il utilise main comme branche par défaut pour tous les nouveaux dépôts avec la commande `git config --global init.defaultBranch main`.

---

## Hébergement du site sur GitHub Pages
27/10/2024

Afin d'héberger mes projets personnels sans payer de nom de domaine ni d'hébergeur, j'ai choisi GitHub Pages. Pour cela, j'ai suivi les étapes suivantes que m'a dicté ChatGPT : 

#### 1. Accédez aux paramètres du dépôt :
- Cliquez sur l'onglet "Settings" dans votre dépôt.
  ![image](https://github.com/user-attachments/assets/8b40322f-bb56-4ef7-bf23-de3e5d93a83c)

#### 2. Descendez jusqu'à la section "Pages" :
- Dans la barre latérale gauche, cliquez sur "Pages".
![image](https://github.com/user-attachments/assets/c775c3e9-a7e9-4692-8dad-d08d8582d189)

#### 3. Configurer la source de GitHub Pages :
- Dans la section "Source", sélectionnez la branche à partir de laquelle vous souhaitez publier votre site (généralement main ou master).
- Vous pouvez aussi sélectionner un dossier, par exemple / (root) ou /docs, selon où vous avez téléchargé vos fichiers.
![image](https://github.com/user-attachments/assets/ce94190e-24f7-425b-b47a-89e54eae9bfc)

- Cliquez sur "Save".

En quelques secondes, mon projet de carte de visite était en ligne à l'adresse suivante : https://sogomis.github.io/business-card/



