---
title: alarms.Alarm
slug: Mozilla/Add-ons/WebExtensions/API/alarms/Alarm
tags:
  - API
  - Add-ons
  - Extensions
  - Non-standard
  - Reference
  - Type
  - WebExtensions
  - alarm
  - alarms
translation_of: Mozilla/Add-ons/WebExtensions/API/alarms/Alarm
---
<div>{{AddonSidebar}}</div>

<p>Cette interface fournit des informations sur une alarme donnée. Cet objet est retourné à partir de {{WebExtAPIRef('alarms.get()')}} et {{WebExtAPIRef('alarms.getAll()')}} et est passé au gestionnaire d'évènement {{WebExtAPIRef('alarms.onAlarm')}}.</p>

<h2 id="Type">Type</h2>

<p>Les valeurs de ce type sont des objets contenant les propriétés suivantes :</p>

<dl>
 <dt><code>name</code></dt>
 <dd><code>string</code> Une chaîne de caractères contenant le nom de l'alarme. Ce nom provient de celui qui a été fourni à la méthode {{WebExtAPIRef('alarms.create()')}} lors de la création de l'alarme.</dd>
 <dt><code>scheduledTime</code></dt>
 <dd><code>double</code> Un nombre qui représente l'heure à laquelle l'alarme doit être déclenchée, exprimée <a href="https://fr.wikipedia.org/wiki/Heure_Unix">en nombre de millisecondes depuis epoch</a>.</dd>
 <dt><code>periodInMinutes</code>{{optional_inline}}</dt>
 <dd><code>double</code> Un nombre qui, s'il n'est pas <code>null</code>, indique que l'alarme est périodique et fournit la période.</dd>
</dl>

<h2 id="Compatibilité_des_navigateur">Compatibilité des navigateur</h2>

<p>{{Compat("webextensions.api.alarms.Alarm")}}</p>

<p>{{WebExtExamples}}</p>

<p><strong>Remerciements :</strong></p>

<p>Cette API est basée sur l'API Chromium <a href="https://developer.chrome.com/extensions/alarms"><code>chrome.alarms</code></a>.</p>

<p>Les données de compatibilité relatives à Microsoft Edge sont fournies par Microsoft Corporation et incluses ici sous la licence Creative Commons Attribution 3.0 pour les États-Unis.</p>