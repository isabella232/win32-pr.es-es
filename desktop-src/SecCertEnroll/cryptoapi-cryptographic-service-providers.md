---
description: Los proveedores asociados a Cryptography API (CryptoAPI) se denominan proveedores de servicios criptográficos (CSP) en esta documentación.
ms.assetid: 28c9d348-7a37-4346-8b75-396d1349b152
title: Proveedores de servicios criptográficos CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c095fe4801cd57d4665fed0deec1649eb0a64420c13e4e5f486c7afc805447
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906585"
---
# <a name="cryptoapi-cryptographic-service-providers"></a>Proveedores de servicios criptográficos CryptoAPI

Los proveedores asociados a Cryptography API [*(CryptoAPI)*](/windows/desktop/SecGloss/c-gly)se denominan proveedores de servicios criptográficos (CSP) en esta documentación. Los CSP suelen implementar algoritmos criptográficos y proporcionar almacenamiento de claves. Por otro lado, los proveedores asociados con CNG separan la implementación del algoritmo del almacenamiento de claves. Los siguientes CSP de Microsoft se distribuyen con Windows Vista y Windows Server 2008.

## <a name="microsoft-base-cryptographic-provider-v10"></a>Proveedor de servicios criptográficos básicos de Microsoft, versión 1.0

Implementa los algoritmos siguientes para aplicar hash, firmar y cifrar contenido.



| Nombre                                            | Usar          | Tipo  | Tamaño de clave (predeterminado/mínimo/máximo) |
|-------------------------------------------------|--------------|-------|----------------------------|
| Estándar de cifrado de datos (DES)                  | Cifrado   | Bloquear | 56/56/56                   |
| Suma de comprobación de autenticación de mensajes con hash (HMAC)   | Aplicación de algoritmo hash      | Any   | 0/0/0                      |
| Suma de comprobación de autenticación de mensajes (MAC)           | Aplicación de algoritmo hash      | Any   | 0/0/0                      |
| Resumen de mensajes 2 (MD2)                          | Aplicación de algoritmo hash      | Any   | 128/128/128                |
| Resumen de mensajes 4 (MD4)                          | Aplicación de algoritmo hash      | Any   | 128/128/128                |
| Resumen de mensajes 5 (MD5)                          | Aplicación de algoritmo hash      | Any   | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Cifrado   | Bloquear | 40/40/56                   |
| RSA Data Security 4 (RC4)                       | Cifrado   | Bloquear | 40/40/56                   |
| Clave RSA Exchange                                | Intercambio de claves | RSA   | 512/384/1024               |
| Firma RSA                                   | de firma      | RSA   | 512/384/16384              |
| Algoritmo hash seguro (SHA1)                    | Aplicación de algoritmo hash      | Any   | 160/160/160                |
| Capa de sockets seguros 3 SHA y MD5 (SSL3 SHAMD5) | Aplicación de algoritmo hash      | Any   | 288/288/288                |



 

## <a name="microsoft-base-dss-and-diffie-hellman-cryptographic-provider"></a>Microsoft Base DSS y Diffie-Hellman criptográfico

Implementa los algoritmos siguientes para admitir el hash, la firma, el cifrado y Diffie-Hellman de claves.



| Nombre                                  | Usar          | Tipo           | Tamaño de clave (predeterminado/mínimo/máximo) |
|---------------------------------------|--------------|----------------|----------------------------|
| Algoritmo de cifrado de mensajes CYLINK   | Cifrado   | Bloquear          | 40/40/40                   |
| Estándar de cifrado de datos (DES)        | Cifrado   | Bloquear          | 56/56/56                   |
| algoritmo Diffie-Hellman clave Exchange clave | Intercambio de claves | Diffie-Hellman | 512/512/1024               |
| Diffie-Hellman algoritmo efímero    | Intercambio de claves | Diffie-Hellman | 512/512/1024               |
| Algoritmo de firma digital (DSA)     | de firma      | Dss            | 1024/512/1024              |
| Resumen de mensajes 5 (MD5)                | Aplicación de algoritmo hash      | Any            | 128/128/128                |
| RSA Data Security 2 (RC2)             | Cifrado   | Bloquear          | 40/40/56                   |
| RSA Data Security 4 (RC4)             | Cifrado   | STREAM         | 40/40/56                   |
| Algoritmo hash seguro (SHA1)          | Aplicación de algoritmo hash      | Any            | 160/160/160                |



 

