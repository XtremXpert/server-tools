# Portage en 20.0

Ce module est le port officiel proposé par la communauté dans
[OCA/server-tools#3771](https://github.com/OCA/server-tools/pull/3771), branche
`20.0-mig-auditlog` du dépôt `DynAppsNV/server-tools`, commit `5c998f43`.

Il est repris ici **tel quel** pour que `maison` puisse l'épingler sur un dépôt
que nous contrôlons, en attendant la fusion de la PR amont. À la fusion, la
source d'`addons.lock` repassera sur `OCA/server-tools`.

Vérifié le 2026-11-09 sur la base `maison_staging` : **80 tests, 0 erreur**.

## Ce que le passage en 20.0 change

- `security/ir.model.access.csv` → `security/ir.access.csv` : le modèle ACL
  s'appelle désormais `ir.access` ;
- le format du CSV change : plus de colonnes `perm_*`, mais une colonne
  `operation` portant un sous-ensemble de `crud` ;
- `model_id` porte le **nom technique** du modèle, plus un xmlid.

## Ne pas modifier ici

Tant que la PR amont est ouverte, toute correction doit lui être proposée
d'abord. Ce dépôt ne fait que l'héberger.
