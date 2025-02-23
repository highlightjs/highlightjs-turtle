# highlightjs-turtle

![logo](https://cygri.github.io/rdf-logos/png/turtle-128.png)
![logo](https://cygri.github.io/rdf-logos/png/sparql-128.png)

[`highlight.js`](https://github.com/highlightjs/highlight.js) syntax definitions for these semantic web languages:
- [Turtle 1.1](https://www.w3.org/TR/turtle/)
- SPARQL 1.1: [Query](https://www.w3.org/TR/sparql11-query/) and [Update](https://www.w3.org/TR/sparql11-update/) languages _(see [BNF grammar](https://www.w3.org/TR/sparql11-query/#sparqlGrammar) and [syntax diagrams](http://rawgit2.com/VladimirAlexiev/grammar-diagrams/master/sparql11-grammar.xhtml))_
- [GraphDB Rules](http://graphdb.ontotext.com/documentation/standard/reasoning.html) (PIE)
- [SHACL Compact](https://w3c.github.io/shacl/shacl-compact-syntax/) _(see [BNF grammar](https://github.com/VladimirAlexiev/grammar-diagrams/raw/master/shaclc-grammar.ebnf) and [syntax diagrams](http://rawgit2.com/VladimirAlexiev/grammar-diagrams/master/shaclc-grammar.xhtml))_ _(still in TODO)_

## Usage

Simply include the Highlight.js library in your webpage or Node app, then load this module.

### Static website or simple usage

Simply load the module after loading Highlight.js. You'll use the minified version found in the `dist` directory. This module is just a CDN build of the language, so it will register itself as the Javascript is loaded.

```html
<script type="text/javascript" src="/path/to/highlight.min.js"></script>
<script type="text/javascript" src="/path/to/pie.min.js"></script>
<script type="text/javascript" src="/path/to/turtle.min.js"></script>
<script type="text/javascript" src="/path/to/sparql.min.js"></script>
<script type="text/javascript">
  hljs.highlightAll();
</script>
```

### With Node or another build system

If you're using Node / Webpack / Rollup / Browserify, etc, simply require the language module, then register it with Highlight.js.

```javascript
var hljs = require('highlight.js');
const { pieGrammar, sparqlGrammar, turtleGrammar } = require("highlightjs-turtle");

hljs.registerLanguage('pie', pieGrammar);
hljs.registerLanguage('sparql', sparqlGrammar);
hljs.registerLanguage('turtle', turtleGrammar);
```


## Links
- http://highlightjs.org for more info on `highlight.js` and a live demo
- [`highlightjs-shexc`](https://github.com/highlightjs/highlightjs-shexc) for another semantic language, SHEX (Shape Expressions)
- [`highlight-to-reveal`](https://github.com/VladimirAlexiev/highlight-to-reveal) for info about using this in [`reveal.js`](https://github.com/hakimel/reveal.js), a tool for web-based presentations _(NOTE: this is outdated!)_

## Contributors
- Mark Ellis, [@ellismarkf](https://github.com/ellismarkf), Stardog Union
- Vladimir Alexiev, [@VladimirAlexiev](https://github.com/VladimirAlexiev), Ontotext Corp
