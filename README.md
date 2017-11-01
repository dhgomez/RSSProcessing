# RSSProcessing

Módulo:	Tecnologías	del	lado	del	servidor:	Cloud	Computing (Procesamiento	de	XML	y	JSON)

Práctica: Procesamiento	de	RSS con	DOM,	SAX y	JSON

RSS	es	un	formato	estándar	basado	en	XML	para	publicar noticias. Se	trata	de	implementar	un	programa	 en	 Java,	 al	 que	 	 pasándole	 una	 dirección	 Web de	 un	 canal de	 noticias	 RSS (por	ejemplo:	http://www.europapress.es/rss/rss.aspx ),	nos	devuelva	como	resultado,	además	de	imprimir	 cierta	información	 por	 pantalla,	 dos	archivos	 con	información	 sobre	 las	 noticias	 del	canal.	

Uno	de	los	archivos	tendrá	formato	XML	y	el	otro	JSON.

Como	información	del	canal	se	mostrará	por		pantalla el	título,	URL	y	descripción	del	canal que	ofrece	las	noticias,	así	como	de	las	noticias	de	dicho	canal.	De	cada	noticia	a	su	vez	habrá	que	mostrar:	título,	URL,	descripción,	fecha	de	publicación	y	categoría.

Además	 también	 habrá	 que	 crear	 un	 documento	 XML de	 salida	 denominado	“noticias_<nombreCanal>.xml”,	 resultado	 de	 procesar	el	 RSS	 de	las	 noticias	 (items)	 del	 canal	elegido, que	 contenga	 la	 información	 sobre	 las	 noticias	 del	 canal,	 siguiendo	 la	 siguiente	estructura:

<noticias canal=”título canal”>
  <noticia> título noticia </noticia>
  <noticia> título noticia </noticia>
  …
</noticias>

Finalmente,	la	misma	información	que	se	ha	almacenado	en	el	fichero	XML	de	salida,	se	ha	de almacenar	en	formato	JSON	en	otro fichero denominado	“noticias_<nombreCanal>.json”	quetambién	se	 obtendrá	 como	 resultado.	 Para	 obtener	 el	 resultado	 en	 formato JSON	 se	 podrá	elegir	entre	dos	posibilidades:

- Utilizar	 directamente	 la	 conversión	 de	 XML	 (del	 fichero	 XML	 con	el	 resultado	 de	
salida)	a	 JSON,	mediante la	clase	 JSONML	existente	que	para	este	 fin	que	se	nos	proporciona	en	JSON.ORG

- Crear	 un	 JSON	 con	 el	 formato	 que	 se	 indica	 a	 continuación,	 similar	 al	 XML	
equivalente:
{“noticias”: [{“noticia”:”tit_noticia1”}, {“noticia”:”tit_noticia2”},…,{“noticia”:”tit_noticiaN”} ] }

Para	 procesar la información	 XML del	 canal	 RSS	 habrá	 que	 implementarlo	 en	 las	 dos	
modalidades	posibles	de	procesamiento	de	información	XML	en	el	servidor:	
a) Utilizando	DOM
b) Utilizando	SAX
  
Las	 dos	 versiones	 o	 proyectos	resultantes,	uno para	 gestión	 del	 RSS	 con	 DOM	 y	 el otro con	
SAX,	se	encapsularán en	 dos	.zip	independientes,	 que	 se	enviaran	a	 través	 de	las	 dos	 tareas	
habilitadas	 para	ello	en	la	 plataforma	Moodle. 

El	 proceso	 de	 conversión	 de	la	información	a	formato	JSON	y	la	obtención	del	fichero	JSON	resultante,	basta	con	incluirla	en	uno	de	los	dos	proyectos.
