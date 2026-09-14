# Suivi J1 — Cap Web

Note ton avancée après chaque TP. Reste factuel, sans données personnelles. Ce fichier te sert pour la capsule et le bilan.

## TP00 — Diagnostic

- Hypothèse : je pensais que le problème principal serait la largeur.
- Action : corrigé le HTML (labels, bouton, main, titres), le CSS (largeurs, border-box) et les deux fonctions JS.
- Résultat : page OK en double-clic, étiquettes cliquables, tout marche au clavier, plus de débordement à 360 px.
- Point non compris : la différence title/h1, le placement de main, la spécificité CSS. Je débute en JS.

## TP01 — Démarrer

- Hypothèse : sans JS, la ligne de statut resterait vide.
- Action : `cd atelier` puis `npm start`, ouvert http://127.0.0.1:3000, repéré main, h1 et p#status dans index.html.
- Résultat : page affichée, le statut vient bien du JS. Hypothèse confirmée.
- Point non compris : rien de bloquant.

## TP02 — HTML

- Hypothèse : remplacer main par div ne changerait rien à l'écran, mais les lecteurs d'écran ne trouveraient plus le contenu principal.
- Action : ajouté header (avec le h1 déplacé dedans), section Discussion avec ul#messages, footer avec span#version.
- Résultat : page OK, titre Discussion et version en attente visibles, status conservé.
- Point non compris : les attributs aria (labelledby, live), à revoir.

## TP03 — Formulaire

- Hypothèse : je pensais qu'Entrée enverrait le formulaire, comme dans une barre de recherche.
- Action : ajouté le formulaire (label, textarea 280 max, bouton Envoyer), recopié le JS fourni dans app.js.
- Résultat : Entrée fait un retour à la ligne, il faut Tab puis Entrée sur le bouton pour envoyer (le statut s'affiche). Le footer montre « version dev » dès le chargement, sans clic.
- Point non compris : comment marchent les .then. Compris : le fetch part au chargement, le submit se déclenche à l'envoi.

## TP04 — Responsive

- Hypothèse : un mot de 60 lettres va dépasser de la boîte et créer un défilement horizontal.
- Action : box-sizing et largeurs souples comme au diagnostic, formulaire en colonne avec Flexbox, focus visible, césure des mots longs. Testé avec un li temporaire puis retiré.
- Résultat : rien ne déborde à 360 ni à 1280, le focus se voit au Tab.
- Point non compris, test 360 / 1280 : compris que zoomer n'est pas un vrai test de largeur, il faut le mode responsive à 360 px.

## Commandes essayées

Note chaque commande avec son dossier de lancement et son résultat exact. Exemple d'état local, depuis la racine étudiante :

```sh
# depuis RACINE_ETUDIANT
git status
git diff
```

Mes essais :

- Dossier : `atelier`
- Commande et résultat : `npm start` → « Cap Web prêt sur http://127.0.0.1:3000/ »
- Problème exact si blocage : aucun.

Si Node ou Git bloque, note le message exact et continue en local sans attendre. Le double-clic sur `diagnostic/index.html` ne remplace pas le serveur pour les modules et l'envoi du TP03.

## Auto-revue finale

- Ce qui s'affiche bien : header, discussion, formulaire et footer avec la version ; page correcte à 360 et 1280 px.
- Ce qui reste fragile au clavier ou à 360 px : rien de cassé constaté, mais le parcours clavier est à re-vérifier après chaque changement.
- Ce que je veux revoir en capsule : la spécificité CSS, Flexbox et les .then du fetch.

## Rappel Git prudent

Git reste optionnel le matin. Vérifie l'état local, ne valide que des fichiers nommés un par un et seulement si Git est configuré. Reste en local ou en ZIP sauf si le formateur précise le circuit avec fork personnel. Aucune invitation ni demande de fusion requise le matin.

## Liens

- [README](README.md)
- [TP00](tp/00-diagnostic.md)
- [TP05](tp/05-bilan.md)
- [Aide-mémoire](ressources/aide-memoire.md)
