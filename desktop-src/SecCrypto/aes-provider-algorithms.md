---
description: En la tabla siguiente se enumeran los algoritmos admitidos por el proveedor de servicios criptográficos de Microsoft Estándar de cifrado avanzado (AES).
ms.assetid: 34d0479f-9d1e-41cd-87b0-6bc18c7a062b
title: Algoritmos de proveedor de AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5e197100060d53304bb5233560dcccae083756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667540"
---
# <a name="aes-provider-algorithms"></a>Algoritmos de proveedor de AES

En la tabla siguiente se enumeran los algoritmos admitidos por el proveedor de servicios criptográficos de Microsoft [*estándar de cifrado avanzado*](../secgloss/a-gly.md) (AES).



| IDENTIFICADOR de algoritmo       | Descripción                                                                                                                                                     | Comentarios                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALG \_ 3DES         | Triple DES.                                                                                                                                                     | Longitud de clave: 168 bits. Modo predeterminado: encadenamiento de bloques de cifrado.<br/> Tamaño de bloque: 64 bits.<br/> No se permiten sal.<br/>                          |
| CALG \_ 3des \_ 112    | Cifrado [*triple des*](../secgloss/t-gly.md) de dos claves.                                                            | Longitud de clave: 112 bits. Modo predeterminado: encadenamiento de bloques de cifrado.<br/> Tamaño de bloque: 64 bits.<br/> No se permiten sal.<br/>                          |
| CALG \_ AES \_ 128     | Algoritmo de cifrado de bloques AES.                                                                                                                                 | Longitud de clave: 128 bits.                                                                                                                                      |
| CALG \_ AES \_ 192     | Algoritmo de cifrado de bloques AES.                                                                                                                                 | Longitud de clave: 192 bits.                                                                                                                                      |
| CALG \_ AES \_ 256     | Algoritmo de cifrado de bloques AES.                                                                                                                                 | Longitud de clave: 256 bits.                                                                                                                                      |
| CALG \_ des          | Cifrado DES.                                                                                                                                                 | Longitud de clave: 56 bits. Modo predeterminado: encadenamiento de bloques de cifrado.<br/> Tamaño de bloque: 64 bits.<br/> No se permiten sal.<br/>                           |
| CALG \_ HMAC         | Algoritmo de hash con claves de MAC.                                                                                                                                       | Cálculo HMAC.                                                                                                                                          |
| \_Mac CALG          | Algoritmo hash con clave de [*código de autentificación de mensajes (Mac)*](../secgloss/m-gly.md) (Mac). | Cifrado de bloqueo de MAC.                                                                                                                                          |
| CALG \_ MD2          | Algoritmo de hash MD2.                                                                                                                                          | Para obtener más información, consulte [*algoritmo MD2*](../secgloss/m-gly.md).                                       |
| CALG \_ MD5          | Algoritmo de hash MD5.                                                                                                                                          | Para obtener más información, vea [*algoritmo MD5*](../secgloss/m-gly.md).                                       |
| CALG \_ RC2          | Algoritmo de cifrado de bloques RC2.                                                                                                                                 | Longitud de clave: 128 bits. Modo predeterminado: encadenamiento de bloques de cifrado.<br/> Tamaño de bloque: 64 bits.<br/> Longitud de sal: se puede establecer.<br/>                  |
| CALG \_ RC4          | Algoritmo de cifrado de flujo RC4.                                                                                                                                | Longitud de clave: 128 bits. Longitud de sal: se puede establecer.<br/>                                                                                                  |
| CALG \_ RSA \_ KEYX    | Algoritmo de intercambio de claves públicas RSA.                                                                                                                              | Longitud de clave: se puede establecer de 384 bits a 16.384 bits en incrementos de 8 bits. Longitud de clave predeterminada: 1.024 bits.<br/>                                            |
| \_firma RSA de CALG \_    | Algoritmo de firma de clave pública RSA.                                                                                                                             | Longitud de clave: se puede establecer de 384 bits a 16.384 bits en incrementos de 8 bits. Longitud de clave predeterminada: 1.024 bits.<br/> La firma se ajusta a PKCS \# 6.<br/> |
| CALG \_ Sha          | Algoritmo de hash SHA.                                                                                                                                          | Para obtener más información, vea [*algoritmo hash seguro*](../secgloss/s-gly.md).               |
| CALG \_ SHA1         | Igual que **CALG \_ Sha**.                                                                                                                                          | Para obtener más información, vea [*algoritmo hash seguro*](../secgloss/s-gly.md).               |
| CALG \_ SHA \_ 256     | Algoritmo de hash SHA.                                                                                                                                          | Longitud de clave: 256 bits. **Windows XP:** Este algoritmo no es compatible.<br/>                                                                           |
| CALG \_ SHA \_ 384     | Algoritmo de hash SHA.                                                                                                                                          | Longitud de clave: 384 bits. **Windows XP:** Este algoritmo no es compatible.<br/>                                                                           |
| CALG \_ SHA \_ 512     | Algoritmo de hash SHA.                                                                                                                                          | Longitud de clave: 512 bits. **Windows XP:** Este algoritmo no es compatible.<br/>                                                                           |
| CALG \_ SSL3 \_ SHAMD5 | Algoritmo de autenticación del cliente de SSL3.                                                                                                                           | Para obtener más información, vea [crear un \_ \_ hash de SHAMD5 de CALG SSL3](creating-a-calg-ssl3-shamd5-hash.md).                                                      |



 

 

 
