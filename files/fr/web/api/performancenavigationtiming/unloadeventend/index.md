---
title: PerformanceNavigationTiming.unloadEventEnd
slug: Web/API/PerformanceNavigationTiming/unloadEventEnd
tags:
  - API
  - Property
  - Propriété
  - Reference
  - PerformanceNavigationTiming
  - Performance Web
translation_of: Web/API/PerformanceNavigationTiming/unloadEventEnd
---
<div>{{APIRef("Navigation Timing")}}{{SeeCompatTable}}</div>

<p>La propriété <strong><code>unloadEventEnd</code></strong> en lecture seule retourne un <a href="/fr/docs/Web/API/DOMHighResTimeStamp"><code>timestamp</code></a> représentant la valeur temporelle égale au temps immédiatement après la fin de l'événement de déchargement du document précédent par l'agent utilisateur. S'il n'y a pas de document précédent, la valeur de cette propriété est <code>0</code>.</p>

<h2 id="Syntax">Syntaxe</h2>

<pre class="brush:js"><var>perfEntry</var>.unloadEventEnd;</pre>

<h3 id="Return_Value">Valeur de retour</h3>

<p>Un <a href="/fr/docs/Web/API/DOMHighResTimeStamp"><code>timestamp</code></a> représentant une valeur temporelle égale au temps immédiatement après que l'agent utilisateur ait terminé l'événement de déchargement du document précédent.</p>

<h2 id="Example">Exemple</h2>

<p>L'exemple suivant illustre l'utilisation de cette propriété.</p>

<pre class="brush:js">function print_nav_timing_data() {
  // Utilise getEntriesByType() pour obtenir uniquement les événements de type "navigation".
  let perfEntries = performance.getEntriesByType("navigation");

  for (let i = 0; i &lt; perfEntries.length; i++) {
    console.log("= Entrée de navigation : entry[" + i + "]");
    let p = perfEntries[i];
    // propriétés du DOM
    console.log("Contenu du DOM chargé = " + (p.domContentLoadedEventEnd - p.domContentLoadedEventStart));
    console.log("Contenu du DOM complet = " + p.domComplete);
    console.log("Contenu du DOM interactif = " + p.interactive);

    // temps de chargement et de déchargement des documents
    console.log("Document chargé = " + (p.loadEventEnd - p.loadEventStart));
    console.log("Document déchargé = " + (p.unloadEventEnd - p.unloadEventStart));

    // autres propriétés
    console.log("type = " + p.type);
    console.log("redirectCount = " + p.redirectCount);
  }
}
</pre>

<h2 id="Specifications">Spécifications</h2>

<table class="standard-table">
  <thead>
    <tr>
      <th scope="col">Spécification</th>
      <th scope="col">Statut</th>
      <th scope="col">Commentaire</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>{{SpecName('Navigation Timing Level 2',
        '#dom-performancenavigationtiming-unloadeventend', 'unloadEventEnd')}}</td>
      <td>{{Spec2('Navigation Timing Level 2')}}</td>
      <td>Définition initiale.</td>
    </tr>
  </tbody>
</table>

<h2 id="Browser_compatibility">Compatibilité des navigateurs</h2>

<p>{{Compat("api.PerformanceNavigationTiming.unloadEventEnd")}}</p>