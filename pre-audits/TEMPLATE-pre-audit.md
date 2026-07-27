# Pré-audit — vX.Y — AAAA-MM-JJ

> Copier ce fichier en `AAAA-MM-JJ_vX.Y.md` avant de le remplir.

- **Version de l'outil** (tag ou commit git) :
- **Changement testé** (un seul) :
- **Hypothèse** (pourquoi ce changement devrait améliorer les chiffres) :
- **Pages testées** (dossier `pages-test/` du) :
- **Nombre de passages** : (2 minimum ; si les passages divergent fortement, le noter en commentaire)

## Résultats par page

Comparer chaque signalement de l'IA à `../erreurs-reference.csv`.

| Page | Erreurs remontées | Confirmées | Fausses alertes | Hallucinations | Manquées | Précision |
|---|---|---|---|---|---|---|
| | | | | | | |
| **Total** | | | | | | |

## Ventilation par critère RGAA

Uniquement les critères où l'IA s'est trompée (fausse alerte, hallucination ou erreur manquée).

| Critère | Confirmées | Fausses alertes | Hallucinations | Manquées | Constat |
|---|---|---|---|---|---|
| | | | | | |

## Désaccords à arbitrer avec l'experte

L'IA signale une erreur absente de la liste de référence, et elle semble réelle : à trancher en session hebdo. Si l'experte confirme, la liste s'enrichit.

| Page | Critère | Signalement de l'IA | Avis de l'experte (après session) |
|---|---|---|---|
| | | | |

## Décision

- [ ] **Gardé** — les chiffres s'améliorent
- [ ] **Annulé** — régression, retour à la version précédente

Reporter la ligne dans `../journal-iterations.csv`.

**Commentaire** (ce qu'on a appris, prochaine hypothèse) :
