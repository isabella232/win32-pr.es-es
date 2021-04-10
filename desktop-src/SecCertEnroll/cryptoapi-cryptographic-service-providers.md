---
description: Los proveedores asociados a Cryptography API (CryptoAPI) se denominan proveedores de servicios criptográficos (CSP) en esta documentación.
ms.assetid: 28c9d348-7a37-4346-8b75-396d1349b152
title: Proveedores de servicios criptográficos de CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50b3820a0d45534bc5c492d843352be038f7ffc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154736"
---
# <a name="cryptoapi-cryptographic-service-providers"></a>Proveedores de servicios criptográficos de CryptoAPI

Los proveedores asociados a Cryptography API ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) se denominan proveedores de servicios criptográficos (CSP) en esta documentación. Normalmente, los CSP implementan algoritmos criptográficos y proporcionan almacenamiento de claves. Los proveedores asociados a CNG, por otro lado, la implementación de algoritmos independientes del almacenamiento de claves. Los siguientes CSP de Microsoft se distribuyen con Windows Vista y Windows Server 2008.

## <a name="microsoft-base-cryptographic-provider-v10"></a>Proveedor de servicios criptográficos básicos de Microsoft, versión 1.0

Implementa los algoritmos siguientes para aplicar el algoritmo hash, firmar y cifrar el contenido.



| Nombre                                            | Use          | Tipo  | Tamaño de la clave (predeterminado/mín./máx.) |
|-------------------------------------------------|--------------|-------|----------------------------|
| Estándar de cifrado de datos (DES)                  | Cifrado   | Bloquear | 56/56/56                   |
| Suma de comprobación de autenticación de mensajes con hash (HMAC)   | Aplicación de algoritmo hash      | Any   | 0/0/0                      |
| Suma de comprobación de autenticación de mensajes (MAC)           | Aplicación de algoritmo hash      | Any   | 0/0/0                      |
| Síntesis del mensaje 2 (MD2)                          | Aplicación de algoritmo hash      | Any   | 128/128/128                |
| Síntesis del mensaje 4 (MD4)                          | Aplicación de algoritmo hash      | Any   | 128/128/128                |
| Síntesis del mensaje 5 (MD5)                          | Aplicación de algoritmo hash      | Any   | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Cifrado   | Bloquear | 40/40/56                   |
| RSA Data Security 4 (RC4)                       | Cifrado   | Bloquear | 40/40/56                   |
| Intercambio de claves RSA                                | Intercambio de claves | RSA   | 512/384/1024               |
| Firma RSA                                   | de firma      | RSA   | 512/384/16384              |
| Algoritmo hash seguro (SHA1)                    | Aplicación de algoritmo hash      | Any   | 160/160/160                |
| Capa de sockets seguros 3 SHA y MD5 (SSL3 SHAMD5) | Aplicación de algoritmo hash      | Any   | 288/288/288                |



 

## <a name="microsoft-base-dss-and-diffie-hellman-cryptographic-provider"></a>Microsoft base DSS y Diffie-Hellman proveedor de servicios criptográficos

Implementa los algoritmos siguientes para admitir el intercambio de claves, la firma, el cifrado y el cifrado de Diffie-Hellman.



| Nombre                                  | Use          | Tipo           | Tamaño de la clave (predeterminado/mín./máx.) |
|---------------------------------------|--------------|----------------|----------------------------|
| Algoritmo de cifrado de mensajes de CYLINK   | Cifrado   | Bloquear          | 40/40/40                   |
| Estándar de cifrado de datos (DES)        | Cifrado   | Bloquear          | 56/56/56                   |
| Algoritmo de intercambio de claves Diffie-Hellman | Intercambio de claves | Diffie-Hellman | 512/512/1024               |
| Algoritmo efímero Diffie-Hellman    | Intercambio de claves | Diffie-Hellman | 512/512/1024               |
| Algoritmo de firma digital (DSA)     | de firma      | DSS            | 1024/512/1024              |
| Síntesis del mensaje 5 (MD5)                | Aplicación de algoritmo hash      | Any            | 128/128/128                |
| RSA Data Security 2 (RC2)             | Cifrado   | Bloquear          | 40/40/56                   |
| RSA Data Security 4 (RC4)             | Cifrado   | Stream         | 40/40/56                   |
| Algoritmo hash seguro (SHA1)          | Aplicación de algoritmo hash      | Any            | 160/160/160                |



 

