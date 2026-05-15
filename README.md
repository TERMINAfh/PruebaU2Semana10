# Actividad 2.6 | Web Scraping con Cheerio

========================================================================
## Objetivo

Procesar HTML en backend usando Node.js, Express y Cheerio
para extraer información y devolverla de forma
estructurada mediante un endpoint API.

========================================================================

## Tec. utilizadas para el desarrollo

-Node.js, Express y Cheerio.

========================================================================

## Instalación

PS C:\Users\Alumnos\Documents\actividad_2_6_cheerio> npm init -y
Wrote to C:\Users\Alumnos\Documents\actividad_2_6_cheerio\package.json:

{
  "name": "actividad_2_6_cheerio",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "type": "commonjs"
}

PS C:\Users\Alumnos\Documents\actividad_2_6_cheerio> npm install express cheerio axios
npm warn deprecated whatwg-encoding@3.1.1: Use @exodus/bytes instead for a more spec-conformant and faster implementation

added 102 packages, and audited 103 packages in 1m

43 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

========================================================================

## Ejecución
 BASH
node src/server.js

========================================================================

## Servidor

 TXT
http://localhost:3000

## Endpoint

### GET /api/scrape

Extrae información desde el archivo HTML local.

### Respuesta

{"success":true,"total":3,"data":[{"name":"Alien vs Depredador","price":"$15.000","stock":"Disponible"},{"name":"Gundam - Comandante Qan","price":"$35.000","stock":"Sin stock"},{"name":"Dark Souls Figura de Caballero Oscuro Vol.3","price":"$55.000","stock":"Disponible"}]}


## Datos extraídos

Utilizando selectores CSS con Cheerio:

 Selector | Dato 
 
 `.name`  | Nombre producto 
 `.price` | Precio 
 `.stock` | Estado stock 

## Manejo de errores

- Archivo scrapeService lo escribi mal ERROR: scrapServices - SOLUCION: scrapeService.
- Errores internos del src por rutas mal escritas.
- Arreglar el css para poder inicializarlo con el html (20 min masomenos analizando)

## Estructura del proyecto

