# HPC_project1
repo pour le projet d'optimisation d'un outil open source du cours HPC

## Reproduction du travail 

Se rendre dans le dossier `sox-14.4.2`, puis lancer les commandes suivantes :

```
./configure
make -s
make install
```

Plus d'info concernant l'installation peut être trouvé dans le fichier `INSTALL`

Pour lancer l'effet que j'ai choisi d'optimiser, le chorus, il faut lancer la commande suivante, depuis le dossier `src` :

`./sox <input> <output> chorus <gain-in> <gain-out> <delay> <decay> <speed> <depth> [ -s | -t ]`

exemple :

`./sox input/test.wav result/test.wav chorus 1.0 0.6 30.0 0.6 1.0 1.0 -s`

Actuellement, le logiciel est en version optimisée.

Pour tester le logiciel en version originale, voici la marche à suivre :

* se rendre dans le dossier `src`
* renomer `chorus.c` en `chorus_opt.c` 
* renomer de `chorus_old.c` pour `chorus.c`
* remonter d'un dossier (`cd ..`)
* `make -s`
* `make install`

Pour ensuite repasser à la version optimisée :

* se rendre dans le dossier `src`
* renomer `chorus.c` en `chorus_old.c ` 
* renomer de `chorus_opt.c` pour `chorus.c`
* remonter d'un dossier (`cd ..`)
* `make -s`
* `make install`
