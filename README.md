# Kaart van Nederland

Symbool font met Nederlandse provincies als karakters. Hiermee kun je
makkelijk, met alleen HTML en CSS, een kaart van Nederland in de browser
tonen. Geïnspireerd door [Stately](https://github.com/intridea/stately), en gemaakt
met behulp van [deze instructies](http://www.intridea.com/blog/2012/4/24/symbol-font).

## Gebruik

Zie de demo-files in `demos`.

## Attributie

De kaart is afkomstig van [Wikipedia](http://nl.wikipedia.org/wiki/Bestand:Karte_der_Provinzen_\(Niederlande\)_-_nl.svg),
en is gemaakt door Hans Erren. De kaart is in Inkscape aangepast en uiteindelijk naar `Nederland.svg` weggeschreven.

## TODO

Ligaturen.

## SVG converteren naar TTF

In plaats van [FreeFontConverter](http://www.freefontconverter.com/)
gebruik ik het volgende [FontForge](http://fontforge.org/) script om de SVG
file naar TTF te converteren:

```
#!/usr/bin/env fontforge -lang=ff
while ($argc > 1)
    Print('')
    Print('Opening '+$1)
    Open($1)
    Print('Saving '+$1:r+'.ttf (fullname: ' + $fullname + ')')
    Print('')
    Generate($1:r+'.ttf')
    Close()
    shift
endloop
Quit(0)
```
