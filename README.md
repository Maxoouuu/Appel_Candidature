# Appel_Candidature
Ce site a été réalisé seul par Maxime Coriton en 1 mois à peu près 

Quel est ce site ? 

Ce site Web permet aux formateurs de la police de créer des stages.
Pour cela il y a 3 étapes :
- le formateur créé son stage avec un code stage valide tel que "AH001" (Création stage)
- la Chef BGS valide ou refuse le stage (Validation stage)
- les BGS finalisent la création de ce stage en y rajoutant 3 informations supplémentaires (Finalisation Stage)

Une fois que ce stage a été crée il apparaît à l'accueil (Appel à candidature)

Comment y accéder ?

- Lancer Xampp (Apache et MySQL)

- Créer une base de données sur phpmyadmin au nom de "appel"

- Importer le fichier sql fournis

- Lancer le site depuis l'endroit habituel où vous lancer vos sites (par exemple): http://localhost/tp/Appel Candidature 

À partir de là vous pouvez vous connecter avec comme matricule "admin" et mdp "admin" (oui ce site n'est pas terminé)

Quelles améliorations ? 

Tout d'abord ce site est encore en cours de développement car la chef BGS a eu de nouvelles idées de fonctionnalité pour l'améliorer (et surtout pour leurs facilités la tache)

Ensuite lors de la création du stage il n'y a AUCUNE vérification d'erreur c'est-à-dire que si le formateur décide de faire un stage un jour férié ou pire, de commencer un stage à une date puis d'indiquer une date de fin qui précède la date de début et bien tant que le code stage est valide, le stage sera crée et affiché sur la page du BGS (validation stage). Mais pas de panique la chef BGS se chargera de supprimer ce stage (à l'avenir de le modifier)

La barre de recherche ne sert pas pour le moment, elle aura pour but de rechercher un stage parmi la liste de stage afficher dans Appel à Candidature

Pour le champ du code stage : une fonction Javascript qui vérifie ce que l'utilisateur rentre et permet d'être sur de ne pas se tromper

Niveau sécurité ? 

Normalement sur ce point-là c'est plutôt pas mal, à l'inscription une variable de session est créé afin de vérifier que l'utilisateur est bien connecté pour utiliser l'ensemble des fonctionnalités du site. 

Les champs lors de la connexion sont protégé à l'injection SQL grace à deux fonctions : stripslashes et mysqli_real_escape_string. Donc à partir de là j'estime que l'administration ne connait pas comment faire une injection SQL.
