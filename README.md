# Solution d'Inventaire Équipements par QR Code — Guide d'utilisation
Ce projet permet de suivre l'emplacement et l'état de 200 équipements à l'aide de QR codes uniques collés sur les appareils. Les utilisateurs peuvent scanner ces QR codes depuis leur téléphone personnel (sans avoir besoin de se connecter à un compte d'entreprise ou à SharePoint) pour consulter la fiche de l'appareil et mettre à jour ses informations en temps réel.

⚙️ Fonctionnement général
Scan du QR Code : L'utilisateur scanne l'étiquette avec son téléphone portable.

Identification : La page demande le mot de passe d'accès de l'équipe (Lipsheim) lors du tout premier scan (le téléphone le mémorise ensuite pour les prochains scans).

Consultation : L'écran affiche la fiche actuelle de l'appareil (Nom, Emplacement, Modifié par, Commentaire et Date de mise à jour).

Mise à jour : L'utilisateur clique sur Modifier, ajuste les informations (le nom de l'appareil reste modifiable s'il y a une correction à faire), puis clique sur Enregistrer. La mise à jour est instantanée.

📂 Contenu du dépôt GitHub
index.html : L'application web mobile qui s'affiche sur le téléphone de l'utilisateur lors du scan. Elle gère l'authentification par mot de passe, l'affichage de la fiche et le formulaire de modification.

inventaire.json : La base de données de l'inventaire. Ce fichier est créé et mis à jour automatiquement au format JSON à chaque fois qu'un utilisateur enregistre un appareil depuis son téléphone.

📊 Comment extraire et consulter l'inventaire sur Excel ?
Vous pouvez récupérer l'intégralité de l'inventaire à plat sous forme de tableau Excel à tout moment :
Ouvrez l'application depuis votre navigateur ou votre téléphone (par exemple via le lien de l'un des QR codes).

Entrez le mot de passe si demandé.

Descendez tout en bas de l'écran et cliquez sur le bouton gris : « 📊 Télécharger tout l'inventaire en Excel (.CSV) ».

Un fichier nommé Inventaire_Complet_QR.csv se télécharge automatiquement. Ouvrez-le directement dans Microsoft Excel pour filtrer, trier ou imprimer votre liste.

🖨️ Guide d'impression des étiquettes (Planches Lyreco 105 x 70 mm)
Le fichier Lyreco_105x70mm_GitHub_V3_200_QRCodes.docx est déjà calibré au millimètre près pour les planches d'étiquettes Lyreco (référence 1.139.869) à 8 étiquettes par page A4 (2 colonnes × 4 lignes).
Consignes d'impression importantes :
Ouvrez le fichier dans Microsoft Word.

Lancez l'impression (Ctrl + P).

Dans les options de l'imprimante, assurez-vous que :
Le format de papier sélectionné est bien A4.

L'option d'échelle est réglée sur 100 % ou Taille réelle (ne cochez jamais "Ajuster à la page" ou "Ajuster à la zone d'impression", sous peine de décaler les étiquettes).

L'impression est configurée en Recto uniquement (Pas de Recto-Verso automatique).

Test recommandé : Imprimez d'abord la première page sur une feuille blanche normale, puis superposez-la devant une planche d'étiquettes Lyreco face à la lumière pour vérifier que les QR codes tombent parfaitement au centre des découpes avant de lancer la totalité des pages.

🔒 Sécurité et confidentialité
Les données de l'inventaire sont stockées de manière sécurisée dans votre dépôt.

Seules les personnes disposant du mot de passe défini (Lipsheim) peuvent charger, lire ou modifier les informations de l'inventaire depuis leur mobile.

En cas de changement de mot de passe ou de modification esthétique de la page de consultation, il vous suffit de modifier le fichier index.html sur GitHub. Il n'est jamais nécessaire de réimprimer ou de recoller les QR codes sur vos appareils, les liens imprimés restent valables indéfiniment.
