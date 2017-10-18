# The Portia-IoT API documentation (v1)

## Querying Portia

### Last dimension

* **URL:**  `http://io.portia.supe.solutions/api/v1/device/`**`<device_hash>`**`/port/`**`<port>`**`/sensor/`**`<sensor>`**`/dimension/`**`<dimension>`**`/last`

* **Method:** `POST`

* **Required URL Params:**

  * `device_hash=[string]`
  * `port=[integer]`
  * `sensor=[integer]`
  * `dimension=[integer]`

* **Required POST Params:**

  * `user_hash=[string]`

* **Success Response:**

  * **Code:** `200 OK`

    * **Content:** `JSON object`

* **Error Response:**

  * **Code:** `403 Forbidden`

    * **Troubleshooting:** `Error on token authentication`

  * **Code:** `404 Not Found`

    * **Troubleshooting:** `Error on request params`

* **Sample Call:**

  * **Javascript:**
    ```javascript
      $.ajax({
        url: "http://io.portia.supe.solutions/api/v1/device/Bk4TsimTbj8vt3hww/port/1/sensor/1/dimension/1/last",
        dataType: "json",
        type: "GET",
        success: function(r) {
          console.log(r);
        }
      });
    ```
    * **Return:** `[{"server_timestamp":1508271656566,"package_local_timestamp":1508271655,"package_type_code":1,"package_username":"agrosensor","package_device_hash":"Bk4TsimTbj8vt3hww","dimension_port_id":2,"dimension_sensor_id":1,"dimension_code":1,"dimension_value":23.2,"dimension_value_string":null,"dimension_unity_code":1,"dimension_thing_code":1,"dimension_thing_local_id":-1}]`

  * **Python:**
    ```python
      import requests
      url = 'http://io.portia.supe.solutions/api/v1/device/Bk4TsimTbj8vt3hww/port/1/sensor/1/dimension/1/last'

      # GET
      r = requests.get(url)

      # Response
      r.text
    ```
    * **Return:** `[{"server_timestamp":1508271656566,"package_local_timestamp":1508271655,"package_type_code":1,"package_username":"agrosensor","package_device_hash":"Bk4TsimTbj8vt3hww","dimension_port_id":2,"dimension_sensor_id":1,"dimension_code":1,"dimension_value":23.2,"dimension_value_string":null,"dimension_unity_code":1,"dimension_thing_code":1,"dimension_thing_local_id":-1}]`

  * **Java:**
    ```java
      StringBuilder result = new StringBuilder();

      URL url = new URL("http://io.portia.supe.solutions/api/v1/device/Bk4TsimTbj8vt3hww/port/1/sensor/1/dimension/1/last");

      HttpURLConnection conn = (HttpURLConnection) url.openConnection();
      conn.setRequestMethod("GET");

      BufferedReader rd = new BufferedReader(new InputStreamReader(conn.getInputStream()));

      String line;
      while ((line = rd.readLine()) != null) {
        result.append(line);
      }

      rd.close();

      return result.toString();
    ```
    * **Return:** `[{"server_timestamp":1508271656566,"package_local_timestamp":1508271655,"package_type_code":1,"package_username":"agrosensor","package_device_hash":"Bk4TsimTbj8vt3hww","dimension_port_id":2,"dimension_sensor_id":1,"dimension_code":1,"dimension_value":23.2,"dimension_value_string":null,"dimension_unity_code":1,"dimension_thing_code":1,"dimension_thing_local_id":-1}]`

### Dimensions with time intervals

* **URL:**  `http://io.portia.supe.solutions/api/v1/device/`**`<device_hash>`**`/port/`**`<port>`**`/sensor/`**`<sensor>`**`/dimension/`**`<dimension>`**`/from/`**`<from_timestamp>`**`/to/`**`<to_timestamp>`**

* **Method:** `POST`

* **Required URL Params:**

  * `device_hash=[string]`
  * `port=[integer]`
  * `sensor=[integer]`
  * `dimension=[integer]`
  * `from_timestamp=[unsigned long]`
  * `to_timestamp=[unsigned long]`

* **Required POST Params:**

  * `user_hash=[string]`

* **Success Response:**

  * **Code:** `200 OK`

    * **Content:** `JSON object`

* **Error Response:**

  * **Code:** `403 Forbidden`

    * **Troubleshooting:** `Error on token authentication`

  * **Code:** `404 Not Found`

    * **Troubleshooting:** `Error on request params`

