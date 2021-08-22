---
description: Los algoritmos siguientes calculan hashes y firmas digitales. Cada uno de estos algoritmos se admite en los proveedores criptográficos de Microsoft Base, Strong y Enhanced.
ms.assetid: 91bf898d-658a-4e45-aa6e-eded46657563
title: Algoritmos hash y de firma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c176b3a21ac5793f249f9aa7aceda897d53ea209f3e8e6bd260dc5ec529c92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006613"
---
# <a name="hash-and-signature-algorithms"></a>Algoritmos hash y de firma

Los algoritmos siguientes [*calculan hashes*](../secgloss/h-gly.md) y [*firmas digitales.*](../secgloss/d-gly.md) Cada uno de estos algoritmos se admite en los proveedores criptográficos de Microsoft Base, Strong y Enhanced. Los detalles internos de estos algoritmos están fuera del ámbito de esta documentación. Para obtener una lista de orígenes adicionales, consulte [Documentación adicional sobre criptografía.](additional-documentation-on-cryptography.md)



| Algoritmos                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MAC de encadenamiento de bloques de cifrado (CBC)<br/>     | Uno de los algoritmos (CALG MAC) implementados por los proveedores de Microsoft es un código de autenticación de mensajes \_ (MAC) [](../secgloss/b-gly.md) [*de*](../secgloss/m-gly.md) cifrado de bloques. Este método cifra los datos base con un cifrado de bloque y, a continuación, usa el último bloque cifrado como [*valor hash.*](../secgloss/h-gly.md) El algoritmo de cifrado utilizado para compilar el MAC es el que se especificó cuando se creó la clave de sesión. <br/>                                                                            |
| HMAC<br/>                                | Algoritmo (CALG \_ HMAC) implementado por proveedores de Microsoft. Este algoritmo también usa una [*clave*](../secgloss/s-gly.md) simétrica para crear el [*hash*](../secgloss/h-gly.md), pero es más complejo que el algoritmo MAC de encadenamiento de bloques de cifrado [*simple*](../secgloss/c-gly.md) (CBC). Se puede usar con cualquier algoritmo hash criptográfico iterado, como MD5 o SHA-1. Para obtener más información, [consulte Creación de un HMAC.](creating-an-hmac.md)<br/>                                                                                       |
| MD2, MD4 y MD5<br/>                   | Rsa Data Security, Inc. desarrolló todos estos algoritmos hash. Estos algoritmos se desarrollaron en orden secuencial. Los tres generan valores hash de 128 bits. Se sabe que los tres tienen puntos débiles y solo se deben usar cuando sea necesario con fines de compatibilidad. Para el código nuevo, se recomienda la familia sha-2 de hashes.<br/> Estos algoritmos son conocidos y se pueden revisar en detalle en cualquier referencia sobre [*criptografía*](../secgloss/c-gly.md).<br/>                                                                                                                                                           |
| Código de autenticación de mensajes (MAC)<br/>   | Los algoritmos MAC son similares [*a los algoritmos hash,*](../secgloss/h-gly.md) pero se calculan mediante una [*clave simétrica*](../secgloss/s-gly.md) (sesión). La clave [*de sesión original*](../secgloss/s-gly.md) es necesaria para volver a compilar el valor hash. El valor hash recomputado se usa para comprobar que no se han cambiado los datos base. Estos algoritmos a veces se denominan algoritmos hash con clave. Para ver qué proveedores de Microsoft admiten MAC, consulte [Proveedores de servicios criptográficos de Microsoft](microsoft-cryptographic-service-providers.md).<br/>    |
| Algoritmo hash seguro (SHA-1)<br/>       | Este algoritmo hash fue desarrollado por el Instituto [*Nacional*](../secgloss/n-gly.md) de Estándares y Tecnología (NIST) y por la Agencia de Seguridad Nacional (NSA). Este algoritmo se desarrolló para su uso con DSA (algoritmo de firma digital) o DSS (estándar de firma digital). Este algoritmo genera un valor [*hash*](../secgloss/h-gly.md) de 160 bits. Se sabe que SHA-1 tiene puntos débiles y solo se debe usar cuando sea necesario por motivos de compatibilidad. Para el código nuevo, se recomienda la familia sha-2 de hashes.<br/> |
| Algoritmo hash seguro: 2 (SHA-2)<br/>   | Este algoritmo hash fue desarrollado como sucesor de SHA-1 por el Instituto [*Nacional*](../secgloss/n-gly.md) de Estándares y Tecnología (NIST) y la Agencia de Seguridad Nacional (NSA). Tiene cuatro variantes: SHA-224, SHA-256, SHA-384 y SHA-512, que se denominan según el número de bits en sus salidas. De estos, SHA-256, SHA-384 y SHA-512 se implementan en el proveedor criptográfico de Microsoft AES.<br/>                                                                                                                                |
| Algoritmo de autorización de cliente SSL3<br/> | Este algoritmo se usa para la autenticación de cliente SSL3. En el protocolo SSL3, se firma una concatenación de un hash MD5 y un hash SHA con una clave [*privada*](../secgloss/p-gly.md)RSA . CryptoAPI 2.0 y los proveedores de servicios criptográficos mejorados y base de Microsoft lo admiten con el tipo [*hash*](../secgloss/h-gly.md) CALG \_ SSL3 \_ SHAMD5. Para obtener más información, vea [Creating a CALG \_ SSL3 \_ SHAMD5 Hash](creating-a-calg-ssl3-shamd5-hash.md).<br/>                                                                                                                                               |



 

 

 
