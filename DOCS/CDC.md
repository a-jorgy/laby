# Cahier des charges du projet

## Principe du jeu
- On incarne le minautor qui a pour but de s'échapper du labyrinthe
- Le labyrinthe est composé de X étages
- On peut jouer en multijoueur (on voit la progression du nombre d'étages de chacun)

## Mécaniques de jeu
- Le minautor a une grande force physique : il peut déplacer des roucher, casser des murs fragiles, etc
- Il a peur du feu et des objets dont il n'a pas l'habitude (torches, carte, ...)
- Pour contrer un de ces objets, il a besoin de trouver un objet lui permettant de les annuler (ex : baguette de vent pour stopper une torche)
- On a un brouillard (que les torches annulent dans un rayon de X blocs)
- Le minautor a une barre d'énergie : déplacer des rochers, courir, etc lui consomment de l'énergie, qui se regénère doucement. Si il trouve un humain, il peut le manger pour se regénerer plus vite son énergie
- Les humains sont limités et ont des movements aléatoires mais pas incohérents (ne pas aller dans un mur ou vers le minautor)
- Les fantomes se balladent aléatoirement dans le labyrinthe. Ils peuvent traverser les murs. Le minautor et les humains ont peur d'eux
- Y'a un chrono (pas de temps limite, le minautor a tout son temps :) )
- Certaines dalles sont cassés (peu reconnaissable) => si on marche dessus, on tombe à l'étage en dessous
- A voir si algos pour générer laby alétoirement (commun à tous les joueurs)
- Pas de barre d'énergie : effets de particules et/ou cornes du minautor en fonction de son niveau d'énergie lors de l'effort
- Si plus d'énergie : peut plus faire d'action utilisant l'énergie, tombe dans les pommes 3s et champ de vision réduit pendant 6s

## HMI
- Launcher avec menu
- Cam qui suit le joueur
- Chrono visible
- Labyrinthe
- Particules lors de l'effort

## Bonne pratiques lors du codage
- Faire des constantes/variables globales (ex : vision de X bloc, ...)
- Commenter !!
- ;
- Nom de classe/variable en xxXxxx : pas de tirets
- utiliser des interfaces

## Images nécessaires
- Minautor (4X3 images pour les 4 positions et le déplacement : arrêt, pied gauche, pied droit)
- Fantomes
- humains
- objets (torches allumé, torche éteinte, carte, baguette de vent, ...)
- murs
- murs fragiles
- sol
- sol fragile
- rochers
- echelles (vers le haut, vers le bas)
- particules d'efforts
- brouillard
- Barre de progression pour les étages
- Logo du jeu :)

## Truc plus techniques
- Fichier de configuration (a quoi ressmeble le laby, ou sont les humains, etc) en JSON
- Langage de programmation en Java
- 1 serveur et X clients
- Communication via WebSockets ?

{
    labyrinthe : [
        [0,1,1,1],
        [fslkdsf]
    ],
    objets : [
        { id : fdfd
            x : 
            y },
            {
                fdsfsd
            }]
}
