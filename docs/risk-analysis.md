# 1. Planification et Analyse des Risques

## 1.1 Identification des acteurs

Dans une plateforme e-learning comme pire2pire.com, plusieurs types d'acteurs interagissent avec le système, chacun aura nécessairement des besoins et des privilèges spécifiques :

| Acteur | Rôle et interactions | Niveau de privilèges |
|--------|----------------------|----------------------|
| **Administrateurs** | Gèrent l'infrastructure, les accès et la sécurité de la plateforme | Élevé |
| **Formateurs** | Publient du contenu pédagogique, interagissent avec les apprenants et évaluent leurs performances | Moyen |
| **Apprenants** | Accèdent aux cours, soumettent des travaux et participent aux activités pédagogiques | Faible |
| **Support technique** | Assure la maintenance et le dépannage de la plateforme | Moyen à élevé |
| **Visiteurs anonymes** | Peuvent naviguer sur certaines parties publiques du site sans authentification | Très limité |

L'identification précise des acteurs, de leurs rôles et de leurs interactions avec la plateforme, nous permettra de définir des mécanismes de sécurité proportionnés aux risques associés à chaque profil.

## 1.2 Analyse des risques et menaces potentielles

Nous avons ici identifié et listé les menaces potentielles pesant sur la plateforme de e-learning, afin de pouvoir évaluer leur impact :

| Menace | Description |
|--------|-------------|
| **Usurpation d'identité** | Un attaquant pourrait compromettre un compte utilisateur (formateur, administrateur, apprenant) |
| **Fuite de données** | Accès non autorisé aux informations sensibles des utilisateurs (emails, mots de passe, progrès d'apprentissage) |
| **Attaques par injection (SQLi, XSS)** | Exploitation de vulnérabilités dans les formulaires et champs de saisie |
| **Dénis de service (DDoS)** | Tentative de surcharge du serveur pour rendre la plateforme indisponible |
| **Hameçonnage (Phishing)** | Tromper les utilisateurs pour obtenir leurs identifiants de connexion |
| **Exploitation des sessions non sécurisées** | Vol de session par absence de protections adéquates (cookies sécurisés, expiration automatique, etc.) |
| **Exploitation de vulnérabilités zero-day** | Utilisation de failles non corrigées dans les composants logiciels |
| **Attaque par force brute** | Tentatives répétées pour deviner les identifiants utilisateurs |
| **Exfiltration de données** | Extraction non autorisée de données sensibles de la plateforme |

## 1.3 Définition des exigences de sécurité

Pour minimiser les risques identifiés, plusieurs exigences devront être mises en place. Nous les avons également associées à un niveau de priorité :

### Exigences critiques (priorité haute)
- **Authentification robuste** : Mise en place de l'authentification multifacteur (MFA) et gestion stricte des mots de passe conformes aux recommandations de l'ANSSI.
- **Chiffrement des données** : Utilisation de TLS pour la transmission des données et chiffrement des informations sensibles en base de données.
- **Protection contre les attaques Web** : Mise en place de pare-feu applicatifs, validation des entrées et règles de Content Security Policy (CSP).

### Exigences importantes (priorité moyenne)
- **Sécurisation des accès** : Gestion des rôles et permissions pour limiter les accès aux ressources sensibles selon le principe du moindre privilège.
- **Journalisation et surveillance** : Enregistrement des événements critiques et mise en place d'une alerte en cas de tentative d'accès suspecte.
- **Protection contre les attaques par force brute** : Limitation du nombre de tentatives de connexion et utilisation de captchas.

### Exigences standard (priorité normale)
- **Plan de réponse aux incidents** : Mise en place de procédures pour identifier, contenir et corriger les failles de sécurité.
- **Formation des utilisateurs** : Sensibilisation aux risques de sécurité, notamment contre le phishing et les mauvaises pratiques.
- **Mise à jour régulière** : Veille sur les nouvelles vulnérabilités découvertes, suivi de l'actualité concernant la sécurité web et application rapide des correctifs de sécurité sur l'ensemble des composants.

Cette analyse servira de fondement pour établir les priorités dans l'implémentation des mesures de sécurité tout au long du cycle de développement de la plateforme.