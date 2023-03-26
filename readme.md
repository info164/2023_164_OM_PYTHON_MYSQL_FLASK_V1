# Module 164 2023.03.25


Le "début de la fin"

---
#### Avant de commencer cette version presque finale.
##### Cette démo. CRUD (Create Read Update Delete) presque complète sur les 3 tables de la base film : Soit "t_film"; "t_genre" et la table intermédiaire "t_genre_film"
* Un serveur MySql doit être installé
  * LARAGON (heidi.sql) ou XAMPP ou UWAMP
  * MAC : MAMP ou https://www.codeur.com/tuto/creation-de-site-internet/version-mysql/
* Python doit être installé.
  * ATTENTION : Cocher la case pour que le "PATH" intègre le programme Python
  * Une fois la "case à cocher" du PATH cochée, il faut choisir d'installer
  * Un peu avant la fin du processus d'intallation, cliquer sur "disabled length limit" et cliquer sur "CLOSE"
  * Le test de Python se fait après avec le programme "PyCharm"
* Installer "GIT"
  * https://gitforwindows.org/
  * Le test de "GIT" se fait dans le programme "PyCharm"
* "PyCharm" (community) doit être intallé, car toutes mes démonstrations sont faites avec cette version de l'IDE. INFO : Vous pouvez télécharger tous les produits de JetBrains car vous êtes étudiant.
  * Lors de l'installation, il faut cocher toutes les options ASSOCIATIONS, ADD PATH, etc
  * Ouvrir "PyCharm" pour la première fois pour le configurer. Choisir le bouton "New Project"
  * Changer le répertoire pour ce nouveau projet, il faut créer un nouveau répertoire "vide" dans votre ordi en local.
  * Il est important d'avoir sélectionné le répertoire que vous venez de créer car "PyCharm" va automatiquement créer un
    environnement virtuel (venv) dans ce répertoire
  * Menu : File->Settings->Editor->General->Auto Import (rubrique Python) cocher "Show auto-import tooltip"
  * PyCharm vient d'ouvrir une fenêtre avec le contenu du "main.py" pour configurer les actions "UNDO" et "REDO"
  * Sélectionner tout le texte avec "CTRL-A" puis "CTRL-X" (Couper), puis "CTL-Z" (UNDO) et faites un REDO "CTRL-Y" et "PyCharm" va vous demander de choisir l'action du "CTRL-Y" raccourci pour faire un "REDO". (Dans 98% des éditeurs de texte, le "CTRL-Y" représente l'action "REDO"... pas chez JetBrains)


## Mode d'emploi de cette démonstration
* Démarrer le serveur MySql (Laragon(heidi.sql), uwamp ou xamp ou mamp, etc))
* Dans "PyCharm", importer MA BD à partir du fichier DUMP
    * Ouvrir le fichier "APP_FILMS_164/database/1_ImportationDumpSql.py"
    * Cliquer avec le bouton droit sur l'onglet de ce fichier et choisir "run" (CTRL-MAJ-F10)
    * En cas d'erreurs : ouvrir le fichier ".env" à la racine du projet, contrôler les indications de connexion pour la
      bd.
* Test simple de la connexion à la BD
    * Ouvrir le fichier "APP_FILMS_164/database/2_test_connection_bd.py"
    * Cliquer avec le bouton droit sur l'onglet de ce fichier et choisir "run" (CTRL-MAJ-F10)
* Démarrer le microframework FLASK
    * Dans le répertoire racine du projet, ouvrir le fichier "run_mon_app.py"
    * Cliquer avec le bouton droit sur l'onglet de ce fichier et choisir "run" (CTRL-MAJ-F10)

	
### Faire une copie du répertoire afin de pouvoir travailler sur une copie et non sur l'original.
  * Fermer "PyCharm"
  * Faire une copie du répertoire où vous venez d'importer "MA" démonstration
  * Renommer cette copie de répertoire : "VOTRENOM_VOTREPRENOM_VOTRECLASSE_VOTRESUJET_164_V3TABLES"
  * Ouvrir ce répertoire. Effacer les 3 sous-répertoires suivants (".git" répertoire caché, ".idea" et "venv")
  * Ouvrir "PyCharm", puis "File"-->"Open..." un projet et choisir le répertoire racine "VOTRENOM_VOTREPRENOM_VOTRECLASSE_VOTRESUJET_164_V3TABLES"
  * Lire et réaliser les étapes du mode d'emploi de la démonstration
  * Quand "MA" démonstration fonctionne, alors il faut passer à "Vos devoirs"
  * 


