🤖 Le robot qui se perd
Une petite page web qui montre comment on fait tourner un robot en rond.
Chaque partie est courte. Tu peux t'arrêter après chacune. Chaque partie finie = ⭐
⭐ 1. L'idée
Un robot copie les textes des sites web pour entraîner une IA.
Ici, on lui tend un piège :
   🤖  →  page 1  →  page 4  →  page 13  →  ...
                                              sans fin
Il lit des pages fausses.
Chaque page l'envoie vers d'autres fausses pages.
Il ne sort jamais.
Tout ce qu'il copie ne sert à rien.

⭐ 2. Comment l'ouvrir
Télécharge le fichier index.html.
Fais un double-clic dessus.
Appuie sur « Lancer le robot ».
Pas besoin d'internet. Pas besoin d'installer quoi que ce soit.

⭐ 3. Les 3 morceaux du fichier
Tout est dans un seul fichier. Pense à une maison :
  🧱 HTML        →  les murs         (ce qu'il y a sur la page)
  🎨 CSS         →  la peinture      (comment c'est joli)
  🧠 JavaScript  →  l'électricité    (ce qui bouge)
Tu n'as pas besoin de tout comprendre. Regarde juste à quoi sert chaque morceau.

⭐ 4. 🧱 HTML : ce qu'on voit
Voici la page, de haut en bas :
┌───────────────────────────────┐
│  Le robot qui se perd         │  ← le titre
├───────────────────────────────┤
│  🤖  [Lancer]  [Recommencer]  │  ← le robot et 2 boutons
├───────────────────────────────┤
│  pages lues | mots copiés | 0 │  ← 3 compteurs
├───────────────────────────────┤
│  Ce que le robot lit          │  ← les fausses pages
├───────────────────────────────┤
│  Que se passe-t-il ?          │  ← l'explication
└───────────────────────────────┘
À retenir : certains éléments ont un nom (un id).
C'est comme une étiquette : le JavaScript s'en sert pour retrouver l'élément et le changer.

⭐ 5. 🎨 CSS : l'apparence
Trois idées seulement :
Gros boutons, grand texte : facile à toucher avec un doigt sur une tablette.
Mode sombre automatique : si ta tablette est en mode sombre, la page l'est aussi.
Le robot se secoue quand il travaille. 🤖

⭐ 6. 🧠 JavaScript : ce que fait le cerveau
On y va en 6 petites étapes.
Étape 1 : les mots
Trois listes de mots : des sujets, des verbes, des compléments.
On prend un mot de chaque liste pour faire une phrase absurde :
 "Le nuage carré"  +  "mange"  +  "la soupe du jeudi"
Étape 2 : le hasard
Un hasard normal change à chaque fois.
Ici, la page n°42 est toujours la même. On l'a prévu exprès.
Étape 3 : fabriquer une fausse page
On donne un numéro à une page. Elle te rend :
2 phrases absurdes ;
3 liens vers d'autres pages.
La règle des liens est simple : numéro × 3, puis +1, +2, +3.
  page 1   →  pages 4, 5, 6
  page 4   →  pages 13, 14, 15
  page 13  →  pages 40, 41, 42
  ... et ça continue sans fin
Il y a toujours une page suivante. Il n'y a jamais de dernière page.
Étape 4 : la mémoire du robot
Le robot retient 3 choses :
Il retient
Exemple
La page où il est
page 13
Combien de pages il a lues
5
Combien de mots il a copiés
62
Étape 5 : une visite
À chaque visite, le robot fait 5 choses :
  1. 📄  Il fabrique la page
  2. 🔢  Il compte : +1 page, + les mots
  3. 🖥️  Il l'affiche en haut de la liste
  4. 🧹  Il garde seulement les 12 dernières
  5. 🎲  Il choisit 1 des 3 liens et y va
Étape 6 : les boutons
Lancer : le robot fait une visite toutes les 0,8 seconde.
Arrêter : il s'arrête. (C'est le même bouton.)
Recommencer : tout revient à 0.

⭐ 7. Le trajet du robot
   Tu appuies sur « Lancer »
             │
             ▼
   ┌─────────────────────┐
   │ Le robot lit une    │◄────────┐
   │ fausse page         │         │
   └─────────┬───────────┘         │
             ▼                     │
   Il copie les mots               │
             ▼                     │
   Il choisit un des 3 liens ──────┘

   Pages utiles trouvées : toujours 0
   
⭐ 8. Petit glossaire

<img width="797" height="363" alt="image" src="https://github.com/user-attachments/assets/91be9b6b-6810-4ff4-a8dd-ea02fb9af645" />

⭐ 9. À toi d'essayer
Change une seule chose, enregistre, puis recharge la page.
🟢 Facile : change un mot dans les listes de l'étape 1.
🟡 Moyen : remplace 800 par 300. Le robot va plus vite !
🔴 Un peu plus dur : change la couleur --accent au début du fichier.
Si quelque chose ne marche plus, annule ton dernier changement.

⚠️ À savoir
C'est une démonstration simplifiée.
Un vrai piège est placé sur un vrai site, et les visiteurs humains ne le voient pas.
Certains robots savent aussi éviter ce genre de piège.
