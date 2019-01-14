# L'Amélioration progressive

- Emplacement : [GitHub](https://github.com/) sur un repository intitulé "`progressive-enhancement`"
- Slides : [La typographie web](la-typographie-web.pdf)
- Temps nécessaire : 4 jours 
- Publier le résultat en tant que GitHub Page
- Remise du projet via ce [formulaire](https://goo.gl/forms/0ZuXfIK8Jl4Nkltm2)

## 1. Sémantique HTML

Ca veut dire quoi "**sémantique**" ?    
Pour bien composer un document HTML, il faut raisonner non pas en termes d'apparence graphique mais en termes de définition de chacun des objets le composant, c.à.d. réfléchir en terme de structure du document.
Utiliser une balise "titre" pour un titre, une balise "définition" pour une définition, etc.  
Concrètement, faire du HTML sémantique consiste à se poser la question : "*Ce bout de texte, c'est quoi : un titre ? Un paragraphe ? Une légende ? Et ce bloc, est-ce un chapitre ? Une note de l'auteur ?*" et en fonction de la réponse, choisir la balise correspondante ou s'en rapprochant le plus.

### Pourquoi la sémantique est importante pour le web developer 

Pour deux raisons :  la **SEO** (position de ton site dans Google) et **l'Accessibilité** (accès à l'information pour tout humain, peu importe son âge ou d'éventuels handicaps).  

#### 1.1 SEO

L'objectif ultime d'un moteur de recherche comme Google est de retourner à un humain les meilleurs résultats possibles pour ce qu'il a cherché (quelques mots). Pour ce faire, Google crée des logiciels tels que le Googlebot, qui indexe le contenu trouvé sur le web en suivant les liens d'une page à une autre, d'un site à l'autre. Via des algorithmes puissants, Google lit et analyse le contenu HTML de chaque page trouvée, ce qui lui permet de "comprendre" ce dont parle la page grâce à la structure HTML (titre, sous-titre, liste, etc). Elle peut ainsi déterminer ce dont parle chaque page, et si celle-ci semble correspondre à la recherche, elle va la retourner à l'utilisateur.

Par conséquent, si nos pages ne sont pas bien sémantiques, Google ne les montrera pas, et vos sites n'auront pas de traffic. 

#### 1.2 Accessibilité
Le web est un projet universel : tout le monde doit avoir accès au contenu. En ce compris les aveugles et mal voyants (toi, un jour). Les aveugles utilisent des "liseuses d'écran" (*screen readers*) qui se basent sur le code HTML pour raconter le site à voix haute. Si ton code html n'est pas sémantique, la page n'aura pas beaucoup de sens à l'écoute (même si visuellement elle rend correctement). N'hésite pas à [tester sur ton propre ordinateur](https://stackoverflow.com/a/43368748/53960).

### Concrètement, la sémantique, c'est simple.
 
La sémantique consiste à choisir les bonnes **balises** et **attributs** pour représenter ton contenu. Note bien que trop de sémantique tue la sémantique. La règle (comme souvent en programmation) est : **le moins de code possible, mais autant que nécessaire.**

#### Balises

Les balises permettent d'indiquer la fonction sémantique d'une portion de contenu dans des "blocs". En HTML, la plupart des blocs fonctionnent avec une balise d'ouverture, et une balise de fermeture.

**Exemple de syntaxe :**

```html
<p>Ceci est un paragraphe.</p>
```

**A toi de jouer !**	

Retranscris [ce document Texte](doc-le-paysan-chinois.txt) en sémantique HTML, donc en utilisant les bons blocs HTML (pas de `div` ni de `span`)  
- Utilise les balises suivantes: `h1`, `h2`, `blockquote`, `q`, `img`, `p`, `img`, `hr`, `figure` et `caption`, `table`, `th`, `tr`, `td`, `ul` ou `ol` et `li`. 
- Retrouve, pour chacune de ces balises, l'origine de leur nom (c'est comme cela qu'on les retient). En cas de doute, cherche la réponse sur [html5doctor.com](http://html5doctor.com).
- Ajoute 2 ou 3 liens de ton choix dans la page HTML via la balise `a`
- Y-a-t-il une partie que l'on pourrait considérer comme une entête ? Si oui, regroupe la dans une balise `header`. 
- Et un pied de page ? Si oui, regroupe ce contenu-là dans une balise `footer`
- Mets toutes les instances des mots "Bien" et "Mal" dans une balise `span` , `em` ou `strong`. 


#### **Les attributs HTML**
Ils permettent de définir les caractéristiques des balises.  Imagine qu'il y ait une balise "humain".    
```<human>Steven Paul Jobs, dit Steve Jobs, (San Francisco, 24 février 1955 - Palo Alto, 5 octobre 2011) est un entrepreneur... </human>```   
Nous pouvons, avec des attributs, décrire cet humain pour le différencier des autres.

```<human name="Steve Job" nationality="USA" origin="Syria" job="CEO" company="Apple" hair="grey">Steven Paul Jobs, dit Steve Jobs, (San Francisco, 24 février 1955 - Palo Alto, 5 octobre 2011) est un entrepreneur... </human>```  

De la sorte, en augmentant la sémantique des balises par des attributs, on a ainsi clarifié pour une machine qui est cet humain là. Remarque la syntaxe:

```html
<balise attribut="valeur">Contenu</balise> 
``` 

**Exercices :**  

- Rajoute l'attribut `Alt` aux images. A quoi sert cet attribut?  
- Ajoute une classe "*bien*" ou "*mal*" aux balises entourant les mots "Bien" et "Mal".
- Trouve l'attribut des liens permettant d'indiquer la page vers laquelle doit mener le lien, et ajoute-le.  
- Fais en sorte que lorsqu'on clique sur les liens, la page s'ouvre dans un nouvel onglet du navigateur.  
- Trouve l'attribut permettant d'afficher une petite boite de texte au survol des liens   
![Exemple](https://cdn.searchenginejournal.com/wp-content/uploads/2008/09/title-usability.jpg)


## Prochaine étape :
[Le CSS](2-CSS.md)
