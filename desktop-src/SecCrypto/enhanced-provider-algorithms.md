---
description: El proveedor criptográfico mejorado de Microsoft admite los algoritmos siguientes.
ms.assetid: d58bcd99-c54b-4fda-9fe1-e10a66707d81
title: Algoritmos de proveedor mejorados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a8be464a57a482fa74fef07de097508508d7e965a5c20817ccbd884bb169e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766106"
---
# <a name="enhanced-provider-algorithms"></a>Algoritmos de proveedor mejorados

El [proveedor criptográfico mejorado de Microsoft](microsoft-enhanced-cryptographic-provider.md) admite los algoritmos siguientes.



| Id. de algoritmo       | Descripción                                                                                                                                                     | Comentarios                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALG \_ 3DES         | Triple DES.                                                                                                                                                     | Longitud de clave: 168 bits. Modo predeterminado: encadenamiento de bloques de cifrado.<br/> Tamaño del bloque: 64 bits.<br/> No se permite sal.<br/>                           |
| CALG \_ 3DES \_ 112    | Cifrado [*DES triple de*](../secgloss/t-gly.md) dos claves.                                                            | Longitud de clave: 112 bits. Modo predeterminado: encadenamiento de bloques de cifrado.<br/> Tamaño del bloque: 64 bits.<br/> No se permite sal.<br/>                           |
| CALG \_ DES          | Cifrado DES.                                                                                                                                                 | Longitud de clave: 56 bits. Modo predeterminado: encadenamiento de bloques de cifrado.<br/> Tamaño del bloque: 64 bits.<br/> No se permite sal.<br/>                            |
| CALG \_ HMAC         | Algoritmo de hash con claves de MAC.                                                                                                                                       | Cálculo HMAC.                                                                                                                                          |
| CALG \_ MAC          | [*Algoritmo*](../secgloss/m-gly.md) hash con clave de código de autenticación de mensajes (MAC). | Bloquear mac de cifrado.                                                                                                                                          |
| CALG \_ MD2          | Algoritmo de hash MD2.                                                                                                                                          | Para obtener más información, vea [*Algoritmo MD2*](../secgloss/m-gly.md).                                       |
| CALG \_ MD5          | Algoritmo de hash MD5.                                                                                                                                          | Para obtener más información, vea [*Algoritmo MD5*](../secgloss/m-gly.md).                                       |
| CALG \_ RC2          | Algoritmo de cifrado de bloque RC2.                                                                                                                                 | Longitud de clave: 128 bits. Modo predeterminado: encadenamiento de bloques de cifrado.<br/> Tamaño del bloque: 64 bits.<br/> Longitud de sal: se puede establecer.<br/>                   |
| CALG \_ RC4          | Algoritmo de cifrado de secuencia RC4.                                                                                                                                | Longitud de clave: 128 bits. Longitud de sal: se puede establecer.<br/>                                                                                                   |
| CALG \_ RSA \_ KEYX    | Algoritmo de intercambio de claves públicas RSA.                                                                                                                              | Longitud de clave: se puede establecer entre 384 bits y 16 384 bits en incrementos de 8 bits. Longitud de clave predeterminada: 1024 bits.<br/>                                            |
| CALG \_ RSA \_ SIGN    | Algoritmo de firma de clave pública RSA.                                                                                                                             | Longitud de clave: se puede establecer entre 384 bits y 16 384 bits en incrementos de 8 bits. Longitud de clave predeterminada: 1024 bits.<br/> La firma se ajusta a PKCS \# 6.<br/> |
| CALG \_ SHA          | Algoritmo de hash SHA.                                                                                                                                          | Para obtener más información, vea [*Secure Hash Algorithm*](../secgloss/s-gly.md).               |
| CALG \_ SHA1         | Igual que CALG \_ SHA.                                                                                                                                              | Para obtener más información, vea [*Secure Hash Algorithm*](../secgloss/s-gly.md).               |
| CALG \_ SSL3 \_ SHAMD5 | Algoritmo de autenticación de cliente SSL3.                                                                                                                           | Para obtener más información, vea [Creating a CALG \_ SSL3 \_ SHAMD5 Hash](creating-a-calg-ssl3-shamd5-hash.md).                                                      |



 

 

 
