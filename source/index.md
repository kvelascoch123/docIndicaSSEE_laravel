---
title: API Reference

language_tabs:
- bash
- javascript
- php

includes:

search: true

toc_footers:
- <a href='http://github.com/mpociot/documentarian'>Documentation Powered by Documentarian</a>
---
<!-- START_INFO -->
# Info

Welcome to the generated API reference.
[Get Postman Collection](www.sidesoft.com.ec/docs/collection.json)

<!-- END_INFO -->

#APIs Alexa


<!-- START_86fc8006ecce93479f27eed48f6131e1 -->
## Autenticación del usuario.

Validación del usuario registrado. Table: al_user

> Example request:

```bash
curl -X GET -G "www.sidesoft.com.ec/api/alexa/user/1/1?alias_name=sed&user_password=consequatur" \
    -H "Content-Type: application/json" \
    -d '{"nombreUsuario":"fugit","contrase\u00f1a":"laudantium"}'

```

```javascript
const url = new URL("www.sidesoft.com.ec/api/alexa/user/1/1");

    let params = {
            "alias_name": "sed",
            "user_password": "consequatur",
        };
    Object.keys(params).forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
}

let body = {
    "nombreUsuario": "fugit",
    "contrase\u00f1a": "laudantium"
}

fetch(url, {
    method: "GET",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get("www.sidesoft.com.ec/api/alexa/user/1/1", [
    'headers' => [
            "Content-Type" => "application/json",
        ],
    'query' => [
            "alias_name" => "sed",
            "user_password" => "consequatur",
        ],
    'json' => [
            "nombreUsuario" => "fugit",
            "contraseña" => "laudantium",
        ],
]);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (500):

```json
{
    "message": "Server Error"
}
```

### HTTP Request
`GET api/alexa/user/{nombre}/{contrasena}`

#### Body Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    nombreUsuario | string |  required  | Nombre del usuario.
    contraseña | string |  required  | Contraseña del usuario'.
#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    alias_name |  required  | Nombre del usuario.
    user_password |  required  | The id of the user.

<!-- END_86fc8006ecce93479f27eed48f6131e1 -->

<!-- START_977e907b88276390119e1fa42a06bbb2 -->
## Reconocimiento del usuario.

Solicitud del nombre del usuario, bienvenida. Table: al_user

> Example request:

```bash
curl -X GET -G "www.sidesoft.com.ec/api/alexa/user/1?alias_name=vero" \
    -H "Content-Type: application/json" \
    -d '{"nombreUsuario":"dolorum"}'

```

```javascript
const url = new URL("www.sidesoft.com.ec/api/alexa/user/1");

    let params = {
            "alias_name": "vero",
        };
    Object.keys(params).forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
}

let body = {
    "nombreUsuario": "dolorum"
}

