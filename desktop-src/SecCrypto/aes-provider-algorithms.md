---
description: En la tabla siguiente se enumeran los algoritmos admitidos por el proveedor de servicios criptográficos Estándar de cifrado avanzado (AES) de Microsoft.
ms.assetid: 34d0479f-9d1e-41cd-87b0-6bc18c7a062b
title: Algoritmos de proveedor de AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5e197100060d53304bb5233560dcccae083756
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173306"
---
# <a name="aes-provider-algorithms"></a>Algoritmos de proveedor de AES

En la tabla siguiente se enumeran los algoritmos admitidos por el proveedor [*de servicios criptográficos Estándar de cifrado avanzado*](../secgloss/a-gly.md) (AES) de Microsoft.



| Id. de algoritmo       | Descripción                                                                                                                                                     | Comentarios                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALG \_ 3DES         | Triple DES.                                                                                                                                                     | Longitud de clave: 168 bits. Modo predeterminado: encadenamiento de bloques de cifrado.<br/> Tamaño del bloque: 64 bits.<br/> No se permite sal.<br/>                          |
| CALG \_ 3DES \_ 112    | Cifrado [*DES triple de*](../secgloss/t-gly.md) dos claves.                                                            | Longitud de clave: 112 bits. Modo predeterminado: encadenamiento de bloques de cifrado.<br/> Tamaño del bloque: 64 bits.<br/> No se permite sal.<br/>                          |
| CALG \_ AES \_ 128     | Algoritmo de cifrado de bloques AES.                                                                                                                                 | Longitud de clave: 128 bits.                                                                                                                                      |
| CALG \_ AES \_ 192     | Algoritmo de cifrado de bloques AES.                                                                                                                                 | Longitud de clave: 192 bits.                                                                                                                                      |
| CALG \_ AES \_ 256     | Algoritmo de cifrado de bloques AES.                                                                                                                                 | Longitud de clave: 256 bits.                                                                                                                                      |
| CALG \_ DES          | Cifrado DES.                                                                                                                                                 | Longitud de clave: 56 bits. Modo predeterminado: encadenamiento de bloques de cifrado.<br/> Tamaño del bloque: 64 bits.<br/> No se permite sal.<br/>                           |
| CALG \_ HMAC         | Algoritmo de hash con claves de MAC.                                                                                                                                       | Cálculo HMAC.                                                                                                                                          |
| CALG \_ MAC          | [*Algoritmo*](../secgloss/m-gly.md) hash con clave de código de autenticación de mensajes (MAC). | Bloquear mac de cifrado.                                                                                                                                          |
| CALG \_ MD2          | Algoritmo de hash MD2.                                                                                                                                          | Para obtener más información, vea [*Algoritmo MD2*](../secgloss/m-gly.md).                                       |
| CALG \_ MD5          | Algoritmo de hash MD5.                                                                                                                                          | Para obtener más información, vea [*Algoritmo MD5*](../secgloss/m-gly.md).                                       |
| CALG \_ RC2          | Algoritmo de cifrado de bloque RC2.                                                                                                                                 | Longitud de clave: 128 bits. Modo predeterminado: encadenamiento de bloques de cifrado.<br/> Tamaño del bloque: 64 bits.<br/> Longitud de sal: se puede establecer.<br/>                  |
| CALG \_ RC4          | Algoritmo de cifrado de secuencia RC4.                                                                                                                                | Longitud de clave: 128 bits. Longitud de sal: se puede establecer.<br/>                                                                                                  |
| CALG \_ RSA \_ KEYX    | Algoritmo de intercambio de claves públicas RSA.                                                                                                                              | Longitud de clave: se puede establecer entre 384 bits y 16 384 bits en incrementos de 8 bits. Longitud de clave predeterminada: 1024 bits.<br/>                                            |
| CALG \_ RSA \_ SIGN    | Algoritmo de firma de clave pública RSA.                                                                                                                             | Longitud de clave: se puede establecer entre 384 bits y 16 384 bits en incrementos de 8 bits. Longitud de clave predeterminada: 1024 bits.<br/> La firma se ajusta a PKCS \# 6.<br/> |
| CALG \_ SHA          | Algoritmo de hash SHA.                                                                                                                                          | Para obtener más información, vea [*Secure Hash Algorithm*](../secgloss/s-gly.md).               |
| CALG \_ SHA1         | Igual que **CALG \_ SHA.**                                                                                                                                          | Para obtener más información, vea [*Secure Hash Algorithm*](../secgloss/s-gly.md).               |
| CALG \_ SHA \_ 256     | Algoritmo de hash SHA.                                                                                                                                          | Longitud de clave: 256 bits. **Windows XP:** Este algoritmo no se admite.<br/>                                                                           |
| CALG \_ SHA \_ 384     | Algoritmo de hash SHA.                                                                                                                                          | Longitud de clave: 384 bits. **Windows XP:** Este algoritmo no se admite.<br/>                                                                           |
| CALG \_ SHA \_ 512     | Algoritmo de hash SHA.                                                                                                                                          | Longitud de clave: 512 bits. **Windows XP:** Este algoritmo no se admite.<br/>                                                                           |
| CALG \_ SSL3 \_ SHAMD5 | Algoritmo de autenticación de cliente SSL3.                                                                                                                           | Para obtener más información, vea [Creating a CALG \_ SSL3 \_ SHAMD5 Hash](creating-a-calg-ssl3-shamd5-hash.md).                                                      |



 

 

 