## <a name="microsoft-base-dss-cryptographic-provider"></a>Proveedor de servicios criptográficos DSS básicos de Microsoft

Implementa los algoritmos siguientes para firmar y el contenido hash:



| Nombre                              | Use     | Tipo | Tamaño de la clave (predeterminado/mín./máx.) |
|-----------------------------------|---------|------|----------------------------|
| Algoritmo de firma digital (DSA) | de firma | DSS  | 1024/512/1024              |
| Síntesis del mensaje 5 (MD5)            | Aplicación de algoritmo hash | Any  | 128/128/128                |
| Algoritmo hash seguro (SHA1)      | Aplicación de algoritmo hash | Any  | 160/160/160                |



 

## <a name="microsoft-base-smart-card-crypto-provider"></a>Proveedor de servicios criptográficos de tarjeta inteligente básicos de Microsoft

Admite tarjetas inteligentes e implementa los siguientes algoritmos para aplicar un algoritmo hash, firmar y cifrar contenido.

| Nombre                                            | Use          | Tipo   | Tamaño de la clave (predeterminado/mín./máx.) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Estándar de cifrado avanzado 128 (AES128)       | Cifrado   | Bloquear  | 128/128/128                |
| Estándar de cifrado avanzado 192 (AES192)       | Cifrado   | Bloquear  | 192/192/192                |
| Estándar de cifrado avanzado 256 (AES256)       | Cifrado   | Bloquear  | 256/256/256                |
| Estándar de cifrado de datos (DES)                  | Cifrado   | Bloquear  | 56/56/56                   |
| Triple DES de clave                              | Cifrado   | Bloquear  | 112/112/112                |
| Triple DES de clave                            | Cifrado   | Bloquear  | 168/168/168                |
| Suma de comprobación de autenticación de mensajes con hash (HMAC)   | Aplicación de algoritmo hash      | Any    | 0/0/0                      |
| Suma de comprobación de autenticación de mensajes (MAC)           | Aplicación de algoritmo hash      | Any    | 0/0/0                      |
| Síntesis del mensaje 2 (MD2)                          | Aplicación de algoritmo hash      | Any    | 128/128/128                |
| Síntesis del mensaje 4 (MD4)                          | Aplicación de algoritmo hash      | Any    | 128/128/128                |
| Síntesis del mensaje 5 (MD5)                          | Aplicación de algoritmo hash      | Any    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Cifrado   | Bloquear  | 128/40/128                 |
| RSA Data Security 4 (RC4)                       | Cifrado   | Stream | 128/40/128                 |
| Intercambio de claves RSA                                | Intercambio de claves | RSA    | 1024/1024/4096             |
| Firma RSA                                   | de firma      | RSA    | 1024/1024/4096             |
| Algoritmo hash seguro (SHA1)                    | Aplicación de algoritmo hash      | Any    | 160/160/160                |
| Algoritmo hash seguro 256 (SHA256)              | Aplicación de algoritmo hash      | Any    | 256/256/256                |
| Algoritmo hash seguro 384 (SHA384)              | Aplicación de algoritmo hash      | Any    | 384/384/384                |
| Algoritmo hash seguro 512 (SHA512)              | Aplicación de algoritmo hash      | Any    | 512/512/512                |
| Capa de sockets seguros 3 SHA y MD5 (SSL3 SHAMD5) | Aplicación de algoritmo hash      | Any    | 288/288/288                |



 

## <a name="microsoft-dh-schannel-cryptographic-provider"></a>Proveedor de servicios criptográficos de Microsoft DH Schannel

Admite el paquete de seguridad de canal seguro (Schannel) que implementa los protocolos de autenticación Capa de sockets seguros (SSL) y seguridad de la capa de transporte (TLS). Este CSP también admite el intercambio de claves Diffie-Hellman e implementa los siguientes algoritmos.