## <a name="microsoft-base-dss-cryptographic-provider"></a>Proveedor de servicios criptográficos DSS básicos de Microsoft

Implementa los algoritmos siguientes para firmar y aplicar hash al contenido:



| Nombre                              | Usar     | Tipo | Tamaño de clave (predeterminado/mínimo/máximo) |
|-----------------------------------|---------|------|----------------------------|
| Algoritmo de firma digital (DSA) | de firma | Dss  | 1024/512/1024              |
| Resumen de mensajes 5 (MD5)            | Aplicación de algoritmo hash | Any  | 128/128/128                |
| Algoritmo hash seguro (SHA1)      | Aplicación de algoritmo hash | Any  | 160/160/160                |



 

## <a name="microsoft-base-smart-card-crypto-provider"></a>Proveedor de servicios criptográficos de tarjeta inteligente básicos de Microsoft

Admite tarjetas inteligentes e implementa los algoritmos siguientes para aplicar hash, firmar y cifrar contenido.

| Nombre                                            | Usar          | Tipo   | Tamaño de clave (predeterminado/mínimo/máximo) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Estándar de cifrado avanzado 128 (AES128)       | Cifrado   | Bloquear  | 128/128/128                |
| Estándar de cifrado avanzado 192 (AES192)       | Cifrado   | Bloquear  | 192/192/192                |
| Estándar de cifrado avanzado 256 (AES256)       | Cifrado   | Bloquear  | 256/256/256                |
| Estándar de cifrado de datos (DES)                  | Cifrado   | Bloquear  | 56/56/56                   |
| Triple DES de dos claves                              | Cifrado   | Bloquear  | 112/112/112                |
| Triple DES de tres claves                            | Cifrado   | Bloquear  | 168/168/168                |
| Suma de comprobación de autenticación de mensajes con hash (HMAC)   | Aplicación de algoritmo hash      | Any    | 0/0/0                      |
| Suma de comprobación de autenticación de mensajes (MAC)           | Aplicación de algoritmo hash      | Any    | 0/0/0                      |
| Resumen de mensajes 2 (MD2)                          | Aplicación de algoritmo hash      | Any    | 128/128/128                |
| Resumen de mensajes 4 (MD4)                          | Aplicación de algoritmo hash      | Any    | 128/128/128                |
| Resumen de mensajes 5 (MD5)                          | Aplicación de algoritmo hash      | Any    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Cifrado   | Bloquear  | 128/40/128                 |
| RSA Data Security 4 (RC4)                       | Cifrado   | STREAM | 128/40/128                 |
| Clave RSA Exchange                                | Intercambio de claves | RSA    | 1024/1024/4096             |
| Firma RSA                                   | de firma      | RSA    | 1024/1024/4096             |
| Algoritmo hash seguro (SHA1)                    | Aplicación de algoritmo hash      | Any    | 160/160/160                |
| Algoritmo hash seguro 256 (SHA256)              | Aplicación de algoritmo hash      | Any    | 256/256/256                |
| Algoritmo hash seguro 384 (SHA384)              | Aplicación de algoritmo hash      | Any    | 384/384/384                |
| Algoritmo hash seguro 512 (SHA512)              | Aplicación de algoritmo hash      | Any    | 512/512/512                |
| Capa de sockets seguros 3 SHA y MD5 (SSL3 SHAMD5) | Aplicación de algoritmo hash      | Any    | 288/288/288                |



 

## <a name="microsoft-dh-schannel-cryptographic-provider"></a>Proveedor criptográfico Schannel de Microsoft DH

Admite el paquete de seguridad de canal seguro (Schannel), que implementa Capa de sockets seguros protocolos de autenticación de seguridad de capa de transporte (TLS) y de seguridad de la capa de transporte (SSL). Este CSP también admite Diffie-Hellman de claves e implementa los algoritmos siguientes.



