---
description: El tamaño de un desafío de acceso de resumen debe ser inferior a 2048 bytes.
ms.assetid: 16c6728a-966b-436f-902d-3e12368986b6
title: Contenido de un desafío de resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a0f6ee840e4965ff9615052b57102409a977e5a90660772e963eaf06eb9875
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883165"
---
# <a name="contents-of-a-digest-challenge"></a>Contenido de un desafío de resumen

El tamaño de un desafío de acceso de resumen debe ser inferior a 2048 bytes. En el ejemplo siguiente se muestra un desafío asignado a la cadena de caracteres szChallenge.


```C++
szChallenge = "realm=\"Microsoft_Example_Forest\",";
algorithm = "MD5-sess\", qop=\"auth\", nonce=\"0123456789abcdef\"";
```



> [!Note]  
> La cadena de desafío se incluye entre comillas dobles y contiene comillas dobles incrustadas. Las comillas dobles insertadas deben ir precedidas (con escape) con una barra diagonal inversa ( \\ ).

 

Un desafío de resumen puede contener las siguientes directivas.



| Directiva         | Descripción                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| realm             | Sugerencia definida por la implementación para el cliente sobre qué [*credenciales*](/windows/desktop/SecGloss/c-gly) son necesarias. El cliente debe mostrar esta información al usuario si solicita credenciales.                                                  |
| algoritmo         | Microsoft Digest admite MD5 y MD5-Sess. Para obtener un rendimiento óptimo, use MD5-Sess.                                                                                                                                                                                                                     |
| qop               | Esta directiva se puede establecer en auth, auth-int o auth-conf. Para obtener más información, vea [Calidad de protección y cifrados.](quality-of-protection-and-ciphers.md)                                                                                                                                       |
| valor de seguridad             | Valor codificado único generado por el servidor para cada desafío. El cliente no debe modificar este valor.                                                                                                                                                                                       |
| Opaco            | Contiene una referencia para el [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly) que se establece. Para obtener más información, vea [Mantener el contexto de seguridad entre conexiones.](maintaining-the-security-context-between-connections.md) |
| cipher (solo SASL) | Lista de cifrados que admite el servidor. Este elemento solo puede estar presente en un desafío DE SASL implícita si la directiva qop especifica auth-conf. Para obtener más información, vea [Calidad de protección y cifrados.](quality-of-protection-and-ciphers.md)                                              |
| charset           | Esta directiva se puede establecer en utf-8 si el servidor puede procesar nombres de usuario y dominios con codificación UTF-8. Si el cliente entiende la directiva charset, puede responder mediante valores con codificación UTF-8.                                                                                                       |



 

Microsoft Digest genera la cadena de desafío Digest para las aplicaciones de servidor. Para obtener más información, [vea Generación del desafío de resumen.](generating-the-digest-challenge.md)

 

 
