# L'Amélioration progressive

[Etape précédente](readme.md)

## 2. Le CSS (Le look)

Le CSS est la techno qui te permet de contrôler l'aspect visuel de ton contenu.  Par exemple, tu peux contrôler l'aspect du texte via ces propriétés : `font-style`, `font-size`, `color`, `line-height`.

Autrement dit, si le HTML te permet de structurer le contenu, le CSS te permet de le **maquiller**, le rendre plus visuellement attractif.

### Syntaxe
Chaque ligne doit se terminer par un `;`

```css
selecteur {
	propriete : valeur ;
	propriete : valeur ;
	/* Ceci est un commentaire */
	propriete : valeur ;
	...
}  
```

Tu peux déclarer autant de propriétés que tu le souhaites. Tu peux même déclarer deux fois la même propriété. Dans ce cas, ce sera la dernière qui sera prise en compte (d'où le terme "cascading").

Pour que le navigateur le prenne en compte, ton CSS doit se trouver soit :

- dans ton fichier HTML, dans une balise `<style>`
- dans un fichier CSS externe, lié à ton HTML via la balise `<link>`


### Concept 1 : sélecteurs CSS

Les sélecteurs CSS te permettent de sélectionner dans ton HTML le contenu à styliser via la balise le contenant.


#### A toi de jouer !

- stylise les paragraphes : utilise une police à empatement, augmente un peu l'interlignage, utilise une taille de base bien lisible. Donne au texte de couleur foncée, mais pas noire.
- stylise les liens de manière à les rendre bien lisibles.
- stylise l'état "survolé" et l'état "visité" des liens.

### Concept 2 : le bloc
 
Toute balise est rendue visuellement sous forme de "bloc" (en anglais on parle du [box model](https://www.w3schools.com/css/css_boxmodel.asp)).  

![Le bloc](css-block.png)  

Tu peux contrôler les dimensions et les espacements de ce bloc :   

- `width`/ `height` : dimensions de largeur et hauteur 
- `border`: contrôle la bordure. Par exemple: `border:1px solid #FF0000;` crée un bord fait d'un trait continu (`solid`) rouge `#FF0000` et de 1px d'épaisseur
- `padding` : l'espace entre le contenu du bloc et son contour (le `border`). Le padding "gonfle" le bloc.  
- `margin` : l'espace autour du bloc, à l'extérieur de lui. Le margin distancie le bloc de son entourage.  

#### Exercices

- Donne au `body` une largeur maximum de 90% 
- Ensuite, centre le `body` en jouant avec la propriété `margin`  
- Fais en sorte que les citations ne prennent en largeur que la moitié de la page   
- En utilisant uniquement la propriété `margin`, positionne les citations au milieu.  
- Augmente la taille du texte dans les citations à 160% de la taille du texte par défaut  
- Donne une couleur légèrement grisée au fond des citations   
- Ajoute une bordure à gauche de chaque citation, de 3px et de couleur brique    
- Le texte des citations touche la bordure, ce n'est pas joli. Ajoute un espace de 30px entre la bordure et le texte de la citation.  
- Fais en sorte que les citations aient un espace vide de 80 pixels au dessus et en dessous.  
- Trouve comment ajouter une couleur de fond à ton `body`
- Change la couleur de fond pour utiliser un dégradé de couleur (va sur [http://www.colinkeany.com/blend/](http://www.colinkeany.com/blend/))
- ajoute une image de fond à ton `body`
- fais en sorte que l'image ne se répète pas 
- change son positionnement à `bottom right` 
- change sa taille à `cover`

#### Les sélecteurs en CSS : class et id
Le plus souvent, on sélectionne les éléments à styliser via l'attribut `class` (`.nom-de-la-classe`) et `id` (`#nom-de-lid`).  

**Exercices**   

- En utilisant uniquement la balise comme sélecteur, mets toutes les citations en italiques.  
	- Identifie les citations des villageois et celles du fermier en assignant à chacune une classe correspondante.  
	- Change la couleur du bord gauche des citations en fonction de la personne qui parle.  

#### Les sélecteurs en CSS : parent et enfant  

**Exercice**

- Sélectionne un élément du `header` et donne lui un fond jaune.

#### Les sélecteurs en CSS : les autres
 
-  `+` et `>` 
-  	Sélectionner via l'attribut `[attribute]`
-   Il y en a quelques autres. Pour te faire une idée de ce qu'ils permettent, va lire la petite [doc officielle](https://www.w3schools.com/cssref/css_selectors.asp), puis joue à [CSS Diner](http://flukeout.github.io/)

**Exercices**  

-   Mets en italique le texte des citations
-   Mets en lettres majuscules toutes les instances des mots "bien" et "mal".
-   Mets en rouge les mots "Mal"
-   Mets en vert les mots "Bien"
-   Stylise la table pour que la couleur de fond de chaque rangée soit en alternance grise ou blanche
-   Au premier élément de la liste (les types de gens), joue avec `background-image` et `padding-right` pour faire apparaître l'image ![bien](bien.png)  
-   Au deuxième élément de la liste (les types de gens), joue avec `background-image` et `padding-right` pour faire apparaître l'image  ![mal](mal.png)  
-   Au troisième élément de la liste (les types de gens), joue avec `background-image` et `padding-right` pour faire apparaître l'image  ![chat](chat.png)  
-   Mets en gras le premier paragraphe

		
### Concept 3 : le positionnement en CSS
Le CSS te permet de définir le positionnement visuel des éléments. C'est probablement le plus riche et donc le plus complexe, car les manières de contrôler le positionnement a eu une histoire plutôt compliquée. Il y a longtemps fallu utiliser des *hacks*. Les choses sont plus stables maintenant, surtout s'il ne faut pas supporter les utilisateurs coincés sur internet explorer 9...  Mais reprenons les choses à leur commencement.
 
#### Comprendre le flux

Chaque bloc HTML hérite (= "reçoit par défaut") d'une propriété "display" qui est soit : `display: inline | inline-block | block`  et s'affiche en fonction de son ordre d'apparition dans le fichier HTML. C'est ce que l'on appelle le **flux de positionnement naturel** ou plus simplement le **flux**.

-  Théorie interactive : https://codepen.io/pixeline/pen/QvrbPv 
-  Exercice : un menu horizontal https://codepen.io/pixeline/pen/PmdPYL 
-  Exercice : une grille https://codepen.io/pixeline/pen/aWavWq  
-  `float` va laisser le block flotter sur le block suivant (au lieu de le pousser à la ligne)

**Exercice**  
 
Fais en sorte que le texte courre autour des images, en utilisant, sur les images, la propriété `float` (ajuste avec du `margin` pour distancier le texte de l'image).   

#### Sortir du flux 

Le flux est le comportement par défaut. Tu peux avoir besoin qu'un élément sorte du flux de position. 

`position : static | relative | absolute | fixed ;`   

La propriété `position` permet de positionner un élément n'importe où (via les propriétés `top` et `left`), à partir des coordonnées de son premier parent en `position: relative` ou `static`. [Expérimente via ce Pen](https://codepen.io/pixeline/pen/vmzNjw?).

**Exercice:**  

- Réalise une [notification d'interface](https://codepen.io/pixeline/pen/dWqMxe)
- [exercice de position absolue](https://codepen.io/pixeline/pen/JNaKJv) 

#### Aller plus loin 
Plus d'informations sur le positionnement CSS : http://fr.learnlayout.com

## Prochaine étape :
[Les webfonts et les bonbons :)](3-webfont-bonbons.md)