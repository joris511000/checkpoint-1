# exercice 1 Gestion de disque
 
## pour créer les deux partion voila ma procédure :
- __fdisk /dev/sdb  pour partionné le disk__ 

- ![](https://github.com/joris511000/checkpoint-1/blob/main/Capture%20d'%C3%A9cran%202024-06-14%20092809.png?raw=true) 
- ![](https://github.com/joris511000/checkpoint-1/blob/main/Capture%20d'%C3%A9cran%202024-06-14%20093440.png?raw=true)

## Formatage des partitions


_
![](https://github.com/joris511000/checkpoint-1/blob/main/Capture%20d'%C3%A9cran%202024-06-14%20094110.png?raw=true)

## montage des Partitions
j'ai egalement desactivé la partition swap deja avtive avec la commande: _swapoff /dev/sda5_

et j'ai monter ma partion le swap avec la commande: _swapon /dev/sdb2_

puis j'ai crée le point de montage DATA avec la commande: _mkdir /mnt/DATA_
et j'ai édité le fiché fstab avec: _nano /etc/fstab_

![](https://github.com/joris511000/checkpoint-1/blob/main/Capture%20d'%C3%A9cran%202024-06-14%20095637.png?raw=true)

enfin j'ai monter mon disque avec: _mount /mnt/DATA_
![](https://github.com/joris511000/checkpoint-1/blob/main/Capture%20d'%C3%A9cran%202024-06-14%20124404.png?raw=true)
![](https://github.com/joris511000/checkpoint-1/blob/main/Capture%20d'%C3%A9cran%202024-06-14%20102023.png?raw=true)






# exercice 2 scrip 
## voicie mon script

![](https://github.com/joris511000/checkpoint-1/blob/main/Capture%20d'%C3%A9cran%202024-06-14%20110030.png?raw=true)

## exemple de bon fonctionnement du script

![](https://github.com/joris511000/checkpoint-1/blob/main/Capture%20d'%C3%A9cran%202024-06-14%20105956.png?raw=true)

# exercice 3 Quiz

1) Donne une ligne de commande bash qui permet de lister la liste des utilisateurs d'un système Linux

Réponse: __cut -d: -f1 /etc/passwd__

2) Quelle commande bash permet de changer les droits du fichier myfile en rwxr—r-- ?

Réponse : __chmod u=rwx,g=r,o=r myfile__

3) Comment faire pour que les fichiers pdf d'un dépôt local git ne soient pas pris en compte lors d'un git push ?

Réponse : __Crée ou edité les fiché gitigmore et ajouté l'extention *.pdf. attention si des fichié PDF son deja dans l'index il faudra les retiré pour cela utilisé la commande git rm --cached *.pdf__

4) Quelles commandes git utiliser pour fusionner les branches main et test_valide ?

Réponse : __git merge test_valide__

5) Donne la(les) ligne(s) de commande(s) bash pour afficher le texte suivant :

Réponse: __echo devant chaque ligne de ce textecomme ce si:__

echo 'Malgré le prix élevé de 100$, il a dit "Bonjour !" au vendeur :'

echo '- "Bonjour est-ce que ce clavier fonctionne bien ?"'

echo '- "Evidemment ! On peut tout écrire avec, que ce soit des pipe | ou bien des backslash \\ !"'

echo '- "Même des tildes ~ ?"'

echo '- "Evidemment !"'

6) La commande jobs -l donne le résultat ci-dessous :__
Quelle commande te permet de mettre en avant le processus gedit ?

Réponce __fg %1__

7) Quels matériels réseaux sont sur la couche 2 et la couche 3 du modèle OSI ? Donne leurs spécificités.

Réponse:  
__switch : Filtrage et transmission des trames en fonction des adresses MAC.__

__Bridge : Relie des segments de réseau local pour limiter la diffusion de trames.__

__Routeur : Sélectionne le meilleur chemin pour le transfert de données entre réseaux différents.__

8) Quels sont les équivalent PowerShell des commandes bash cd, cp, mkdir, ls.

Réponse: __cd=set-location / cp=copy-Item / mkdir=New-Item / ls=Get-ChildItem__

9) Dans la trame ethernet, qu'est-ce que le payload ?

Réponse: __la charge utile  est la partie des données transmises qui constitue le message réellement prévu.__

10) Pourquoi les classes IP sont remplacées par le CIDR ?
Réponse :

 __CIDR remplace les classes IP en raison de sa capacité à mieux gérer les ressources limitées d'adresses IPv4, à permettre une allocation plus efficace des adresses en fonction des besoins réels des réseaux.__






