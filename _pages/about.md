---
layout: about
title: about
permalink: /
subtitle: Staff AI Research Scientist, Natural Language Processing, Writer Inc.

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info:

selected_papers: false # rendered in the page body instead, so the heading can link to Google Scholar
social: true # includes social icons at the bottom of the page

announcements:
  enabled: false # includes a list of news items
  scrollable: false # adds a vertical scroll bar if there are more than 3 news items
  limit: 3 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
---

I am a Staff AI Research Scientist at [Writer](https://writer.com/) and Visiting Researcher in the [Natural Language Processing (NLP) group](https://www.cst.cam.ac.uk/research/themes/natural-language-processing) at the University of Cambridge.

My main research focus is automatic Grammatical Error Detection and Correction (GED/GEC), but I have also worked on codeswitching (using more than one language in a sentence), automatic annotation, artificial data generation, robust evaluation, and discourse parsing. I built and maintain the ERRor ANnotation Toolkit ([ERRANT](https://github.com/chrisjbryant/errant)), which is widely used to measure progress in GEC, and also led the Building Educational Applications Shared Task on Grammatical Error Correction ([BEA-2019](https://www.cl.cam.ac.uk/research/nl/bea2019st/)).

I completed my PhD as a member of [Churchill College](https://www.chu.cam.ac.uk/) at the University of Cambridge where I was supervised by [Ted Briscoe](https://www.cl.cam.ac.uk/~ejb1/) and supported by the Institute for Automated Language Teaching and Assessment ([ALTA](http://alta.cambridgeenglish.org/)). Before that, I worked as a Research Assistant in the [School of Computing](https://www.comp.nus.edu.sg/) at the National University of Singapore under [Hwee Tou Ng](https://www.comp.nus.edu.sg/~nght/). I completed a MSc in Speech and Language Processing and an undergraduate MA(Hons) in Chinese and Linguistics, both at the [University of Edinburgh](https://www.ed.ac.uk/).

Download: <a href="{{ '/assets/pdf/cv/2026_CV_Academic.pdf' | relative_url }}">Academic CV</a>  
Download: <a href="{{ '/assets/pdf/cv/2026_CV_Industry.pdf' | relative_url }}">Industry CV</a>

<h2>
  <a href="https://scholar.google.com/citations?user=jMq-Pg4AAAAJ" style="color: inherit">selected publications</a>
</h2>

<div class="publications">
  {% bibliography --group_by none --query @*[selected=true]* %}
</div>
