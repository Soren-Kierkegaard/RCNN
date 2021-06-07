# RCNN
Un petite implémentation de l'algo RCNN sur des images aérienne d'avions.

# Architecture

![RCNN-Archit](https://raw.githubusercontent.com/D3lt4lph4/papers/master/docs/images/imagedetection/rcnn/rcnn_network.png)

- Le modèle de base pour le Transfert Learning est le modèle VGG-16
- On a conserver qu'une seule sortie (la valeur de sortie est "background" ou "Airplane"
- On utilise la fonction < selective search > pour proposé divers régions (~2K images) selon la couleur, texture, ...
- Chacune de ces ~2K région et envoyé au modèle pour nous dire s'il s'agit d'un "fond" ou d'un "avion"
-   Si oui, alors dessiner la predicted bounding box proposée

# Dataset

- Les données provienne de http://www.escience.cn/people/JunweiHan/NWPU-RESISC45.html
- Le jeu d'entrainement https://www.kaggle.com/aceofspades914/cgi-planes-in-satellite-imagery-w-bboxes peut aussi être utilisé en modifiant les chemins et un peu le code
- Le jeu de donnée consiste en des images satellite d'avions accompagné de leur ground truth aka : leur coord x, y, h, w dans l'image

# ! WARNING !

- La consomation peut-être potentiellement élevée

# Résultats

<table>
  <tr>
    <th> Précision </th>
    <th> 96 % </th>
  </tr>
</table>

# Acknowlege

- Originly coded in Ap. 2020
