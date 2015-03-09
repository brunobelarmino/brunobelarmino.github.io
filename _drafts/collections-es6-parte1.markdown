---
layout:     post
title:      "Collections ES6 parte 1"
subtitle:   "Novas estruturas de dados do Javascript"
date:       2015-03-09 09:00:00
author:     "Bruno Belarmino"
header-img: "img/post-bg-02.jpg"
# disqus-identifier: "2015-03-09-collections-es6-parte1"
---

<p>Fala Amigos!</p>

<p>
	Dando continuidade a nossa série sobre as novidades do Javascript, vamos falar hoje sobre collections.
</p>

<h4>Sets e Maps</h4>

<p>
	Historicamente a única collection que vinha por padrão no Javascript era o <em>Array</em>. Mas a partir do ES6 temos novos tipos como: <em>Set</em>, <em>WeakSet</em>, <em>Map</em> e <em>WeakMap</em>.  
</p>

<h4>Set</h4>

<p>
	Para quem tem conhecimento em linguagens de programação como C#, Java, Ruby e Python esta collection não é uma novidade, mas para quem tem conhecimento somente em Javascript sim. Sendo assim, segue a definição:
</p>

<p>
	<em>Set</em> é um tipo de collection que não permite valores duplicados. Utilizando <em>Set</em> não é possível acessar um valor como é feito com <em>Array</em>, normalmente você valida para ver se o valor está presente ou itera sobre os valores.
</p>

<pre>
	<code>
		var set = new Set(); //cria um novo Set
		set.add(1); //adiciona um valor

		//número de valores no set
		set.size; // 1

		//verifica se o valor existe dentro do Set
		set.has(1); // true

		set.delete(1); //remove um determinado valor do Set

		set.has(1); // false
		set.size; // 0

		var set2 = new Set([1, 2, 3]); //cria um novo Set a partir de um Array

		set2.size; // 3

		//itera sobre os valores do Set
		for (let valor of set2) {
		  console.log(valor);
		}

		//o código acima tem o output: 
		// 1
		// 2
		// 3

		set2.clear(); //remove todos os valores do Set
		set2.size; // 0
	</code>
</pre>