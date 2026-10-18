# Déclaration d'usage de l'IA — DM1

**Nom et prénom :** AHOMLANTO Yann
**Pseudo Kaggle :** Yann AHOMLANTO
**Dépôt (lien) :** https://github.com/Loickaht/projetgit
**Rendu :** DM1 (devoir maison 1, carnets J1 et J2)
**Date :** 18 octobre 2026

---

## 1. Ce que j'ai produit moi-même

Le raisonnement sur plusieurs questions : la classification des six colonnes de la table de crédit (Q15), les parties 2, 3 et 5 de la Q1 (référence, prédicteur constant, réponse au collègue à 83 %), et les prédictions des Q7, Q8 et Q14 avant chaque mesure. J'ai exécuté le carnet, lu chaque résultat et identifié moi-même la colonne gagnante du balayage (Q2). Je n'ai écrit aucune ligne de code seul.

## 2. Ce que j'ai fait avec un assistant

| Outil utilisé | Ce qu'il a produit | Ce que j'ai vérifié moi-même |
|---|---|---|
| Claude (Anthropic) | Explications des notions du cours (référence, barre de bruit, fuite, colonne qui disparaît, arrêt anticipé, plafond des données) | J'ai relu chaque explication et répondu aux questions posées avant de passer au code |
| Claude | Tout le code des Q1, Q2, Q3, Q4, Q5, Q7, Q8, Q9, Q11, Q12, Q14 et Q15 | J'ai exécuté chaque cellule, vérifié que les contrôles passaient et lu les chiffres obtenus |
| Claude | La mise en forme des phrases (lectures, verdicts, justifications), à partir de mes réponses ou de ses explications quand je bloquais | J'ai vérifié que chaque phrase correspond aux chiffres de MON carnet |
| Claude | La correction de mes erreurs : Q1 (parties 1 et 3), Q15 (date_defaut, canal), Q7 et Q8 (lecture des écarts en barres) | J'ai compris pourquoi mes réponses initiales étaient fausses |

Deux points signalés honnêtement :
- **Q4** : j'ai oublié d'écrire mes prédictions avant la mesure. Elles ont été ajoutées après, et c'est indiqué en commentaire dans le code.
- **Q12** : un contrôle reste « À REVOIR ». Mon outil ne trouve que deux colonnes suspectes, qui sont toutes deux de vraies fuites ; je n'ai pas inventé un faux verdict pour passer le contrôle.

## 3. Ce que je ne saurais pas expliquer

<!-- Je n'ai pas encore vraiment compris comment marche le modele en detail et certaine ligne de code. Donc je ne pourrais pas defender mon code srictement ligne par ligne  -->

- Le détail du code de la fonction `suspects` (Q12) : je comprends les deux signes (le vide et la valeur), mais pas chaque ligne de `value_counts` et `isin`.
- Le calcul de la simulation de la Q11 (vider la colonne dans la validation au taux du test) ligne par ligne.
- Pourquoi l'incertitude sur un écart-type estimé avec 20 tirages vaut environ 16 % (Q5).
- Le fonctionnement interne de la forêt aléatoire et de la régression logistique (newton-cholesky).

## 4. Chiffres

- score interne mesuré : **82,51 %** (exactitude de validation, référence 81,75 %)
- score public déclaré : **non obtenu**, la soumission de `submission.csv` sur Kaggle a échoué le 18 octobre 2026. Le carnet tourne de bout en bout en « Save & Run All » (version réussie sur Kaggle).