| Nombre                                   | Use                | Tipo           | Tamaño de la clave (predeterminado/mín./máx.) |
|----------------------------------------|--------------------|----------------|----------------------------|
| Algoritmo de cifrado de mensajes de CYLINK    | Cifrado         | Bloquear          | 40/40/40                   |
| Estándar de cifrado de datos (DES)         | Cifrado         | Bloquear          | 56/56/56                   |
| Triple DES de clave                     | Cifrado         | Bloquear          | 112/112/112                |
| Triple DES de clave                   | Cifrado         | Bloquear          | 168/168/168                |
| Algoritmo de intercambio de claves Diffie-Hellman  | Intercambio de claves       | Diffie-Hellman | 512/512/4096               |
| Algoritmo efímero Diffie-Hellman     | Intercambio de claves       | Diffie-Hellman | 512/512/4096               |
| Algoritmo de firma digital (DSA)      | de firma            | DSS            | 1024/512/1024              |
| Síntesis del mensaje 5 (MD5)                 | Aplicación de algoritmo hash            | Any            | 128/128/128                |
| RSA Data Security 2 (RC2)              | Cifrado         | Bloquear          | 40/40/128                  |
| RSA Data Security 4 (RC4)              | Cifrado         | Stream         | 40/40/128                  |
| Algoritmo hash seguro (SHA1)           | Aplicación de algoritmo hash            | Any            | 160/160/160                |
| Clave de cifrado Schannel                | Cifrado         | Schannel       | 0/0/-1                     |
| Tecla MAC Schannel                       | Cifrado/hash | Schannel       | 0/0/-1                     |
| Hash del patrón Schannel                   | Cifrado/hash | Schannel       | 0/0/-1                     |
| Capa de sockets seguros (SSL3) Master     | Cifrado         | Schannel       | 384/384/384                |
| Maestro de seguridad de la capa de transporte (TLS1) | Cifrado         | Schannel       | 384/384/384                |



 

## <a name="microsoft-enhanced-cryptographic-provider-v10"></a>Proveedor de servicios criptográficos mejorados de Microsoft, versión 1.0

Proporciona una mayor seguridad que el proveedor de servicios criptográficos de base de Microsoft v 1.0 usando claves más largas con algunos de los algoritmos existentes y implementando algoritmos adicionales.



