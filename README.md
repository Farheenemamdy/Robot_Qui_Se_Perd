# Robot_Qui_Se_Perd
🤖 Le robot qui se perd
Une petite démonstration pour comprendre comment on piège un robot qui copie les sites web afin d'entraîner une IA.
Créée avec l'aide de Claude (une IA). Ce fichier t'explique le code, un petit morceau à la fois.

1. L'idée en 3 phrases
Un robot visite un site et copie tous les textes qu'il trouve.
Ici, chaque page contient des liens vers d'autres fausses pages.
Le robot ne sort jamais du piège, et tout ce qu'il copie est sans valeur.

3. Comment l'ouvrir
Télécharge le fichier index.html.
Fais un double-clic dessus : il s'ouvre dans ton navigateur.
Appuie sur « Lancer le robot ».
C'est tout. Pas d'installation, pas d'internet nécessaire.

5. Le fichier en 3 morceaux
Tout est dans un seul fichier, index.html. Il contient 3 parties :
┌─────────────────────────────────────────┐
│  index.html                             │
│                                         │
│  🧱 HTML  →  le squelette (ce qu'il y a)│
│  🎨 CSS   →  les habits (à quoi ça      │
│              ressemble)                 │
│  🧠 JS    →  le cerveau (ce que ça fait)│
└─────────────────────────────────────────┘
Une maison : le HTML = les murs, le CSS = la peinture, le JavaScript = l'électricité.

7. 🧱 HTML : ce qu'il y a sur la page
Cinq blocs, de haut en bas :
Bloc
Ce que c'est
Titre
« Le robot qui se perd »
Commandes
Le robot 🤖, son message, et 2 boutons
Compteurs
3 cases : pages lues, mots copiés, pages utiles
« Ce que le robot lit »
La liste des fausses pages
« Que se passe-t-il ? »
L'explication pour le public
Chaque élément important a un nom (un id), par exemple id="n-pages".
Ce nom permet au JavaScript de le retrouver pour le modifier.

9. 🎨 CSS : à quoi ça ressemble
Quatre idées à retenir :
Les couleurs sont écrites une seule fois au début (--accent, --texte…), puis réutilisées partout. Pour changer une couleur, on change une seule ligne.
Le texte est grand et les boutons sont gros (52 pixels de haut) : c'est fait pour être touché avec un doigt sur une tablette.
Le mode sombre est automatique : si ta tablette est en mode sombre, la page change de couleurs toute seule.
Le robot bouge quand il travaille (secoue). Si quelqu'un a désactivé les animations sur son appareil, le robot reste immobile.

11. 🧠 JavaScript : ce que ça fait, étape par étape
Étape 1 : les mots pour fabriquer de fausses pages
const sujets = ["Le nuage carré", "La lune bleue", ...];
const verbes = ["mange", "chante pour", ...];
const complements = ["la soupe du jeudi", ...];
Trois listes de mots. On en prend un de chaque pour fabriquer une phrase absurde :
« Le nuage carré mange la soupe du jeudi. »

Étape 2 : un hasard « à graine » (hasard)
Un hasard normal donne un résultat différent à chaque fois.
Ici, on veut que la page n°42 soit toujours la même.
On donne donc au hasard un numéro de départ (la « graine ») : même numéro, même résultat.

Étape 3 : fabriquer une fausse page (fabriquerPage)
Tu lui donnes un numéro, elle te rend :
2 phrases absurdes ;
3 liens vers d'autres pages : numéro × 3 + 1, + 2 et + 3.
page 1  →  pages 4, 5, 6
page 4  →  pages 13, 14, 15
page 13 →  pages 40, 41, 42
         ... et ainsi de suite, sans fin
Comme il y a toujours 3 pages suivantes, il n'y a jamais de dernière page.

Étape 4 : la mémoire du robot
let numeroActuel = 1;   // la page où il se trouve
let pagesLues = 0;      // combien de pages il a lues
let motsCopies = 0;     // combien de mots il a copiés
let minuteur = null;    // sert à répéter l'action
Quatre petites cases où le robot garde ce qu'il sait.
let veut dire : « cette case peut changer ».

Étape 5 : une visite (visiter)
À chaque visite, le robot fait 5 choses :
1. 📄 Il fabrique la page où il se trouve
2. 🔢 Il compte : +1 page, + les mots copiés
3. 🖥️ Il affiche la page en haut de la liste
4. 🧹 Il garde seulement les 12 dernières pages à l'écran
5. 🎲 Il choisit un des 3 liens au hasard et y va

Étape 6 : lancer et arrêter (lancer, arreter)
lancer : demande à l'ordinateur de répéter visiter toutes les 0,8 seconde (setInterval(visiter, 800)).
arreter : arrête cette répétition (clearInterval).
Le même bouton fait les deux : s'il est arrêté, il lance ; s'il tourne, il arrête.

Étape 7 : le bouton « Recommencer »
Il arrête le robot, remet tous les compteurs à 0 et vide la liste.
7. Le trajet complet
   Clic sur « Lancer le robot »
              │
              ▼
   ┌──────────────────────┐
   │  Le robot visite     │◄──────────┐
   │  une fausse page     │           │
   └──────────┬───────────┘           │
              ▼                       │
   Il copie les mots, +1 sur          │
   les compteurs                      │
              ▼                       │
   Il choisit un des 3 liens ─────────┘
   (toutes les 0,8 seconde)

   Pages utiles trouvées : toujours 0
   
8. Petit glossaire

<img width="798" height="408" alt="image" src="https://github.com/user-attachments/assets/1270c20f-e732-4304-9c19-03e9da33427e" />


10. À toi d'essayer
Change une seule chose à la fois, enregistre, puis recharge la page :
Les mots : remplace un mot dans les listes de l'étape 1.
La vitesse : remplace 800 par 300 (plus rapide) ou 2000 (plus lent).
Les couleurs : change --accent au début du CSS.
Si quelque chose casse, annule ton dernier changement.

⚠️ À savoir
C'est une démonstration simplifiée. Un vrai piège se place sur un vrai site web, et les visiteurs humains ne le voient pas. Certains robots savent aussi reconnaître et éviter ce genre de piège.
