!!! info "Dans ce cours nous utiliserons essentiellement le langage Python."

!!! summary "Pourquoi ?" 
    Ce langage possède une syntaxe relativement simple qui nous permet de coder vite et bien.
    Les programmes fonctionnent rapidement et la mise au point est facilitée avec le mode interactif.
    Cet apprentissage avec Python vous donnera les bases essentielles de la programmation
    et sera facilement transposable sur un autre langage.

    L'environnement Python possède un atout de taille : de nombreuses librairies spécialisées permettent
    d'intégrer de nouvelles fonctionnalités en un claquement de doigts :
    
    - Le traitement des données : Panda, Bokeh
    - Le web : Django
    - Les mathématiques : Numpy, Scipy
    - L'intelligence artificielle : Keras, Tensorflow
    - Le jeu : Pygame
    - L'image : PIL, OpenCV
    - ...

### Python sur sa machine
??? info "Vérification de l'installation et de la version de Python installé sur votre ordinateur"
    Il se peut qu'une version de Python soit déjà présente sur votre ordinateur. Suivez les indications ci-dessous
    pour le savoir
    === "Sous windows"
        !!! help "1- Avec l'outil de recherche (la loupe) rechercher l'application ```cmd```"
        ![](../images/install/install_win/cmd01.png){ width=60% }
        !!! help "2- une fois l'application lancée, tapez la commande ```python --version```"
        ![](../images/install/install_win/cmd02.png){ width=60% }
        ![](../images/install/install_win/cmd02.png){ width=60% }
        !!! conclu "Si python est présent, la commande répond en donnant la version existante sur l'ordinateur"
        ![](../images/install/install_win/cmd03.png){ width=60% }
        !!! help "3- Pour connaître le répertoire d'installation, tapez la commande ```where python```"
        ![](../images/install/install_win/cmd04.png){ width=60% }
        !!! conclu "La commande répond en donnant tous les chemins trouvés"
        ![](../images/install/install_win/cmd05.png){ width=60% }

    === "Sous Mac"
        !!! help "1- Avec l'outil de recherche (la loupe) rechercher l'application ```terminal```"
        ![](../images/install/install_mac/cmd01.png){ width=30% }
        !!! help "2- une fois l'application lancée, tapez la commande ```python3 --version```"
        ![](../images/install/install_mac/cmd02.png){ width=60% }
        !!! conclu "Si python est présent, la commande répond en donnant la version existante sur l'ordinateur"
        ![](../images/install/install_mac/cmd03.png){ width=60% }
        !!! help "3- Pour connaître le répertoire d'installation, tapez la commande ```where python3```"
        ![](../images/install/install_mac/cmd04.png){ width=60% }
        !!! conclu "La commande répond en donnant tous les chemins trouvés"
        ![](../images/install/install_mac/cmd05.png){ width=60% }### Installer Python