* **Sample Call:**

  * **Javascript:**
    ```javascript
      $.ajax({
        url: "http://io.portia.supe.solutions/api/v1/device/Bk4TsimTbj8vt3hww/port/1/sensor/1/dimension/1/from/1508330521/to/1508330591",
        dataType: "json",
        type: "GET",
        success: function(r) {
          console.log(r);
        }
      });
    ```
    * **Return:** `[{"server_timestamp":1508271656566,"package_local_timestamp":1508271655,"package_type_code":1,"package_username":"agrosensor","package_device_hash":"Bk4TsimTbj8vt3hww","dimension_port_id":2,"dimension_sensor_id":1,"dimension_code":1,"dimension_value":23.2,"dimension_value_string":null,"dimension_unity_code":1,"dimension_thing_code":1,"dimension_thing_local_id":-1}, {"server_timestamp":1508271656566,"package_local_timestamp":1508271655,"package_type_code":1,"package_username":"agrosensor","package_device_hash":"Bk4TsimTbj8vt3hww","dimension_port_id":2,"dimension_sensor_id":1,"dimension_code":1,"dimension_value":23.2,"dimension_value_string":null,"dimension_unity_code":1,"dimension_thing_code":1,"dimension_thing_local_id":-1}]`

  * **Python:**
    ```python
      import requests
      url = 'http://io.portia.supe.solutions/api/v1/device/Bk4TsimTbj8vt3hww/port/1/sensor/1/dimension/1/from/1508330521/to/1508330591'

      # GET
      r = requests.get(url)

      # Response
      r.text
    ```
    * **Return:** `[{"server_timestamp":1508271656566,"package_local_timestamp":1508271655,"package_type_code":1,"package_username":"agrosensor","package_device_hash":"Bk4TsimTbj8vt3hww","dimension_port_id":2,"dimension_sensor_id":1,"dimension_code":1,"dimension_value":23.2,"dimension_value_string":null,"dimension_unity_code":1,"dimension_thing_code":1,"dimension_thing_local_id":-1}, {"server_timestamp":1508271656566,"package_local_timestamp":1508271655,"package_type_code":1,"package_username":"agrosensor","package_device_hash":"Bk4TsimTbj8vt3hww","dimension_port_id":2,"dimension_sensor_id":1,"dimension_code":1,"dimension_value":23.2,"dimension_value_string":null,"dimension_unity_code":1,"dimension_thing_code":1,"dimension_thing_local_id":-1}]`

  * **Java:**
    ```java
      StringBuilder result = new StringBuilder();

      URL url = new URL("http://io.portia.supe.solutions/api/v1/device/Bk4TsimTbj8vt3hww/port/1/sensor/1/dimension/1/from/1508330521/to/1508330591");

      HttpURLConnection conn = (HttpURLConnection) url.openConnection();
      conn.setRequestMethod("GET");

      BufferedReader rd = new BufferedReader(new InputStreamReader(conn.getInputStream()));

      String line;
      while ((line = rd.readLine()) != null) {
        result.append(line);
      }

      rd.close();

      return result.toString();
    ```
    * **Return:** `[{"server_timestamp":1508271656566,"package_local_timestamp":1508271655,"package_type_code":1,"package_username":"agrosensor","package_device_hash":"Bk4TsimTbj8vt3hww","dimension_port_id":2,"dimension_sensor_id":1,"dimension_code":1,"dimension_value":23.2,"dimension_value_string":null,"dimension_unity_code":1,"dimension_thing_code":1,"dimension_thing_local_id":-1}, {"server_timestamp":1508271656566,"package_local_timestamp":1508271655,"package_type_code":1,"package_username":"agrosensor","package_device_hash":"Bk4TsimTbj8vt3hww","dimension_port_id":2,"dimension_sensor_id":1,"dimension_code":1,"dimension_value":23.2,"dimension_value_string":null,"dimension_unity_code":1,"dimension_thing_code":1,"dimension_thing_local_id":-1}]`

### Last dimension

* **URL:**  `http://io.portia.supe.solutions/api/v1/devices/`

* **Method:** `POST`

* **Required POST Params:**

  * `user_hash=[string]`

* **Success Response:**

  * **Code:** `200 OK`

    * **Content:** `JSON object`

