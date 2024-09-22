# openalex-explore

Exploring the OpenAlex datasets.

Website: <https://lambdamusic.github.io/openalex-explore/>

## Credits 

* OpenAlex https://docs.openalex.org/
* Python API https://github.com/J535D165/pyalex 
* Foam Tree https://get.carrotsearch.com/foamtree/latest/demos/


## OpenAlex Topics and Keywords

Best is to look into the [official data documentation](https://help.openalex.org/hc/en-us/sections/24734432836887-Data). 

But the gist of it is this

[Topics](https://help.openalex.org/hc/en-us/articles/24736129405719-Topics)

> Works in OpenAlex are tagged with Topics using an automated system that takes into account the available information about the work, including title, abstract, source (journal) name, and citations. There are around 4,500 Topics. Topics are grouped into subfields, which are grouped into fields, which are grouped into top-level domains. This is shown in the diagram below, along with the counts for each.


[Keywords](https://help.openalex.org/hc/en-us/articles/24736201130391-Keywords): 

> Our team put together a new implementation of keywords based on our Topics. There are currently over 26,000 keywords and we expect to add more as time goes on. [...] With our new topics system that was developed in coordination with CWTS, we came out with a list of 10 keywords for each topic. In order to assign keywords to works, we took the topics assigned to that work (at most 3 topics), pulled the keywords associated with those topics (at most 30 keywords, for now) and then determined the similarity of the keyword to the title/abstract using embeddings (and the BGE M3-Embedding model).

Also worth looking into the paper  [https://docs.google.com/document/d/1bDopkhuGieQ4F8gGNj7sEc8WSE8mvLZS/edit#heading=h.5w2tb5fcg77r](https://docs.google.com/document/d/1bDopkhuGieQ4F8gGNj7sEc8WSE8mvLZS/edit#heading=h.5w2tb5fcg77r)

## Development

* `build` folder is used to generate outputs
* then move results to `docs` for publishing on <https://lambdamusic.github.io/openalex-explore/>
* jupyter notebooks contain all data extraction logic


## About

This repo: https://github.com/lambdamusic/openalex-explore

**DISCLAIMER** 

I am not affiliated to the OpenAlex project. 

