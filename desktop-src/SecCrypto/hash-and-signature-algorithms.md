---
description: Los algoritmos siguientes calculan los hashes y las firmas digitales. Cada uno de estos algoritmos es compatible con los proveedores de servicios criptográficos de Microsoft base, Strong y mejorado.
ms.assetid: 91bf898d-658a-4e45-aa6e-eded46657563
title: Algoritmos hash y de firma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc1ca0819aebc01bba342410eda20b626349f1b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669892"
---
# <a name="hash-and-signature-algorithms"></a>Algoritmos hash y de firma

Los algoritmos siguientes calculan los [*hashes*](../secgloss/h-gly.md) y las [*firmas digitales*](../secgloss/d-gly.md). Cada uno de estos algoritmos es compatible con los proveedores de servicios criptográficos de Microsoft base, Strong y mejorado. Los detalles internos de estos algoritmos están fuera del ámbito de esta documentación. Para obtener una lista de orígenes adicionales, consulte la [documentación adicional sobre la criptografía](additional-documentation-on-cryptography.md).



| Algoritmos                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MAC de encadenamiento de bloques de cifrado (CBC)<br/>     | Uno de los algoritmos (CALG \_ Mac) que implementan los proveedores de Microsoft es un [*cifrado de bloque*](../secgloss/b-gly.md) [*código de autentificación de mensajes (Mac)*](../secgloss/m-gly.md) (Mac). Este método cifra los datos base con un cifrado de bloques y, a continuación, usa el último bloque cifrado como el valor [*hash*](../secgloss/h-gly.md) . El algoritmo de cifrado usado para compilar el equipo MAC es el que se especificó cuando se creó la clave de sesión. <br/>                                                                            |
| HMAC<br/>                                | Un algoritmo (CALG \_ HMAC) implementado por proveedores de Microsoft. Este algoritmo también usa una [*clave simétrica*](../secgloss/s-gly.md) para crear el [*hash*](../secgloss/h-gly.md), pero es más complejo que el algoritmo Mac simple de [*encadenamiento de bloques de cifrado*](../secgloss/c-gly.md) (CBC). Se puede usar con cualquier algoritmo hash criptográfico iterado, como MD5 o SHA-1. Para obtener más información, vea [crear un HMAC](creating-an-hmac.md).<br/>                                                                                       |
| MD2, MD4 y MD5<br/>                   | Los algoritmos hash fueron desarrollados por RSA Data Security, Inc. Estos algoritmos se desarrollaron en orden secuencial. Los tres valores de hash de 128 bits de generación. Los tres se sabe que tienen debilidades y solo se deben usar cuando sea necesario por compatibilidad. Para el nuevo código, se recomienda la familia de algoritmos hash SHA-2.<br/> Estos algoritmos son muy conocidos y se pueden revisar en detalle en cualquier referencia sobre [*Criptografía*](../secgloss/c-gly.md).<br/>                                                                                                                                                           |
| Código de autentificación de mensajes (MAC) (MAC)<br/>   | Los algoritmos de MAC son similares a los algoritmos [*hash*](../secgloss/h-gly.md) , pero se calculan mediante una clave [*simétrica*](../secgloss/s-gly.md) (sesión). La [*clave de sesión*](../secgloss/s-gly.md) original es necesaria para volver a calcular el valor hash. El valor hash recalculado se usa para comprobar que los datos base no se cambiaron. Estos algoritmos a veces se denominan algoritmos hash con clave. Para ver qué proveedores de Microsoft son compatibles con MAC, consulte [proveedores de servicios criptográficos de Microsoft](microsoft-cryptographic-service-providers.md).<br/>    |
| Algoritmo hash seguro (SHA-1)<br/>       | Este algoritmo hash fue desarrollado por el National [*Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST) y por National Security Agency (NSA). Este algoritmo se desarrolló para su uso con DSA (algoritmo de firma digital) o DSS (estándar de firma digital). Este algoritmo genera un valor [*hash*](../secgloss/h-gly.md) de 160 bits. Se sabe que SHA-1 tiene debilidades y solo se debe usar cuando sea necesario por compatibilidad. Para el nuevo código, se recomienda la familia de algoritmos hash SHA-2.<br/> |
| Algoritmo hash seguro-2 (SHA-2)<br/>   | Este algoritmo hash se desarrolló como sucesor de SHA-1 por el [*Instituto Nacional de estándares y Tecnología*](../secgloss/n-gly.md) (NIST) y National Security Agency (NSA). Tiene cuatro variantes, SHA-224, SHA-256, SHA-384 y SHA-512, que se denominan según el número de bits en sus salidas. De estos, SHA-256, SHA-384 y SHA-512 se implementan en el proveedor de servicios criptográficos AES de Microsoft.<br/>                                                                                                                                |
| Algoritmo de autorización de cliente de SSL3<br/> | Este algoritmo se utiliza para la autenticación de cliente de SSL3. En el protocolo SSL3, una concatenación de un hash MD5 y un hash SHA se firma con una [*clave privada*](../secgloss/p-gly.md)RSA. CryptoAPI 2.0 y los proveedores de servicios criptográficos mejorados y base de Microsoft lo admiten con el tipo de [*hash*](../secgloss/h-gly.md) CALG \_ SSL3 \_ SHAMD5. Para obtener más información, vea [crear un \_ \_ hash de SHAMD5 de CALG SSL3](creating-a-calg-ssl3-shamd5-hash.md).<br/>                                                                                                                                               |



 

 

 
