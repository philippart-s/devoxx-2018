Avant de commencer peut être est-ce mieux de vous renseigner sur [Markdown](https://fr.wikipedia.org/wiki/Markdown) :).  
Et aussi d'aller voir ici ce sera peut être plus joli : https://github.com/philippart-s/devoxx-2018  
Enfin de lire directement la matrice en lisant ci-dessous ;)

# Devoxx 2018
 - c'est quoi : une conférence par des développeurs pour des développeurs
 - c'est où : à Paris

# Le programme du jour 1
 - Le data streaming.
 - Etre un architecte logiciel en 2018.
 - Moigrer à Boot 2.
 - Java et Docker.

# Le data streaming
Le data streaming c'est cool, avec la programmation réactive c'est encore plus cool.
A méditer en ces jours de création de nouvelle plateforme batch java réactif afin de ne peut être pas tout faire avec une seule approche (SpringBatch par exemple) mais choisir la bonne solution à utiliser pour le data streaming et la programmation réactive semble être interressante à au moins étudier ...

Attention aussi à la magie des containers, à la fin ça tourne sur une machine qui mutualise ses ressources :).
Enfin Vert.x semble de plus en plus mûre et est une solution à regarder de prêt même si Spring n'a pas dit son dernier mot dans la programmation réactive.

# Etre architecte en 2018
Conférence assez étrange, ça trollait plus que dans le bureau (je ne savais pas que c'était possible ...).
J'ai bien aimé le fait de présenter le rôle de l'architecte applicatif comme étant l'architecte d'une application avant tout et donc étant plus un rôle dans une équipe de développement qu'une personne transverse à pleins d'équipes dans sa grande tour. Cela n'empêche pas d'avoir une architecture applicative d'entreprise définissant les grands standards :).
L'architecte logiciel peut aussi être un rôle au sein du projet pour une application mais il est plus simple et quasiment obligatoire d'avoir une ligne directrice dans une grande entreprise pour le choix des technologoies afin de garantir que la connaissance ne se pert pas dans une multiplication de choix tecnologique (mainteance, exploitabilité, ...).
Ensuite l'importance des contrats et de l'urbanisation du SI, une fois qu'un service est appelé c'est considéré comme immutable et il faut accepter qu'il fait parti du patrimoine et le faire évoluer sans jamais rien casser (on ajoute on ne supprime pas).

Enfin j'ai bien aimé ces deux dernières choses :
 - **"Un architecte est éphémère mais les arhitectures perdurent."**
 - **Arhitecutre Decision Record (ADR)** : pourquoi j'ai pris ma décision, dans quel conditions, quelles conséquences. (title, contexte,decision,status, consequence). Cette doc très simple doit faire une page et doit faire partie du projet et le suivre dans sa vie ... On n'aurait pas l'outil idéal ? (spoilers : github & Markdown).

# Migrer à Boot 2
Alors là la bonne nouvelle c'est qu'il y a des docs qui expliquent ça chez Spring, la mauvaise c'est que cela ne se fait pas sans douleurs et que c'est quasiment obligatoire car la dépréciasiont de Boot 1 va très vite arriver.
Ce qu'il faut retenir c'est que cette migration casse énormément de choses sur actuator et les métriques (amis DPI si vous m'entendez :)).
Enfin et rien que pour pourvoir utiliser Spring Reactive et Flux ça vaut le coup de migrer :D.

# Conclusion du jour 1
Les gros sujets qui reviennent en boucle :
 - Boot (on a bien fait de choisir ça :)),
 - Programmation réactive : on a bien fait de vouloir y aller pour le streaming :),
 - Les micros services : on a bien fait de commencer à étudier ça :),
 - le angular bashing au profit de react ... euh

Sinon je vous ai déjà parlé du découpage en pizzas teams et partage d'environnement de travail pour une équipes ayant tous les profils (dev -> prod) ?
Il y a clairement des vrais retours postifs (humain **ET** business) et ne pas y aller semble être le meilleur moyen d'échouer dans les futurs projets et la garantie de ne pas être en capacité de suivre les évolutions techniques.