| Nombre                                            | Use          | Tipo   | Tamaño de la clave (predeterminado/mín./máx.) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Estándar de cifrado de datos (DES)                  | Cifrado   | Bloquear  | 56/56/56                   |
| Triple DES de clave                              | Cifrado   | Bloquear  | 112/112/112                |
|                                                 | Cifrado   | Bloquear  | 168/168/168                |
| Suma de comprobación de autenticación de mensajes con hash (HMAC)   | Aplicación de algoritmo hash      | Any    | 0/0/0                      |
| Suma de comprobación de autenticación de mensajes (MAC)           | Aplicación de algoritmo hash      | Any    | 0/0/0                      |
| Síntesis del mensaje 2 (MD2)                          | Aplicación de algoritmo hash      | Any    | 128/128/128                |
| Síntesis del mensaje 4 (MD4)                          | Aplicación de algoritmo hash      | Any    | 128/128/128                |
| Síntesis del mensaje 5 (MD5)                          | Aplicación de algoritmo hash      | Any    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Cifrado   | Bloquear  | 128/40/128                 |
| RSA Data Security 4 (RC4)                       | Cifrado   | Stream | 128/40/128                 |
| Intercambio de claves RSA                                | Intercambio de claves | RSA    | 1024/384/16384             |
| Firma RSA                                   | de firma      | RSA    | 1024/384/16384             |
| Algoritmo hash seguro (SHA1                     | Aplicación de algoritmo hash      | Any    | 160/160/160                |
| Capa de sockets seguros 3 SHA y MD5 (SSL3 SHAMD5) | Aplicación de algoritmo hash      | Any    | 288/288/288                |



 

## <a name="microsoft-enhanced-dss-and-diffie-hellman-cryptographic-provider"></a>Microsoft Enhanced DSS y Diffie-Hellman proveedor de servicios criptográficos

Proporciona una mayor seguridad que Microsoft base DSS y Diffie-Hellman CSP de proveedor de servicios criptográficos usando claves más largas con algunos de los algoritmos existentes y implementando algoritmos adicionales.



| Nombre                                  | Use          | Tipo           | Tamaño de la clave (predeterminado/mín./máx.) |
|---------------------------------------|--------------|----------------|----------------------------|
| Algoritmo de cifrado de mensajes de CYLINK   | Cifrado   | Bloquear          | 40/40/40                   |
| Estándar de cifrado de datos (DES)        | Cifrado   | Bloquear          | 56/56/56                   |
| Triple DES de clave                    | Cifrado   | Bloquear          | 112/112/112                |
| Triple DES de clave                  | Cifrado   | Bloquear          | 168/168/168                |
| Algoritmo de intercambio de claves Diffie-Hellman | Intercambio de claves | Diffie-Hellman | 1024/512/4096              |
| Algoritmo efímero Diffie-Hellman    | Intercambio de claves | Diffie-Hellman | 1024/512/4096              |
| Algoritmo de firma digital (DSA)     | de firma      | DSS            | 1024/512/1024              |
| Síntesis del mensaje 5 (MD5)                | Aplicación de algoritmo hash      | Any            | 128/128/128                |
| RSA Data Security 2 (RC2)             | Cifrado   | Bloquear          | 128/128/128                |
| RSA Data Security 4 (RC4)             | Cifrado   | Stream         | 128/128/128                |
| Algoritmo hash seguro (SHA1)          | Aplicación de algoritmo hash      | Any            | 160/160/160                |



 

## <a name="microsoft-enhanced-rsa-and-aes-cryptographic-provider"></a>Proveedor de servicios criptográficos RSA y AES mejorado de Microsoft

Implementa los algoritmos siguientes para firmar, cifrar y el contenido hash.



| Nombre                                            | Use          | Tipo   | Tamaño de la clave (predeterminado/mín./máx.) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Estándar de cifrado avanzado 128 (AES128)       | Cifrado   | Bloquear  | 128/128/128                |
| Estándar de cifrado avanzado 192 (AES192)       | Cifrado   | Bloquear  | 192/192/192                |
| Estándar de cifrado avanzado 256 (AES256)       | Cifrado   | Bloquear  | 256/256/256                |
| Estándar de cifrado de datos (DES)                  | Cifrado   | Bloquear  | 56/56/56                   |
| Triple DES de clave                              | Cifrado   | Bloquear  | 112/112/112                |
| Triple DES de clave                            | Cifrado   | Bloquear  | 168/168/168                |
| Suma de comprobación de autenticación de mensajes con hash (HMAC)   | Aplicación de algoritmo hash      | Any    | 0/0/0                      |
| Suma de comprobación de autenticación de mensajes (MAC)           | Aplicación de algoritmo hash      | Any    | 0/0/0                      |
| Síntesis del mensaje 2 (MD2)                          | Aplicación de algoritmo hash      | Any    | 128/128/128                |
| Síntesis del mensaje 4 (MD4)                          | Aplicación de algoritmo hash      | Any    | 128/128/128                |
| Síntesis del mensaje 5 (MD5)                          | Aplicación de algoritmo hash      | Any    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Cifrado   | Bloquear  | 128/128/128                |
| RSA Data Security 4 (RC4)                       | Cifrado   | Stream | 128/128/128                |
| Intercambio de claves RSA                                | Intercambio de claves | RSA    | 1024/384/16384             |
| Firma RSA                                   | de firma      | RSA    | 1024/384/16384             |
| Algoritmo hash seguro (SHA1)                    | Aplicación de algoritmo hash      | Any    | 160/160/160                |
| Algoritmo hash seguro (SHA256)                  | Aplicación de algoritmo hash      | Any    | 256/256/256                |
| Algoritmo hash seguro (SHA384)                  | Aplicación de algoritmo hash      | Any    | 384/384/384                |
| Algoritmo hash seguro (SHA512)                  | Aplicación de algoritmo hash      | Any    | 512/512/512                |
| Capa de sockets seguros 3 SHA y MD5 (SSL3 SHAMD5) | Aplicación de algoritmo hash      | Any    | 288/288/288                |



 

## <a name="microsoft-rsa-schannel-cryptographic-provider"></a>Proveedor de servicios criptográficos de Microsoft RSA Schannel

Admite el paquete de seguridad de canal seguro de RSA (Schannel) que implementa los protocolos de autenticación Capa de sockets seguros (SSL) y seguridad de la capa de transporte (TLS).



| Nombre                                            | Use                | Tipo     | Tamaño de la clave (predeterminado/mín./máx.) |
|-------------------------------------------------|--------------------|----------|----------------------------|
| Estándar de cifrado avanzado 128 (AES128)       | Cifrado         | Bloquear    | 128/128/128                |
| Estándar de cifrado avanzado 256 (AES256)       | Cifrado         | Bloquear    | 256/256/256                |
| Estándar de cifrado de datos (DES)                  | Cifrado         | Bloquear    | 56/56/56                   |
| Triple DES de clave                              | Cifrado         | Bloquear    | 112/112/112                |
| Triple DES de clave                            | Cifrado         | Bloquear    | 168/168/168                |
| Suma de comprobación de autenticación de mensajes con hash (HMAC)   | Aplicación de algoritmo hash            | Any      | 0/0/0                      |
| Suma de comprobación de autenticación de mensajes (MAC)           | Aplicación de algoritmo hash            | Any      | 0/0/0                      |
| Síntesis del mensaje 5 (MD5)                          | Aplicación de algoritmo hash            | Any      | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Cifrado         | Bloquear    | 128/128/128                |
| RSA Data Security 4 (RC4)                       | Cifrado         | Stream   | 128/128/128                |
| Intercambio de claves RSA                                | Intercambio de claves       | RSA      | 1024/384/16384             |
| Clave de cifrado Schannel                         | Cifrado         | Schannel | 0/0/-1                     |
| Hash del patrón Schannel                            | Cifrado/hash | Schannel | 0/0/-1                     |
| Tecla MAC Schannel                                | Cifrado/hash | Schannel | 0/0/-1                     |
| Algoritmo hash seguro (SHA1)                    | Aplicación de algoritmo hash            | Any      | 160/160/160                |
| Maestro de capa de sockets seguros 2 (SSL2)             | Cifrado         | Schannel | 40/40/192                  |
| Maestro de capa de sockets seguros 3 (SSL3)             | Cifrado         | Schannel | 384/384/384                |
| Capa de sockets seguros 3 SHA y MD5 (SSL3 SHAMD5) | Aplicación de algoritmo hash            | Any      | 288/288/288                |
| Maestro de seguridad de la capa de transporte (TLS1)          | Cifrado         | Schannel | 384/384/384                |



 

## <a name="microsoft-strong-cryptographic-provider"></a>Proveedor de servicios criptográficos seguros de Microsoft

Implementa los algoritmos siguientes.



| Nombre                                            | Use          | Tipo   | Tamaño de la clave (predeterminado/mín./máx.) |
|-------------------------------------------------|--------------|--------|----------------------------|
| Estándar de cifrado de datos (DES)                  | Cifrado   | Bloquear  | 56/56/56                   |
| Triple DES de clave                              | Cifrado   | Bloquear  | 112/112/112                |
| Triple DES de clave                            | Cifrado   | Bloquear  | 168/168/168                |
| Suma de comprobación de autenticación de mensajes con hash (HMAC)   | Aplicación de algoritmo hash      | Any    | 0/0/0                      |
| Suma de comprobación de autenticación de mensajes (MAC)           | Aplicación de algoritmo hash      | Any    | 0/0/0                      |
| Síntesis del mensaje 2 (MD2)                          | Aplicación de algoritmo hash      | Any    | 128/128/128                |
| Síntesis del mensaje 4 (MD4)                          | Aplicación de algoritmo hash      | Any    | 128/128/128                |
| Síntesis del mensaje 5 (MD5)                          | Aplicación de algoritmo hash      | Any    | 128/128/128                |
| RSA Data Security 2 (RC2)                       | Cifrado   | Bloquear  | 128/40/128                 |
| RSA Data Security 4 (RC4)                       | Cifrado   | Stream | 128/40/128                 |
| Intercambio de claves RSA                                | Intercambio de claves | RSA    | 1024/384/16384             |
| Firma RSA                                   | de firma      | RSA    | 1024/384/16384             |
| Algoritmo hash seguro (SHA1)                    | Aplicación de algoritmo hash      | Any    | 160/160/160                |
| Capa de sockets seguros 3 SHA y MD5 (SSL3 SHAMD5) | Aplicación de algoritmo hash      | Any    | 288/288/288                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descripción de los proveedores de servicios criptográficos](understanding-cryptographic-providers.md)
</dt> </dl>

 

 
