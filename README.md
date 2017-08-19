# firebase-fillform [![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/manufosela/firebase-fillform)

It generate a form based in a firebase path to fill it easyly.

Works with an array of objects with a level of deep. 

The fields can be simple fields or arrays.

For example: 
```json
{
  "movies" : [ {
    "classification" : ["science fiction", "adventure" ],
    "colección" : "Star Wars",
    "director" : "George Lucas",
    "formato" : "blue-ray",
    "titulo" : "The Phantom Menace",
    "valoracion" : 10
   } ]
 }
```

Is mandatory it exists in the path at least one entry because **The component uses the first entry in the path to get the fields and generate the form.**

You can use a firebase path to show a select option in a field. To do this the firebase path must have the same name of the field.

For example:
```json
{
  "classification" : [ "science fiction", "adventure", "drama", "comedy", "horror", "psychological thriller", "crime", "romantic", "historical" ],
  "movies" : [ {
    "classification" : ["science fiction", "adventure" ],
    "colección" : "Star Wars",
    "director" : "George Lucas",
    "formato" : "blue-ray",
    "titulo" : "The Phantom Menace",
    "valoracion" : 10
   } ]
 }
```

Now the *clasification* field it is not a free field, it is shown like a select with the list values.

https://github.com/manufosela/firebase-fillform

# Use
<firebase-fillform path="/firebase_path" api-key="firebase_api_key" domain="firebase_domain"></firebase-fillform>

Put the component in your polymer app.

* **path** value of the path to get fields to fill
* **api-key** value of the api-key of your firebase database
* **domain** value of the domain of your firebase database.

**IMPORTANT:** If use 2 or more *firebase-fillform* components in the same page, only define path and api-key in the first component to avoid conflicts and firebase-app object redefinition.

Configure Firebase:
* Enable google login method authentication
* Add a domain if necessary

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

<h3>Basic firebase-fillform demo</h3>
<h4>Simple</h4>
<firebase-fillform name='simple-example' path="/clasificacion" api-key="AIzaSyBaehmgaklz_vaqsBVZhvBm0fsD7PF8PHQ" domain="coleccion-peliculas"></firebase-fillform>
<h3>Complex</h3>
<firebase-fillform name='complex-example' path="/peliculas" debug="true"></firebase-fillform>
</div>
```