| Nombre                                   | Usar                | Tipo           | Tamaño de clave (predeterminado/mínimo/máximo) |
|----------------------------------------|--------------------|----------------|----------------------------|
| Algoritmo de cifrado de mensajes CYLINK    | Cifrado         | Bloquear          | 40/40/40                   |
| Estándar de cifrado de datos (DES)         | Cifrado         | Bloquear          | 56/56/56                   |
| Triple DES de dos claves                     | Cifrado         | Bloquear          | 112/112/112                |
| Triple DES de tres claves                   | Cifrado         | Bloquear          | 168/168/168                |
| algoritmo Diffie-Hellman clave Exchange clave  | Intercambio de claves       | Diffie-Hellman | 512/512/4096               |
| Diffie-Hellman algoritmo efímero     | Intercambio de claves       | Diffie-Hellman | 512/512/4096               |
| Algoritmo de firma digital (DSA)      | de firma            | Dss            | 1024/512/1024              |
| Resumen de mensajes 5 (MD5)                 | Aplicación de algoritmo hash            | Any            | 128/128/128                |
| RSA Data Security 2 (RC2)              | Cifrado         | Bloquear          | 40/40/128                  |
| RSA Data Security 4 (RC4)              | Cifrado         | STREAM         | 40/40/128                  |
| Algoritmo hash seguro (SHA1)           | Aplicación de algoritmo hash            | Any            | 160/160/160                |
| Clave de cifrado de Schannel                | Cifrado         | Schannel       | 0/0/-1                     |
| Clave MAC de Schannel                       | Cifrado y hash | Schannel       | 0/0/-1                     |
| Hash maestro de Schannel                   | Cifrado y hash | Schannel       | 0/0/-1                     |
| Capa de sockets seguros (SSL3) Master     | Cifrado         | Schannel       | 384/384/384                |
| Maestro de seguridad de la capa de transporte (TLS1) | Cifrado         | Schannel       | 384/384/384                |



 

## <a name="microsoft-enhanced-cryptographic-provider-v10"></a>Proveedor de servicios criptográficos mejorados de Microsoft, versión 1.0

Proporciona una seguridad más sólida que el proveedor criptográfico base de Microsoft v1.0 mediante el uso de claves más largas con algunos de los algoritmos existentes y la implementación de algoritmos adicionales.



| Nombre                                            | Usar          | Tipo   | Tamaño de clave (predeterminado/mínimo/máximo) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Estándar de cifrado de datos (DES)                  | Cifrado   | Bloquear  | 56/56/56                   |
| Triple DES de dos claves                              | Cifrado   | Bloquear  | 112/112/112                |
|                                                 | Cifrado   | Bloquear  | 168/168/168                |
| Suma de comprobación de autenticación de mensajes con hash (HMAC)   | Aplicación de algoritmo hash      | Any    | 0/0/0                      |
| Suma de comprobación de autenticación de mensajes (MAC)           | Aplicación de algoritmo hash      | Any    | 0/0/0                      |
| Resumen de mensajes 2 (MD2)                          | Aplicación de algoritmo hash      | Any    | 128/128/128                |
| Resumen de mensajes 4 (MD4)                          | Aplicación de algoritmo hash      | Any    | 128/128/128                |
| Resumen de mensajes 5 (MD5)                          | Aplicación de algoritmo hash      | Any    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Cifrado   | Bloquear  | 128/40/128                 |
| RSA Data Security 4 (RC4)                       | Cifrado   | STREAM | 128/40/128                 |
| Clave RSA Exchange                                | Intercambio de claves | RSA    | 1024/384/16384             |
| Firma RSA                                   | de firma      | RSA    | 1024/384/16384             |
| Algoritmo hash seguro (SHA1)                     | Aplicación de algoritmo hash      | Any    | 160/160/160                |
| Capa de sockets seguros 3 SHA y MD5 (SSL3 SHAMD5) | Aplicación de algoritmo hash      | Any    | 288/288/288                |



 

## <a name="microsoft-enhanced-dss-and-diffie-hellman-cryptographic-provider"></a>Proveedor de servicios criptográficos Diffie-Hellman DSS y microsoft enhanced

Proporciona mayor seguridad que el CSP del proveedor de servicios criptográficos de microsoft base Diffie-Hellman mediante claves más largas con algunos de los algoritmos existentes e implementando algoritmos adicionales.



