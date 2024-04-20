# **Introduction**
Un serveur web est un élément essentiel de l’infrastructure d’Internet. Voici ce que vous devez savoir à son sujet :

Définition :

Un serveur web est un logiciel de communication qui agit comme un intermédiaire entre le serveur où les données sont hébergées et l’ordinateur du client (utilisateur).
Il permet des connexions bidirectionnelles ou unidirectionnelles, synchrones ou asynchrones, avec n’importe quelle application cliente, y compris les navigateurs web.

Composants matériels et logiciels :

Au niveau des composants matériels, un serveur web est un ordinateur qui stocke les fichiers constituant un site web (documents HTML, images, feuilles de style CSS, fichiers JavaScript) et les envoie aux appareils des utilisateurs qui visitent le site.
Au niveau des composants logiciels, un serveur web contient différents fragments qui contrôlent l’accès aux fichiers hébergés. Le minimum requis est un serveur HTTP, qui comprend les URL et le protocole HTTP (utilisé par les navigateurs pour afficher les pages web).

Il existe deux types de serveurs web :

Serveur web statique : Il envoie les fichiers hébergés “tels quels” vers le navigateur. Il est composé d’un ordinateur et d’un serveur HTTP.
Serveur web dynamique : En plus du serveur HTTP, il inclut d’autres composants logiciels tels qu’un serveur d’applications et une base de données. Il met à jour les fichiers hébergés avant de les envoyer au navigateur via HTTP.

Fonctionnement :

Lorsqu’un navigateur a besoin d’un fichier hébergé sur un serveur web, il envoie une requête via HTTP.
Le serveur web (matériel) reçoit la requête et le serveur HTTP (logiciel) renvoie le document demandé grâce au même protocole.
Les serveurs web dynamiques utilisent des modèles HTML pour générer des pages à la volée, en remplissant ces modèles avec des données provenant d’une base de données.

En résumé, un serveur web est un élément clé de la mise à disposition des sites web sur Internet, permettant aux utilisateurs d’accéder aux contenus via leurs navigateurs. Il joue un rôle essentiel dans la communication entre les serveurs et les clients


# **Création d'un serveur web sous ubuntu serveur**

Installer Apache :

Le serveur HTTP Apache est l’un des serveurs web les plus utilisés au monde. Pour l’installer, ouvrez un terminal et exécutez les commandes suivantes :

```
sudo apt update
sudo apt install apache2
```

Cela installera Apache et ses dépendances.

Configurer le pare-feu :

Vous devez autoriser le trafic HTTP (port 80) à travers le pare-feu. Utilisez la commande suivante pour autoriser Apache :

```
sudo ufw allow 'Apache'
```

Si vous prévoyez d’utiliser HTTPS (port 443), vous pouvez également autoriser le profil Apache Full.

Tester Apache :

Ouvrez un navigateur web et accédez à l’adresse IP de votre serveur. Vous devriez voir une page affichant des informations sur votre installation d’Apache
.
Configurer votre site web :
Placez vos fichiers HTML, CSS, JavaScript, etc., dans le répertoire /var/www/html/.

Vous pouvez utiliser FileZilla ou WinSCP pour placer vos ficiers dans votre serveur web.

Vous pouvez également installer PHP et MySQL pour créer des sites web dynamiques, c'est ce qu'on va voir dans la section suivante.

# **Installation de MySQL et de PHP**

Pour installer ces logiciels, effectuez la commande suivante:

```
Sudo apt install mysql-server php5 libapache2-mod-php5 php5-mysql
```

Voilà! Votre serveur web est opérationnel!