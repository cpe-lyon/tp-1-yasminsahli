Yasmin SAHLI - 3ICS

# TP1 – Installation d’Ubuntu Server et prise en main du shell

## Exercice 2 - Prise en main de l’interpréteur de commandes 

Manuel
1.	Le rôle de la commande which est de produire le chemin complet des commandes du shell.
2.	man which -k option
3.	Pour quitter le manuel il faut taper q.
4.	Pour afficher la première page de la section 6 du manuel j’ai utilisé la commande : man 6 intro
Cette section a pour description : « Section 6 of the manual describes the games and funny little programs available on the system. »

Navigation dans l’arborescence
1.	cd /var/log 
2.	 cd ..
3.	 cd
4.	cd -
5.	 Nous n’avons pas les droits pour accéder au dossier root 
6.	 La commande sudo n’est pas disponible, car nous n’avons pas installé le package
7.	
```bash
cd ..
mkdir Dossier1 Dossier2
cd Dossier1
touch Fichier1
cd Dossier2
mkdir Dossier2.1
mkdir Dossier 2.2
cd Dossier2.2
touch Fichier2
touch Fichier3
```

8.	 On ne peut pas supprimer le Fichier1 depuis le dossier personnel.  Et on ne peut pas supprimer le Dossier1 car la commande rm permet de supprimer des fichiers et non pas des dossiers.
9.	Rmdir supprime un dossier mais seulement s’il est vide.
10.	Le Dossier2 n’étant pas vide il n’est pas supprimé par cette commande.
11.	 rm –r Dossier2 est la commande qui permet de supprimer le dossier2 et ce qui le compose

Commandes importantes
1.	 Pour afficher l’heure on utilise la commande : date. La commande time est un chronomètre qui calcule le temps lors de l’exécution d’un logiciel.
2.	 Les fichiers commençants par un point sont des fichiers initialement cachés.
3.	 Le programme ls se trouve grâce à ce chemin : /usr/bin/ls
4.	 La commande ll de connaitre les droits de chaque utilisateur (lecture/suppression /exécution). La commande manuelle de ll est ls -alF
5.	Pour afficher le contenu du dossier /bin on fait : ls /bin 
6.	 Ls .. affiche les dossiers et fichers précédents.
7.	  Pour afficher le chemin complet du dossier courant on utilise pwd et on optient ce chemin : /home/User
8.	 La commande echo ‘bip’ > plop exécutée 2 fois affiche le mot bip dans le fichier plop même si on réitère la commande plusieurs fois.
9.	 La commande echo ‘bip’ >> plop exécutée 2 fois affiche le mot bip 3 fois dans le fichier plop, le mot sera donc affiché autant de fois que l’on exécute la commande.
10.	 Cette commande affiche toto et bloque l’utilisation de la ligne de commande durant 10 secondes.  C’est la concaténation de deux commandes.
11.	La commande file affiche le type du fichier choisie, par exemple un texte ASCII 
12.	 Echo ‘Hello Toto !’ > original et pour modifier le contenu de original on fait echo ‘Hello Toto Modif !’ > original et pour afficher le contenu de lien_phy on fait cat lien_phy. Le contenu est le même dans les deux fichiers. Pour supprimer original on fait rm original et le fichier orignal est supprimé mais le fichier lien_phy et son contenu existe toujours.
13.	 Pour modifier lien_phy on fait : echo ‘Hello Toto Modif Bis !’ > lien_phy et si on modifie lien_phy la modifiction se fait aussi dans lien_sym. Et si on supprime lien_phy avec la commande rm lien_phy cella supprime aussi le lien symbolique. 
14.	 Pour afficher le fichier syslog on fait la commande cd /var/log puis cat syslog et pour arreter le défilement et le reprendre on fait la commande : tail -f
15.	 head -5 syslog affiche les 5 premières lignes du fichiers et tail -15 syslog pour afficher les 15 dernières lignes. Pour les lignes 10 à 20 on utilise : cat syslog | tail –n +10 | head –n 10
16.	 Cela affiche les logs dans un lecteur de fichier plus facile d’utilisation.
17.	 Ce fichier contient les noms de tous les utilisateurs man -5 psswd
18. cat /etc/passwd | awk '{ print $1 }' | sort -r
19. cat /etc/passwd | wc -l
20. Man -k conversion | wc -l
21. Find / -name passwd
22. Find / -name passed 2>/dev /null > ˜/list_passwd_files.txt
23. Grep « alias ll=«  -r ˜, il se trouve dans «˜/.bashrc »
24/25. Impossible d’installer locate
 
## Exercice 3 - Découverte de l’éditeur de texte nano 
1.	Touch log.txt pour créer le fichier. Puis cp /var/log/syslog log.txt. Et on peut l’ouvrir nano log.txt
2.	Remplacer le mot kernel par noyau on fait : Ctrl \ kernel noyau A
3. Alt + A puis Ctrl + K et en bas du fichier on fait Ctrl + U 	 
4.	Alt U permet d’annuler l’action précédente

## Exercice 4 - Personnalisation du shell 

Questions 1 à 3 sont le test de commandes 

4. \A[\033[01;35m] - \u@\h[\033[32m]:[\033[01;34m]\w[\033[36m]$

