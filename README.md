# Projet 3NPM - Application de Gestion de Liste Noire de Numéros de Téléphone

## Description

Cette application Node.js reçoit des SMS et ajoute les numéros de téléphone à une liste noire si le message contient le mot "STOP". Elle permet également de récupérer la liste complète des numéros blacklistés et de vérifier si un numéro spécifique est blacklisté.

## Fonctionnalités

- **Recevoir et Traiter les SMS** : Reçoit des requêtes POST et ajoute le numéro à la liste noire si le message contient "STOP".
- **Récupérer Tous les Numéros de Téléphone Blacklistés** : Permet de récupérer la liste complète des numéros blacklistés.
- **Vérifier Si un Numéro de Téléphone Est Blacklisté** : Permet de vérifier si un numéro spécifique est blacklisté.

## Installation

### Prérequis

- Node.js
- MongoDB
- curl 

Etape 1: Configuration de l'environnement

    Installer Node.js et npm :
    Assurez-vous d'avoir Node.js et npm installés sur votre machine. Vous pouvez vérifier cela avec les commandes :


node -v
npm -v


Installation de Curl
Installer Curl sur Windows en utilisant WinGet (depuis Windows 10)

À partir de Windows 10, vous pouvez également utiliser WinGet, le gestionnaire de paquets natif de Microsoft, pour installer Curl :

    Ouvrir PowerShell en tant qu'administrateur :
        Cliquez avec le bouton droit sur le menu Démarrer, sélectionnez "Windows PowerShell (Admin)".

    Installer Curl avec WinGet :
        Tapez la commande suivante dans PowerShell : winget install curl

    Suivez les instructions à l'écran pour terminer l'installation.

Vérifier l'installation de Curl en ouvrant l'invite de commande windows et tapez la commande suivante  curl --version



Initialisation du projet:
Créez un répertoire pour votre projet

mkdir projet_3npm
cd projet_3npm
npm init -y

Installation des dépendances 
Installez les packages nécessaires (depuis le terminal votre environement de travail tels que pycharm,visualcode........)

npm install express mongoose express-validator 

Étape 2 : Configuration de la base de données

    Installer MongoDB :
    Si ce n'est pas déjà fait, installez MongoDB sur votre machine 

    Créer une base de données et une collection :
    Vous pouvez créer une base de données appelée obd et une collection blacklist.


    Étape 3 : Créer le serveur Express

    Structure du projet :
    Créez une structure de dossiers pour votre projet. 



    Étape 4 : Lancer le serveur

  
    Démarrez votre serveur en exécutant la commande node app.js  (depuis l'invite de commande de votre environement de travail tels pycharm, visualcode.....)
    lorsque le server demarre et que la base de donnee se connecter effectuer les test 

    TEST

    pour le test ouvrez l'invite de commande et taper les commandes suivantes
    
    
    pour l'ajout d'un numero 
    curl -X POST http://localhost:5000/api/blacklist/add -H "Content-Type: application/json" -d "{\"From\": \"+33612345678\", \"Message\": \"STOP\"}"

    pour afficher la iste des numeros blacklitstes

    curl http://localhost:5000/api/blacklist


    pour verifier un numero blacklisté

    curl http://localhost:5000/api/blacklist/check?phoneNumber=%2B33612345678# projet-3npm
