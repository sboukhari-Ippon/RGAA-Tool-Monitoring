# Pré-audit — vX.Y — AAAA-MM-JJ

> Copier ce fichier en `AAAA-MM-JJ_vX.Y.md` avant de le remplir. Les lignes *(exemple)* montrent ce qui est attendu : les remplacer.

- **Version de l'outil** (tag ou commit git) :
- **Changement testé** (un seul) :
- **Hypothèse** (pourquoi ce changement devrait améliorer les chiffres) :
- **Pages testées** (dossier `pages-test/` du) :
- **Nombre de passages** : (2 minimum ; si les passages divergent fortement, le noter en commentaire)

## Résultats par page

Comparer chaque signalement de l'IA à `../erreurs-reference.csv` :

- **Vraies erreurs** : signalements de l'IA qui correspondent à une ligne de la liste de l'experte.
- **Fausses alertes** : l'élément existe mais il est conforme.
- **Hallucinations** : l'élément signalé n'existe pas dans la page.
- **Manquées** : erreurs de la liste de l'experte que l'IA n'a pas remontées.

Vérification : Erreurs remontées = Vraies erreurs + Fausses alertes + Hallucinations.

| Page | Erreurs remontées | Vraies erreurs | Fausses alertes | Hallucinations | Manquées |
|---|---|---|---|---|---|
| *(exemple)* declaration/index | 6 | 4 | 1 | 1 | 3 |
| | | | | | |
| **Total** | | | | | |

## Ventilation par critère RGAA

Uniquement les critères où l'IA s'est trompée (fausse alerte, hallucination ou erreur manquée).

| Critère | Vraies erreurs | Fausses alertes | Hallucinations | Manquées |
|---|---|---|---|---|
| *(exemple)* 10.7 — prise de focus visible | 1 | 0 | 0 | 2 |
| | | | | |

## Désaccords à arbitrer avec l'experte

L'IA signale une erreur absente de la liste de référence, et elle semble réelle : à trancher en session hebdo. Si l'experte confirme, la liste s'enrichit.

| Page | Critère | Signalement de l'IA | Avis de l'experte (après session) |
|---|---|---|---|
| *(exemple)* declaration/index | 8.9 | `<p class="fr-h3">` : balise utilisée à des fins de présentation | Confirmé → ajouté à la liste le 04/08 |
| | | | |

## Décision

- [ ] **Gardé** — les chiffres s'améliorent
- [ ] **Annulé** — régression, retour à la version précédente

Reporter la ligne dans `../journal-iterations.csv` (la colonne précision s'y calcule : vraies erreurs ÷ erreurs remontées, dans l'exemple 4 ÷ 6 = 67 %).

**Commentaire** (ce qu'on a appris, prochaine hypothèse) :
