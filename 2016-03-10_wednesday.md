### [schedule](http://2016.code4lib.org/schedule/day-3)

---

### keynote

by [head](http://2016.code4lib.org/Gabriel-Weinberg) of duckduckgo

- problems
    - [the pants that stalked me on the web], since 2010
    - prices varying based on users' information 2012
    - no regulation of this
    - filter bubble -- same search; different results
        - can be good in some opt-in contexts, like amazon or netflix
        - problem is not knowing, ann gets msnbc, elaine gets fox news -- people staying in internal bubble which inflames partisanship
        - example using 'gun control' search
    - 17% of americans are altering their use of tech platforms based on snowden revelations

- privacy desire -- some polls show that only single-digit % of users care about privacy. But...
    - 40% of american internet users would like their search engines not to track them
    - 86% have taken some steps to mask digital footprint
    - 91% of adult americans agree or strongly agree that consumers have lost control of how personal info is collected & used by companies

- snowden, apple, europe have initiated talk about privacy

- incognito doesn't prevent tracking while you have any tabs open, many people don't know this

- "frictionless privacy" -- people don't want to be inconvenienced

- [DuckDuckHack](http://duckduckhack.com)
    - for coders to write... plugins?... to allow communities to better get results they want
    - so `MySQL` getting a set of instant answers, or `regex`, or stack-exchange communities
    - ['people in space'](https://duckduckgo.com/?q=people+in+space&t=osx&ia=answer) -- a community developed an api
    - ['color picker'](https://duckduckgo.com/?q=color+picker&t=osx&ia=colorpicker)

- goal
    - building the world's most trusted search engine

- their business model tries to focus on things that google won't try:
    - privacy
    - open-source community search results

- they get them at yahoo and... dig? big?

- bang operator -- from question... what's this?
    - [post](http://mhj.tc/post/60194055815/bangbang-operator-for-duckduckgo)

- good question: thoughts on libraries' desire for 'if you liked this, you might like this' -- thought, there can be ways to enable opt-in in a forthright transparent way, but not a lot of examples in the wild.

- :) -- looking for a verb: 'go duck-it'

---

## lightning talks

Sean Aery from Duke -- Finding Aid work
- sticky title, corresponding series info at top
- added links to images
- sticky menu via scrollspy.js, cherrypicked part of bootstrap
- uses archivespace IDs

Chad (an organizer)
- remembrance of Dan Chudnov's talk
- embiggened for a few years -- they considered bigger venues that were away from the c4l spirit
- conference cost is too inexpensive

Github as Knowledgebase; H.Tebbe/NCState
- templates for high-tech walls and spaces
- they specify dimensions, font-sizes, where bezel-ish things are
- templates initially: intranet, lib website, goggle-drive, computers
- github desktop, can diff images
- challenges -- can be tricky to get people up to speed with github

Leveraging the public cloud to complement your ILS
- Sholmo, [Alma](http://www.exlibrisgroup.com/category/AlmaOverview)
- example of sending notifications to student
- uses [twilio](https://www.twilio.com)

simple javascript making hero
- [#mashcat](http://www.mashcat.info) info
- searchbox example

single sign-on
- steelson smith, yale
- user data is library data... did i get that right?
- more and more library accounts -- ils, illiad, etc
- institutional sso can help campus, but what about guests?
- identity is just another service
- [openID Connect](http://openid.net/connect/) -- Identity over OAuth2 -- great slide
    - users get a single signon, shib and non-shib
    - backend they auth into a service provider -- app goes to provider
    - means you have an OAuth2 server
    - if you have an api-first methodology -- users can use their preferred credentials to use lib systems
    - man this was _great_ -- get those prezi slides

code+art ncstate
- student visualization contest -- hunt library big screens
- Christie Digital Systems (maker of MicroTiles)
- 'creative coding' -- making art with code
- 'fractal forest' -- making fractal trees on a planet
- 'WKNC Visualizer' -- visualizing campus radio listening -- birds, and beat reflection
- not clear how many cs-ers are interested in art, and how many designers are interested in code
- 2 new faculty hires interested in creative coding
- creative-coding workshop vs hackathon -- look at those %s
- competitions may not be best way to get talent
- shifting focus from contest to inclusive programming

[opquenamespace.org](http://opaquenamespace.org)
- ryan wick, oregon state
- they wanted a way to have uris for internal heading-strings
- wanted to define new predicates
- powered by [controlled-vocabulary-manager code](https://github.com/OregonDigital/ControlledVocabularyManager)

metadata story
- robert haschart, uva
- data from delhi, india
- plan-a: change workflow -- can't
- plan-b: ocr -- ocr not quite good enough
- all records contain a 010 field
    - ocr + lccn lookup -- do a lookup in worldcat
    - but some of the records already exist
    - lccn not always unique
    - sometimes page upside down
- plan-c: rotate pages and couple other things -- success

fauxbr, etc in Pika
- james.staub@nashville.gov
- record-grouping
- Life of Pi example -- citwide read
    - patrons with long queues for some overdrives -- others available
- single result citation -- and formats grouped together
- groupwork id

---

[Community-driven AV Solutions](http://2016.code4lib.org/Free-your-workflows-and-the-rest-will-follow-communitydriven-AV-solutions-through-open-source-workflow-development)

by (http://2016.code4lib.org/speakers.html#dinah-handel) and (http://2016.code4lib.org/speakers.html#ashley-blewer)

- workflows often not shared
- practice...
- reasons why people don't share stuff given
- a/v stuff is hard
    - diverse formats, many proprietary
    - big files
- info on open-source, open-access, open-file-formats, microservice, concepts
- media microservices -- did i miss a url? -- bash scripts
- vrecord
- qctools -- helps detect problems after digitization
- media crunch -- verifies files are what they say they are -- and/or media-info?
- archivematica -- uses suite of tools
- mkv - matroska - format or standard being developed
- ffmprovisor -- platform for sharing scripts
- [avaa](http://avaa.bavc.org/artifactatlas/index.php/A/V_Artifact_Atlas) -- [bay area video coalition](https://www.bavc.org/)

---

[Indoor-Positioning-Services-Location-Based-Recommendations](http://2016.code4lib.org/Indoor-Positioning-Services-Location-Based-Recommendations)
by (http://2016.code4lib.org/speakers.html#jim-hahn) from illinois.edu

- can promote e-resources when in stacks
- blue-dot where they are, red-dote where item is
- 'popular items near me'
- ['estimote beacons'](http://estimote.com) -- placed above tiles -- blue-tooth low-energy
    - lighthouse analogy w/radio waves instead of light
- positions into an sql table
- indoor sdk that could infer position -- but they used a map library
- math emergency - trilateration -- measurement of distances
- modular apis -- Minrva APIs
- pased on patron-locations, lookups on shelf-range and popularity
- beacon locations in above tiles -- metal stacks caused problems
- cs students developed app for testing -- tool can infer what beacons are perceived
- there's an estimate testing app
- authentication -- api-tokens
- securing local db
- awareness of estimote-cloud gathering info

---

[ArchivesSpaceArchivematicaDSpace-Workflow-Integration](http://2016.code4lib.org/ArchivesSpaceArchivematicaDSpace-Workflow-Integration)

by (http://2016.code4lib.org/speakers.html#mike-shallcross) -- univ of michigan

- had lots of homegrown systems
- 2014, combined physical/digital processing operations
- dspace since 2008, but now hydra partner
- goals
    - streamline ingest, depost into repository; automate
    - curation eco-system; microservices
- development tasks...
- appraisal tab in archivematica
    - exposes the data archivematica is gathering to curators
    - can characterize content -- they're interested in identifying ie credit-card, ssns, phone-numbers etc
    - review/preview files
    - can tag content
- archivesSpace pane
    - can add premis data, other metadata
    - can add objects
    - can drag and drop files/metadata, and archivematica will go to town on that
    - more info on last slide

---

[Scribe-Toward-a-general-framework-for-community-transcription](http://2016.code4lib.org/Scribe-Toward-a-general-framework-for-community-transcription)

by (http://2016.code4lib.org/speakers.html#paul-beaudoin) of NYPL Labs

- [scribe](https://scribeproject.github.io)
- [zooniverse.org](https://www.zooniverse.org)
- labs and zooniverse came together to work together
- scribe
    - configured around questions
    - type of doc
    - locations in doc
    - questions about the answers to those questions -- they amplify or reduce the validity of the answers
    - notion, one doesn't configure schema, but questions
- example - Emigrant City
    - 5,000 unique contributions; 500,000 classifications
    - user initially asked to make financial box on mortgage amount
    - another user asked to enter amount
    - two other users confirmed that -- in this project that was elevated to 'consensus'
    - example of 60-ish percent confidence on date
- labs.nypl.org

---

[Issues-to-consider-before-pushing-out-an-Open-Source-Project](http://2016.code4lib.org/Issues-to-consider-before-pushing-out-an-Open-Source-Project)

by Edward M. Corrado -- U.of Alabama

- licensing issues
- what do we have to think about in terms of support
- working up a basic checklist
- points
    - are there existing tools
    - does it have to be open-source?
    - legal considerations
    - sustainability and community
    - test
- [beforeOSS](https://docs.google.com/document/d/1qeopBc1X8CQ7gy4uk6oH3XHLt5hIHzJBUKaQY-PWOEQ/edit#heading=h.d5q7ied5yy7w)

---