El número de serie del volumen es 78B6-DD46
C:.
├───node_modules
│   ├───accepts
│   ├───agent-base
│   │   ├───dist
│   │   │   └───src
│   │   └───src
│   ├───asynckit
│   │   └───lib
│   ├───axios
│   │   ├───dist
│   │   │   ├───browser
│   │   │   ├───esm
│   │   │   └───node
│   │   └───lib
│   │       ├───adapters
│   │       ├───cancel
│   │       ├───core
│   │       ├───defaults
│   │       ├───env
│   │       │   └───classes
│   │       ├───helpers
│   │       └───platform
│   │           ├───browser
│   │           │   └───classes
│   │           ├───common
│   │           └───node
│   │               └───classes
│   ├───body-parser
│   │   ├───lib
│   │   │   └───types
│   │   └───node_modules
│   │       └───iconv-lite
│   │           ├───encodings
│   │           │   └───tables
│   │           ├───lib
│   │           │   └───helpers
│   │           └───types
│   ├───boolbase
│   ├───bytes
│   ├───call-bind-apply-helpers
│   │   ├───.github
│   │   └───test
│   ├───call-bound
│   │   ├───.github
│   │   └───test
│   ├───cheerio
│   │   ├───dist
│   │   │   ├───browser
│   │   │   │   ├───api
│   │   │   │   └───parsers
│   │   │   ├───commonjs
│   │   │   │   ├───api
│   │   │   │   └───parsers
│   │   │   └───esm
│   │   │       ├───api
│   │   │       └───parsers
│   │   └───src
│   │       ├───api
│   │       └───parsers
│   ├───cheerio-select
│   │   └───lib
│   │       └───esm
│   ├───combined-stream
│   │   └───lib
│   ├───content-disposition
│   ├───content-type
│   ├───cookie
│   ├───cookie-signature
│   ├───css-select
│   │   └───lib
│   │       ├───esm
│   │       │   ├───helpers
│   │       │   └───pseudo-selectors
│   │       ├───helpers
│   │       └───pseudo-selectors
│   ├───css-what
│   │   └───lib
│   │       ├───commonjs
│   │       └───es
│   ├───debug
│   │   └───src
│   ├───delayed-stream
│   │   └───lib
│   ├───depd
│   │   └───lib
│   │       └───browser
│   ├───dom-serializer
│   │   └───lib
│   │       └───esm
│   ├───domelementtype
│   │   └───lib
│   │       └───esm
│   ├───domhandler
│   │   └───lib
│   │       └───esm
│   ├───domutils
│   │   └───lib
│   │       └───esm
│   ├───dunder-proto
│   │   ├───.github
│   │   └───test
│   ├───ee-first
│   ├───encodeurl
│   ├───encoding-sniffer
│   │   └───dist
│   │       ├───commonjs
│   │       └───esm
│   ├───entities
│   │   └───lib
│   │       ├───esm
│   │       │   └───generated
│   │       └───generated
│   ├───es-define-property
│   │   ├───.github
│   │   └───test
│   ├───es-errors
│   │   ├───.github
│   │   └───test
│   ├───es-object-atoms
│   │   ├───.github
│   │   └───test
│   ├───es-set-tostringtag
│   │   └───test
│   ├───escape-html
│   ├───etag
│   ├───express
│   │   └───lib
│   ├───finalhandler
│   ├───follow-redirects
│   ├───form-data
│   │   ├───lib
│   │   └───node_modules
│   │       ├───mime-db
│   │       └───mime-types
│   ├───forwarded
│   ├───fresh
│   ├───function-bind
│   │   ├───.github
│   │   └───test
│   ├───get-intrinsic
│   │   ├───.github
│   │   └───test
│   ├───get-proto
│   │   ├───.github
│   │   └───test
│   ├───gopd
│   │   ├───.github
│   │   └───test
│   ├───has-symbols
│   │   ├───.github
│   │   └───test
│   │       └───shams
│   ├───has-tostringtag
│   │   ├───.github
│   │   └───test
│   │       └───shams
│   ├───hasown
│   │   └───.github
│   ├───htmlparser2
│   │   ├───dist
│   │   │   ├───commonjs
│   │   │   └───esm
│   │   ├───node_modules
│   │   │   └───entities
│   │   │       ├───dist
│   │   │       │   ├───commonjs
│   │   │       │   │   ├───generated
│   │   │       │   │   └───internal
│   │   │       │   └───esm
│   │   │       │       ├───generated
│   │   │       │       └───internal
│   │   │       └───src
│   │   │           ├───generated
│   │   │           └───internal
│   │   └───src
│   ├───http-errors
│   ├───https-proxy-agent
│   │   └───dist
│   ├───iconv-lite
│   │   ├───.github
│   │   ├───.idea
│   │   │   ├───codeStyles
│   │   │   └───inspectionProfiles
│   │   ├───encodings
│   │   │   └───tables
│   │   └───lib
│   ├───inherits
│   ├───ipaddr.js
│   │   └───lib
│   ├───is-promise
│   ├───math-intrinsics
│   │   ├───.github
│   │   ├───constants
│   │   └───test
│   ├───media-typer
│   ├───merge-descriptors
│   ├───mime-db
│   ├───mime-types
│   ├───ms
│   ├───negotiator
│   │   └───lib
│   ├───nth-check
│   │   └───lib
│   │       └───esm
│   ├───object-inspect
│   │   ├───.github
│   │   ├───example
│   │   └───test
│   │       └───browser
│   ├───on-finished
│   ├───once
│   ├───parse5
│   │   ├───dist
│   │   │   ├───cjs
│   │   │   │   ├───common
│   │   │   │   ├───parser
│   │   │   │   ├───serializer
│   │   │   │   ├───tokenizer
│   │   │   │   └───tree-adapters
│   │   │   ├───common
│   │   │   ├───parser
│   │   │   ├───serializer
│   │   │   ├───tokenizer
│   │   │   └───tree-adapters
│   │   └───node_modules
│   │       └───entities
│   │           ├───dist
│   │           │   ├───commonjs
│   │           │   │   └───generated
│   │           │   └───esm
│   │           │       └───generated
│   │           └───src
│   │               └───generated
│   ├───parse5-htmlparser2-tree-adapter
│   │   └───dist
│   │       └───cjs
│   ├───parse5-parser-stream
│   │   └───dist
│   │       └───cjs
│   ├───parseurl
│   ├───path-to-regexp
│   │   └───dist
│   ├───proxy-addr
│   ├───proxy-from-env
│   ├───qs
│   │   ├───.github
│   │   ├───dist
│   │   ├───lib
│   │   └───test
│   ├───range-parser
│   ├───raw-body
│   │   └───node_modules
│   │       └───iconv-lite
│   │           ├───encodings
│   │           │   └───tables
│   │           ├───lib
│   │           │   └───helpers
│   │           └───types
│   ├───router
│   │   └───lib
│   ├───safer-buffer
│   ├───send
│   ├───serve-static
│   ├───setprototypeof
│   │   └───test
│   ├───side-channel
│   │   ├───.github
│   │   └───test
│   ├───side-channel-list
│   │   ├───.github
│   │   └───test
│   ├───side-channel-map
│   │   ├───.github
│   │   └───test
│   ├───side-channel-weakmap
│   │   ├───.github
│   │   └───test
│   ├───statuses
│   ├───toidentifier
│   ├───type-is
│   │   └───node_modules
│   │       └───content-type
│   │           └───dist
│   ├───undici
│   │   ├───docs
│   │   │   └───docs
│   │   │       ├───api
│   │   │       └───best-practices
│   │   ├───lib
│   │   │   ├───api
│   │   │   ├───cache
│   │   │   ├───core
│   │   │   ├───dispatcher
│   │   │   ├───encoding
│   │   │   ├───handler
│   │   │   ├───interceptor
│   │   │   ├───llhttp
│   │   │   ├───mock
│   │   │   ├───util
│   │   │   └───web
│   │   │       ├───cache
│   │   │       ├───cookies
│   │   │       ├───eventsource
│   │   │       ├───fetch
│   │   │       ├───infra
│   │   │       ├───subresource-integrity
│   │   │       ├───webidl
│   │   │       └───websocket
│   │   │           └───stream
│   │   ├───scripts
│   │   └───types
│   ├───unpipe
│   ├───vary
│   ├───whatwg-encoding
│   │   └───lib
│   ├───whatwg-mimetype
│   │   └───lib
│   └───wrappy
└───src
    ├───controllers
    ├───data
    ├───routes
    ├───services
    └───Styles
