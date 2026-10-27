---
layout: page
permalink: /publications/
title: publications
description: publications in reversed chronological order.
nav: true
nav_order: 5
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">

<h2 class="bibliography">preprints & under review</h2>
{% bibliography --group_by none --query @*[status=preprint] %}

<h2 class="bibliography">published</h2>
{% bibliography --query @*[status!=preprint] %}

</div>
