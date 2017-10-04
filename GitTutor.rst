###############
Tutorial Github
###############


Crear un nou Repositori
=======================

Crea un nou repositori, obrir i executar:

::

	$git init


Descarregar un repositori Existent
==================================

Per crear una copia local executar:

::

	$git clone /path/to/repository

Si es tracta d'un servidor remot:

::

	$git clone username@host:/path/to/repository


Flux de treball
===============

- El repositori local esta composat per tres "Arbres" administrats per git. El primer es el *Directori de treball* que conte els arxius.
- El segon es *l'index*, que actua com a zona intermitja.
- El tercer es el *HEAD*, que apunta l'ultim commit realitzat.


Add & Commit
============

Per registrar canvis i afegir-los a *l'index* s'executa:

::

	$git add <filename>
	$git add .

Aquest es el primer pas. Per fer *commit* a aquests canvis s'executa:

::

	$git commit -m "Commit message"

Després del *Commit* l'arxiu està inclos dins del *HEAD*, però encara no esta pujat al *Repositori remot*.


Enviament de canvis
===================

Els canvis ara son a la copia local del *HEAD*, per enviar-los al *Repositori remot* s'ha d'executar:

::

	$git push origin master

Es pot canviar el parametre *master* per alguna branca (ara expliquem les branques).


Branques
========

Les branques s'usen per desenvolupar funcionalitats aïllades unes d'altres. La branca *"master"* es la branca per defecte.
Crea una nova branca executant:

::

	$git checkout -b nom-de-branca

Per canviar de branca s'executa:

::

	$git checkout nom-de-branca

Per borrar una branca:

::

	$git branch -d nom-de-branca

La branca també no es pujara al *Repositori remot* fins que no li fem *push*:

::

	$git push origin nom-de-branca 


Actualitzar & fusionar
======================

Per actualitzar el *repositori local* i descarregar i fusionar els canvis remots:

::

	$git pull


Substituir canvis locals
========================

En cas de cagarla, pots substituir els *canvis locals* per l'ultim contingut del *HEAD* amb:

::

	$git checkout -- <filename>

Si vols desfer *TOTS* els canvis locals, pots portar l'ultima versió del servidor amb:

::

	$git fetch origin
	$git reset --hard origin/master

