---
title: BirdIdentifierBackend | v1 v1.0.0
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - ruby: Ruby
  - python: Python
  - php: PHP
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v4.0.1 -->

<h1 id="birdidentifierbackend-v1">BirdIdentifierBackend | v1 v1.0.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

<h1 id="birdidentifierbackend-v1-birds">Birds</h1>

## post__birds_identification_classify

> Code samples

```shell
# You can also use wget
curl -X POST /birds/identification/classify \
  -H 'Content-Type: multipart/form-data'

```

```http
POST /birds/identification/classify HTTP/1.1

Content-Type: multipart/form-data

```

```javascript
const inputBody = '{
  "image": "string"
}';
const headers = {
  'Content-Type':'multipart/form-data'
};

fetch('/birds/identification/classify',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'multipart/form-data'
}

result = RestClient.post '/birds/identification/classify',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'multipart/form-data'
}

r = requests.post('/birds/identification/classify', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'multipart/form-data',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/birds/identification/classify', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/birds/identification/classify");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"multipart/form-data"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/birds/identification/classify", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /birds/identification/classify`

> Body parameter

```yaml
image: string

```

<h3 id="post__birds_identification_classify-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|version|query|integer,string(int32)|false|none|
|body|body|object|true|none|
|» image|body|[IFormFile](#schemaiformfile)(binary)|false|none|

<h3 id="post__birds_identification_classify-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__birds_identification_persona

> Code samples

```shell
# You can also use wget
curl -X POST /birds/identification/persona \
  -H 'Content-Type: multipart/form-data'

```

```http
POST /birds/identification/persona HTTP/1.1

Content-Type: multipart/form-data

```

```javascript
const inputBody = '{
  "image": "string"
}';
const headers = {
  'Content-Type':'multipart/form-data'
};

fetch('/birds/identification/persona',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'multipart/form-data'
}

result = RestClient.post '/birds/identification/persona',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'multipart/form-data'
}

r = requests.post('/birds/identification/persona', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'multipart/form-data',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/birds/identification/persona', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/birds/identification/persona");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"multipart/form-data"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/birds/identification/persona", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /birds/identification/persona`

> Body parameter

```yaml
image: string

```

<h3 id="post__birds_identification_persona-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|version|query|integer,string(int32)|false|none|
|body|body|object|true|none|
|» image|body|[IFormFile](#schemaiformfile)(binary)|false|none|

<h3 id="post__birds_identification_persona-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="birdidentifierbackend-v1-heartbeat">Heartbeat</h1>

## get__heartbeat

> Code samples

```shell
# You can also use wget
curl -X GET /heartbeat

```

```http
GET /heartbeat HTTP/1.1

```

```javascript

fetch('/heartbeat',
{
  method: 'GET'

})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/heartbeat',
  params: {
  }

p JSON.parse(result)

```

```python
import requests

r = requests.get('/heartbeat')

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/heartbeat', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/heartbeat");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/heartbeat", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /heartbeat`

<h3 id="get__heartbeat-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

<h2 id="tocS_IFormFile">IFormFile</h2>
<!-- backwards compatibility -->
<a id="schemaiformfile"></a>
<a id="schema_IFormFile"></a>
<a id="tocSiformfile"></a>
<a id="tocsiformfile"></a>

```json
"string"

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string(binary)|false|none|none|