??? info "Installation de Python"
    === "Sous Windows"
        Cette installation est à faire une unique fois sur votre ordinateur personnel        
        !!! help "1- lancez votre navigateur préféré et allez sur le site python.org, dans la section downloads"
        ![](../images/install/site_python_win.png)
        !!! help "2- cliquez sur le bouton Download Python 3.10.5 (attention la version peut-être différente) pour lancer le téléchargement"
        !!! conclu "Le site détecte automatiquement la bonne version pour votre ordinateur"
        !!! help "3- Lancez le fichier téléchargé, une fenêtre d'installation apparaît"
        ![](../images/install/install_win/install02.png){ width=60% }
        !!! warning "N'oubliez pas de cliquer les 2 cases en bas (Install... et Add Python...), avant de passer à l'étape suivante"
        !!! help "4- Cliquez sur le bouton Customize installation (pas d'installation rapide)"
        ![](../images/install/install_win/install03.png){ width=50% }
        !!! warning "Cochez les bonnes cases avant de passer à l'étape suivante"
        ![](../images/install/install_win/install04.png){ width=60% }
        !!! warning "Vérifiez que le répertoire d'installation soit bien le répertoire des programmes de Windows"
        ![](../images/install/install_win/install05.png){ width=60% }
        !!! done "Python est installé"
        !!! danger "Si vous souhaitez désinstaller une version, il vous faut relancer l'installateur d'origine"
        ![](../images/install/install_win/desinstall.png){ width=60% }

    === "Sous Mac"
        Cette installation est à faire une unique fois sur votre ordinateur personnel        
        !!! help "1- lancez votre navigateur préféré et allez sur le site python.org, dans la section downloads"
        ![](../images/install/site_python_mac.png)
        !!! help "2- cliquez sur le bouton Download Python 3.10.5 (attention la version peut-être différente) pour lancer le téléchargement"
        !!! conclu "Le site détecte automatiquement la bonne version pour votre ordinateur"
        !!! help "3- Lancez le fichier téléchargé, une fenêtre d'installation apparaît"
        ![](../images/install/install_mac/install01.png){ width=60% }
        !!! help "4- Cliquez sur le bouton Continuer"
        ![](../images/install/install_mac/install02.png){ width=60% }
        !!! help "5- Cliquez sur le bouton Continuer"
        ![](../images/install/install_mac/install03.png){ width=60% }
        !!! help "6- Cliquez sur le bouton Continuer"
        ![](../images/install/install_mac/install04.png){ width=60% }
        !!! help "7- Cliquez sur le bouton Accepter"
        ![](../images/install/install_mac/install05.png){ width=60% }
        !!! help "8- Cliquez sur le bouton Continuer"
        ![](../images/install/install_mac/install06.png){ width=60% }
        !!! help "9- Cliquez sur le bouton Installer"
        ![](../images/install/install_mac/install07.png){ width=60% }
        !!! done "le programme s'installe"
        ![](../images/install/install_mac/install08.png){ width=60% }
        !!! help "10- le programme est installé"
### Installer des librairies
??? info "Installer des librairies"
    === "Sous Windows"""
        !!! help "1- Avec l'outil de recherche (la loupe) rechercher l'application ```cmd```"
        ![](../images/install/install_win/cmd01.png){ width=60% }
        !!! help "2- une fois l'application lancée, tapez la commande ```python.exe -m pip install --upgrade pip``` pour mettre à jour l'application d'installation"
        ![](../images/install/install_win/pip01.png){ width=60% }
        !!! help "3- puis tapez la commande  ```python.exe -m pip install pygame```, dans cet exemple, il s'agit d'installer le package pygame"
        ![](../images/install/install_win/pip02.png){ width=60% }
    === "Sous Mac""
        !!! help "1- Avec l'outil de recherche (la loupe) rechercher l'application ```terminal```"
        ![](../images/install/install_mac/cmd01.png){ width=40% }
        !!! help "2- une fois l'application lancée, tapez la commande ```python3 -m pip install --upgrade pip``` pour mettre à jour l'application d'installation"
        ![](../images/install/install_mac/pip01.png){ width=70% }
        !!! help "3- puis tapez la commande  ```python3 -m pip install pygame```, dans cet exemple, il s'agit d'installer le package pygame"
        ![](../images/install/install_mac/pip02.png){ width=70% }