PS C:\Users\Alumnos\Documents\actividad_2_6_cheerio> tree
Listado de rutas de carpetas
El número de serie del volumen es 78B6-DD46
C:.
├───node_modules
│   ├───accepts
│   ├───agent-base
│   │   ├───dist
│   │   │   └───src
│   │   └───src
│   ├───asynckit
│   │   └───lib
│   ├───axios
│   │   ├───dist
│   │   │   ├───browser
│   │   │   ├───esm
│   │   │   └───node
│   │   └───lib
│   │       ├───adapters
│   │       ├───cancel
│   │       ├───core
│   │       ├───defaults
│   │       ├───env
│   │       │   └───classes
│   │       ├───helpers
│   │       └───platform
│   │           ├───browser
│   │           │   └───classes
│   │           ├───common
│   │           └───node
│   │               └───classes
│   ├───body-parser
│   │   ├───lib
│   │   │   └───types
│   │   └───node_modules
│   │       └───iconv-lite
│   │           ├───encodings
│   │           │   └───tables
│   │           ├───lib
│   │           │   └───helpers
│   │           └───types
│   ├───boolbase
│   ├───bytes
│   ├───call-bind-apply-helpers
│   │   ├───.github
│   │   └───test
│   ├───call-bound
│   │   ├───.github
│   │   └───test
│   ├───cheerio
│   │   ├───dist
│   │   │   ├───browser
│   │   │   │   ├───api
│   │   │   │   └───parsers
│   │   │   ├───commonjs
│   │   │   │   ├───api
│   │   │   │   └───parsers
│   │   │   └───esm
│   │   │       ├───api
│   │   │       └───parsers
│   │   └───src
│   │       ├───api
│   │       └───parsers
│   ├───cheerio-select
│   │   └───lib
│   │       └───esm
│   ├───combined-stream
│   │   └───lib
│   ├───content-disposition
│   ├───content-type
│   ├───cookie
│   ├───cookie-signature
│   ├───css-select
│   │   └───lib
│   │       ├───esm
│   │       │   ├───helpers
│   │       │   └───pseudo-selectors
│   │       ├───helpers
│   │       └───pseudo-selectors
│   ├───css-what
│   │   └───lib
│   │       ├───commonjs
│   │       └───es
│   ├───debug
│   │   └───src
│   ├───delayed-stream
│   │   └───lib
│   ├───depd
│   │   └───lib
│   │       └───browser
│   ├───dom-serializer
│   │   └───lib
│   │       └───esm
│   ├───domelementtype
│   │   └───lib
│   │       └───esm
│   ├───domhandler
│   │   └───lib
│   │       └───esm
│   ├───domutils
│   │   └───lib
│   │       └───esm
│   ├───dunder-proto
│   │   ├───.github
│   │   └───test
│   ├───ee-first
│   ├───encodeurl
│   ├───encoding-sniffer
│   │   └───dist
│   │       ├───commonjs
│   │       └───esm
│   ├───entities
│   │   └───lib
│   │       ├───esm
│   │       │   └───generated
│   │       └───generated
│   ├───es-define-property
│   │   ├───.github
│   │   └───test
│   ├───es-errors
│   │   ├───.github
│   │   └───test
│   ├───es-object-atoms
│   │   ├───.github
│   │   └───test
│   ├───es-set-tostringtag
│   │   └───test
│   ├───escape-html
│   ├───etag
│   ├───express
│   │   └───lib
│   ├───finalhandler
│   ├───follow-redirects
│   ├───form-data
│   │   ├───lib
│   │   └───node_modules
│   │       ├───mime-db
│   │       └───mime-types
│   ├───forwarded
│   ├───fresh
│   ├───function-bind
│   │   ├───.github
│   │   └───test
│   ├───get-intrinsic
│   │   ├───.github
│   │   └───test
│   ├───get-proto
│   │   ├───.github
│   │   └───test
│   ├───gopd
│   │   ├───.github
│   │   └───test
│   ├───has-symbols
│   │   ├───.github
│   │   └───test
│   │       └───shams
│   ├───has-tostringtag
│   │   ├───.github
│   │   └───test
│   │       └───shams
│   ├───hasown
│   │   └───.github
│   ├───htmlparser2
│   │   ├───dist
│   │   │   ├───commonjs
│   │   │   └───esm
│   │   ├───node_modules
│   │   │   └───entities
│   │   │       ├───dist
│   │   │       │   ├───commonjs
│   │   │       │   │   ├───generated
│   │   │       │   │   └───internal
│   │   │       │   └───esm
│   │   │       │       ├───generated
│   │   │       │       └───internal
│   │   │       └───src
│   │   │           ├───generated
│   │   │           └───internal
│   │   └───src
│   ├───http-errors
│   ├───https-proxy-agent
│   │   └───dist
│   ├───iconv-lite
│   │   ├───.github
│   │   ├───.idea
│   │   │   ├───codeStyles
│   │   │   └───inspectionProfiles
│   │   ├───encodings
│   │   │   └───tables
│   │   └───lib
│   ├───inherits
│   ├───ipaddr.js
│   │   └───lib
│   ├───is-promise
│   ├───math-intrinsics
│   │   ├───.github
│   │   ├───constants
│   │   └───test
│   ├───media-typer
│   ├───merge-descriptors
│   ├───mime-db
│   ├───mime-types
│   ├───ms
│   ├───negotiator
│   │   └───lib
│   ├───nth-check
│   │   └───lib
│   │       └───esm
│   ├───object-inspect
│   │   ├───.github
│   │   ├───example
│   │   └───test
│   │       └───browser
│   ├───on-finished
│   ├───once
│   ├───parse5
│   │   ├───dist
│   │   │   ├───cjs
│   │   │   │   ├───common
│   │   │   │   ├───parser
│   │   │   │   ├───serializer
│   │   │   │   ├───tokenizer
│   │   │   │   └───tree-adapters
│   │   │   ├───common
│   │   │   ├───parser
│   │   │   ├───serializer
│   │   │   ├───tokenizer
│   │   │   └───tree-adapters
│   │   └───node_modules
│   │       └───entities
│   │           ├───dist
│   │           │   ├───commonjs
│   │           │   │   └───generated
│   │           │   └───esm
│   │           │       └───generated
│   │           └───src
│   │               └───generated
│   ├───parse5-htmlparser2-tree-adapter
│   │   └───dist
│   │       └───cjs
│   ├───parse5-parser-stream
│   │   └───dist
│   │       └───cjs
│   ├───parseurl
│   ├───path-to-regexp
│   │   └───dist
│   ├───proxy-addr
│   ├───proxy-from-env
│   ├───qs
│   │   ├───.github
│   │   ├───dist
│   │   ├───lib
│   │   └───test
│   ├───range-parser
│   ├───raw-body
│   │   └───node_modules
│   │       └───iconv-lite
│   │           ├───encodings
│   │           │   └───tables
│   │           ├───lib
│   │           │   └───helpers
│   │           └───types
│   ├───router
│   │   └───lib
│   ├───safer-buffer
│   ├───send
│   ├───serve-static
│   ├───setprototypeof
│   │   └───test
│   ├───side-channel
│   │   ├───.github
│   │   └───test
│   ├───side-channel-list
│   │   ├───.github
│   │   └───test
│   ├───side-channel-map
│   │   ├───.github
│   │   └───test
│   ├───side-channel-weakmap
│   │   ├───.github
│   │   └───test
│   ├───statuses
│   ├───toidentifier
│   ├───type-is
│   │   └───node_modules
│   │       └───content-type
│   │           └───dist
│   ├───undici
│   │   ├───docs
│   │   │   └───docs
│   │   │       ├───api
│   │   │       └───best-practices
│   │   ├───lib
│   │   │   ├───api
│   │   │   ├───cache
│   │   │   ├───core
│   │   │   ├───dispatcher
│   │   │   ├───encoding
│   │   │   ├───handler
│   │   │   ├───interceptor
│   │   │   ├───llhttp
│   │   │   ├───mock
│   │   │   ├───util
│   │   │   └───web
│   │   │       ├───cache
│   │   │       ├───cookies
│   │   │       ├───eventsource
│   │   │       ├───fetch
│   │   │       ├───infra
│   │   │       ├───subresource-integrity
│   │   │       ├───webidl
│   │   │       └───websocket
│   │   │           └───stream
│   │   ├───scripts
│   │   └───types
│   ├───unpipe
│   ├───vary
│   ├───whatwg-encoding
│   │   └───lib
│   ├───whatwg-mimetype
│   │   └───lib
│   └───wrappy
└───src
    ├───controllers
    ├───data
    ├───routes
    ├───services
    └───Styles
