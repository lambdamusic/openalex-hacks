# OpenAlex hacks

Notebooks and code snippets aimed at learning about / exploring the [OpenAlex](https://openalex.org/) datasets.

See also [this website](https://lambdamusic.github.io/openalex-hacks) for example visualizations resulting from the code. 


## Topics and Keywords

The topics classification in OpenAlex consists of various thousand categories organised into a 4-level hierarchy. 

The gist of it is:

[Topics](https://help.openalex.org/hc/en-us/articles/24736129405719-Topics)

> Works in OpenAlex are tagged with Topics using an automated system that takes into account the available information about the work, including title, abstract, source (journal) name, and citations. There are around 4,500 Topics. Topics are grouped into subfields, which are grouped into fields, which are grouped into top-level domains. This is shown in the diagram below, along with the counts for each.


[Keywords](https://help.openalex.org/hc/en-us/articles/24736201130391-Keywords): 

> Our team put together a new implementation of keywords based on our Topics. There are currently over 26,000 keywords and we expect to add more as time goes on. [...] With our new topics system that was developed in coordination with CWTS, we came out with a list of 10 keywords for each topic. In order to assign keywords to works, we took the topics assigned to that work (at most 3 topics), pulled the keywords associated with those topics (at most 30 keywords, for now) and then determined the similarity of the keyword to the title/abstract using embeddings (and the BGE M3-Embedding model).

See the [official data documentation](https://help.openalex.org/hc/en-us/sections/24734432836887-Data) for more, and in particular also worth looking into the paper  [OpenAlex: End-to-End Process for Topic Classification](https://docs.google.com/document/d/1bDopkhuGieQ4F8gGNj7sEc8WSE8mvLZS/edit#heading=h.5w2tb5fcg77r)

### Exploring the topics tree

The [notebook 2024-09-topics-explore.ipynb](/src/2024-09-topics-explore.ipynb) pulls the topics dataset and turns it into a nice [FoamTree visualization](https://lambdamusic.github.io/openalex-hacks/foamtree/).

### Rendering the data as SKOS

[SKOS](https://www.w3.org/2004/02/skos/intro) provides a standard way to represent knowledge organization systems using the Resource Description Framework (RDF). Encoding this information in RDF allows it to process it using various tools developed for Knowledge Graph applications. 

This [notebook 2024-09-skos.ipynb](/src/2024-09-skos.ipynb) loads the topics dataset and generates a SKOS ontology: [openalex-topics-rdf.ttl](/src/data/openalex-topics-rdf.ttl). 

Two sample visualizations of the ontology have been generated (using [Ontospy](https://lambdamusic.github.io/Ontospy/)): 

* Multi page HTML documentation (one page per entity)
* Single page HTML documentation
* D3 bubble chart



### Credits 

* OpenAlex https://docs.openalex.org/
* Python API https://github.com/J535D165/pyalex 
* Foam Tree https://get.carrotsearch.com/foamtree/latest/demos/



## Development

* `src` folder includes jupyter notebooks with all data extraction logic
* `build` folder is used to generate outputs
* put results into `docs` for publishing via github pages ie on <https://lambdamusic.github.io/openalex-hacks/>


### Disclaimer

This code is mainly a hack and can contain errors. 

I am not affiliated to the OpenAlex project. 

