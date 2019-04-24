# README

## Niveau facile

* Quel est le nombre total d'objets Album contenus dans la base (sans regarder les id bien sûr) ?

```347 (Album.count)```

* Qui est l'auteur de la chanson "White Room" ?

```Eric Clapton```

* Quelle chanson dure exactement 188133 milliseconds ?

```Perfect```

* Quel groupe a sorti l'album "Use Your Illusion II" ?

```Guns N Roses```

## Niveau Moyen

* Combien y a t'il d'albums dont le titre contient "Great" ? (indice)

```13 albums```

* Supprime tous les albums dont le nom contient "music".

    ```Création d'un array d'objet Album puis destroy avec t.each { |l| p l.destroy}```

* Combien y a t'il d'albums écrits par AC/DC ?
    
    ```a = Album.where(artist: 'AC/DC') puis a.count = 2```

* Combien de chanson durent exactement 158589 millisecondes ?

```0```

## Niveau Difficile

Pour ces questions, tu vas devoir effectuer des boucles dans la console Rails. C'est peu commun mais c'est faisable, tout comme dans IRB.

* puts en console tous les titres de AC/DC.

```
titres = Track.where(artist: 'AC/DC') puis titres.each { |t| puts t.title}
```

* puts en console tous les titres de l'album "Let There Be Rock".

```titi = Track.where(album: 'Let There Be Rock') puis titi.each { |k| puts k.title}```
    
* Calcule le prix total de cet album ainsi que sa durée totale.

    ```titi.sum('price') donne $7.92``` 

* Calcule le coût de l'intégralité de la discographie de "Deep Purple".
    
```Track.where(artist: 'Deep Purple').sum('price') donne $90.09 ```

* Modifie (via une boucle) tous les titres de "Eric Clapton" afin qu'ils soient affichés avec "Britney Spears" en artist.