# Vos devoirs :
* Placer votre "DUMP" à la place de celui de ma "BD" films. Votre "DUMP" doit se nommer "VOTRENOM_VOTREPRENOM_VOTRECLASSE_VOTRESUJET_164.SQL"
  * Dans le répertoire "database" vous devez placer vos fichiers (PDF: Cahier des charges, MCD, MLD, dictionnaires des données et SQL : requêtes, etc)
  * Ouvrir le fichier "APP_FILMS_164/database/1_ImportationDumpSql.py"
    * Cliquer avec le bouton droit sur l'onglet de ce fichier et choisir "run" (CTRL-MAJ-F10)
    * En cas d'erreurs : ouvrir le fichier ".env" à la racine du projet, contrôler les indications de connexion pour la
      bd.
* Test simple de la connexion à la BD
    * Ouvrir le fichier "APP_FILMS_164/database/2_test_connection_bd.py"
	* Modifier "MA" requête par votre requête
    * Cliquer avec le bouton droit sur l'onglet de ce fichier et choisir "run" (CTRL-MAJ-F10)	  
	  
A) Modifier MES requêtes AFFICHER (READ) du CRUD(Create Read Update Delete) sur la table "t_genre"
  *	Ouvrir le fichier "APP_FILMS_164/genres/gestion_genres_crud.py"
  * Modifier les requêtes "SELECT" sur la table "t_genre" par des "SELECT" sur une de vos "t_????"
    * Faites d'abord un "SELECT * FROM t_votre_table_a_vous"
  * Modifier dans le répertoire "TEMPLATES" la page html consacrée à l'affichage pour ma "t_genre", il faut ouvrir "APP_FILMS_164/templates/genres_afficher.html"
  * Vous devez vous aider de "CTRL-R"(scope : fichier) ou "CTRL-SHIFT-R"(scope : tout le projet)
  * utiliser la commande "magique" de "PyCharm" comparer deux fichiers "CTRL-D" (menu "View"-->"Compare With...") entre le fichier de mon projet qui fonctionne et le votre qui est presque fonctionnel.

B) Une fois que l'affichage est fonctionnel et uniquement dans ce cas :
  * Vous devez alors changer les noms de variables en Python pour les adapter à votre sujet
    * Exemple : "strsql_genres_afficher" doit s'écrire avec un nom qui correspond mieux à votre sujet de BD

# Évaluation de votre module 164
Dans le but de l'évaluation du module 164, chaque semaine, vous devez déposer votre travail (fichier zip du repository de votre Github) sur le moodle de l'EPSIC
 
  * Si vous ne pouvez pas avancer, vous DEVEZ vous entraider (votre groupe DISCORD est là pour cela)
  * Je suis là pour vous aider, mais il faut que vous me posiez des questions, par mail, cela est parfaitement possible
  * Je vais observer votre avance sur votre github où vous avez défini mon adresse couriel officielle comme "collaborateur" à votre github
  * Réaliser un "COMMIT" avec un message qui indique votre avance en quelques mots
  * Réaliser un "PUSH" dans votre "GITHUB" privé, n'oubliez pas de m'inviter avec mon adresse officielle (déjà donnée)

  * Dans votre github. Créer un fichier "zip" à télécharger sur votre disque local vous DEVEZ le déposer sur Moodle de l'EPSIC dans la semaine correspondante
  * Le lien de votre github doit être dans un fichier "txt" que vous DEVEZ déposer sur Moodle de l'EPSIC dans la semaine correspondante
  * Il faut respecter mes consignes énoncées dans ce fichier "readme.md" et sur le MOODLE de l'EPSIC. Sinon, vous ne pourrez plus prétendre à l'excellence, soit la note de "6"
    * Le but de ce module 164 est de faire un CRUD sur votre BD, pas de faire du code. Donc faites ce qui est demandé pas plus, ni moins


# Pour "rafraîchir" les versions des packages (Terminal de "PyCharm") 

  * pip3 freeze > requirements.txt
  * pip3 install pipupgrade
  * pipupgrade --verbose --latest --yes

