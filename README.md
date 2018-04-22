Avant de commencer peut-être est-ce mieux de vous renseigner sur [Markdown](https://fr.wikipedia.org/wiki/Markdown) :).  
Et aussi d'aller voir ici ce sera peut-être plus joli : https://github.com/philippart-s/devoxx-2018  
ou alors de lire directement la matrice en lisant ci-dessous ;)

# Devoxx 2018
 - c'est quoi : une conférence par des développeurs pour des développeurs
 - c'est où : à Paris

# Le programme du jour 1
 - Le data streaming.
 - Etre un architecte logiciel en 2018.
 - Migrer à Boot 2.

## Le data streaming
Le data streaming c'est cool, avec la programmation réactive c'est encore plus cool.
A méditer en ces jours de création de nouvelle plateforme batch java réactif, il est clair que tous les patterns ne seront pas couverts avec une seule approche (SpringBatch par exemple). Le data streaming doit être développé avec la bonne techno pour ne pas avoir l'effet inverse de ce qu'il peut apporter et la programmation réactive semble être intéressante à au moins étudier ...

Attention aussi à la magie des containers, à la fin ça tourne sur une machine qui mutualise ses ressources :).
Enfin [Vert.x](https://vertx.io/) semble de plus en plus mûre et est une solution à regarder de prêt même si Spring n'a pas dit son dernier mot dans la programmation réactive.

## Etre architecte en 2018
Conférence assez étrange, ça trollait plus que dans le bureau (je ne savais pas que c'était possible ...).
J'ai bien aimé le fait de présenter le rôle de l'architecte applicatif comme étant l'architecte d'une application avant tout et donc étant plus un rôle dans une équipe de développement qu'une personne transverse à plusieurs équipes dans sa grande tour. Cela n'empêche pas d'avoir une architecture applicative d'entreprise définissant les grands standards :).
L'architecte logiciel peut aussi être un rôle au sein du projet pour une application mais il est plus simple et quasiment obligatoire d'avoir un ou des choix d'entreprise pour les technologies afin de garantir que la connaissance ne se perd pas dans une multiplication de choix technologiques (maintenance, exploitabilité, ...).
Ensuite l'importance des contrats des services et de l'urbanisation du SI, une fois qu'un service est appelé c'est considéré comme immutable et il faut accepter qu'il fait partie du patrimoine et le faire évoluer sans jamais rien casser (on ajoute on ne supprime pas).

Enfin j'ai bien aimé ces deux dernières choses :
 - **"Un architecte est éphémère mais les architectures perdurent."**
 - **Architecture Decision Record (ADR)** : pourquoi j'ai pris ma décision, dans quelles conditions, quelles conséquences. (titre, contexte, décisions, statuts, conséquences). Cette doc très simple doit faire une page et doit faire partie du projet et le suivre dans sa vie ... On n'aurait pas l'outil idéal ? (spoilers : github & Markdown).

## Migrer à Boot 2
Alors là la bonne nouvelle c'est qu'il y a des docs qui expliquent ça chez Spring, la mauvaise c'est que cela ne se fait pas sans douleurs et que c'est quasiment obligatoire car la dépréciassion de Boot 1 va très vite arriver.
Ce qu'il faut retenir c'est que cette migration casse énormément de choses sur actuator et les métriques (amis DPI si vous m'entendez :)).
Enfin et rien que pour pourvoir utiliser Spring Reactive et Flux ça vaut le coup de migrer :D.

## Conclusion du jour 1
Les gros sujets qui reviennent en boucle :
 - Boot (on a bien fait de choisir ça :)),
 - Programmation réactive : on fait bien fait de vouloir y aller pour le streaming :),
 - Les micros services : on a bien fait de commencer à étudier ça :),
 - le angular bashing au profit de react ... euh

Sinon je vous ai déjà parlé du découpage en pizzas teams et partage d'environnement de travail pour une équipe ayant tous les profils (dev -> prod) ?
Il y a clairement des vrais retours positifs (humain **ET** business) et ne pas y aller semble être le meilleur moyen d'échouer dans les futurs projets et la garantie de ne pas être en capacité de suivre les évolutions techniques. Par contre il faut s'en donner les moyens, l'agilité n'est pas **magique** (PO, SM, coach agile, ...) et nécessite de vrais investimments humains et matériels (faire un kanban dans un bureau et parler de sprints ne transforme pas un projet en agile).

# Le programme du jour 2
 - keynotes
 - devops as service
 - spring Reactive

