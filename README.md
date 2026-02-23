\# Membrane API Gateway



Java tabanlı açık kaynaklı API Gateway kullanılarak JSON/SOAP/REST entegrasyonu.



\## Proje Hakkında



Bu projede Membrane API Gateway üzerinde iki farklı entegrasyon gerçekleştirilmiştir:



\- \*\*JSON → SOAP → JSON\*\*: Dış dünyadan gelen JSON istekleri SOAP formatına dönüştürülüp WSDL servisine iletilir, gelen cevap JSON'a çevrilerek döndürülür.

\- \*\*JSON → JSON\*\*: Dış dünyadan gelen JSON istekleri REST servisine iletilir, gelen cevap anlamlı hata kodlarıyla zenginleştirilmiş JSON formatında döndürülür.



\## Endpointler



| Method | URL | Açıklama |

|--------|-----|----------|

| POST | http://localhost:2026/api/hello | JSON → SOAP → JSON |

| POST | http://localhost:2026/api/login | JSON → JSON |

| GET | http://localhost:9000 | Admin Console |



\## Kurulum



1\. \[Membrane API Gateway](https://github.com/membrane/api-gateway/releases/latest) indir ve aç

2\. `conf/proxies.xml` dosyasını bu repodaki ile değiştir

3\. Başlat:

```cmd

cd membrane-api-gateway-7.1.0

membrane.cmd

```



\## Test



\*\*SayHello:\*\*

```json

POST http://localhost:2026/api/hello

{ "Name": "emre" }

```



\*\*Login:\*\*

```json

POST http://localhost:2026/api/login

{ "username": "emre", "password": "123", "rememberMe": false }

```



\## Detaylı Dokümantasyon



Kurulum, konfigürasyon, kod açıklamaları ve örnekler için:

\[Membrane API Gateway Dokümantasyon](docs/Membrane\_API\_Gateway\_Dokumantasyon.docx)



\## Teknolojiler



\- Membrane API Gateway 7.1.0

\- Groovy Script

\- SOAP / WSDL

\- REST / JSON

