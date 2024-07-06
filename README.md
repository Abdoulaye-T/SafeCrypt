# SafeCrypt
SafeCrypt est une application web permettant de chiffrer et de déchiffrer des messages à l'aide de plusieurs méthodes de cryptographie : César, Vigenère et AES. Elle offre une interface utilisateur intuitive pour saisir des messages, sélectionner des méthodes de cryptage/décryptage, et gérer des clés de chiffrement.
# Fonctionnalités
Chiffrement César : Utilise un décalage pour chiffrer le message.
Chiffrement Vigenère : Utilise une clé de texte pour chiffrer le message.
Chiffrement AES : Utilise la méthode AES-256-CBC pour chiffrer le message avec une clé et un vecteur d'initialisation.
# Installatiion
1. Clonez le dépôt :
git clone https://github.com/votre-utilisateur/safecrypt.git
cd safecrypt
2. Configurez votre base de données en utilisant le fichier db.php.

3. Importez les tables nécessaires dans votre base de données :
CREATE TABLE messages (
    id INT AUTO_INCREMENT PRIMARY KEY,
    message_original TEXT NOT NULL,
    message_crypter TEXT NOT NULL,
    cle VARCHAR(255) NOT NULL,
    methode VARCHAR(50) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

CREATE TABLE message_decrypter (
    id INT AUTO_INCREMENT PRIMARY KEY,
    message_crypter TEXT NOT NULL,
    message_decrypter TEXT NOT NULL,
    cle VARCHAR(255) NOT NULL,
    methode VARCHAR(50) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
4. Assurez-vous que db.php contient les bonnes informations de connexion à la base de données.

5. Déployez les fichiers sur votre serveur web et accédez à index.php via votre navigateur.

# Utilisation
## Chiffrement
1. Naviguez vers Crypter.php.
2. Entrez le message à chiffrer.
3. Sélectionnez la méthode de chiffrement et entrez la clé (décalage pour César, clé pour Vigenère et AES).
4. Cliquez sur "Crypter" pour obtenir le message chiffré.
## Déchiffrement
1. Naviguez vers Decrypter.php.
2. Entrez le message chiffré.
3. Sélectionnez la méthode de déchiffrement et entrez la clé correspondante.
4. Cliquez sur "Décrypter" pour obtenir le message original.

# Technologies utilisées
PHP : Langage de script côté serveur pour la logique de cryptage/décryptage.
Bootstrap : Framework CSS pour un design réactif et moderne.
MySQL : Base de données relationnelle pour stocker les messages chiffrés et déchiffrés.

# Contribuer
Les contributions sont les bienvenues ! Veuillez soumettre un pull request ou ouvrir une issue pour discuter des modifications que vous souhaitez apporter.
# Licence
Ce projet est sous licence MIT. Voir le fichier LICENSE pour plus de détails.

# Remerciements
Merci à tous ceux qui ont contribué à ce projet !
