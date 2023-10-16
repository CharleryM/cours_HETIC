
<h1> JavaScypre natif</h1>

<h2> Vocabulaire</h2>

<h3>objets natifs</h3>


Un ***objet*** de programation = entitée avec des propriétés manipulables avec des méthodes.
***métode*** = fonction qui s'aplique à des objets


`array` sert a créer un tableau. on peut en créer un en le définissant comme variable ( exemple : `let tableau = []` )
l'objet `map` mémorise l'ordre des clés-valeurs 


programe ***syncrone*** = exécute les choses ***l'une après l'autre*.**<br>
programme ***asyncrone*** = exécute les chose ***sans attandre d'avoir toutes les données.*** il revient sur la chose lorsqu'il aura toutes les infos 
qu'il aura besoin. il utilise une promesse.

`split` est une méthode native qui permet de transformer une chaine de caractères.<br>
On doit lui mettre une condition pour la faire fonctionner. la condition utiliser sera couper du tableau. concrètement si la condition est un espace insécable, il ne pourra pas y avoir d'espace dans le tableau créer.

`callback` = fonction dans une fonction sui utilise le résulta de la première fonction pour renvoyer un résultat.

`constructor`  est une **méthode** qui est utilisée pour créer et initialiser un objet lorsqu'on utilise une `class`.

`super()` est utilisé afin d'appeler ou d'accéder à des fonctions définies sur l'objet parent

<h3>Les promesses</h3>


***une promesse***  se met soit dans une variable soit dans une fonction **en priorité dans une fonction** puisque on va la retourner. elle ne peut avoir qu'**un unique** résultat

on peut lui enchainer des `.then` et `chatch`<br>
`.then` renvoie une nouvelle promesse.<br>
`try` en cas de réussite sinon  il passe au `.catch` = en cas d'erreur<br>
`finally` s'exécute après `try` et `chatchpour`nettoyer des données inutilisés. Il renvoie le résulta au prochain `.then` ou `.catch`. il afirme la fin de la ***promesse***.<br>
Un *gestionaire finally* ne doit rien renvoyer. dans  le cas contraire le résultat est <sup>silancieusement ignoré</sup>

la fontion donner a une promesse s'appelle un **executeur** Il se lance tout seul. Il ne peut avoir qu'un seul état et est définitif.
	
	let promise = new Promise ((resolve, rejet)=>{
		//fonction de la promesse
	})


<h4> propriété de la promesse</h4>


 `state` son état de base est "pending" en cas de succès il passe à "fullfilled" ou "rejected" si il y a un.<br>
`result` est de base "undifine" et passe a "value" pour un succès (resolve) ou "error" en cas de rejet (reject).


<h4> Les class</h4>

pour ajouter une ***méthode*** à un ***objet*** on utilise ":"

	let variable = []
	class exemple extend variable{
		constructor(mode)
		super(mode)
		//suite du code
	}


<h3>Les évenements</h3>

Il y a deux types d'évenements :
- les évenement lié à la page tel que `onload` ou `onclic`

- les évenements liés au materiel tel que`onKeyDown`


<h3>Les coockies</h3>

Les ***coockies***  un fichier qui contiens (en général ) une information de l'utilisateur. une utilisation basique, l'utilisation de cookies pour garder en mémoir les informmations d'autantification tel que le mail et le mode passe. on appelle la fonction avec 

	Document.coockie

<h4>options</h4>

`user` indique l'utilisateur enregistrer dans le coockie.

`path=/` indique que le coockie sera actif dans tout le site.

`domaine=exemple.com` le coockie serra actif dans tout les domaine qui se termine par ce qu'on a définit.

`expires` définis une date d'expiration. par défaut le coockie disparet dès qu'on ferme la page.

`max-age` permet de donner un temps d'expiraration en seconde.

`secure` est une option qui permet de sécuriter. le coockie peut être envoyer uniquement en HTTPS.

`saveorigin` permet de faire croire au navigateur que les requètes de plusieurs serveurs disctinct qu'ils ont la même aurigine.

`samesite=lax` envoie les cookies uniquement sur lesrequères GET

`samesite=strict` pas de cookie si l'utilisateur vient d'un autre site.

<h5>Vocabulaire de developpeur</h5>

 silencieusement ignoré = la machine de dit même pas qu'il y a quelque chose d'ignoré.