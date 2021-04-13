---
description: El tamaño de un desafío de acceso implícita debe ser inferior a 2048 bytes.
ms.assetid: 16c6728a-966b-436f-902d-3e12368986b6
title: Contenido de un desafío de síntesis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f90dd78ae28536f6e2d07882f69335975df14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153845"
---
# <a name="contents-of-a-digest-challenge"></a>Contenido de un desafío de síntesis

El tamaño de un desafío de acceso implícita debe ser inferior a 2048 bytes. En el ejemplo siguiente se muestra un desafío asignado a la cadena de caracteres szChallenge.


```C++
szChallenge = "realm=\"Microsoft_Example_Forest\",";
algorithm = "MD5-sess\", qop=\"auth\", nonce=\"0123456789abcdef\"";
```



> [!Note]  
> La cadena de desafío está entre comillas dobles y contiene comillas dobles incrustadas. Las comillas dobles incrustadas deben ir precedidas de una barra diagonal inversa ( \\ ).

 

Un desafío de síntesis puede contener las siguientes directivas.



| Directiva         | Descripción                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| realm             | Una sugerencia definida por la implementación al cliente sobre qué [*credenciales*](/windows/desktop/SecGloss/c-gly) se requieren. El cliente debe mostrar esta información al usuario si solicita las credenciales.                                                  |
| algoritmo         | Microsoft Digest admite MD5 y MD5-SESS. Para obtener un rendimiento óptimo, use MD5-SESS.                                                                                                                                                                                                                     |
| qop               | Esta Directiva se puede establecer en auth, auth-int o auth-conf. Para obtener más información, vea [calidad de protección y cifrado](quality-of-protection-and-ciphers.md).                                                                                                                                       |
| valor de seguridad             | Valor codificado único generado por el servidor para cada desafío. El cliente no debe modificar este valor.                                                                                                                                                                                       |
| opaco            | Contiene una referencia para el [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly) que se está estableciendo. Para obtener más información, vea [mantener el contexto de seguridad entre conexiones](maintaining-the-security-context-between-connections.md). |
| Cipher (solo SASL) | La lista de cifrados que admite el servidor. Este elemento puede estar presente en un desafío de SASL implícito solo si la Directiva qop especifica auth-conf. Para obtener más información, vea [calidad de protección y cifrado](quality-of-protection-and-ciphers.md).                                              |
| charset           | Esta Directiva se puede establecer en UTF-8 Si el servidor puede procesar nombres de usuario y territorios codificados en UTF-8. Si el cliente entiende la Directiva charset, puede responder mediante valores con codificación UTF-8.                                                                                                       |



 

Microsoft Digest genera la cadena de desafío de síntesis para las aplicaciones de servidor. Para obtener más información, consulte [generación del desafío de síntesis](generating-the-digest-challenge.md).

 

 
