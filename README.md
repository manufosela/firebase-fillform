# firebase-fillform [![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/manufosela/firebase-fillform)

Form to fill firebase path. 

Is mandatory it exists in the path at least one entry. The component uses the first entry in the path to get the fields and generate the form.
Works with an array of objects with a level of deep. The fields can be simple fields or arrays.
For example:

"candidatos" : [ {
    "cliente_potencial" : [ "Cliente1" ],
    "edad" : 46,
    "nivel_ingles" : "A2",
    "nombre" : "prueba",
    "perfil" : [ "FrontEnd" ]
  }
]

https://github.com/manufosela/firebase-fillform

# Use
<firebase-fillform path="/firebase_path" api-key="firebase_api_key" domain="firebase_domain"></firebase-fillform>

Put the component in your polymer app.

* **path** value of the path to get fields to fill
* **api-key** value of the api-key of your firebase database
* **domain** value of the domain of your firebase database.

<!---
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="firebase-fillform.html">
    <style>
      html, body { height:500px; max-height:500px; min-height:500px; }
    </style>
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
<firebase-fillform path="/candidatos" api-key="AIzaSyBZBEvTJmRwVorU7a5V4PZR6QXCkrx7tdM" domain="karteradekontratacion"></firebase-fillform>
```
