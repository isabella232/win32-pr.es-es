---
description: 'A diferencia de Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separa los proveedores criptográficos de los proveedores de almacenamiento de claves.'
ms.assetid: ce29bc97-049e-4c82-979f-4c805a318ba0
title: Proveedores de algoritmos criptográficos CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fd98a7eb6fd159c54977cdf8b72ebffd747da48
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467085"
---
# <a name="cng-cryptographic-algorithm-providers"></a>Proveedores de algoritmos criptográficos CNG

A diferencia de Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separa los proveedores criptográficos de los proveedores de almacenamiento de claves. Las operaciones básicas de algoritmo criptográfico, como el hash y la firma, se denominan operaciones primitivas o simplemente primitivas. CNG incluye un proveedor que implementa los algoritmos siguientes.

-   [Algoritmos simétricos](#symmetric-algorithms)
-   [Algoritmos asimétricos](#asymmetric-algorithms)
-   [Algoritmos de hash](#hashing-algorithms)
-   [Algoritmos Exchange clave](#key-exchange-algorithms)
-   [Temas relacionados](#related-topics)

## <a name="symmetric-algorithms"></a>Algoritmos simétricos



| Nombre                                   | Modos admitidos                                                                                                                                                                                                 | Tamaño de clave en bits (predeterminado/mínimo/máximo) |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| Estándar de cifrado avanzado (AES)     | ALMAC, CBC, CFB8, CFB128, GCM, CCM, GMAC, CMAC, AES Key Wrap, XTS<br/> **Windows 8:** Comienza la compatibilidad con los modos CFB128 y CMAC.<br/> **Windows 10:** Comienza la compatibilidad con el modo XTS-AES.<br/> | 128/192/256                        |
| Estándar de cifrado de datos (DES)         | BANCO CENTRAL, CBC, CFB8, CFB64<br/> **Windows 8:** Comienza la compatibilidad con el modo CFB64.<br/>                                                                                                                   | 56/56/56                           |
| Estándar de cifrado de datos XORed(DESX)   | BANCO CENTRAL, CBC, CFB8, CFB64 <br/> **Windows 8:** Comienza la compatibilidad con el modo CFB64.<br/>                                                                                                                  | 192/192/192                        |
| Estándar de cifrado de datos triple (3DES) | BANCO CENTRAL, CBC, CFB8, CFB64 <br/> **Windows 8:** Comienza la compatibilidad con el modo CFB64.<br/>                                                                                                                  | 112/168                            |
| RSA Data Security 2 (RC2)              | Se admiten los modos DE LAN, CBC, CFB8 y CFB64.<br/> **Windows 8:** Comienza la compatibilidad con el modo CFB64.<br/>                                                                                              | De 16 a 128 en incrementos de 8 bits      |
| RSA Data Security 4 (RC4)              |                                                                                                                                                                                                                 | De 8 a 512, en incrementos de 8 bits      |



 

## <a name="asymmetric-algorithms"></a>Algoritmos asimétricos



| Nombre                              | Notas                                                                                                                                                                             | Tamaño de clave en bits (predeterminado/mínimo/máximo)                                                                            |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Algoritmo de firma digital (DSA) | La implementación se ajusta a FIPS 186-3 para tamaños de clave entre 1024 y 3072 bits. <br/> La implementación se ajusta a FIPS 186-2 para tamaños de clave de 512 a 1024 bits.<br/> | De 512 a 3072, en incrementos de 64 bits<br/> **Windows 8:** Comienza la compatibilidad con una clave de 3072 bits.<br/> |
| RSA                               | Incluye algoritmos RSA que usan PKCS1, codificación o relleno de relleno óptimo de cifrado asimétrico (OAEP) o relleno de texto no cifrado de esquema de firma probabilística (PSS).               | De 512 a 16384, en incrementos de 64 bits                                                                            |



 

## <a name="hashing-algorithms"></a>Algoritmos de hash



| Nombre                               | Notas               | Tamaño de clave en bits (predeterminado/mínimo/máximo) |
|------------------------------------|---------------------|------------------------------------|
| Algoritmo hash seguro 1 (SHA1)     | Incluye HmacSha1   | 160/160/160                        |
| Algoritmo hash seguro 256 (SHA256) | Incluye HmacSha256 | 256/256/256                        |
| Algoritmo hash seguro 384 (SHA384) | Incluye HmacSha384 | 384/384/384                        |
| Algoritmo hash seguro 512 (SHA512) | Incluye HmacSha512 | 512/512/512                        |
| Resumen de mensajes 2 (MD2)             | Incluye HmacMd2    | 128/128/128                        |
| Resumen de mensajes 4 (MD4)             | Incluye HmacMd4    | 128/128/128                        |
| Resumen de mensajes 5 (MD5)             | Incluye HmacMd5    | 128/128/128                        |



 

## <a name="key-exchange-algorithms"></a>Algoritmos Exchange clave




| Nombre del algoritmo | Notas | Tamaño de clave en bits (predeterminado/mínimo/máximo) | 
|----------------|-------|------------------------------------|
| Diffie-Hellman key Exchange algorithm | De 512 a 4096, en incrementos de 64 bits | 
| Curva elíptica Diffie-Hellman (ECDH) | Incluye curvas que usan claves públicas de 256, 384 y 521 bits, como se especifica en SP800-56A. | 256/384/521 | 
| Algoritmo de firma digital de curva elíptica (ECDSA) | Incluye curvas que usan claves públicas de 256, 384 y 521 bits, como se especifica en FIPS 186-3.<blockquote>[!Note]<br />Para mostrar todas las curvas elípticas con nombre, use <strong>certutil displayEccCurve</strong>.</blockquote><br /> | 256/384/521 | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Identificadores de algoritmo CNG**](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[Funciones primitivas criptográficas de CNG](/windows/desktop/SecCNG/cng-cryptographic-primitive-functions)
</dt> <dt>

[Descripción de los proveedores criptográficos](understanding-cryptographic-providers.md)
</dt> </dl>

 

