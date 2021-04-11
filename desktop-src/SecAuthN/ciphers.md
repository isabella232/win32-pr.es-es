---
description: El material siguiente solo es válido cuando se usa Digest como mecanismo SASL. Los cifrados y el cifrado no están disponibles para la autenticación HTTP mediante Microsoft Digest.
ms.assetid: 3836b064-241f-4276-af08-557bdc53bb36
title: Ciphers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9637fee72e6f9521968eed432dcd83947a5ddd01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276165"
---
# <a name="ciphers"></a>Ciphers

El material siguiente solo es válido cuando se usa Digest como mecanismo SASL. Los cifrados y el cifrado no están disponibles para la autenticación HTTP mediante Microsoft Digest.

Una directiva de cifrado de un desafío SASL de síntesis contiene una lista de los cifrados admitidos por un servidor que requiere comunicaciones confidenciales. La Directiva Cipher solo se puede incluir si la Directiva qop se establece en "auth-conf". Los cifrados reconocidos por Microsoft Digest se muestran en la siguiente tabla, en orden de mayor a menor.



| Valor de cifrado | Descripción                                                                                                                                                                                                                                                                                    |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RC4        | El cifrado RC4 con una clave de 128 bits.                                                                                                                                                                                                                                                             |
| dicha       | El cifrado [*triple des*](/windows/desktop/SecGloss/t-gly) en el modo [*CBC*](/windows/desktop/SecGloss/c-gly) con Ede con la misma clave para cada fase E (modo de dos claves). La longitud total de la clave es de 112 bits. |
| "RC4-56"     | El cifrado RC4 con una clave de 56 bits.                                                                                                                                                                                                                                                              |
| "RC4-40"     | El cifrado RC4 con una clave de 40 bits.                                                                                                                                                                                                                                                              |
| des        | El cifrado del [*estándar de cifrado de datos*](/windows/desktop/SecGloss/d-gly) (des) en el modo de [*encadenamiento de bloques de cifrado*](/windows/desktop/SecGloss/c-gly) (CBC) con una clave de 56 bits. |



 

Cuando una aplicación de servidor solicita confidencialidad (qop = "auth-conf") Microsoft Digest generará un desafío que ofrece al cliente todos los cifrados instalados en el servidor y que es compatible con el resumen. El cliente de síntesis seleccionará el cifrado más seguro disponible. Para obtener más información sobre cómo especificar la confidencialidad, consulte [generación del desafío de síntesis](generating-the-digest-challenge.md).

 

 
