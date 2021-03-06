# Sito dell'associazione Assob.it

Il sistema Git, github, [github pages](https://pages.github.com/) e jekyll costituiscono un insieme di strumenti molto utili per la manutenzione collaborativa di un sito Web e la nostra associazione deve basarsi necessariamente sulla collaborazione.

## Per cominciare (non esperti)


* Bisogna iscriversi a Github
* Seguire le istruzioni sulle [FAQ](https://github.com/assobit/assobit.github.io/wiki/FAQ) per fare le operazioni comuni usando solo github.com

Le pull requests (modifiche proposte) sono attualmente valutate da me ma sono discusse pubblicamente. Spero prestissimo di avere collaboratori (più sono meglio sto).

### To have
Un sistema per dare al non esperto immediata visibilità delle sue modifiche. Se uno dei nostri legali fa modifiche a una parte di testo vorrà vedere come viene e sarebbe bello dargli la possibilità di apprezzare un 'anteprima delle modifiche. Attualmente github non visualizza anteprime di un tuo repository se non tramite github pages ed è possibile solo un sito github pages per account utente (da esplorare la possibilità di fare pagine di progetto con gh-pages).

## Per cominciare (esperti di git)
* Bisogna iscriversi a Github
* Fare un [fork](https://help.github.com/articles/fork-a-repo/) di questo repository creando una copia sul proprio account github
* Clonare il repo in locale

	git clone *urlRepositoryDaClonare

* [Configurare il repository di origine come "upstream" con il comando git remote](https://help.github.com/articles/configuring-a-remote-for-a-fork). In questo modo IL *NOSTRO FORK* sarà configurato come "origin"
*configurare il *REPOSITORY DI ORIGINE* come "upstream"

	git remote add upstream *urlDelRepositoryOrigineDelClone

* [mantenerlo sincronizzato con quello di origine](https://help.github.com/articles/syncing-a-fork/)
In sintesi si tratta di recuperare spesso tutte le branch dal repository di origine (upstream) fare il merge, fare il commit e il push **sul proprio repository su github**

	git fetch upstream

Fare il checkout della branch del proprio repository da sincronizzare con quello di origine (es:master)

	git checkout master

	git merge upstream/master

fare le modifiche e poi aggiornare la propria copia su github del repository

	git push

* Aprire una branch per ogni gruppo di modifiche uniformi (è più ordinato)
* quando una modifica è pronta per essere sottoposta ai "committers" si [apre una pull request sul proprio repository forkato](https://help.github.com/articles/using-pull-requests/) di github. Questo non è altro che un invito ai committers a "tirare dentro" al repository ufficiale le modifiche su cui abbiamo lavorato.

### Per vedere i risultati del proprio lavoro in locale è necessario installare github-pages come "gemma" in Ruby

[Qui le istruzioni ufficiali](https://help.github.com/articles/using-jekyll-with-pages/)


   gem install bundler
   cd assobit.github.io
   bundle install # il Gemfile corretto è già nel repository
	 bundle exec jekyll serve --baseurl ''


Poi dovete andare con un browser alla pagina 127.0.0.1:4000

## Errori e Problemi

Contattate la mailing list dell'associazione o lasciate una nota sul repo oppure (meglio) forkate, modificate e aprite una pull request
