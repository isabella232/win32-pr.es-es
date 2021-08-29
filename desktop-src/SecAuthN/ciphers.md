---
description: El siguiente material solo es válido cuando se usa Digest como mecanismo SASL. Los cifrados y el cifrado no están disponibles para la autenticación HTTP mediante Microsoft Digest.
ms.assetid: 3836b064-241f-4276-af08-557bdc53bb36
title: Ciphers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d406b610964cb07e88295c472d89a600586308d482f02e7f04633f2a01be6b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883515"
---
# <a name="ciphers"></a>Ciphers

El siguiente material solo es válido cuando se usa Digest como mecanismo SASL. Los cifrados y el cifrado no están disponibles para la autenticación HTTP mediante Microsoft Digest.

La directiva de cifrado de un desafío de SASL implícita contiene una lista de los cifrados admitidos por un servidor que requiere comunicaciones confidenciales. La directiva de cifrado solo se puede incluir si la directiva qop está establecida en "auth-conf". Los cifrados reconocidos por Microsoft Digest se enumeran en la tabla siguiente, en orden de más fuerte a más débil.



| Valor de cifrado | Descripción                                                                                                                                                                                                                                                                                    |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "rc4"        | Cifrado RC4 con una clave de 128 bits.                                                                                                                                                                                                                                                             |
| "3des"       | Cifrado [*de DES*](/windows/desktop/SecGloss/t-gly) triple en [*modo CBC*](/windows/desktop/SecGloss/c-gly) con EDE con la misma clave para cada fase E (modo de dos claves). La longitud total de la clave es de 112 bits. |
| "rc4-56"     | Cifrado RC4 con una clave de 56 bits.                                                                                                                                                                                                                                                              |
| "rc4-40"     | Cifrado RC4 con una clave de 40 bits.                                                                                                                                                                                                                                                              |
| "des"        | Cifrado [*estándar de cifrado*](/windows/desktop/SecGloss/d-gly) de datos (DES) en modo de encadenamiento de bloques de cifrado (CBC) con una clave de 56 bits. [](/windows/desktop/SecGloss/c-gly) |



 

Cuando una aplicación de servidor solicita confidencialidad (qop="auth-conf") Microsoft Digest generará un desafío que ofrece al cliente todos los cifrados instalados en el servidor y admitidos por Digest. El cliente de resumen seleccionará el cifrado más seguro disponible. Para obtener más información sobre cómo especificar la confidencialidad, vea [Generación del desafío de resumen](generating-the-digest-challenge.md).

 

 