fetch(url, {
    method: "GET",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get("www.sidesoft.com.ec/api/alexa/user/1", [
    'headers' => [
            "Content-Type" => "application/json",
        ],
    'query' => [
            "alias_name" => "vero",
        ],
    'json' => [
            "nombreUsuario" => "dolorum",
        ],
]);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (500):

```json
{
    "message": "Server Error"
}
```

### HTTP Request
`GET api/alexa/user/{nombre}`

#### Body Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    nombreUsuario | string |  required  | Nombre del usuario.
#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    alias_name |  required  | Nombre del usuario.

<!-- END_977e907b88276390119e1fa42a06bbb2 -->

<!-- START_434fbc0237e6bb50c5db08f2228b8564 -->
## Áreas.

Todas las áreas registradas.

> Example request:

```bash
curl -X GET -G "www.sidesoft.com.ec/api/alexa/areas?ninguno=nihil" \
    -H "Content-Type: application/json" \
    -d '{"ninguno":"vero"}'

```

```javascript
const url = new URL("www.sidesoft.com.ec/api/alexa/areas");

    let params = {
            "ninguno": "nihil",
        };
    Object.keys(params).forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
}

let body = {
    "ninguno": "vero"
}

fetch(url, {
    method: "GET",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get("www.sidesoft.com.ec/api/alexa/areas", [
    'headers' => [
            "Content-Type" => "application/json",
        ],
    'query' => [
            "ninguno" => "nihil",
        ],
    'json' => [
            "ninguno" => "vero",
        ],
]);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (500):

```json
{
    "message": "Server Error"
}
```

### HTTP Request
`GET api/alexa/areas`

#### Body Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    ninguno | ninguno |  optional  | optional Ninguno.
#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    ninguno |  optional  | optional Ningun parametro.

<!-- END_434fbc0237e6bb50c5db08f2228b8564 -->

<!-- START_3f8be4723214005fb4a3d877c4457b31 -->
## Factor.

Todos los factors registrados mediante el área. Table: al_factor inner al_area

> Example request:

```bash
curl -X GET -G "www.sidesoft.com.ec/api/alexa/area/1?description=eveniet" \
    -H "Content-Type: application/json" \
    -d '{"nombreArea":"voluptatum"}'

```

```javascript
const url = new URL("www.sidesoft.com.ec/api/alexa/area/1");

    let params = {
            "description": "eveniet",
        };
    Object.keys(params).forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
}

let body = {
    "nombreArea": "voluptatum"
}

fetch(url, {
    method: "GET",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get("www.sidesoft.com.ec/api/alexa/area/1", [
    'headers' => [
            "Content-Type" => "application/json",
        ],
    'query' => [
            "description" => "eveniet",
        ],
    'json' => [
            "nombreArea" => "voluptatum",
        ],
]);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (500):

```json
{
    "message": "Server Error"
}
```

### HTTP Request
`GET api/alexa/area/{description}`

#### Body Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    nombreArea | string |  required  | Nombre del area.
#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    description |  required  | Descripción del área .

<!-- END_3f8be4723214005fb4a3d877c4457b31 -->

<!-- START_9cd2d091485eebceaa2e1f418103ca02 -->
## Indicadores.

Todos los indicadores registrados según el factor. Table: al_indicators inner al_factor

> Example request:

```bash
curl -X GET -G "www.sidesoft.com.ec/api/alexa/indicadores/1?factor=odio" \
    -H "Content-Type: application/json" \
    -d '{"nombreFactor":"dolores"}'

```

```javascript
const url = new URL("www.sidesoft.com.ec/api/alexa/indicadores/1");

    let params = {
            "factor": "odio",
        };
    Object.keys(params).forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
}

let body = {
    "nombreFactor": "dolores"
}

fetch(url, {
    method: "GET",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get("www.sidesoft.com.ec/api/alexa/indicadores/1", [
    'headers' => [
            "Content-Type" => "application/json",
        ],
    'query' => [
            "factor" => "odio",
        ],
    'json' => [
            "nombreFactor" => "dolores",
        ],
]);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (500):

```json
{
    "message": "Server Error"
}
```

### HTTP Request
`GET api/alexa/indicadores/{nombreFactor}`

#### Body Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    nombreFactor | string |  required  | Nombre del factor.
#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    factor |  required  | Nombre del factor.

<!-- END_9cd2d091485eebceaa2e1f418103ca02 -->

<!-- START_713b8a0bc9bfbddcb6e0baf708038119 -->
## Monto Actual Año.

Cálculo del monto actual respecto al Año. Table: al_indicators_years

> Example request:

```bash
curl -X GET -G "www.sidesoft.com.ec/api/alexa/monthly/1/1?name=est&year=ratione" \
    -H "Content-Type: application/json" \
    -d '{"nombreIndicador":"quaerat","a\u00f1o":"delectus"}'

```

```javascript
const url = new URL("www.sidesoft.com.ec/api/alexa/monthly/1/1");

    let params = {
            "name": "est",
            "year": "ratione",
        };
    Object.keys(params).forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
}

let body = {
    "nombreIndicador": "quaerat",
    "a\u00f1o": "delectus"
}

fetch(url, {
    method: "GET",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get("www.sidesoft.com.ec/api/alexa/monthly/1/1", [
    'headers' => [
            "Content-Type" => "application/json",
        ],
    'query' => [
            "name" => "est",
            "year" => "ratione",
        ],
    'json' => [
            "nombreIndicador" => "quaerat",
            "año" => "delectus",
        ],
]);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (500):

```json
{
    "message": "Server Error"
}
```

### HTTP Request
`GET api/alexa/monthly/{anio}/{nombre}`

#### Body Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    nombreIndicador | string |  required  | Nombre del indicador.
    año | string |  required  | Año de busqueda .
#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    name |  required  | Nombre del indicador.
    year |  required  | Año de busqueda.

<!-- END_713b8a0bc9bfbddcb6e0baf708038119 -->

<!-- START_647de820ee7a5b00d45d3a5c1d1a6e90 -->
## Token Insert.

Insertar token.
Guardar el token , usuario, indicador consultado en la tabla al_token_user.

> Example request:

```bash
curl -X GET -G "www.sidesoft.com.ec/api/alexa/tokenInsert/1/1/1/1?nombre_indicador=eum&month=numquam&year=non&token=cum" \
    -H "Content-Type: application/json" \
    -d '{"nombreIndicador":"aut","mes":"tempore","a\u00f1o":11,"token":"odio"}'

```

```javascript
const url = new URL("www.sidesoft.com.ec/api/alexa/tokenInsert/1/1/1/1");

    let params = {
            "nombre_indicador": "eum",
            "month": "numquam",
            "year": "non",
            "token": "cum",
        };
    Object.keys(params).forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
}

let body = {
    "nombreIndicador": "aut",
    "mes": "tempore",
    "a\u00f1o": 11,
    "token": "odio"
}

fetch(url, {
    method: "GET",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get("www.sidesoft.com.ec/api/alexa/tokenInsert/1/1/1/1", [
    'headers' => [
            "Content-Type" => "application/json",
        ],
    'query' => [
            "nombre_indicador" => "eum",
            "month" => "numquam",
            "year" => "non",
            "token" => "cum",
        ],
    'json' => [
            "nombreIndicador" => "aut",
            "mes" => "tempore",
            "año" => "11",
            "token" => "odio",
        ],
]);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (500):

```json
{
    "message": "Server Error"
}
```

### HTTP Request
`GET api/alexa/tokenInsert/{indicador}/{mes}/{anio}/{tokenEncrpt}`

#### Body Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    nombreIndicador | string |  required  | Nombre del indicador.
    mes | string |  required  | Mes de busqueda.
    año | integer |  required  | Año de busqueda.
    token | string |  required  | Token encrypt.
#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    nombre_indicador |  required  | Nombre del indicador.
    month |  required  | Mes de busqueda.
    year |  required  | Año de busqueda.
    token |  required  | Token encrypt.

<!-- END_647de820ee7a5b00d45d3a5c1d1a6e90 -->

<!-- START_4810a67f708e8eb514515bfb7c3eb00e -->
## Configuración.

Configuración del usuario y organización.
Utilidad: Determinar la organización del usuario.

> Example request:

```bash
curl -X GET -G "www.sidesoft.com.ec/api/alexa/configuration/1?id_org=et" \
    -H "Content-Type: application/json" \
    -d '{"Id_Organizaci\u00f3n":"et"}'

```

```javascript
const url = new URL("www.sidesoft.com.ec/api/alexa/configuration/1");

    let params = {
            "id_org": "et",
        };
    Object.keys(params).forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
}

let body = {
    "Id_Organizaci\u00f3n": "et"
}

fetch(url, {
    method: "GET",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get("www.sidesoft.com.ec/api/alexa/configuration/1", [
    'headers' => [
            "Content-Type" => "application/json",
        ],
    'query' => [
            "id_org" => "et",
        ],
    'json' => [
            "Id_Organización" => "et",
        ],
]);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (500):

```json
{
    "message": "Server Error"
}
```

### HTTP Request
`GET api/alexa/configuration/{id_org}`

#### Body Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    Id_Organización | string |  required  | Nombre del indicador.
#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    id_org |  required  | Nombre del indicador.

<!-- END_4810a67f708e8eb514515bfb7c3eb00e -->

<!-- START_8240b15b3a3ad14a758c05c0f42039b3 -->
## Comparación.

Comparación de todos los indicadores.

Utilidad: Current_ye

> Example request:

```bash
curl -X GET -G "www.sidesoft.com.ec/api/alexa/comparationGetAll?ninguno=sunt" \
    -H "Content-Type: application/json" \
    -d '{"ninguno":"facere"}'

```

```javascript
const url = new URL("www.sidesoft.com.ec/api/alexa/comparationGetAll");

    let params = {
            "ninguno": "sunt",
        };
    Object.keys(params).forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
}

let body = {
    "ninguno": "facere"
}

fetch(url, {
    method: "GET",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get("www.sidesoft.com.ec/api/alexa/comparationGetAll", [
    'headers' => [
            "Content-Type" => "application/json",
        ],
    'query' => [
            "ninguno" => "sunt",
        ],
    'json' => [
            "ninguno" => "facere",
        ],
]);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (500):

```json
{
    "message": "Server Error"
}
```

### HTTP Request
`GET api/alexa/comparationGetAll`

#### Body Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    ninguno | ninguno |  optional  | optional Ninguno.r.
#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    ninguno |  optional  | optional Ningun parametro.

<!-- END_8240b15b3a3ad14a758c05c0f42039b3 -->

<!-- START_14452c994821a2f21411993c6e5b27db -->
## Comparación.

Comparación del indicador.
Utilidad: Txt_affirmative, respuesta de alexa.

> Example request:

```bash
curl -X GET -G "www.sidesoft.com.ec/api/alexa/comparation/1?ninguno=quo" \
    -H "Content-Type: application/json" \
    -d '{"ninguno":"doloribus"}'

```

```javascript
const url = new URL("www.sidesoft.com.ec/api/alexa/comparation/1");

    let params = {
            "ninguno": "quo",
        };
    Object.keys(params).forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
}

let body = {
    "ninguno": "doloribus"
}

fetch(url, {
    method: "GET",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get("www.sidesoft.com.ec/api/alexa/comparation/1", [
    'headers' => [
            "Content-Type" => "application/json",
        ],
    'query' => [
            "ninguno" => "quo",
        ],
    'json' => [
            "ninguno" => "doloribus",
        ],
]);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (500):

```json
{
    "message": "Server Error"
}
```

### HTTP Request
`GET api/alexa/comparation/{nombre}`

#### Body Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    ninguno | ninguno |  optional  | optional Ninguno.
#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    ninguno |  optional  | optional Ningun parametro.

<!-- END_14452c994821a2f21411993c6e5b27db -->

#APIs Web


<!-- START_5ae08a65ca3674ca267b4dfd59b02e98 -->
## Indicador por mes.

Datos del indicador respecto al mes y año.
Utilidad: Visualización de la pagina respecto a los datos del Indicador y Mes

> Example request:

```bash
curl -X GET -G "www.sidesoft.com.ec/indicadorMY/1/1/1/1?name=ea&month=exercitationem&year=velit&token=placeat" \
    -H "Content-Type: application/json" \
    -d '{"nombreIndicador":"ut","mes":"odio","a\u00f1o":5,"token":"laborum"}'

```

```javascript
const url = new URL("www.sidesoft.com.ec/indicadorMY/1/1/1/1");

    let params = {
            "name": "ea",
            "month": "exercitationem",
            "year": "velit",
            "token": "placeat",
        };
    Object.keys(params).forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
}

let body = {
    "nombreIndicador": "ut",
    "mes": "odio",
    "a\u00f1o": 5,
    "token": "laborum"
}

fetch(url, {
    method: "GET",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get("www.sidesoft.com.ec/indicadorMY/1/1/1/1", [
    'headers' => [
            "Content-Type" => "application/json",
        ],
    'query' => [
            "name" => "ea",
            "month" => "exercitationem",
            "year" => "velit",
            "token" => "placeat",
        ],
    'json' => [
            "nombreIndicador" => "ut",
            "mes" => "odio",
            "año" => "5",
            "token" => "laborum",
        ],
]);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (500):

```json
{
    "message": "Server Error"
}
```

### HTTP Request
`GET indicadorMY/{nombre}/{mes}/{anio}/{token}`

#### Body Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    nombreIndicador | string |  required  | Nombre del indicador.
    mes | string |  required  | Mes de busqueda.
    año | integer |  required  | Año de busqueda.
    token | string |  required  | Token encrypt.
#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    name |  required  | Nombre del indicador.
    month |  required  | Mes de busqueda respecto al indicador.
    year |  required  | Año de busqueda respecto al indicador.
    token |  required  | Token encrypt.

<!-- END_5ae08a65ca3674ca267b4dfd59b02e98 -->

<!-- START_3562ba6d9cac05857ed07381d38de248 -->
## Indicador por año.

Datos del indicador respecto al año.
Utilidad: Visualización de la pagina respecto a los datos del Indicador respecto al Año.

> Example request:

```bash
curl -X GET -G "www.sidesoft.com.ec/indicadorY/1/1/1?name=doloremque&year=quibusdam&token=quia" \
    -H "Content-Type: application/json" \
    -d '{"nombreIndicador":"molestias","a\u00f1o":6,"token":"earum"}'

```

```javascript
const url = new URL("www.sidesoft.com.ec/indicadorY/1/1/1");

    let params = {
            "name": "doloremque",
            "year": "quibusdam",
            "token": "quia",
        };
    Object.keys(params).forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
}

let body = {
    "nombreIndicador": "molestias",
    "a\u00f1o": 6,
    "token": "earum"
}

fetch(url, {
    method: "GET",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get("www.sidesoft.com.ec/indicadorY/1/1/1", [
    'headers' => [
            "Content-Type" => "application/json",
        ],
    'query' => [
            "name" => "doloremque",
            "year" => "quibusdam",
            "token" => "quia",
        ],
    'json' => [
            "nombreIndicador" => "molestias",
            "año" => "6",
            "token" => "earum",
        ],
]);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (500):

```json
{
    "message": "Server Error"
}
```

### HTTP Request
`GET indicadorY/{nombre}/{anio}/{token}`

#### Body Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    nombreIndicador | string |  required  | Nombre del indicador.
    año | integer |  required  | Año de busqueda.
    token | string |  required  | Token encrypt.
#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    name |  required  | Nombre del indicador.
    year |  required  | Año de busqueda respecto al indicador.
    token |  required  | Token encrypt.

<!-- END_3562ba6d9cac05857ed07381d38de248 -->

<!-- START_32537bc0483bd53395292518dc3aeafd -->
## Push Notifications.

Notificación del indicador en aplicación móvil.

> Example request:

```bash
curl -X GET -G "www.sidesoft.com.ec/push/1?token=vero" \
    -H "Content-Type: application/json" \
    -d '{"token":"et"}'

```

```javascript
const url = new URL("www.sidesoft.com.ec/push/1");

    let params = {
            "token": "vero",
        };
    Object.keys(params).forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
}

let body = {
    "token": "et"
}

fetch(url, {
    method: "GET",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get("www.sidesoft.com.ec/push/1", [
    'headers' => [
            "Content-Type" => "application/json",
        ],
    'query' => [
            "token" => "vero",
        ],
    'json' => [
            "token" => "et",
        ],
]);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response:

```json
null
```

### HTTP Request
`GET push/{token}`

#### Body Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    token | string |  required  | Token app_movil.
#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    token |  required  | Token app_movil.

<!-- END_32537bc0483bd53395292518dc3aeafd -->

<!-- START_f245be16f54f8d01fc355fddef8a19ae -->
## Indicador respecto al mes V1.

Versión 1, permite ver la pagina sin cumplir la validación del token ni tiempo límite de visualización.

> Example request:

```bash
curl -X GET -G "www.sidesoft.com.ec/indicadorMYv1/1/1/1?name=ex&month=voluptates&year=et" \
    -H "Content-Type: application/json" \
    -d '{"nombreIndicador":"et","mes":"vel","a\u00f1o":11}'

```

```javascript
const url = new URL("www.sidesoft.com.ec/indicadorMYv1/1/1/1");

    let params = {
            "name": "ex",
            "month": "voluptates",
            "year": "et",
        };
    Object.keys(params).forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
}

let body = {
    "nombreIndicador": "et",
    "mes": "vel",
    "a\u00f1o": 11
}

fetch(url, {
    method: "GET",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get("www.sidesoft.com.ec/indicadorMYv1/1/1/1", [
    'headers' => [
            "Content-Type" => "application/json",
        ],
    'query' => [
            "name" => "ex",
            "month" => "voluptates",
            "year" => "et",
        ],
    'json' => [
            "nombreIndicador" => "et",
            "mes" => "vel",
            "año" => "11",
        ],
]);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (500):

```json
{
    "message": "Server Error"
}
```

### HTTP Request
`GET indicadorMYv1/{nombre}/{mes}/{anio}`

#### Body Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    nombreIndicador | string |  required  | Nombre del indicador.
    mes | string |  required  | Mes de busqueda.
    año | integer |  required  | Año de busqueda.
#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    name |  required  | Nombre del indicador.
    month |  required  | Mes de busqueda respecto al indicador.
    year |  required  | Año de busqueda respecto al indicador.

<!-- END_f245be16f54f8d01fc355fddef8a19ae -->

<!-- START_2a2ade87b5d7c5bda68ab6f49a5aa5fc -->
## Indicador respecto al año V1.

Versión 1, permite ver la pagina sin cumplir la validación del token ni tiempo límite de visualización.

> Example request:

```bash
curl -X GET -G "www.sidesoft.com.ec/indicadorYv1/1/1?name=excepturi&year=id" \
    -H "Content-Type: application/json" \
    -d '{"nombreIndicador":"exercitationem","a\u00f1o":1}'

```

```javascript
const url = new URL("www.sidesoft.com.ec/indicadorYv1/1/1");

    let params = {
            "name": "excepturi",
            "year": "id",
        };
    Object.keys(params).forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
}

let body = {
    "nombreIndicador": "exercitationem",
    "a\u00f1o": 1
}

fetch(url, {
    method: "GET",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get("www.sidesoft.com.ec/indicadorYv1/1/1", [
    'headers' => [
            "Content-Type" => "application/json",
        ],
    'query' => [
            "name" => "excepturi",
            "year" => "id",
        ],
    'json' => [
            "nombreIndicador" => "exercitationem",
            "año" => "1",
        ],
]);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (500):

```json
{
    "message": "Server Error"
}
```

### HTTP Request
`GET indicadorYv1/{nombre}/{anio}`

#### Body Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    nombreIndicador | string |  required  | Nombre del indicador.
    año | integer |  required  | Año de busqueda.
#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    name |  required  | Nombre del indicador.
    year |  required  | Año de busqueda respecto al indicador.

<!-- END_2a2ade87b5d7c5bda68ab6f49a5aa5fc -->

#Controlador Base.


<!-- START_8c1fc07f8977ce5bdd2660544db9d37f -->
## Validacion Usuario Token Web.

Desencriptar el toquen verificar segun el usuario, determinar el limite de visualización de la página web.

> Example request:

```bash
curl -X GET -G "www.sidesoft.com.ec/api/alexa/validateTokenUser/1/1?token=nostrum" \
    -H "Content-Type: application/json" \
    -d '{"token":"iste"}'

```

```javascript
const url = new URL("www.sidesoft.com.ec/api/alexa/validateTokenUser/1/1");

    let params = {
            "token": "nostrum",
        };
    Object.keys(params).forEach(key => url.searchParams.append(key, params[key]));

let headers = {
    "Content-Type": "application/json",
    "Accept": "application/json",
}

let body = {
    "token": "iste"
}

fetch(url, {
    method: "GET",
    headers: headers,
    body: body
})
    .then(response => response.json())
    .then(json => console.log(json));
```

```php

$client = new \GuzzleHttp\Client();
$response = $client->get("www.sidesoft.com.ec/api/alexa/validateTokenUser/1/1", [
    'headers' => [
            "Content-Type" => "application/json",
        ],
    'query' => [
            "token" => "nostrum",
        ],
    'json' => [
            "token" => "iste",
        ],
]);
$body = $response->getBody();
print_r(json_decode((string) $body));
```


> Example response (500):

```json
{
    "message": "Server Error"
}
```

### HTTP Request
`GET api/alexa/validateTokenUser/{token}/{idUser}`

#### Body Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    token | string |  required  | Token encrypt.
#### Query Parameters

Parameter | Status | Description
--------- | ------- | ------- | -----------
    token |  required  | Token encrypt.

<!-- END_8c1fc07f8977ce5bdd2660544db9d37f -->


