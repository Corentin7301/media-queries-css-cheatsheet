# Media queries cheatsheet | aide mémoire

## BREAKPOINTS

```css
@media screen and (min-width: 640px) {
	/* Small mobile */
}

@media screen and (min-width: 768px) {
	/* Mobile */
}

@media screen and (min-width: 1024px) {
	/* Tablet */
}

@media screen and (min-width: 1216px) {
	/* Desktop */
}

@media screen and (min-width: 1536px) {
	/* Large desktop */
}
```

## USAGE

### Example :

**MOBILE** (first), pas de media screen, tout ce qui ne sera pasdans un media query se comportera comme ce qui est défini sans media screen :

(EN: No media screen, anything that is not in a media query will behave like what is defined without a media screen:)

```css
#header {
    display: flex;
    background-color: red;
    color: white;
}
```

**TOUT ECRAN DE PLUS DE 1216px**, toutes les modifications faites ici seront effectives pour un écran de plus de 1216px de côté et écraseront ou s'ajouteront aux déclarations sans media screen.

(EN: **ANY SCREEN LARGER THAN 1216px**, any changes made here will be effective for a screen larger than 1216px sideways and will overwrite or be added to statements without media screen.)

```css
@media screen and (min-width: 1216px) {
    #header {
        display: none;
    }
}
```

  ### C'est à dire :

* En mobile on aura : 

(EN: In mobile we will have: )

```css
    /* display: flex; */
    /* background-color: red; */
    /* color: white; */
```

* En plus de 1216px on aura : 

(EN: In most of 1216px we will have: )

```css
    /* display: none; */
    /* background-color: red; */
    /* color: white; */
```