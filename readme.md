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

j'ai réalisé une 

### Contenu du repository



*Ce projet a été réalisé dans le cadre de la formation [Data Analyst](https://openclassrooms.com/fr/paths/65-data-analyst), d'OpenClassrooms.*