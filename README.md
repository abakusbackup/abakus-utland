# abakus-utland
Blogg for prosjektet Abakus Utland i backup. Bloggen skal brukes for å dele Abakus-medlemmers erfaringer fra utveksling.

## Hvordan fungerer det?
Dette [GitHub-repoet](https://help.github.com/articles/about-repositories/) har aktivert [GitHub Pages](https://pages.github.com/). Systemet som brukes er [Jekyll](http://jekyllrb.com), som enkelt lar en skrive innlegg med [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) for så å publisere dem som HTML. Når man gjør endringer i repoet, 'bygges' siden på nytt (altså Markdown blir HTML) og innholdet legges ut på [nettsiden](http://utland.abakus.no). Utover nettadressen (som Webkom ordner med), kan alle endringer gjøres direkte fra dette repoet.

## Legg til et nytt innlegg
Opprett en ny fil med navnet `YYYY-MM-DD-post-title.md`. I denne legger du innlegget du vil publisere.
Den øverste delen av dokumentet er metadata om innlegget, som tittel og dato det er publisert. Ellers bruker du bare Markdown for å formatere innlegget.

    ---
    layout: post
    title:  "Example post"
    date:   2017-04-09 14:56:46 +0200
    categories: category1 category2
    ---

    # Some new fantastic post
    Let me tell you about the time I ... 

Alt under `---` blir altså innholdet i innlegget.

`categories` er en oppramsing, separert av mellomrom, av hvilke kategorier innlegget tilhører. Disse kategoriene kan bli brukt til å sortere innlegg. Se ellers under tema i denne filen. Der finner du tema (utseender) på en Jekyll-blogg, som bruker disse kategoriene til å sortere innhold.

## Legg til en ny side
Dersom du ønsker å opprette en ny side, er det bare å opprette en ny fil i rotmappen til dette prosjektet. Gi den et navn som har noe å gjøre med hva siden skal handle om, for eksempel `example-page.md`.

Den øverste delen av dokumentet er metadata om siden, som tittel og adressen (`permalink`) til den. Ellers bruker du bare Markdown for å formatere siden. Eksempel:

    ---
    layout: page
    title: Example page
    permalink: /example/
    ---
    # My new fantastic example page
    Hello world!
    
    ## Some smaller header
    Hello _country_!
    
Alt under `---` blir altså innholdet på siden.

## Endre tema (utseendet)
Tema settes ved hjelp av `_config.yml`. Der er det et felt `theme: minima`, hvor altså den siste delen (her `minima`) sier hvilke tema siden bruker. Man kan finne mange temaer på [Jekyll Themes](http://jekyllthemes.org/). GitHub har ikke støtte for alle temaer ut av boksen, så noen må installeres. Det er bare å laste ned temaet, og legge inn her. Du kan lese hvordan [her](https://help.github.com/articles/adding-a-jekyll-theme-to-your-github-pages-site/).

## Andre filer
* `CNAME` sørger for at http://utland.abakus.no peker til denne bloggen
* `Gemfile` og `Gemfile.lock` er filer [Ruby](https://www.ruby-lang.org/en/) (det Jekyll kjører på) trenger for å skjønne at det er snakk om en Jekyll-applikasjon.
* [`.gitignore`](https://git-scm.com/docs/gitignore)
