---
layout: page
title: Home
id: home
permalink: /
---

# Bienvenue ! 🌱

<p style="padding: 3em 1em; background: #f5f7ff; border-radius: 4px;">
  Take a look at <span style="font-weight: bold">[[Your first note]]</span> to get started on your exploration.
</p>

Ce lieu est avant tout un espace personnel, mon petit bout d'internet où je peux exposer un peu tout ce qui m'anime et ce que je suis. Un petit cheminement vers plus d'épanouissement et de confiance en moi.

Je l'ai voulu dans l'esprit des pages personnelles qu'on pouvait encore trouver il y a de ça une dizaine d'années, avant que tout le monde commence à se soucier de ce que les autres penseront de leurs créations.



<strong>Les notes récemment mises à jour</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
