---
description: 'A diferencia de Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separa los proveedores de servicios criptográficos de los proveedores de almacenamiento de claves.'
ms.assetid: ce29bc97-049e-4c82-979f-4c805a318ba0
title: Proveedores de algoritmos criptográficos CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc64926236157e581ce6406d95681bd8d4add14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648526"
---
# <a name="cng-cryptographic-algorithm-providers"></a>Proveedores de algoritmos criptográficos CNG

A diferencia de Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separa los proveedores de servicios criptográficos de los proveedores de almacenamiento de claves. Las operaciones básicas de los algoritmos criptográficos como la firma y el hash se denominan operaciones primitivas o simplemente primitivas. CNG incluye un proveedor que implementa los algoritmos siguientes.

-   [Algoritmos simétricos](#symmetric-algorithms)
-   [Algoritmos asimétricos](#asymmetric-algorithms)
-   [Algoritmos de hash](#hashing-algorithms)
-   [Algoritmos de intercambio de claves](#key-exchange-algorithms)
-   [Temas relacionados](#related-topics)

## <a name="symmetric-algorithms"></a>Algoritmos simétricos



| Nombre                                   | Modos admitidos                                                                                                                                                                                                 | Tamaño de clave en bits (predeterminado/mín./máx.) |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| Estándar de cifrado avanzado (AES)     | ECB, CBC, CFB8, CFB128, GCM, CCM, GMAC, CMAC, encapsulado de claves AES, XTS<br/> **Windows 8:** Comienza la compatibilidad con los modos CFB128 y CMAC.<br/> **Windows 10:** Se inicia la compatibilidad con el modo XTS-AES.<br/> | 128/192/256                        |
| Estándar de cifrado de datos (DES)         | ECB, CBC, CFB8, CFB64<br/> **Windows 8:** Se inicia la compatibilidad con el modo CFB64.<br/>                                                                                                                   | 56/56/56                           |
| Estándar de cifrado de datos XORed (DESX)   | ECB, CBC, CFB8, CFB64 <br/> **Windows 8:** Se inicia la compatibilidad con el modo CFB64.<br/>                                                                                                                  | 192/192/192                        |
| Estándar de cifrado de datos triple (3DES) | ECB, CBC, CFB8, CFB64 <br/> **Windows 8:** Se inicia la compatibilidad con el modo CFB64.<br/>                                                                                                                  | 112/168                            |
| RSA Data Security 2 (RC2)              | Se admiten los modos ECB, CBC, CFB8 y CFB64.<br/> **Windows 8:** Se inicia la compatibilidad con el modo CFB64.<br/>                                                                                              | de 16 a 128 en incrementos de 8 bits      |
| RSA Data Security 4 (RC4)              |                                                                                                                                                                                                                 | de 8 a 512, en incrementos de 8 bits      |



 

## <a name="asymmetric-algorithms"></a>Algoritmos asimétricos



| Nombre                              | Notas                                                                                                                                                                             | Tamaño de clave en bits (predeterminado/mín./máx.)                                                                            |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Algoritmo de firma digital (DSA) | La implementación se ajusta a FIPS 186-3 para tamaños de clave entre los bits 1024 y 3072. <br/> La implementación se ajusta a FIPS 186-2 para tamaños de clave de 512 a 1024 bits.<br/> | de 512 a 3072, en incrementos de 64 bits<br/> **Windows 8:** Se inicia la compatibilidad con la clave de 3072 bits.<br/> |
| RSA                               | Incluye algoritmos RSA que usan codificación y relleno de cifrado asimétrico (OAEP) óptimos de cifrado asimétrico (OAEP) o relleno de texto sin formato del esquema de firma probabilística (PSS).               | de 512 a 16384, en incrementos de 64 bits                                                                            |



 

## <a name="hashing-algorithms"></a>Algoritmos de hash



| Nombre                               | Notas               | Tamaño de clave en bits (predeterminado/mín./máx.) |
|------------------------------------|---------------------|------------------------------------|
| Algoritmo hash seguro 1 (SHA1)     | Incluye HmacSha1   | 160/160/160                        |
| Algoritmo hash seguro 256 (SHA256) | Incluye HmacSha256 | 256/256/256                        |
| Algoritmo hash seguro 384 (SHA384) | Incluye HmacSha384 | 384/384/384                        |
| Algoritmo hash seguro 512 (SHA512) | Incluye HmacSha512 | 512/512/512                        |
| Síntesis del mensaje 2 (MD2)             | Incluye HmacMd2    | 128/128/128                        |
| Síntesis del mensaje 4 (MD4)             | Incluye HmacMd4    | 128/128/128                        |
| Síntesis del mensaje 5 (MD5)             | Incluye HmacMd5    | 128/128/128                        |



 

## <a name="key-exchange-algorithms"></a>Algoritmos de intercambio de claves



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nombre del algoritmo</th>
<th>Notas</th>
<th>Tamaño de clave en bits (predeterminado/mín./máx.)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Algoritmo de intercambio de claves Diffie-Hellman</td>

<td>de 512 a 4096, en incrementos de 64 bits</td>
</tr>
<tr class="even">
<td>Diffie-Hellman de curva elíptica (ECDH)</td>
<td>Incluye curvas que usan claves públicas 256, 384 y 521 bits como se especifica en SP800-56A.</td>
<td>256/384/521</td>
</tr>
<tr class="odd">
<td>Algoritmo de firma digital de curva elíptica (ECDSA)</td>
<td>Incluye curvas que usan claves públicas de 256, 384 y 521, tal y como se especifica en FIPS 186-3.
<blockquote>
[!Note]<br />
Para mostrar todas las curvas elípticas con nombre, use <strong>certutil displayEccCurve</strong>.
</blockquote>
<br/></td>
<td>256/384/521</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Identificadores de algoritmo CNG**](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[Funciones primitivas criptográficas de CNG](/windows/desktop/SecCNG/cng-cryptographic-primitive-functions)
</dt> <dt>

[Descripción de los proveedores de servicios criptográficos](understanding-cryptographic-providers.md)
</dt> </dl>

 

