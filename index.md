---
layout: default
title: Project site
tagline: Go for it 
description: This is GitHub Pages
v1: abcd
v2: efgh
work_left:
  - name: isitgo
    image: /images/isitgo.png
    caption: isitgoonair.net homepage
    description: a website
  - name: disko
    image: /images/disko.png
    caption: Disko
    description: a website
animals:
   - family: mammal 
     nme: dolphin
   - family: mammal 
     nme: whale
   - family: bird 
     nme: sparrow
---


### Github front matter with liquid tags

Github jekyll support liquid tag using double curly braces with object "page".

I have created the following front matters with custom variables such as tagline, description, v1 and v2

```
 ---
 layout: page
 title: Project site
 tagline: Go for it 
 description: This is GitHub Pages
 v1: abcd
 v2: efgh
animals:
   - family: mammal 
     nme: dolphin
   - family: mammal 
     nme: whale
   - family: bird 
     nme: sparrow
 ---
```

### Using the variables via liquid tag

To get the values of the custom variables from the front matters, use liquid tags.
Jekyll liquid tags consist of double curly braces like so.

```
  {% raw %}  {{page.v1}} {% endraw %}
  {% raw %}  {{page.v2}}  {% endraw %}
```

**The result**

**tagline value is:** {{page.tagline}}

**description value is:** {{page.description}}

**v1 value is:** {{page.v1}}
**v2 value is:** {{page.v2}}

### Liquid code CONTROLS using curly braces and percentage signs

**Collection of items**

Retrieve data on **animals**
{% for item in page.animals %}
  family:{{ item.family }} <br/>
  name: {{ item.nme }}<br/>
{% endfor %}


Retrieve data on **work-left**

{% for item in page.work_left %}
  Name is:{{ item.name }} <br/>
  image is: {{ item.image }}<br/>
  description: {{item.description}}<br/>
{% endfor %}

     
  
---

Others


