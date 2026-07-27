# Suivi des pré-audits ultraA11y

Documents de suivi de la démarche décrite dans [`../methodo-pre-audit-rgaa.html`](../methodo-pre-audit-rgaa.html).
Format CSV + Markdown : versionnable dans git, comparable d'une version à l'autre, remplissable par l'IA. Les CSV s'ouvrent dans Excel, LibreOffice ou Grist.

## Les fichiers

| Fichier | C'est quoi | Quand le remplir |
|---|---|---|
| `erreurs-reference.csv` | La liste des vraies erreurs, validée par l'experte. La référence contre laquelle chaque pré-audit est comparé. | Étape A2 (mise en place), puis enrichie en session hebdo |
| `criteres-couverts.md` | Les critères RGAA qu'ultraA11y prétend vérifier | Étape A3, revu quand l'outil évolue |
| `journal-iterations.csv` | Une ligne par version de l'outil : le changement, les 4 chiffres, la décision | Étape B5, à chaque itération |
| `pre-audits/` | Un compte rendu par pré-audit (copier `TEMPLATE-pre-audit.md`) | Étapes B2 à B4, à chaque passage |

## Le cycle en bref

1. Une modification de l'outil, une seule, taguée dans git.
2. Lancer ultraA11y sur les pages de test figées (2 à 3 passages).
3. Copier `pre-audits/TEMPLATE-pre-audit.md` → `pre-audits/2026-07-28_v0.5.md` et le remplir en comparant à `erreurs-reference.csv`.
4. Reporter les 4 chiffres dans `journal-iterations.csv` avec la décision (gardé / annulé).
5. Les désaccords notés dans le compte rendu partent en arbitrage à la session hebdo avec l'experte.

## Les 4 chiffres

- **Précision** : % d'erreurs réelles parmi les erreurs remontées.
- **Hallucinations** : nombre d'erreurs portant sur des éléments qui n'existent pas dans la page.
- **Fausses alertes** : nombre d'erreurs remontées qui n'en sont pas (l'élément existe mais est conforme).
- **Erreurs manquées** : nombre d'erreurs de la liste de l'experte que l'IA n'a pas vues.

Les nombres bruts ne sont comparables que si le jeu de pages de test ne change pas. Si on ajoute des pages, le noter dans le journal : c'est un nouveau point de départ.
