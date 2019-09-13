# LOH(): Brecha de seguridad

Sois miembros de un nuevo grupo de hackers y el pasado fin de semana entrásteis en varios equipos consiguiendo datos sensibles de algunos de los usuarios, entre los cuales se encuentran algunos personajes famosos.

Vuestro grupo, **Legion of Hell**, o "LOH()", ahora necesita publicar los datos para que todo el mundo pueda acceder a ellos y completar así su venganza.

Como hay un poco de prisa os van a facilitar instrucciones para crear, de manera incremental, una webapp donde consultar los datos:

## Fase 1

Vamos a pintar una primera versión de los datos, sin filtrado ni nada, lo importante es que la información esté fuera.

Pero el grupo de back tiene que preparar el siguiente ataque así que nos han proporcionado un mock de los datos finales para que podamos ir avanzado:

```json
[
  {
    "name": "Francisco Molina",
    "email": "paco.molina@gmail.com",
    "passwords": ["redbull", "contraseña", "god"],
    "bank": {
      "iban": "ES57 3919 3283 8402 7522 0643",
      "pin": "8970"
    }
  },
  {
    "name": "Bruno Díaz",
    "email": "bruno.diaz@aol.com",
    "passwords": ["bruno-y-ricardo", "thebatrocks", "BB"],
    "bank": {
      "iban": "US24 0776 0001 0000 0000 0001",
      "pin": "0228"
    }
  },
  {
    "name": "Angeles Iglesias",
    "email": "angeles.iglesias@hotmail.com",
    "passwords": ["sword", "0000", "123"],
    "bank": {
      "iban": "ES39 2002 4104 2471 4443 4466",
      "pin": "6732"
    }
  },
  {
    "name": "Lourdes Parra",
    "email": "lourdes.parra@gmail.com",
    "passwords": ["bonnie", "123", "0000"],
    "bank": {
      "iban": "ES23 9636 3150 7215 8752 3353",
      "pin": "3127"
    }
  }
]
```

De cada usuario habéis conseguido: el nombre, el email, las 3 últimas contraseñas, y con esos datos, el IBAN del banco y su PIN para la oficina online.

Nos piden que la aplicación esté hecha con React y que pinte estos datos con estilo espartano, en el componente `App.js`.

## Fase 2

La **Tech lead** de LOH() os pide ahora que organicemos un poco el proyecto para que no parezcamos un grupo de indio de hacking, que se vea que aquí hay nivel.

Nos piden al menos 4 componentes nuevos:

- `Page.js`, que se cargará desde `App.js` y mostrará nuestra página principal.
- `Header.js`, que en un futuro contendrá nuestro logo pero nadie está muy seguro de ello porque la gente de programación no encuentra a un diseñador al que chantajear para que haga el logo, por ahora tendrá el título "Legion of Hell".
- `DataList.js`, con la lista de datos.
- `DataCard`, con la tarjeta de datos de cada usuario hackeado.
- `Footer.js`, con el texto "LOH()" y un pequeño reloj con la hora local del usuario, que tirará del estado de su propio componente, no de `App.js`.

## Fase 3

Parece que la api se le está atragantando al equipo de back porque hay personajes importantes y las autoridades están intentando localizar el origen del problema (vosotros).

Os piden que vayáis avanzado y creéis un componente `Filters.js` con un filtro por el email, de manera que cualquiera pueda consultar si su email ha sido comprometido.

La UX Lead Engineer no quiere que se filtre con un botón, sino que conforme escriba el usuario se vayan filtrando los datos.

## Fase 4

Parece que es necesario mostrar cuántos registros habéis conseguido así que nos piden un componente `Status.js` localizado entre los filtros y el listado, que mostrará en todo momento los datos mostrados. Si al filtrar hay 3 registros, tendrá que decir "Mostrando 3 registros", si solo hay uno "Mostrando 1 registro", y así.

Todavía no se sabe cuántos datos se han recogido.

## Fase 5

Vale, el grupo del back ha repelido el ataque del gobierno y por fin ha tenido tiempo de preparar el backend para la api final, y este es nuestro endpoint: `https://raw.githubusercontent.com/Adalab/m3-tutoria-2/master/assets/data/bulk.json`.

> Os avisan de que el formato final puede diferir del que enviaron para los datos iniciales.

Todo debería seguir igual salvo que hay que usar [la fuente `Ubuntu Mono`](https://fonts.google.com/specimen/Ubuntu+Mono), y bajo el nombre del equipo debe aparecer la fecha del ataque que debe estar incluída en los datos que devuelve el servidor.

## Fase 6

Una vez completado todo esto os piden darle un aspecto muy hacker, os dan libertar, pero quieren ver qué sois capaces de hacer.

**¡Al turrón!**