## keynotes
Très intéressantes avec notamment le modèle de l'Estonie qui a dû tout inventer son système administratif en 30 ans et a fait le choix du tout numérique. On verra que la France essaie aussi de se lancer dans l'aventure mais ça c'est plutôt en jour 3 ;).
Ensuite une keynote avec un "vrai" architecte, comprenez par-là issu de l'immobilier où on apprends que le secteur de l'immobilier n'a pas forcément sût faire sa révolution numérique mais qu'il s'y attelle et qu'en plus cela peut bénéficier au bien-être au travail en aménageant des espaces de travail "intelligents" (un exemple parmi tant d'autres : une salle de réunion se libère si au bout de 20 mins elle constate qu'il n'y a personne grâce à des capteurs, cela ferait fureur chez nous non ? ;)).

## DevOps as service
Je veux ça !!! :)  
Beaucoup d'éléments que j'ai déjà abordé mais l'idée ici est d'apporter plus vite de la valeur au business, d'être capable plus vite de faire machine arrière ou changer des fonctionnalités en production.

Et comme toujours c'est avant tout un changement de conception des choses avec comme point central une équipe multi-profils qui a un but commun : délivrer de la plus-value plus vite et de meilleure qualité.

Cela permet aussi d'améliore la satisfaction des développeurs avec une vision plus rapide de ce qui est mis en place en production sans avoir l'impression de coder pendant des mois sans voir ce que cela donne "en vrai" (le bien-être au travail ... ;)).

Une autre chose que j'ai trouvé intéressant est que plutôt que de mettre en place une documentation figée et qui peine à évoluer dans le temps privilégier une zone d'échanges avec questions / réponses à la stack overflow (je pense que le site a prouvé son utilité et son bon fonctionnement :)),
Dans le même esprit : proposer de fonctionner en interne comme le font les projets open source : lorsqu'une équipe développe quelque chose qui pourrait servir à d'autres (par exemple un logger) externaliser ce projet dans un repo git et le proposer en utilisation comme un projet open source (issues, participation au développement, ...).

En résumé :
 - commencer petit et penser gros
 - sélectionner quelques projets représentatifs de ce que fait l'Entreprise
  - choisir le critère à améliorer (1 seul) : coût, vélocité, qualité
  - trouver des témoins positifs
  - avoir des objectifs mesurables
 - fournir des templates standards et laisse-les customiser
 - ne pas oublier la mesurabilité des plateformes
 - faciliter la communication

## Reactive Spring
Ah une conf en anglais de bon matin ... sur un sujet pas évident : un bon mal de crâne en perspective.
Et j'avais raison !  
Mais honnêtement ça valait le coup car c'est quelque chose à surveiller de très près et on sent que la programmation réactive avec la programmation fonctionnelle sont deux mouvements qui vont clairement faire évoluer la façon dont nous développons nos applications.
Le ticket d'entrée est certes élevé (qui a dit que j'étais trop vieux pour ces conneries ?) mais il apporte de vraies nouvelles façons d'aborder les problèmes.

## Conclusion du jour 2
Journée moins instance que la première avec des sujets plus techniques mais pas moins intéressants qui confirment encore plus le mouvement de fond de l'agilité mais aussi du devops et de la nécessité d'industrialiser les étapes de construction et de déploiement des applications tout en laissant de l'autonomie aux équipes de développement.

# Jour 3
## Programme du jour 3
 - keynotes
 - du monolythe spaghetti aux microsservices
 - open api
 - le développeur repend le digital en main

## keynotes
Des keynotes très variées et très intéressantes. J'en retiendrai deux :
 - la french road qui se veut une réponse à ce que nous avons vu au jour 2 avec le tout numérique estonien. Plus qu'une réponse d'ailleurs c'est plus un inspiration du modèle estonien et ils ne s'en cachent pas. Le coup de la carte unique et sécurisé ça donne envie de suivre de près ce sujet.
 - les ordinateurs et algorithmes quantiques : très intéressant même si je n'ai pas tout compris mais il paraît que c'est normal :).
 Remet en cause quasiment tout ce que l'on a appris à l'école et ouvre des champs d'application encore inconnus à ce jour.
 Ce qui ne trompe pas c'est que tous les grands éditeurs du marché ont une initiative autour des algos quantiques (les gars du Lab si vous m'entendez ;)).