* **Error Response:**

  * **Code:** `403 Forbidden`

    * **Troubleshooting:** `Error on token authentication`

* **Sample Call:**

  * **Javascript:**
    ```javascript
      $.ajax({
        url: "http://io.portia.supe.solutions/api/v1/devices",
        dataType: "json",
        type: "GET",
        success: function(r) {
          console.log(r);
        }
      });
    ```
    * **Return:** `["WR3432-24D22waew4", "R3wrwq32-24FwaeR4", "d3wrwq32r24Fwa566", "4333Arwq3wfw24Fwa"]`

  * **Python:**
    ```python
      import requests
      url = 'http://io.portia.supe.solutions/api/v1/devices'

      # GET
      r = requests.get(url)

      # Response
      r.text
    ```
    * **Return:** `["WR3432-24D22waew4", "R3wrwq32-24FwaeR4", "d3wrwq32r24Fwa566", "4333Arwq3wfw24Fwa"]`

  * **Java:**
    ```java
      StringBuilder result = new StringBuilder();

      URL url = new URL("http://io.portia.supe.solutions/api/v1/devices");

      HttpURLConnection conn = (HttpURLConnection) url.openConnection();
      conn.setRequestMethod("GET");

      BufferedReader rd = new BufferedReader(new InputStreamReader(conn.getInputStream()));

      String line;
      while ((line = rd.readLine()) != null) {
        result.append(line);
      }

      rd.close();

      return result.toString();
    ```
    * **Return:** `["WR3432-24D22waew4", "R3wrwq32-24FwaeR4", "d3wrwq32r24Fwa566", "4333Arwq3wfw24Fwa"]`

<!-- ### List users devices/paths

* **URL:**  `http://io.portia.supe.solutions/api/v1/user/<username>/devices`

* **Method:**  `GET`

*  **Required POST Params:**

 * `text=[string]`
 * `similarity=[float]` [between 0 and 1]
 * `ontology=[ontologyID]` [see ontology IDs]
   

* **Success Response:**

  * **Code:** 200 <br />
  * **Content:** JSON object <br />

* **Error Responses:**

  * **Code:** `415 Unsupported Media Type` <br />
  * **Troubleshooting:** Check parameters


  * **Code:**  `404 NOT FOUND`  <br />
  * **Troubleshooting:**  Ontology ID not found

  * **Sample Call:**

  * **Code:** 
    ```javascript
      $.ajax({
        url: "http://ontomatch.lis.ic.unicamp.br/api/rest/resource",
        dataType: "json",
        type : "POST",
        data: { text: "chest pain", similariy: 0.8, ontology:"hfo" },
        success : function(r) {
          console.log(r);
        }
      });
    ```

    * **Return:**  `{"uri":"http://bmi.utah.edu/ontologies/hfontology/C0008031","label":"Chest Pain","similarity":1.0}`

### Based on a given similarity threshold (/api/rest/resources)


* **URL:**    `/api/rest/resource`

* **Method:**  `POST`
  
*  **Required POST Params:**

   * `text=[string]`
   * `n=[float]` [the service will return the **n** most similar entities]
   * `ontology=[ontologyID]` [see ontology IDs]
     

* **Success Response:**

  * **Code:** 200 <br />
  * **Content:** JSON array <br />

 
* **Error Responses:**

  * **Code:** `415 Unsupported Media Type` <br />
    **Troubleshooting:** Check parameters


  * **Code:**  `404 NOT FOUND`  <br />
    **Troubleshooting:**  Ontology ID not found

* **Sample Call:**
  
    * **Code:** 
  ```javascript
    $.ajax({
      url: "http://ontomatch.lis.ic.unicamp.br/api/rest/resources",
      dataType: "json",
      type : "POST",
      data: { text: "chest pain", n: 5, ontology:"hfo" },
      success : function(r) {
        console.log(r);
      }
    });
  ```

    * **Return:**  

    ```json
    [
    {"uri":"http://bmi.utah.edu/ontologies/hfontology/C0008031","label":"Chest Pain","similarity":1.0},
    {"uri":"http://bmi.utah.edu/ontologies/hfontology/C0030193","label":"Pain","similarity":0.7071067690849304},
    {"uri":"http://bmi.utah.edu/ontologies/hfontology/C0000737","label":"Abdominal Pain","similarity":0.5}
    ]
    ``` 
-->