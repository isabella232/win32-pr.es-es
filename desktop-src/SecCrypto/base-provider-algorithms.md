---
description: El proveedor de servicios criptográficos básicos de Microsoft admite los siguientes algoritmos.
ms.assetid: 767d5192-6e8f-488a-b954-29d56488ccbb
title: Algoritmos de proveedor base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dee99bc67769e0a7e91f2d0ecc635576336fd5ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669823"
---
# <a name="base-provider-algorithms"></a>Algoritmos de proveedor base

El proveedor de servicios criptográficos básicos de Microsoft admite los siguientes algoritmos.



| IDENTIFICADOR de algoritmo                  | Descripción                                                                                                                                                               | Comentarios                                                                                                                                                                |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALG \_ MD2<br/>          | Algoritmo hash MD2<br/>                                                                                                                                          | Para obtener más información, consulte [*algoritmo MD2*](../secgloss/m-gly.md).<br/>                                         |
| CALG \_ MD5<br/>          | Algoritmo hash MD5<br/>                                                                                                                                          | Para obtener más información, vea [*algoritmo MD5*](../secgloss/m-gly.md).<br/>                                         |
| CALG \_ Sha<br/>          | Algoritmo hash SHA<br/>                                                                                                                                          | Para obtener más información, vea [*algoritmo hash seguro*](../secgloss/s-gly.md).<br/>                 |
| CALG \_ SHA1<br/>         | Igual que CALG \_ Sha<br/>                                                                                                                                              | Para obtener más información, vea [*algoritmo hash seguro*](../secgloss/s-gly.md).<br/>                 |
| \_Mac CALG<br/>          | Algoritmo hash con clave de [*código de autentificación de mensajes (Mac)*](../secgloss/m-gly.md) (Mac)<br/> | Cifrado de bloqueo de MAC.<br/>                                                                                                                                            |
| CALG \_ HMAC<br/>         | Algoritmo hash con clave de MAC<br/>                                                                                                                                       | Cálculo HMAC.<br/>                                                                                                                                            |
| CALG \_ SSL3 \_ SHAMD5<br/> | Algoritmo de autenticación del cliente de SLL3<br/>                                                                                                                           | Para obtener más información, vea [crear un \_ \_ hash de SHAMD5 de CALG SSL3](creating-a-calg-ssl3-shamd5-hash.md).<br/>                                                        |
| \_firma RSA de CALG \_<br/>    | Algoritmo de firma de clave pública RSA<br/>                                                                                                                             | Longitud de clave: se puede establecer entre 384 bits y 16.384 bits en incrementos de 8 bits.<br/> Longitud de clave predeterminada: 512 bits.<br/> La firma se ajusta a PKCS \# 6.<br/> |
| CALG \_ RSA \_ KEYX<br/>    | Algoritmo de intercambio de claves públicas RSA<br/>                                                                                                                              | Longitud de clave: se puede establecer entre 384 bits y 1024 bits en incrementos de 8 bits.<br/> Longitud de clave predeterminada: 512 bits.<br/>                                              |
| CALG \_ RC2<br/>          | Algoritmo de cifrado de bloques RC2<br/>                                                                                                                                 | Longitud de clave: 40 bits.<br/> Modo predeterminado: encadenamiento de bloques de cifrado.<br/> Tamaño de bloque: 64 bits.<br/> Longitud de sal: 88 bits.<br/>                        |
| CALG \_ RC4<br/>          | Algoritmo de cifrado de flujo RC4<br/>                                                                                                                                | Longitud de clave: 40 bits.<br/> Longitud de sal: 88 bits.<br/>                                                                                                        |
| CALG \_ des<br/>          | Cifrado DES<br/>                                                                                                                                                 | Para obtener más información, vea [*estándar de cifrado de datos*](../secgloss/d-gly.md) (des).<br/>  |



 

 

 
