# Business Card

Bienvenue dans ce projet simple de carte de visite. 
Mon objectif est de me familiariser avec les meilleures pratiques de développement, de documentation et de gestion de code source.
Dans ce fichier, je documente mes avancées dans ce projet avec notamment les problèmes rencontrés et leurs résolutions.

---

## [26/10/2024] Connexion du projet local à GitHub

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
