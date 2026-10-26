---
name: setup
description: Configurer Assistant Mail IMAP après installation, ajouter une deuxième adresse mail à tout moment, retrouver le site de configuration ou gérer les connexions existantes.
---

# Configurer Assistant Mail IMAP

Lancer ce parcours lorsque l’utilisateur démarre la configuration proposée après installation, demande de connecter une première ou une autre adresse, veut retrouver le site de configuration ou souhaite vérifier que le plugin est prêt.

## Ajouter ou gérer une adresse après l’installation

Reconnaître aussi les demandes « comment ajouter une autre adresse mail ? », « connecter une deuxième boîte », « ajouter un compte », « où gérer mes adresses ? » ou « retrouver le site de configuration ».

Pour une simple demande d’explication ou de lien, répondre immédiatement avec le lien officiel ci-dessous et les étapes. Ne pas lire ni rechercher les mails, ni appeler list_mailboxes uniquement pour retrouver une adresse de site déjà connue. Ne pas renvoyer l’utilisateur chercher dans les paramètres du plugin.

Réponse de référence, à adapter à sa langue :
« Pour ajouter une autre adresse, ouvre [Gérer mes boîtes mail](https://assistant-mail-imap.turakam.chatgpt.site/). Dans “Ajouter une boîte mail”, indique son nom, son adresse, son hébergeur et son mot de passe, puis clique sur “Connecter cette boîte”. Tes boîtes déjà connectées restent disponibles. Reviens ensuite ici pour utiliser la nouvelle adresse. »

Le mot de passe se saisit uniquement dans le formulaire sécurisé, jamais dans la conversation. Si l’utilisateur a déjà fourni une adresse dans son message, ne pas lui demander de la répéter dans le chat et ne pas demander son mot de passe. L’inviter à terminer la connexion dans le formulaire.

Si l’utilisateur demande de retirer une adresse, donner le même lien et expliquer le bouton « Déconnecter » de la boîte concernée ; cela retire l’accès du plugin sans supprimer de mails. Ne rien déconnecter de sa propre initiative.

Après qu’il confirme l’ajout, appeler list_mailboxes pour vérifier la nouvelle connexion avant d’annoncer qu’elle est disponible. Si elle n’apparaît pas, demander seulement le message affiché par le formulaire.

Les étapes ci-dessous concernent la première installation et les vérifications demandées. Une simple question sur l’ajout d’une adresse reçoit directement la réponse et le lien ci-dessus.

## Vérifier avant de demander une configuration

Appeler list_mailboxes du plugin Assistant Mail IMAP. Utiliser uniquement les connexions de ce service, sans reprendre celles d’un autre plugin. Cet appel ne lit pas les messages et ne modifie aucune boîte.

Si une ou plusieurs boîtes sont déjà connectées :
- Confirmer simplement que le plugin est prêt, en indiquant leurs noms sans afficher d’identifiants techniques.
- Donner deux exemples de demandes, dont une recherche dans une boîte précise et une recherche dans toutes les boîtes.
- Proposer le lien de configuration uniquement pour ajouter une autre adresse ou gérer les connexions. Ne pas demander de reconnecter une boîte existante.

Si aucune boîte n’est connectée :
- Expliquer clairement : « Bienvenue ! Le plugin est installé. Il reste à connecter ta première boîte mail. »
- Afficher immédiatement le lien principal : [Configurer ma première adresse mail](https://assistant-mail-imap.turakam.chatgpt.site/).
- Si un outil d’ouverture de page est disponible sur cet appareil, ouvrir cette adresse officielle dans le navigateur ou le panneau du chat. Toujours laisser aussi le lien visible ; ne pas affirmer que la page est ouverte sans confirmation de l’outil.
- Donner trois étapes courtes : nommer la boîte et indiquer son adresse ; choisir l’hébergeur ; saisir le mot de passe dans le formulaire et cliquer sur « Connecter cette boîte ».
- Préciser que les paramètres des six hébergeurs proposés sont renseignés automatiquement. Pour un autre hébergeur, choisir « Autre serveur IMAP » et utiliser ses paramètres.
- Préciser brièvement que certains fournisseurs demandent un mot de passe dédié ou d’application.
- Expliquer que l’utilisateur revient ensuite dans ChatGPT pour poser ses questions.

Si les outils ne sont pas encore disponibles ou si la connexion personnelle à ChatGPT est requise :
- Ne pas annoncer que le plugin est en panne et ne pas prétendre avoir vérifié les boîtes.
- Donner le lien de configuration et inviter à terminer la connexion du plugin dans ChatGPT si nécessaire.
- Ne jamais afficher de détails techniques, de pile d’erreur ou de message d’échec opaque à la place du guidage.

## Après la connexion

Quand l’utilisateur indique avoir terminé, rappeler list_mailboxes pour confirmer l’enregistrement. Ne pas traiter l’ouverture de la page, un clic ou la saisie du formulaire comme une connexion réussie.
- Si une boîte apparaît, confirmer son nom et dire que la configuration est terminée.
- Si elle n’apparaît pas, demander uniquement le message affiché par le formulaire, sans demander le mot de passe.
- Suggérer une première demande simple, sans lancer une lecture de messages non nécessaire au parcours.

## Règles de confidentialité et limites

Les identifiants et mots de passe se saisissent exclusivement dans le formulaire officiel. Ne jamais les demander dans le chat, les copier depuis un autre plugin, les lire dans un gestionnaire de mots de passe, remplir automatiquement un secret, ni déconnecter ou modifier une boîte existante pour un test.

La connexion reste en lecture seule. Ne pas envoyer, supprimer ou modifier de mail. La version actuelle accepte l’IMAP chiffré sur le port 993, avec mot de passe ou mot de passe d’application ; les autorisations OAuth Google/Microsoft ne sont pas encore proposées. Le service permet jusqu’à 10 boîtes par utilisateur.

La configuration après installation est un parcours proposé par ChatGPT que l’utilisateur lance. Ne pas promettre une redirection forcée ou une configuration sans action de l’utilisateur.
