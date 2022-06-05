# Axe Dev Tools à la ligne de commande

Au lieu d'utiliser [WAVE](https://wave.webaim.org/), qui ne produit pas de rapport exploitable, je me suis tourné vers [Axe DevTools](https://www.deque.com/axe/devtools/), dont le core est ouvert et qui produit un rapport en [JSON](). De plus, il est possible de l'exécuter à la ligne de commande. Il utilise alors Selenium, un outil pour contrôler un navigateur par programmation.

Voici [une présentation](https://marcysutton.github.io/a11y-and-ci/#/30) qui explique le tout.

J'ai écrit ce script pour l'exécuter afin de simplifier les choses.

## Notes

Il y a 2 erreurs que j'ai rencontré avant de pouvoir le faire fonctionner :

- Your Firefox profile cannot be loaded
- DevToolsActivePort file doesn't exist while trying to initiate Chrome Browser


Selenium a un problème avec les dernières versions des navigateurs. Il semble que Selenium ait besoin d'un répertoire pour écrire sur le disque. La [solution](https://github.com/mozilla/geckodriver/releases) est donc de créer un répertoire temporaire et de lui dire de l'utiliser. D'où le

`TMPDIR=$HOME/tmp`

avant de lancer la commande.

