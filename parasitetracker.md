---
layout: default
title: "parasite tracker"
status: unlisted
---

Collections related to the [Parasite Tracker](https://parasitetracker.org) project. Click on badge to see records. 

[update page](https://github.com/globalbioticinteractions/globalbioticinteractions.github.io/blob/master/_data/parasitetracker.tsv) / [ask a question](https://github.com/ParasiteTracker/data-issues-observations-and-questions/issues)

|indexed|institution|platform|contact|
|---|---|---|---|---|
{% assign cols = site.data.parasitetracker | sort: "institution" -%}
{% for c in cols -%}
{%- assign globi-badge = c.globi_id | prepend: "https://api.globalbioticinteractions.org/interaction.svg?accordingTo=" | uri_escape -%} 
{%- assign globi-url = c.globi_id | prepend: "https://globalbioticinteractions.org/?accordingTo=" | uri_escape -%} 
[![badge]({{ globi-badge }})]({{ globi-url }}) | {{ c.institution }} | {{ c.platform }} | {{ c.contact }} | 
{% endfor -%}