# Conexión ESP32 con AWS

## Enlaces adicionales:

- Notebook en Google Colab: [Enlace](https://colab.research.google.com/drive/1Clb5V8ymgrTo86_vCC9nAFpP6yE7fI9F?usp=sharing)

## ¿Cómo ejecutar?:
- Generar credenciales para un objeto en AWS IoT
- Generar un archivo `Secrets.h` en el que se pegarán todas las credenciales:

```cpp
#include <pgmspace.h>
 
#define SECRET
#define THINGNAME ""                         //change this
 
const char WIFI_SSID[] = "";               //change this
const char WIFI_PASSWORD[] = "";           //change this
const char AWS_IOT_ENDPOINT[] = "";       //change this
 
// Amazon Root CA 1
static const char AWS_CERT_CA[] PROGMEM = R"EOF(
-----BEGIN CERTIFICATE-----

-----END CERTIFICATE-----
)EOF";
 
// Device Certificate                                               //change this
static const char AWS_CERT_CRT[] PROGMEM = R"KEY(
-----BEGIN CERTIFICATE-----

-----END CERTIFICATE-----
)KEY";
 
// Device Private Key                                               //change this
static const char AWS_CERT_PRIVATE[] PROGMEM = R"KEY(
-----BEGIN RSA PRIVATE KEY-----

-----END RSA PRIVATE KEY-----
)KEY";
```
