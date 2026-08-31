Dépôt Git Bachelor EPFL par Anthony Gabino



\# Notes de cours — Bachelor Mathématique



Notes prises en LaTeX lors que BA3 en bachélore de mathématique à l'EPFL



\## Matières


Il y a un dossier pour chaque matière vu lors de ce semestre. Chaque matière possède son propre dossier dans lequel se trouve le PDF des notes de cours ainsi que les différents fichiers LaTeX nécessaires si vous voulez compiler les fichiers de votre côté.

De plus les pdf ont été conçut en \documentclass[book] ainsi il est préférable sur consulter les fichiers .pdf avec l'affichage livre car la mise en page a été pensé en conséquence. 


\## Structure



```

├── BA3/

│    ├── Analyse III - Lebesgue/

│   	 ├── Analyse III - Lesbesgue.tex

│        ├── Analyse III - Lesbesgue.pdf   

│   	 └── chapitres/

│    ├── Algèbre II - groupes/

│      	 ├── Algèbre II - groupes.tex

│        ├── Algèbre II - groupes.pdf    

│   	 └── chapitres/


│    ├── shared/

│        ├── preamble.tex       # Importation des packages

│        ├── commands.tex    # Commandes communes (ℝ, ℕ, …)

│        └── titlepage.tex    # Template de page de titre

│    ├── .gitignore #fichier git permettant de supprimer du dépôt les fichiers de compilation LaTeX

│    └── README.md



```


\## Compilation



Chaque cours se compile indépendamment depuis son dossier (cependant il est important de bien vérfier que vous avez bien télécharger le dossier "shared" car dans le cas écheant, le fichier ne se compilera pas):



```bash

cd "Analyse III - Lebesgue"

latexmk -pdf "Analyse III - Lebesgue.tex"

```



\## Prérequis

\- Une distribution LaTeX en ligne — \[Overleaf] (https://www.overleaf.com/), mais je vous déconseille de passer par Overleaf, la structure des dossiers et la conception du projet a été conçut sur un IDE local. Ainsi je vous conseil d'utuliser plûtot :

\- Une distribution LaTeX complète — \[MiKeX] (https://miktex.org/) (Linux/Windows/MacOS) + une IDE vous permettant de compiler des fichiers LaTeX -- \[TeXstudio] (https://www.texstudio.org/) ou \[Texmaker] (https://www.xm1math.net/texmaker/) ainsi d'un lecteur de fichier .pdf (qui n'est pas Adobe reader), je vous conseil \[Sumatra PDF] (https://www.sumatrapdfreader.org/free-pdf-reader) qui est bien plus léger et surtout qui permet la compilation du fichier en temps réel ce qu'Adobe ne peut pas faire (si vous utilisez Adobe vous serez obligé d'ouvrir et de fermer le fichier .pdf à chaque fois, ce qui n'est pas très opti) 



\## Gitignore

Afin d'avoir une meilleur lisibilté sur le dépot GitHub, tout les fichiers liés à la compilation latex tel que les fichiers ".aux", ".fls", ".log"... ne se trouvent pas sur le GitHub mais ils se créeront automatiquement une fois que vous lancerez la compilation de votre côté pour la première fois.

