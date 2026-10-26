# Plugins de Turakam83

Marketplace personnelle pour les clients compatibles avec les catalogues de plugins GitHub.

## Assistant Mail IMAP — version d’essai

Connectez plusieurs boîtes IMAP, recherchez vos messages, lisez vos pièces jointes et téléchargez leurs originaux. Le service fonctionne en lecture seule : aucun envoi, déplacement, suppression ou changement de l’état lu/non lu.

- [Site de configuration](https://assistant-mail-imap.turakam.chatgpt.site/)
- Version du paquet : **1.0.4**
- Serveur MCP : `https://assistant-mail-imap.turakam.chatgpt.site/mcp`

## Ajouter la marketplace

Dans l’application de bureau disposant de cette fonction :

1. Ouvrir **Plugins → Ajouter → Ajouter une marketplace**.
2. Renseigner **https://github.com/Turakam83/assistant-mail-imap-marketplace** comme dépôt GitHub.
3. Garder la branche **main**. Si un champ demande le chemin du catalogue, indiquer **.agents/plugins/marketplace.json** ; s’il demande seulement le dossier racine du dépôt, le laisser vide.
4. Ouvrir **Plugins de Turakam83**, puis installer **Assistant Mail IMAP**.

Le catalogue est à `.agents/plugins/marketplace.json`. Un client qui attend un autre format de catalogue nécessite une adaptation. La disponibilité des marketplaces varie selon l’application et sa version ; une installation par catalogue local ne garantit pas la présence du plugin dans ChatGPT sur le web ou sur mobile.

## Accès au service et première connexion

**Un dépôt public ne donne pas accès au site privé.** Cette version est destinée aux essais avec des personnes invitées par le propriétaire du site. Demander l’accès avant d’ajouter une boîte. Le fonctionnement complet depuis un autre compte invité reste à valider.

1. Accepter l’invitation au site avec son propre compte ChatGPT.
2. Terminer l’autorisation OAuth proposée lors de la connexion du plugin. Cette autorisation relie ChatGPT au service ; elle ne remplace pas l’identification IMAP auprès de l’hébergeur mail.
3. Ouvrir le site avec le même compte, puis choisir **Ajouter une boîte mail**.
4. Saisir les identifiants de messagerie uniquement dans le formulaire officiel. Ne jamais les placer dans une conversation, une issue GitHub ou un fichier de ce dépôt.
5. Revenir dans ChatGPT et demander, par exemple, « Quelles boîtes mail sont connectées ? ».

Si la connexion du plugin n’aboutit pas, ne pas supprimer l’authentification ni réutiliser le compte d’une autre personne. L’autorisation de connexion et les accès Sites doivent être vérifiés. Ne pas confondre l’installation du paquet avec une connexion fonctionnelle.

## Fonctions et limites

- Jusqu’à 10 boîtes par utilisateur ; paramètres préremplis pour six hébergeurs et saisie d’un autre serveur IMAP.
- IMAP chiffré sur le port 993 avec mot de passe ou mot de passe d’application. Les connexions mail exigeant OAuth Google/Microsoft ne sont pas proposées dans cette version.
- Recherche par dossier, lecture des messages, liste des pièces jointes, téléchargement des originaux jusqu’à 10 Mo.
- Extraction de texte : PDF avec couche texte (200 pages maximum), TXT/CSV, DOCX et XLSX. Pas d’OCR intégré ; les valeurs Excel enregistrées sont lues sans recalcul.
- Le site sépare les connexions par compte. La validation de bout en bout avec un autre compte invité est une étape de test encore nécessaire.

## Ce que contient ce dépôt

Le catalogue, les consignes, une icône et la configuration publique du serveur MCP. Aucun mot de passe, clé interne, compte mail connecté, message, pièce jointe ou code serveur privé n’est inclus.

Le code du service et sa base de données ne sont pas hébergés sur GitHub. Le plugin nécessite que le service reste disponible. Cette publication n’est pas une publication dans le répertoire officiel d’OpenAI et ne constitue pas une approbation par OpenAI.

## Assistance

Signaler un problème dans [les issues du dépôt](https://github.com/Turakam83/assistant-mail-imap-marketplace/issues), sans identifiants ni contenu de messagerie. Pour une demande d’accès privé, contacter directement le propriétaire par un canal déjà connu ; ne pas publier son adresse personnelle dans une issue.
