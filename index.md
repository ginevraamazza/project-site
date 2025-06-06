---
layout: default
---

<!DOCTYPE html>
<html lang="it">
<head>
  <meta charset="UTF-8">
  <title>Benvenuti</title>
</head>
<body>
  <h1>Knowledge Engeneering for Humanities - Semantic Enrichment of Rimini's Monument Entities in the Wikidata Knowledge Graph</h1>
  <p> This project aims to semantically <strong>enrich</strong> the digital representations of Rimini’s most significant monuments within the Wikidata Knowledge Graph, using techniques and tools from computer science and knowledge engineering.
The work focuses on retrieving and analyzing structured data related to the cultural heritage of Rimini, identifying missing or incomplete semantic properties (such as architectural style, building material, official websites, and inscriptions) in Wikidata items and suggesting and constructing RDF triples via SPARQL CONSTRUCT queries to enrich entities.
<br>
     We use SPARQL queries to extract, filter, and validate data:
- To list all monuments located in Rimini and select a relevant subset.
- To analyze the completeness of key semantic properties.
- To cross-reference with external authoritative sources (e.g., Rimini’s municipal website and scholarly guides) for validation.  di GitHub Pages.</p>

  <h2>Sezioni</h2>
  <ul>
    <li>📂 Codice: <a href="https://github.com/ginevraamazza/project-site">Vai al repository</a></li>
    <li>📄 Documentazione: coming soon...</li>
    <li>🧪 Esperimenti: coming soon...</li>
  </ul>

  <hr>
  <p>Hai bisogno di aiuto con il sito? Contattami!</p>


There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project. ciaoooo
prova prova prova. Viva il Toad!!!!!!
# Header 1

This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

## Header 2

> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

### Header 3

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

With this query we identify all the monuments in Rimini, to find those that will be enriched later.

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX wd: <http://www.wikidata.org/entity/>
PREFIX wdt: <http://www.wikidata.org/prop/direct/>
PREFIX wikibase: <http://wikiba.se/ontology#>
PREFIX bd: <http://www.bigdata.com/rdf#>
SELECT DISTINCT *
WHERE { 
  ?monuments wdt:P17 wd:Q38 ;
            wdt:P131 wd:Q13369 ;
            wdt:P1435 wd:Q26971668 ;
            rdfs:label ?monument_name .
  ?monuments wdt:P131 ?moncity .
  ?moncity rdfs:label ?city .
  FILTER (lang(?monument_name) = "it")
  FILTER (lang(?city) = "it")
}
 LIMIT 100


##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
</body>
</html>
The final element.
```
