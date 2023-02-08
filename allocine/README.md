# README

2.1. Exo 1 : Allociné

creer un movie de mon choix avec une save compris :
- Movie.create(name: "INTERSTELLAR", year: 2014, genre: "Science fiction, Drama", synopsys:"Le film raconte les aventures d’un groupe d’explorateurs qui utilisent une faille récemment découverte dans l’espace-temps afin de repousser les limites humaines et partir à la conquête des distances astronomiques dans un voyage interstellaire. ", director : "Christopher nolan", allocine_rating: 4.5, my_rating: 5.0, already_seen: true )

Modifie la note Allociné de Beowulf pour qu'elle soit à 4,7. Ce chef-d’œuvre mérite d'être reconnu comme tel.
- Movie.find_by(name: Beowulf).update(allocine_rating: 4.7)

Modifie le genre de l'Exorciste pour que ça soit une comédie. Avec un peu de chance ta petite soeur va tomber dessus.
- Movie.where(name: "L'EXORCISTE").update(genre: "Comedie")

Affiche, avec une commande en Movie.where, l'ensemble des films que tu as déjà vus.
- Movie.where(already_seen: true)

À partir de cet array de films que tu as déjà vus, supprime le premier de ta BDD
- Movie.where(already_seen: true).delete