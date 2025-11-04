# Site Terra Cotta - WordPress

## 📋 Description

Site web WordPress pour Terra Cotta, développé avec WordPress 6.8.1, utilisant le thème Astra et plusieurs plugins essentiels.

## 🛠️ Prérequis

- **PHP** : 8.2.18 ou supérieur
- **MySQL** : 8.3.0 ou supérieur
- **Serveur web** : Apache ou Nginx
- **Outils recommandés** :
  - WAMP/XAMPP/MAMP (pour développement local)
  - phpMyAdmin (pour gestion de la base de données)

## 📥 Installation

### Méthode 1 : Installation complète (Recommandée)

1. **Préparation de l'environnement**
   - Installez un serveur web local (WAMP/XAMPP/MAMP)
   - Créez une base de données MySQL vide nommée `cms`
   - Notez les identifiants de connexion à la base de données

2. **Configuration de la base de données**
   - Ouvrez phpMyAdmin
   - Créez une nouvelle base de données nommée `cms`
   - Importez le fichier `cms.sql` fourni dans le projet

3. **Configuration des fichiers**
   - Extrayez tous les fichiers du projet dans votre dossier web (ex: `C:\wamp64\www\terracotta\`)
   - Modifiez le fichier `wp-config.php` avec vos paramètres de connexion :
     ```php
     define( 'DB_NAME', 'cms' );
     define( 'DB_USER', 'root' );
     define( 'DB_PASSWORD', 'votre_mot_de_passe' );
     define( 'DB_HOST', 'localhost' );
     ```

4. **Configuration du fichier hosts (Optionnel - pour émuler le domaine)**
   - **Windows** : Modifiez `C:\Windows\System32\drivers\etc\hosts` (en tant qu'administrateur)
   - Ajoutez la ligne : `127.0.0.1   www.terracotta.com`
   - **Mac/Linux** : Modifiez `/etc/hosts` avec `sudo nano /etc/hosts`
   - Ajoutez la ligne : `127.0.0.1   www.terracotta.com`

5. **Permissions des fichiers**
   - Dossiers : 755
   - Fichiers : 644

6. **Accès au site**
   - Ouvrez votre navigateur et allez sur : `http://localhost/terracotta/` ou `http://www.terracotta.com/terracotta/`

### Méthode 2 : Installation avec UpdraftPlus

Si vous avez des sauvegardes UpdraftPlus dans le dossier `wp-content/updraft/` :

1. Installez WordPress 6.8.1
2. Installez le plugin UpdraftPlus
3. Restaurez les sauvegardes depuis le tableau de bord WordPress

## 🔐 Accès à l'administration

- **URL d'administration** : `http://www.terracotta.com/terracotta/wp-admin/` ou `http://localhost/terracotta/wp-admin/`
- **Email** : `maxime@mlentmt.be` ou `it@mail.com`
- **Mot de passe** : `CMS2025eafc` (pour maxime@mlentmt.be) ou `EAFC2025cms` (pour it@mail.com)

⚠️ **Important** : Changez ces mots de passe après la première connexion pour des raisons de sécurité.

## 🔌 Plugins installés

| Plugin | Statut | Version | Description |
|--------|--------|---------|-------------|
| Astra Sites | Actif | 4.6.0 | Import de templates préconçus |
| UpdraftPlus | Actif | 1.25.6 | Sauvegarde automatique |
| SecuPress | Actif | 2.3.20.1 | Sécurité renforcée |
| Yoast SEO | Actif | 22.7 | Optimisation SEO |
| Ultimate Addons for Gutenberg | Actif | 2.0.0 | Blocs Gutenberg supplémentaires |
| SureForms | Actif | 1.0.0 | Formulaires de contact |
| SureMails | Actif | 1.0.0 | Gestion des emails |

## 📁 Structure du projet

```
terracotta/
├── wp-admin/          # Interface d'administration WordPress
├── wp-content/        # Contenu personnalisé
│   ├── plugins/       # Extensions installées
│   ├── themes/        # Thèmes (Astra)
│   ├── uploads/       # Fichiers médias
│   └── updraft/       # Sauvegardes
├── wp-includes/       # Fichiers système WordPress
├── wp-config.php      # Configuration principale
├── cms.sql            # Export de la base de données
├── documentation_technique_terracotta.html  # Documentation complète
└── README.md          # Ce fichier
```

## 🎨 Thème

- **Thème actif** : Astra
- **Personnalisation** : Voir la documentation HTML pour les détails de personnalisation

## 📚 Documentation

Pour plus de détails sur :
- La restauration complète
- La configuration des plugins
- La logique de navigation
- Les choix techniques

Consultez le fichier `documentation_technique_terracotta.html` inclus dans le projet.

## 🔧 Dépannage

### Problème de connexion à la base de données
- Vérifiez que MySQL est démarré
- Vérifiez les identifiants dans `wp-config.php`
- Assurez-vous que la base de données `cms` existe

### Erreur 404
- Vérifiez les permissions des fichiers
- Vérifiez la configuration Apache/Nginx
- Vérifiez que le module `mod_rewrite` est activé

### Problème d'affichage
- Videz le cache du navigateur
- Vérifiez que tous les plugins sont activés
- Vérifiez les logs d'erreur PHP

## 📝 Notes importantes

- **Sécurité** : Changez les mots de passe par défaut
- **Sauvegardes** : Effectuez des sauvegardes régulières avec UpdraftPlus
- **Mises à jour** : Maintenez WordPress, les thèmes et plugins à jour
- **URL** : Si vous changez l'URL du site, mettez à jour les URLs dans la base de données

## 👤 Auteur

**Maxime Lecomte**
- Site web : https://www.maximelecomte.be
- GitHub : https://github.com/maximelcmt/

## 📅 Informations du projet

- **Dates de création** : du 25 juin au 1er juillet 2025
- **Version WordPress** : 6.8.1
- **Version PHP** : 8.2.18
- **Version MySQL** : 8.3.0

## 📄 Licence

Ce projet est un site WordPress personnalisé. WordPress est sous licence GPL v2 ou ultérieure.

---

Pour toute question ou problème, consultez la documentation technique complète ou contactez l'administrateur du site.