| Nombre                                  | Usar          | Tipo           | Tamaño de clave (predeterminado/mínimo/máximo) |
|---------------------------------------|--------------|----------------|----------------------------|
| Algoritmo de cifrado de mensajes CYLINK   | Cifrado   | Bloquear          | 40/40/40                   |
| Estándar de cifrado de datos (DES)        | Cifrado   | Bloquear          | 56/56/56                   |
| Dos DES triples clave                    | Cifrado   | Bloquear          | 112/112/112                |
| Tres DES triples clave                  | Cifrado   | Bloquear          | 168/168/168                |
| Diffie-Hellman key Exchange algorithm | Intercambio de claves | Diffie-Hellman | 1024/512/4096              |
| Diffie-Hellman algoritmo efímero    | Intercambio de claves | Diffie-Hellman | 1024/512/4096              |
| Algoritmo de firma digital (DSA)     | de firma      | Dss            | 1024/512/1024              |
| Resumen de mensajes 5 (MD5)                | Aplicación de algoritmo hash      | Any            | 128/128/128                |
| RSA Data Security 2 (RC2)             | Cifrado   | Bloquear          | 128/128/128                |
| RSA Data Security 4 (RC4)             | Cifrado   | STREAM         | 128/128/128                |
| Algoritmo hash seguro (SHA1)          | Aplicación de algoritmo hash      | Any            | 160/160/160                |



 

## <a name="microsoft-enhanced-rsa-and-aes-cryptographic-provider"></a>Proveedor criptográfico RSA y AES mejorado de Microsoft

Implementa los algoritmos siguientes para firmar, cifrar y aplicar hash al contenido.



| Nombre                                            | Usar          | Tipo   | Tamaño de clave (predeterminado/mínimo/máximo) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Estándar de cifrado avanzado 128 (AES128)       | Cifrado   | Bloquear  | 128/128/128                |
| Estándar de cifrado avanzado 192 (AES192)       | Cifrado   | Bloquear  | 192/192/192                |
| Estándar de cifrado avanzado 256 (AES256)       | Cifrado   | Bloquear  | 256/256/256                |
| Estándar de cifrado de datos (DES)                  | Cifrado   | Bloquear  | 56/56/56                   |
| Dos DES triples clave                              | Cifrado   | Bloquear  | 112/112/112                |
| Tres DES triples clave                            | Cifrado   | Bloquear  | 168/168/168                |
| Suma de comprobación de autenticación de mensajes con hash (HMAC)   | Aplicación de algoritmo hash      | Any    | 0/0/0                      |
| Suma de comprobación de autenticación de mensajes (MAC)           | Aplicación de algoritmo hash      | Any    | 0/0/0                      |
| Resumen de mensajes 2 (MD2)                          | Aplicación de algoritmo hash      | Any    | 128/128/128                |
| Resumen de mensajes 4 (MD4)                          | Aplicación de algoritmo hash      | Any    | 128/128/128                |
| Resumen de mensajes 5 (MD5)                          | Aplicación de algoritmo hash      | Any    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Cifrado   | Bloquear  | 128/128/128                |
| RSA Data Security 4 (RC4)                       | Cifrado   | STREAM | 128/128/128                |
| Clave RSA Exchange                                | Intercambio de claves | RSA    | 1024/384/16384             |
| Firma RSA                                   | de firma      | RSA    | 1024/384/16384             |
| Algoritmo hash seguro (SHA1)                    | Aplicación de algoritmo hash      | Any    | 160/160/160                |
| Algoritmo hash seguro (SHA256)                  | Aplicación de algoritmo hash      | Any    | 256/256/256                |
| Algoritmo hash seguro (SHA384)                  | Aplicación de algoritmo hash      | Any    | 384/384/384                |
| Algoritmo hash seguro (SHA512)                  | Aplicación de algoritmo hash      | Any    | 512/512/512                |
| Capa de sockets seguros 3 SHA y MD5 (SSL3 SHAMD5) | Aplicación de algoritmo hash      | Any    | 288/288/288                |



 

## <a name="microsoft-rsa-schannel-cryptographic-provider"></a>Proveedor criptográfico Schannel de Microsoft RSA

Admite el paquete de seguridad de canal seguro RSA (Schannel), que implementa protocolos de autenticación Capa de sockets seguros (SSL) y seguridad de la capa de transporte (TLS).