## Open API
Le successeur de swagger, en fait swagger reste l'implémentation et open API les spécifications.
Cela fait quelque temps que je m'intéresse à cette API et je pense que l'on peut clairement y gagner pour construire notre référentiel de services, alors certes c'est très orienté REST mais cela nous aiderai grandement à commencer à avoir une approche contrat first.

Encore une chose à étudier de près ...

## Du monolithe spaghetti aux micros services
Une conférence un peu fouillis où j'ai peiné à ressortir clairement des points.  
Ce que j'ai pu retenir de ce REX c'est qu'une application monolithe n'est pas forcément mal au moment où elle est faite (tehno, business, ...), c'est ne rien faire ensuite qui est mal. Malgré cela, le découpage en micros services n'est pas aisé et il n'existe pas de recette magique, même si l'approche [DDD](https://en.wikipedia.org/wiki/Domain-driven_design) semble aider dans cette démarche.

Il faut aussi s'outiller, l'apparition de centaines de services ne peut se faire si on fait tout à la main. A titre d'exemple l'équipe en charge de la CI est passée de 1 personne à 8 en trois ans.

## Le développeur repend le digital en main
**Le digital c'est tout ce qui est en rapport avec les doigts ...** :D ... Parlons plutôt de révolution **numérique**.

Une conférence qui fait du bien là où ça fait mal : l'estime de soi en tant que développeur.
Le développeur est la valeur ajoutée dorénavant dans un monde du logiciel libre et gratuit il faut donc qu'une telle valeur soit au centre des préoccupations.
Il faut aussi tout faire pour qu'un développeur puisse travailler dans les meilleurs conditions et sans lui faire changer de contexte constamment, le temps perdu à de telles choses est au final de l'argent de perdu car ce sont les applications qui sont créées moins vite. Un développeur qui utilise les bons outils est aussi bien plus performant et le surcoût associé (souvent faible) est amorti par la productivité augmentée (on passe quand sous linux ? :p).

La révolution numérique (et non digitale) doit venir de l'IT et des développeurs ce sont eux qui ont la connaissance technique et qui peuvent apporter de la plus-value mais cela signifie aussi que juste faire le job ne suffit pas il faut le faire en se dépassant : *"A grands pouvoirs grandes responsabilités !"*.
La révolution numérique (et non digitale souvenez-vous) ce n'est pas juste sortir une web app et une application mobile c'est inventer un nouveau business grâce à la technologie.

Enfin il faut maximiser la valeur client et non maximiser des indicateurs projets qui ne signifient rien, apporter très vite de la valeur en production est un réel plus (qui a dit agile et devops ?).

# Conclusion sur ce Devoxx 2018
Ces trois jours de conférence sont toujours aussi intense (un peu le soir aussi ;)) et toujours aussi passionnant tant sur les aspects techniques qu'organisationnels.  
Il est essentiel d'y aller que l'on soit développeur, chef de projet ou même manageur, peut-être pas les trois jours mais il y a forcément à prendre dans tout ce qui présenté.  
Cela donne vraiment envie de faire bouger les choses, la réalité nous rattrape un peu lorsque l'on revient en se disant que cela ne va pas être si simple mais soyons optimistes, comme on nous l'a souvent répété le métier de développeur n'est plus à considérer comme étant négatif mais bien au contraire.

En résumé sur ces trois jours :
 - l'agilité c'est bien mais il faut pouvoir le faire dans de bonnes conditions matérielles (espaces dédiés, ...) et humaines (équipe dédiée, PO, SM, ...) et ne pas aller jusqu'au devops lorsque l'on veut gérer un projet en utilisant une approche agile c'est se priver de tout un pan de cette philosophie !
 - le métier de développeur c'est cool il ne faut plus en avoir honte, bien au contraire il faut le mettre en avant mais aussi proposer des innovations c'est notre rôle. On ne peut plus se contenter de "juste faire le travail" on a un devoir de pousser notre entreprise vers sa révolution numérique
 - enfin d'un point de vue technique et développement le choix de Spring Boot (aka Boot) est clairement une bonne chose car c'est une vraie lame de fond qui emporte tout sur son passage et notamment notre bon vieux JEE. La programmation réactive arrive aussi en force et il va falloir s'y préparer si on veut profiter des possibilités qu'elle apporte en termes de performances et de réactivité. On peut aussi constater que certaines technos semblent arriver à leur âge de maturité, comme Docker par exemple qui semble être maintenant une évidence !

 A l'année prochaine :).

 Si il y a des erreurs n'hésitez pas à faire une Issue ou une Pull Request ;)
