# Conversion du JSON à CSV

Le format JSON, celui produit par Axe DevTools, n'est pas très pratique pour manipuler les données dans un tableur comme Excel ou les importer dans un gestion de projets comme GitLab.

`json2csv` sert donc à convertir le rapport au format importable dans GitLab (`title;description`) et peut être lu dans Excel.

Pour ce faire, `json2csv` emploie [jq](https://stedolan.github.io/jq/).