# Watch List 🎬

Une petite application web pour créer ses **listes de films** (« Classiques », « Films de Noël », « À voir ce week-end »…) et y ranger des films avec un commentaire.

> Exercice réalisé pendant le bootcamp **Le Wagon** (AI Software Development), en août 2026.

## Ce que fait l'application

- Voir toutes ses listes
- Créer une nouvelle liste
- Ouvrir une liste et voir les films qu'elle contient
- Ajouter un film à une liste avec un commentaire (un *bookmark*, c'est-à-dire un marque-page)
- Retirer un film d'une liste

## Comment c'est construit

Trois modèles (les « tables » de la base de données) :

```
List  ──<  Bookmark  >──  Movie
(liste)   (marque-page    (film)
           + commentaire)
```

- Une **liste** contient plusieurs films, grâce aux marque-pages.
- Un **film** peut être dans plusieurs listes.
- Un même film ne peut pas être ajouté deux fois dans la même liste.

## Technologies

Ruby 3.4 · Ruby on Rails 8.1 · PostgreSQL · Bootstrap 5 · Simple Form

## Lancer le projet sur son ordinateur

```bash
bundle install
rails db:create db:migrate db:seed
rails server
```

Puis ouvrir http://localhost:3000/lists
