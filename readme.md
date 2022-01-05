# Détecteur de faux billets

## Contexte

L’Organisation nationale de lutte contre le faux-monnayage (ONCFM) a pour bojectif de mettre en place des méthodes d'identification des contrefaçons de billets en euros.

Dans ce projet, nous sommes missionné par l'ONCFM pour créer un programme capable de détecter l'authenticité d'un billet à partir de ses dimensions. 

## Cahier des charges

Les données fournis contiennent les dimensions de 1500 billets chacun déja identifiés avec six informations géométriques :
- length : la longueur du billet (en mm) ;
- height_left : la hauteur du billet (mesurée sur le côté gauche, en mm) ; 
- height_right : la hauteur du billet (mesurée sur le côté droit, en mm) ; 
- margin_up : la marge entre le bord supérieur du billet et l'image de celui-ci (en mm) ; 
- margin_low : la marge entre le bord inférieur du billet et l'image de celui-ci (en mm) ; 
- diagonal : la diagonale du billet (en mm).

L'algorihtme doit pouvoir récupérer les données d'un fichier contenant des dimensions et doit être le plus performant possible.

## Méthodologie

Suivant le cahier des charges, on mets en concurence 2 méthodes de prédiction :
- une régression logistique classique
- un k-means (utilisant les centroîdes)

J'ai en premier lieu réalisé une analyse descriptive des données qui a mis en évidence la présence de données manquantes concernant la variable "margin_low".
Gràce à une matrice de corrélation, j'ai sélectionné des variables corrélées avec "margin_low" pour réaliser une régression linéaire pour prédire et compléter ces valaurs manquantes.

Pour la mise en place des algorithmes de prédiction, j'ai réaliser un échantionnage des données :
- 80% pour le traning test
- 20% pour le testing test

> Aprés avoir réaliser les test sur les différentes méthode de prédiction, j'ai choisi la régression logisitque classique qui présente le meilleur score de précision pour le programme de détection.


*Ce projet a été réalisé dans le cadre de la formation [Data Analyst](https://openclassrooms.com/fr/paths/65-data-analyst), d'OpenClassrooms.*