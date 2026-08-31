Dépôt Git Bachelor EPFL par Anthony Gabino



\# Notes de cours — Bachelor Mathématique



Notes prises en LaTeX lors des différentes années de Bachelor de mathématiques



\## Matières


Il y a un dossier par semestre contenant un dossier de chaque matière vu lors de ce semestre. Chaque branche possède son propre dossier dans lequel se trouve le PDF des notes de cours ainsi que les différents fichiers LaTeX nécessaires si vous voulez compiler les fichiers de votre côté.



\## Structure



```

├── BA1/

│    ├── Algèbre linéaire avancée I/

│   	 ├── algèbre linéaire I.tex

│        ├── algèbre linéaire I.pdf    

│   	 └── chapitres/

│    ├── Analyse avancée I/

│ 	 ├── Analyse avancée I.tex

│        ├── Analyse avancée I.pdf    

│   	 └── chapitres/

│    ├── ...

├── BA2/ …

├── BA3/ …


├── shared/

│   ├── preamble.tex       # Importation des packages

│   ├── commands.tex    # Commandes communes (ℝ, ℕ, …)

│   └── titlepage.tex    # Template de page de titre

└── README.md

```


\## Compilation



Chaque cours se compile indépendamment depuis son dossier (cependant il est important de bien vérfier que vous avez bien télécharger le dossier "shared" car dans le cas écheant, le fichier ne se compilera pas):



```bash

cd "BA1/algèbre linéaire avancée I"

latexmk -pdf "Algèbre linéaire avancée I.tex"

```



\## Prérequis

\- Une distribution LaTeX en ligne — \[Overleaf] (https://www.overleaf.com/), mais je vous déconseille de passer par Overleaf, la structure des dossiers et la conception du projet a été conçut sur un IDE local. Ainsi je vous conseil d'utuliser plûtot :

\- Une distribution LaTeX complète — \[MiKeX] (https://miktex.org/) (Linux/Windows/MacOS) + une IDE vous permettant de compiler des fichiers LaTeX -- \[TeXstudio] (https://www.texstudio.org/) ou \[Texmaker] (https://www.xm1math.net/texmaker/)



\## Gitignore

Afin d'avoir une meilleur lisibilté sur le dépot GitHub, tout les fichiers liés à la compilation latex tel que les fichiers ".aux", ".fls", ".log"... ne se trouvent pas sur le GitHub mais ils se créeront automatiquement une fois que vous lancerez la compilation de votre côté pour la première fois.

