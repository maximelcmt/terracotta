# Instructions pour pousser le projet sur GitHub

## ✅ État actuel
- ✅ Dépôt Git initialisé
- ✅ Tous les fichiers ajoutés
- ✅ Commit initial créé
- ✅ README.md créé avec instructions d'installation
- ✅ .gitignore créé

## 📋 Étapes pour pousser sur GitHub

### Option 1 : Utiliser GitHub CLI (Recommandé)

1. **S'authentifier avec GitHub CLI :**
   ```powershell
   gh auth login
   ```
   - Suivez les instructions pour vous connecter à votre compte GitHub
   - Choisissez votre méthode d'authentification préférée

2. **Créer le dépôt sur GitHub et pousser le code :**
   ```powershell
   cd c:\wamp64\www\terracotta
   gh repo create terracotta --public --source=. --remote=origin --description="Site WordPress Terra Cotta - Documentation et installation"
   git push -u origin main
   ```

   Si votre branche s'appelle `master` au lieu de `main` :
   ```powershell
   git push -u origin master
   ```

### Option 2 : Créer le dépôt manuellement sur GitHub

1. **Créer le dépôt sur GitHub :**
   - Allez sur https://github.com/new
   - Nom du dépôt : `terracotta`
   - Description : `Site WordPress Terra Cotta - Documentation et installation`
   - Visibilité : Public (ou Privé selon votre choix)
   - **NE PAS** initialiser avec README, .gitignore ou licence
   - Cliquez sur "Create repository"

2. **Ajouter la remote et pousser :**
   ```powershell
   cd c:\wamp64\www\terracotta
   git remote add origin https://github.com/maximelcmt/terracotta.git
   git branch -M main
   git push -u origin main
   ```

   Si votre branche s'appelle `master` :
   ```powershell
   git branch -M master
   git push -u origin master
   ```

## 🔍 Vérification

Après le push, vérifiez que tout est bien en ligne :
- Ouvrez https://github.com/maximelcmt/terracotta
- Vérifiez que le README.md s'affiche correctement
- Vérifiez que tous les fichiers sont présents

## 📝 Notes importantes

- Le fichier `wp-config.php` est dans le `.gitignore` pour des raisons de sécurité (contient les identifiants de base de données)
- Les sauvegardes dans `wp-content/updraft/` sont également ignorées
- Le fichier `cms.sql` est inclus pour la restauration de la base de données

## 🆘 En cas de problème

Si vous rencontrez des problèmes d'authentification :
- Utilisez un Personal Access Token : https://github.com/settings/tokens
- Configurez-le avec la commande : `git remote set-url origin https://VOTRE_TOKEN@github.com/maximelcmt/terracotta.git`

