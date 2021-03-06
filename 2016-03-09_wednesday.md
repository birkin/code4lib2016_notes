### [schedule](http://2016.code4lib.org/schedule/day-2)

---

### [linked open dime novels](http://2016.code4lib.org/Linked-Open-Dime-Novels-or-19th-Century-Fiction-and-21st-Century-Data)
by (http://2016.code4lib.org/speakers.html#demian-katz) and (http://2016.code4lib.org/speakers.html#matthew-short)

- 5-10 cents each mid-19th C.
- bibliographic nightmares -- eg different pseudonyms shared by several real-world authors

- started with ontology work -- creativework, edition, copy and series
- [dimenovels.org](https://dimenovels.org) (demian)
- [rda unconstrained](http://www.rdaregistry.info/Elements/u/#)

- pseudonym issue: dime:HasCredit -> dimenovels.org.name, and then the dimenovels.org.name is related to foaf

- dimenovels.org built on [geeby-deeby](https://github.com/demiankatz/Geeby-Deeby)

- demian: easy to get away with not knowing much about underlying html technologies -- eg content-negotiation -- really encourages us to learn about them tho.

- both mods and marc to allow for uris associated with strings

- duplicate work of reconciliation not bad -- helps expose data issues

- wrote/used [Murpoint](https://github.com/FalveyLibraryTechnology/Murpoint) "...tool was created to harvest all RDF from a specific domain..."

- used [ARC2](https://github.com/semsol/arc2), php/mysql library and triplestore

- example of underlying rdf, search, then go to an item, eg (https://dimenovels.org/Item/3921/Show), and replace Show with RDF, (https://dimenovels.org/Item/3921/RDF)


---

### [semantic search](http://2016.code4lib.org/Beyond-the-Keyword-Creative-Search-and-Query-Expansions-based-on-DBpedia)

- synonyms

- semantic keywords

- dbpedia.org/Page/School -- that doesn't work; explore

- child computer-game example
    - child -> teenager
    - computer-game -> video game

- case study: fashion design -- brainforks:8080/creativebook/Fashion_design -- try later
    - showed example of overdrive covers for different categories
    - some outliers

- use breadcrumbs so user knows where stuff's coming from

- example of serendipity/discovery eg getting from iv to camelback

- how many is too many alternates? says amazon gets a sweet-spot of 8-10, oclc shows too many

- need to filter, keeping only most relevant results -- google ngram, she uses python & restful api
     - new words underrepresented, like `email`, or scientific terms
     - :8080/getfreq/[["1gram"]],more -- is that really a part of the url -- ted thinks yes -- check that out

- fault tolerance
    - lemmas
    - capitalization
    - Singplu

- github, [Minervax](https://github.com/minervax/)

---

### [doing rdf](http://2016.code4lib.org/So-You-Think-You-Want-to-Migrate-to-RDF)

by eben & steven

- focusing on predicates

- which vocab to decide on?
    - vocabs get their value from reuse

- [linked open vocabularies](http://lov.okfn.org/dataset/lov/)
- same as

- domain and range...

- range
    - extent example in marc -- might do a lookup and think you could use the extent element they showed -- but the doc for that shows that it expects certain structured data not good for you.
    - so, what if others are using it anyway in a non-compliant way?
    - mint your own or use a less-used one?

- domains
    - latest thinking is that these mean very little -- i'm confused... everyone says, like demian, you get this as you really work on it
    - extinction can happen -- may still need to store stuff locally

- minting predacates
    - (http://opaquenamespace.org)

- xml to rdf can be tricky -- they gave an einstein example

- change thinking from record to relational-database model

- orderedness -- how to deal with that in rdf?
    - eg name-order predicate concept they're thinking about

- performance
    - one example, one-request every 3 seconds
    - solution is caching
    - rails -- using linked-data-fragments to caching layer -- caveat, not latest data

- oregon digital vocab manager

- conclusions -- is it worth it?
    - painful
    - users won't see difference
    - rdf doesn't auto-make it more shareable
    - "maybe"

---

### [catalogers](http://2016.code4lib.org/How-not-to-waste-catalogers-time-Making-the-most-of-subject-headings)

by (http://2016.code4lib.org/speakers.html#john-mark-ockerbloom)

- specifying subjects -- priority, relatedness

- loc example

- solr not sole solution

- tricky to explore laterally

- he includes, in sorting logic, subject-heading awareness -- also more recent is priviledged, assuming more knowledge

- one goal: link terms that people search for, like 'battle of germantown' -- with lc subject headings -- via indirect lookups like in the semantic search talk
    - me, thought... what if search terms like 'battle of germantown' could be treated as rdf entites... what would that offer? if we had a local ted-ish identity-hub, what could link to that search term? if lc contains that subject-heading, we could include that -- if wikipedia contains that specific subject-heading, we could include that. ok. so what does that then allow...
        - tl: we could bump results by number of wikipedia edits -- popularity -- or at least depth of interest/knowledge
        - tl: easyb data to help determine popularity
            - me: easyA article data for popularity of related articles
        - we could bump results base on the number of links available -- loc, wikipedia, etc
        - we could display alternate/related issues by querying
        - maybe we only care about the most popular search terms for this

- gives example of how blmatter term doesn't exist in lc, but does in wikipedia.

- [mashcat](http://www.mashcat.info) -- how catalogers and coders can work better together

---

### [burnout](http://2016.code4lib.org/The-Modern-Day-Sisyphus-libtech-Burnout-and-You)

by (http://2016.code4lib.org/speakers.html#becky-yoose)

- managers, make it safer
    - give agency to staff
    - push back when team asked to do too much (eg asking whether a or b should be cut)
    - refer staff to other resources they may need

- be aware that privilege plays a big role in being able to take advantage of opportunities that others provide
    - so look for ways to make opportunities available to less privileged

---

### lightning talks

- idea for simplifying collection of libanalytics
    - push-button device sends signal to raspberry pi to macro
    - other uses: 'how are we doing?', 'need backup'

- ANTS -- transferring digital records to the archive
    - greg wiedman
    - ants is a python app
    - runs checksums, does some checks, records paths, creates a baggit bag, and transfers now
    - desktop needed for checksums
    - authentication useful

- [Lentil](https://github.com/NCSU-Libraries/lentil), by NCSU libraries
    - instagram api changes, which require users to have to give permission to folk to use those images via the api
    - can get key for exemption from public api requirements
    - submission requirements for instagram -- be specific (valid use-cases that reflect their issues), persistent, lucky
    - sample api submission box

- kate deibel
    - sharing pieces of things difficult
    - dissecting code takes skill
    - don't share as monolithic repository
    - share independent components
    - show/handled dependencies
    - easy customization & deployment
    - orbiscascade.org -- working on primo software toolkit

- michael gibney
    - [xmlaminar](https://github.com/upenn-libraries/xmlaminar) -- tool for working with arbitrarily large amounts of xml

- doi into core metadata
    - michael berkowski
    - [link](https://z.umn.edu/introduction.php)
    - content-negotiation crash course
    - provide 'Accept' http request header to ask for josn, xml, etc -- comma separated list -- can give preferential treatment
    - dx.doi.org, `Accept: application/citeproc+json`
    - must follow location redirects
    - examine returned content-type

- quicksearch now opensource
    - kevin beswick, ncsu -- ncsu single-search platform
    - single-search, bento-box search based on rails
    - vagrant, ansible-playbooks
    - modular & extensible
    - statics & best-bets
    - uses searchers -- based on gems that are easy to write

- [sphinx](http://www.sphinx-doc.org/en/stable/) for documentation
    - [AtoM](https://www.accesstomemory.org/en/) development documentation was problematic
    - write in [restructured text](http://docutils.sourceforge.net/rst.html)
    - me: can convert from restructured text to markdown via [pandoc](http://pandoc.org)

- justin from gwu
    - programming and software development consultation services
    - scheduled in 30 minute blocks -- using scheduling software
    - list of what's in scope -- pretty broad
    - out of scope: cs assignments, not TAs or tutoring -- referrals
    - why: want to support scholarship -- forces them to get out of cubes and talk to real people
    - results for 3 months(?)
        - there is a demand
        - setting up github pages
        - how to prepare for tech interview
        - raising their team's visbility

- [RMap](http://rmap-project.info/rmap/)
    - portico -- karen hanson?

---

### [Janus](http://2016.code4lib.org/Janus-Nodejs-Handler-for-all-Library-Searches)

by [david-naughton](http://2016.code4lib.org/speakers.html#david-naughton) -- u.of minnesota

- [Janus](https://github.com/mozilla/node-janus)

- "small application; doesn't do much" -- his words

- common problem
    - many search targets
    - gathering statics on library usage -> trying to correlate with student success/value

- one solution, bento box, like ncsu; jonathan has one too

- one handler to rule all search forms

- search forms  -->  janus  --> targets
    - so janus can gather searches

- benefits
    - single code-base to maintain
    - automate deletion of search data

- url api -- x/janus?search=darwin

- challenges setting it up
    - [guzzle](http://docs.guzzlephp.org/en/latest/) http library -- but had problems with javascript
    - nodejs installation
    - asynchrony

- node.js for testing
    - not rubust http sever, need referse proxy, nginx
    - for daemon, forever or supervisor
    - they used apache & passenger
        - he has an undocumented configuration

---

### [Getty research portal](http://2016.code4lib.org/Getty-Research-Portal-Reboot-Angular-and-Elasticsearch-for-Metadata-Search-Aggregation)

by [Ley](http://2016.code4lib.org/speakers.html#susan-ley) and [Cahan](http://2016.code4lib.org/speakers.html#adam-cahan)

- [portal](http://portal.getty.edu/portal/landing)

- conversion from java to [AngularJS](https://angularjs.org) & [Elasticsearch](https://www.elastic.co/products/elasticsearch).

- Angular
    - popular
    - databinding
    - good testing
    - MVC
    - the [styleguide](https://github.com/johnpapa/angular-styleguide) they use
    - architecture
        - querybuilder-service, search-service, savedrecord-service, data-service, storage-service

- Elasticsearch
    - scales
    - did their own mapping
    - art example
    - interesting UI -- intead of eliminating zero-length facets -- show/unshow checkboxes to indicate what's `active`

---

### [architecture is politics](http://2016.code4lib.org/Architecture-is-politics-the-power-and-the-perils-of-systems-design)

by [dre](http://2016.code4lib.org/speakers.html#andreas-orphanides)

- design ethics
    - me: googling links
        - (http://mlab.uiah.fi/polut/Yhteiskunnalliset/lisatieto_ethics_primer.html)

- persuasion
- dark pattern
    - making decisions on the user's behalf
    - combining optional with required (avg software)
    - steering users

- can u set things up so that user doesn't mess up -- ATM

- sharktooth design -- warning

- spinners on page

- default to all

- "design pursuades"

- refworks basics -- simple, gives context

- provide affordances to user's benefit
- user should recognize
- don't disguise

- parkway system bridges too low -- to stop buses of low-income folk

- ny condos -- low/high entrances

- "politics is architecture"

- the scunthorpe problem

- do
    - recognize your biases
    - diversify design practices
    - understand you culture

- system's interests vs users' interests
    - 80/20 pareto rule
    - great slide on advertising MB vs editorial MB
    - have smartphone?

- recognize & acknowledge compromises

---

### [creative disintegration](http://2016.code4lib.org/Constructive-disintegration-reimagining-the-library-platform-as-microservices)

by [sebastian-hammer](http://2016.code4lib.org/speakers.html#sebastian-hammer)

- ils via microservices

- stars with empty box

- 'app store' (incubator/makerspace)
    - catalog
    - patrons
    - circ
    - e+p acq

- intitial research library focus
    - citations?
    - inst.repository
    - publishing platform
    - other
        - plugins

- common UI layer -- initially based on react

- storage layers:
    - metadata, users, items, KB
    - if someone wants to use a different db or a triple-store, they can

- language
    - agnostic
    - microservices
    - restful interactions
    - focus on the interface
    - possibility of pieces hosted by different entities

- me:
    - what's the vetting for something being in the app store?
        - thought: no hardcoded urls, so user can be sure of no hidden calls
        - hmmn... if focus is on interfaces -- i could imagine a propritary vendor offering one of the pieces hosted that's closed-source, that culls data -- which would be ok -- as long as there are other kinds of app-store options

- sign up for [more info](https://www.futureisopen.org)

---

### [api-first approach](http://2016.code4lib.org/Transcending-Traditional-Systems-and-Labels-An-APIFirst-Archives-Approach-at-NPR)

by (http://2016.code4lib.org/speakers.html#camille-salas), (http://2016.code4lib.org/speakers.html#will-boyd), (http://2016.code4lib.org/speakers.html#john-nelson)

- 1970's mission --> 21st century solutions

- Use Artemis
    - [2012](http://www.wnyc.org/story/245470-npr-librarian-kee-malesky-new-york/)
    - [2012/2013](http://www.npr.org/sections/npr-extra/2012/08/23/159910472/a-look-to-the-future-one-archive-tape-at-a-time)

- requirements
    - flexible
    - searchable
    - scaleable
    - generates reports
    - access to historical stuff for reuse

- data-model (Trapper Keeper)

- nosql

- hypermedia over restful -- data-structure
    - what's hypermedia in this context? me googling rest vs hypermedia...
        - (http://www.mashery.com/blog/stop-talking-about-hypermedia-and-rest-start-building-adaptable-apis)
        - (https://en.wikipedia.org/wiki/HATEOAS)
        - (https://spring.io/guides/gs/rest-hateoas/)

- microservices-ISH -- what's that?

- x likes angular over backbone
- yeoman and jenkins -- so deployment's easy

- every application state is stored in the url

- proxy layer, api in front of api, to handle authentication initially, but now other things too
    - query/cache taxonomy
    - query taxonomy
    - running bulk updates
    - get/set user prefs
    - other things were listed

- mysql query: 1 minute
- dynamoBD/Elastic ingestion: 1 hour.

- lesson-learned: stakeholders focus on UI, not API, important to manage expectations

- (https://twitter.com/npr_rad)

---

### breakout: vivo/linked-data/git-data

- interests here
    - vivo/[simplectic](http://symplectic.co.uk/services/open-profile-services/)
        - learning about it
        - getting it set up
    - using git for data for versioning/trust
    - linked-data/rdf

- michael gibney mentioned [git-annex](https://git-annex.branchable.com)

- my interest
    - i like idea of[whosonfirst](https://whosonfirst.mapzen.com) / [data](https://github.com/whosonfirst/whosonfirst-data)

- matt: shouldn't think of strong demarcation between metadata and data -- eg getty data thought of by many users as metadata, but it's a big dataset updated and curated as data. Whether something is data or metadata is often contextual.

- me: how would data stored in the vivo triple-store be versioned?

- [git lfs](https://git-lfs.github.com) -- 'Git Large File Storage' for videogame/ iiif support

- interesting, you can re-serialize rdf without the hash being the same if you make the serializations non-deterministic

---

### [desktop electron](http://2016.code4lib.org/Building-Desktop-Applications-using-Web-Technologies-with-Electron)

by [Jason Ronallo](http://2016.code4lib.org/Building-Desktop-Applications-using-Web-Technologies-with-Electron)

- Why desktop?
    - standout & focus

- Why not desktop?
    - gui toolkits and different skillsets

- slack, discord, atom from github, wordpress desktop -- also hardware configuration apps

- what is electron?
    - [chromium](https://www.chromium.org) plus node.js

- has full disk access
    - read/delete files

- and machine access
    - camera & microphone

- issues with electron -- cross-platform but...
    - packaging
    - building installers not so easy
    - OS differences
    - rebuilding native modules

- [awesome electron](https://github.com/sindresorhus/awesome-electron)


---

### [beyond the bento box](http://2016.code4lib.org/Beyond-the-Bento-Box-Using-linked-data-and-smart-algorithms-to-integrate-repository-data-in-context)

by (http://2016.code4lib.org/speakers.html#jordan-fields) of the - marmot library network of colorado
and (http://2016.code4lib.org/speakers.html#mark-noble)

- choose your own adventure analogy -- you're given relevant options/resources from whereever you are in your search

- based on vufind, renamed pica (marmot -> pica)

- alternate info available in results -- eg catalog results, but also from, say, book item page via the sidebar
- marmot library network

- background searches on entities related to their search-term
    - i'd think on an item-page, based on entities related to the subjects/keywords associated with the item -- people / places / events

- sources: whosonfirst, geonames, internal catalog and geneology and archive, wikipedia, [find a grave](http://www.findagrave.com)

- issues:
    - lc subject different from ebsco subject different from other subjects (like image-tagging)
    - when to use linked data, when to use algorithm

---

### [getting a job](http://2016.code4lib.org/What-does-it-take-to-get-a-job-these-days-Analyzing-jobscode4liborg-data-to-understand-current-technology-skillsets)

by [monica-maceli](http://2016.code4lib.org/speakers.html#monica-maceli), from [Pratt](https://www.pratt.edu/academics/information/)

- curriculum analysis

    - curriculum -> jobs -> practitioners -- where are the gaps? --> curriculum
    - looked through boatload of programs
    - measuered topic areas and number of courses
    - cool, crawling the catalogs of programs with beautiful soup

- jobs analysis

    - text based data like title, location, and human tagging
    - db dump: titles, descriptions, editor-assigned tags
    - analysis with R
        - text-mining with tm package
        - plotting correlations with R graphics package
        - term-clustering with hclust in core stats package
        - showed summary: developer / services & web / metadata + archivist...
        - javascript, php, xml, metadata...
        - looked at related terms of main terms

- practitioners' needs

    - [John Burke's 2015 survey](http://users.miamioh.edu/burkejj/)
    - commonly occuring skillsets

---

### [blacklight authorities browse](http://2016.code4lib.org/Building-a-userfriendly-authorities-browse-in-Blacklight)

by (http://2016.code4lib.org/speakers.html#jennifer-colt) and Frances Webb

- less duplication and more clarity compared to voyager
- tried to avoid any dead-ends
    - eg 'heart attack' -> see 'myocardial infarction'
    - they've made sure that all bib alternate-terms bring up results

- doesn't need to affect the UI, can just focus on making sure the indexer works well

- beware of undifferentiated name-records in reconciliation

- they make a db of if this, see this -- and index that db info into the solr record

- sort vs filing -- interesting examples of things to watch out for, eg example of 'dutch east indies' concept vs 'the dutch in east indies' concept

---

### [Utilizing-digital-scholarship-to-foster-new-research-in-Special-Collections](http://2016.code4lib.org/Making-new-discoveries-from-old-data-Utilizing-digital-scholarship-to-foster-new-research-in-Special-Collections)

by (http://2016.code4lib.org/speakers.html#matt-carruthers)

- result, visualization on demand, customized to user's research question

- findings -- people, organizations, x
    - EAD -> [EAC-CPF](http://www2.archivists.org/groups/technical-subcommittee-on-eac-cpf/encoded-archival-context-corporate-bodies-persons-and-families-eac-cpf) -- companion standard

- tools
    - see slide showing 'commonly available tools'

- eac-cpf -> xslt -> tab-delimited text

- xslt
    - name of connection
    - type of entity
    - type of connection
    - link to more info

- visualization
    - [cytoscape](http://www.cytoscape.org) -- desktop
    - showed example of children's literature graph
    - shows relationship by color-coded connector
    - but has a cloud-service, [CyNetShare](http://idekerlab.github.io/cy-net-share/)
        - showed example, with short google url

- goals
    - streamline the workflow
    - pilot projects
    - cynetshare is opensource, so they could also host local publications

---

### [Building-a-multiprocessing-web-crawler-for-ethnographic-research](http://2016.code4lib.org/Curate-my-web-crawl-Building-a-multiprocessing-web-crawler-for-ethnographic-research)

by (http://2016.code4lib.org/speakers.html#kim-pham) and (http://2016.code4lib.org/speakers.html#kirsta-stapelfeldt) and 'Alejandro Paz'

- "...current mobilizations of public opinion rarely stop at borders..." -- uh, was it Nancy Frasier?

- mediacat -- django app
    - uses a library called [readability](https://github.com/buriy/python-readability)

- good listing of challenges in presentation

- [code](https://github.com/UTMediaCAT)

---
