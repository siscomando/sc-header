sc-header
============

This is sc-header element to all the header of the SisComando app.

Usage
======

### Step 1: Use 'core-header' class
Use the class 'core-header' to the core-header-panel shadow DOM to make the select
in content tag correctly. This is way that we have to apply effects. It's "polymized"!
Internally this occurs if you to use core-header-panel because of this:
```
<content select="core-toolbar, .core-header"></content>
```

```
...
<body>
 <core-header-panel>
    <!-- We using the class core-header to apply effects from paper-elements -->
     <sc-header class="core-header">
     </sc-header>
 </core-heder-panel>
```

### Step 2: To define attribute issueInfo
The issueInfo receives the values to show in header. The default required fields are:
register, title, uga, ugs, created_at.

- register is ticket number
- title is the service name
- uga is responsible sector by treatment
- ugs is responsible sector by customer agreement
- create_at is date that ticket that was created by final customer

```
...
<body>
 <core-header-panel>
     <sc-header class="core-header"
     issueInfo=='{"register": "#2015RI/000046XXX", "title":"SICAP - SISTEMA DE CALCULOS E PERICIAS - AMBIENTE", "uga": "SUPGS", "ugs": "SUNFJ", "created_at":"19/02/2015 13h27"}'>
     </sc-header>
 </core-heder-panel>
```

### Final: Your app must have this appearance
```
<body fullbleed vertical layout unresolved>

  <core-header-panel>
      <sc-header class="core-header"
      issueInfo ='{"register": "#2015RI/000046393", "title":"SICAP - SISTEMA DE CALCULOS E PERICIAS - AMBIENTE", "uga": "SUPGS", "ugs": "SUNFJ", "created_at":"19/02/2015 13h27"}'>
      </sc-header>
  </core-header-panel>


</body>
```

Advanced Usage
===============

### Search
The search feature uses the core-ajax component to search. It's expected by default the fields:

```
{
    "thumbnail": "http://api.randomuser.me/portraits/thumb/men/70.jpg",
    "short_header": "umnome_umadesc",
    "description": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam commodo nisl in accumsan consequat. Donec vitae lectus tempor.",
    "type_content": {
        "name": "mural",
        "icon_img": "http://lorempixel.com/16/16/",
        "icon_html": "<i class='fb-iconfb-heart'>"
    },
    "dated": "21/03/2015 18h21"
}
```
This requires that your model have something similar the fields above.
