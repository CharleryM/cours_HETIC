
<h1> JavaScypre natif</h1>

<h2> Vocabulaire</h2>


Un ***objet*** de programation = entitée avec des propriétés manipulables avec des méthodes.
***métode*** = fonction qui s'aplique à des objets


`array` sert a créer un tableau. on peut en créer un en le définissant comme variable ( exemple : `let tableau = []` )
l'objet `map` mémorise l'ordre des clés-valeurs 


programe ***syncrone*** = exécute les choses ***l'une après l'autre*.**<br>
programme ***asyncrone*** = exécute les chose ***sans attandre d'avoir toutes les données.*** il revient sur la chose lorsqu'il aura toutes les infos 
qu'il aura besoin. il utilise une promesse.


`callback` = fonction dans une fonction sui utilise le résulta de la première fonction pour renvoyer un résultat.


<h2>Les promesses</h2>


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


<h3> propriété de la promesse</h3>


 `state` son état de base est "pending" en cas de succès il passe à "fullfilled" ou "rejected" si il y a un.<br>
`result` est de base "undifine" et passe a "value" pour un succès (resolve) ou "error" en cas de rejet (reject).




<h2>Vocabulaire de developpeur</h2>

 silencieusement ignoré = la machine de dit même pas qu'il y a quelque chose d'ignoré.