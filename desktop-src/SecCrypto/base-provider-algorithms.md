---
description: El proveedor criptográfico base de Microsoft admite los algoritmos siguientes.
ms.assetid: 767d5192-6e8f-488a-b954-29d56488ccbb
title: Algoritmos de proveedor base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6b6f3af49529ad46e70dd154c06febf433f5fb483861f7c0b2530af7ebbef2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879755"
---
# <a name="base-provider-algorithms"></a>Algoritmos de proveedor base

El proveedor criptográfico base de Microsoft admite los algoritmos siguientes.



| Id. de algoritmo                  | Descripción                                                                                                                                                               | Comentarios                                                                                                                                                                |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALG \_ MD2<br/>          | Algoritmo hash MD2<br/>                                                                                                                                          | Para obtener más información, vea [*Algoritmo MD2*](../secgloss/m-gly.md).<br/>                                         |
| CALG \_ MD5<br/>          | Algoritmo hash MD5<br/>                                                                                                                                          | Para obtener más información, vea [*Algoritmo MD5*](../secgloss/m-gly.md).<br/>                                         |
| CALG \_ SHA<br/>          | Algoritmo hash SHA<br/>                                                                                                                                          | Para obtener más información, vea [*Secure Hash Algorithm*](../secgloss/s-gly.md).<br/>                 |
| CALG \_ SHA1<br/>         | Igual que CALG \_ SHA<br/>                                                                                                                                              | Para obtener más información, vea [*Secure Hash Algorithm*](../secgloss/s-gly.md).<br/>                 |
| CALG \_ MAC<br/>          | [*Algoritmo hash con*](../secgloss/m-gly.md) clave de código de autenticación de mensajes (MAC)<br/> | Bloquear mac de cifrado.<br/>                                                                                                                                            |
| CALG \_ HMAC<br/>         | Algoritmo hash con clave MAC<br/>                                                                                                                                       | Cálculo HMAC.<br/>                                                                                                                                            |
| CALG \_ SSL3 \_ SHAMD5<br/> | Algoritmo de autenticación de cliente SLL3<br/>                                                                                                                           | Para obtener más información, vea [Creating a CALG \_ SSL3 \_ SHAMD5 Hash](creating-a-calg-ssl3-shamd5-hash.md).<br/>                                                        |
| CALG \_ RSA \_ SIGN<br/>    | Algoritmo de firma de clave pública RSA<br/>                                                                                                                             | Longitud de clave: se puede establecer de 384 bits a 16 384 bits en incrementos de 8 bits.<br/> Longitud de clave predeterminada: 512 bits.<br/> La firma se ajusta a PKCS \# 6.<br/> |
| CALG \_ RSA \_ KEYX<br/>    | Algoritmo de intercambio de claves públicas RSA<br/>                                                                                                                              | Longitud de clave: se puede establecer de 384 bits a 1024 bits en incrementos de 8 bits.<br/> Longitud de clave predeterminada: 512 bits.<br/>                                              |
| CALG \_ RC2<br/>          | Algoritmo de cifrado de bloques RC2<br/>                                                                                                                                 | Longitud de clave: 40 bits.<br/> Modo predeterminado: encadenamiento de bloques de cifrado.<br/> Tamaño del bloque: 64 bits.<br/> Longitud de sal: 88 bits.<br/>                        |
| CALG \_ RC4<br/>          | Algoritmo de cifrado de flujo RC4<br/>                                                                                                                                | Longitud de clave: 40 bits.<br/> Longitud de sal: 88 bits.<br/>                                                                                                        |
| CALG \_ DES<br/>          | Cifrado DES<br/>                                                                                                                                                 | Para obtener más información, [*vea Estándar de cifrado de datos*](../secgloss/d-gly.md) (DES).<br/>  |



 

 

 