### Des outils pour développer
??? info "Les environnements de développement"
    Pour créer des programmes vous pouvez utiliser un éditeur de texte standard, mais ce n'est pas le choix le plus pratique et le plus efficace.

    Un environnement de développement (IDE) fournit une interface adaptée aux différentes tâches du développeur.

    Plusieurs choix possibles :

    - des applications sur l'ordinateur, 2 essentiellement :
        - Thonny, un environnement léger qui permet un déboguage rapide
        - Visual Studio Code, un environnement plus professionnel
    - des applications en ligne :
        - Python Tutor, essentiellement pour apprendre les mécanismes principaux de la programmation
        - Basthon : un éditeur python en ligne
        - Replit : une application en ligne qui permet le travail en équipe sur le même fichier
    - Vous aurez aussi la possibilité de travailler directement en ligne sur ce site

    === "Thonny"
        Un éditeur simple et basique, qui permet de faire du pas à pas facilement (pour déboguer ou comprendre un programme)
        !!! help "1- pour le télécharger, RDV sur le site https://thonny.org"
        ![](../images/IDE/thonny01.png)
        !!! help "2- télécharger la version de votre ordinateur (PC ou mac), pour l'installer sur votre machine"
        ![](../images/IDE/thonny02.png){ width=50% }
        !!! help "3- cliquez sur le bouton 'install for users', puis pour les écrans suivants acceptez par défaut"
        ![](../images/IDE/thonny04.png){ width=50% }
        !!! help "4- lors du premier lancement vous pouvez choisir la langue par défaut"
        !!! warning "Thonny installe sa propre version de Python, ce qui oblige en particulier à installer les nouvelles librairies par l'intermédiaire de l'interface Thonny"
        ![](../images/IDE/thonny05.png)
        !!! help "5- dans le menu Outils, avec la commande ```Gérer les paquets...```"
        ![](../images/IDE/thonny06.png)
        !!! help "6- Une recherche du module souhaité, puis son installation"
        
    === "Visual Studio Code"
        Un éditeur beaucoup plus professionnel, mais rapide et très performant. A l'origine c'est un produit gratuit dérivé du produit phare de chez Microsoft 'Visual Studio'. Il a été très vite adopté par de nombreux développeurs et est devenu un produit régulièrement maintenu et amélioré. Il est toujours gratuit, robuste et mature. De plus grâce à ses modules il pourra vous servir pour beaucoup d'autres langages
        !!! help "1- pour le télécharger, RDV sur le site https://code.visualstudio.com/ et cliquez sur le bouton Download"
        ![](../images/IDE/VSC01.png)
        !!! help "2- télécharger la version de votre ordinateur (PC, mac ou linux), pour l'installer sur votre machine"
        ![](../images/IDE/VSC03.png){ width=60% }
        !!! help "3- sélectionnez 'Je comprends et ...' et cliquez sur Suivant"
        ![](../images/IDE/VSC04.png){ width=60% }
        !!! help "4- gardez le dossier de destination proposé et cliquez sur Suivant"
        ![](../images/IDE/VSC05.png){ width=60% }
        !!! help "5 cliquez sur Suivant"
        ![](../images/IDE/VSC06.png){ width=60% }
        !!! help "6- vous pouvez opter pour une icone sur le bureau, cliquez sur Suivant"
        ![](../images/IDE/VSC07.png){ width=60% }
        !!! help "7- cliquez sur Installer"
        
        !!! info "Après cette première installation, il va falloir ajouter quelques extensions pour pouvoir être vraiment opérationnel"
            > Nous allons pour cela utiliser l'option 'extensions' sur le coté gauche de l'application
            >
            > Il existe de nombreuses extensions
            >     
    === "Python tutor"
        Il existe une option originale pour découvrir la programmation en Python grâce au logiciel en ligne Python Tutor. Cet outil permet de visualiser en live le déroulement d'un programme.

        C'est un outil pédagogique de choix qui de plus ne requiert aucune installation.

        Python Tutor a été créé par Philip Guo, professeur assistant à l'université de Californie. Il a crée Python Tutor pour aider les gens à comprendre ce qu'il se passe chaque fois qu'une ligne de code est exécutée.

        Disponible en licence libre, cet outil est accessible depuis le site : [http://pythontutor.com/live.html](http://pythontutor.com/live.html)
        !!! help "On créé son code, on clique sur le bouton 'Visualize Execution'"
        ![](../images/IDE/PT01.png) 
        ![](../images/IDE/PT02.png)       
        !!! help "On exécute le programme pas à pas"
        ![](../images/IDE/PT03.png)
    === "Basthon"
        Si vous ne pouvez pas installer d'application sur votre machine et que vous souhaitez tout de même tester quelques programmes Python, vous avez la solution Basthon.

        Un site en ligne qui permet de faire tourner vos programmes. Cette application est relativement puissante et vous pourrez faire tourner pratiquement tous les programmes à voir cette année. La documentation est très bien faite (en français).


        !!! summary "disponible sur le site [https://basthon.fr](https://basthon.fr)"
        ![](../images/IDE/basthon01.png)
        !!! summary "La console Python"
        ![](../images/IDE/basthon02.png)

        !!! info "Il existe même un module tutor qui permet d'utiliser l'application en ligne Python Tutor"

        ```python
        from tutor import tutor

        a = 5
        a = a + 1

        tutor()
        ``` 

    === "Replit"
        Un autre style de site en ligne. A la façon GitHub, ce site permet de créer des programmes en équipe, avec une interface d'exécution