| Nombre                                            | Usar                | Tipo     | Tamaño de clave (predeterminado/mínimo/máximo) |
|-------------------------------------------------|--------------------|----------|----------------------------|
| Estándar de cifrado avanzado 128 (AES128)       | Cifrado         | Bloquear    | 128/128/128                |
| Estándar de cifrado avanzado 256 (AES256)       | Cifrado         | Bloquear    | 256/256/256                |
| Estándar de cifrado de datos (DES)                  | Cifrado         | Bloquear    | 56/56/56                   |
| Dos DES triples clave                              | Cifrado         | Bloquear    | 112/112/112                |
| Tres DES triples clave                            | Cifrado         | Bloquear    | 168/168/168                |
| Suma de comprobación de autenticación de mensajes con hash (HMAC)   | Aplicación de algoritmo hash            | Any      | 0/0/0                      |
| Suma de comprobación de autenticación de mensajes (MAC)           | Aplicación de algoritmo hash            | Any      | 0/0/0                      |
| Resumen de mensajes 5 (MD5)                          | Aplicación de algoritmo hash            | Any      | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Cifrado         | Bloquear    | 128/128/128                |
| RSA Data Security 4 (RC4)                       | Cifrado         | STREAM   | 128/128/128                |
| Clave RSA Exchange                                | Intercambio de claves       | RSA      | 1024/384/16384             |
| Clave de cifrado de Schannel                         | Cifrado         | Schannel | 0/0/-1                     |
| Hash maestro de Schannel                            | Cifrado y hash | Schannel | 0/0/-1                     |
| Clave MAC de Schannel                                | Cifrado y hash | Schannel | 0/0/-1                     |
| Algoritmo hash seguro (SHA1)                    | Aplicación de algoritmo hash            | Any      | 160/160/160                |
| Patrón de capa de sockets seguros 2 (SSL2)             | Cifrado         | Schannel | 40/40/192                  |
| Patrón de capa de sockets seguros 3 (SSL3)             | Cifrado         | Schannel | 384/384/384                |
| Capa de sockets seguros 3 SHA y MD5 (SSL3 SHAMD5) | Aplicación de algoritmo hash            | Any      | 288/288/288                |
| Maestro de seguridad de la capa de transporte (TLS1)          | Cifrado         | Schannel | 384/384/384                |



 

## <a name="microsoft-strong-cryptographic-provider"></a>Proveedor de servicios criptográficos seguros de Microsoft

Implementa los algoritmos siguientes.



| Nombre                                            | Usar          | Tipo   | Tamaño de clave (predeterminado/mínimo/máximo) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Estándar de cifrado de datos (DES)                  | Cifrado   | Bloquear  | 56/56/56                   |
| Dos DES triples clave                              | Cifrado   | Bloquear  | 112/112/112                |
| Tres DES triples clave                            | Cifrado   | Bloquear  | 168/168/168                |
| Suma de comprobación de autenticación de mensajes con hash (HMAC)   | Aplicación de algoritmo hash      | Any    | 0/0/0                      |
| Suma de comprobación de autenticación de mensajes (MAC)           | Aplicación de algoritmo hash      | Any    | 0/0/0                      |
| Resumen de mensajes 2 (MD2)                          | Aplicación de algoritmo hash      | Any    | 128/128/128                |
| Resumen de mensajes 4 (MD4)                          | Aplicación de algoritmo hash      | Any    | 128/128/128                |
| Resumen de mensajes 5 (MD5)                          | Aplicación de algoritmo hash      | Any    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Cifrado   | Bloquear  | 128/40/128                 |
| RSA Data Security 4 (RC4)                       | Cifrado   | STREAM | 128/40/128                 |
| Clave RSA Exchange                                | Intercambio de claves | RSA    | 1024/384/16384             |
| Firma RSA                                   | de firma      | RSA    | 1024/384/16384             |
| Algoritmo hash seguro (SHA1)                    | Aplicación de algoritmo hash      | Any    | 160/160/160                |
| Capa de sockets seguros 3 SHA y MD5 (SSL3 SHAMD5) | Aplicación de algoritmo hash      | Any    | 288/288/288                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descripción de los proveedores criptográficos](understanding-cryptographic-providers.md)
</dt> </dl>

 

 
