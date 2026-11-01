# Replica — mode chat / iPhone / Cowork (adaptation pour Ed)

Ce fichier adapte le pipeline Replica quand il est lancé depuis claude.ai (chat, app iPhone, Cowork) et non depuis Claude Code. Répondre en français.

## Démarrage de chaque étape

1. Cloner cette copie : `git clone --depth 1 https://github.com/eddiagimmo-hue/replica-skill /home/claude/replica-skill` (si déjà présent, `git pull`).
2. Lire `README.md` puis le `SKILL.md` de l'étape demandée (`replica-<étape>/SKILL.md`) et le suivre intégralement, avec les adaptations ci-dessous.
3. Si l'étape a besoin des sorties d'une étape précédente (`replica/…`), les restaurer depuis le dépôt projet (voir « Sauvegarde »). Si elles n'existent pas, dire quelle étape lancer d'abord.

## Adaptations

- **Outils Python** (`imgdiff.py`, `parity.py`, `reviews.py`, `contrast.py`, `sweep.py`, `listing.py`) : les lancer avec `python3 -I`. Si leur exécution est refusée dans la session, réécrire la vérification soi-même en Python standard en appliquant exactement les règles décrites dans le SKILL.md de l'étape, et le signaler en une ligne.
- **Sauvegarde entre sessions** : chaque conversation repart d'une machine vide. Le travail d'un projet (dossier `replica/` + code) vit dans un dépôt GitHub d'Ed dédié au projet (ex. `eddiagimmo-hue/<nom-du-projet>`). Si ce dépôt n'existe pas et ne peut pas être créé depuis la session, demander à Ed de le créer vide dans l'app GitHub (un seul tap), puis l'ajouter à la session et y pousser le travail à la fin de chaque étape. À défaut, livrer un zip.
- **Déploiement** : utiliser le connecteur Vercel (ou Lovable si Ed le préfère). Comptes, domaine, paiement et clés live : c'est Ed qui les crée ; Claude donne les valeurs exactes.
- **Étapes qui demandent le PC** : cliquer dans le compte d'Ed sur l'app d'origine (recon) et les tests manuels dans un vrai navigateur (test) passent par Claude in Chrome sur son PC. Depuis l'iPhone : sources publiques uniquement, et lister ce qui reste à faire au PC.
- **entrepreneur** : pour un logiciel professionnel français, ajouter forums et sites comparatifs français aux sources.
- Rien ne part en production, et aucune action payante n'a lieu, sans l'accord explicite d'Ed.
