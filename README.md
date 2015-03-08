sc-header
============

This is sc-header element to all the header of the SisComando app.

Usage
======

### To define attribute issueInfo
The issueInfo receives the values to show in header. The default required fields are:
register, title, uga, ugs, created_at.

- register is ticket number
- title is the service name
- uga is responsible sector by treatment
- ugs is responsible sector by customer agreement
- create_at is date that the ticket was created by final customer

```
...
<body>
 <core-header-panel>
     <sc-header
     issueInfo=='{"register": "#2015RI/000046XXX", "title":"SICAP - SISTEMA DE
     CALCULOS E PERICIAS - AMBIENTE", "uga": "SUPGS", "ugs": "SUNFJ",
     "created_at":"19/02/2015 13h27"}'>
     </sc-header>
 </core-heder-panel>
```
