---
description: Las claves criptográficas son fundamentales para las operaciones criptográficas.
ms.assetid: dda7b527-1522-4b43-8d8e-44ce7983a9aa
title: Claves criptográficas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25647d64aafa8d996c60df37d1f5b5a86226451e1a0f3a3cfefc7ef405f3a11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876305"
---
# <a name="cryptographic-keys"></a>Claves criptográficas

[*Las claves criptográficas*](../secgloss/c-gly.md) son fundamentales para las operaciones criptográficas. Muchos esquemas criptográficos constan de pares de operaciones, como cifrado y descifrado, o firma y comprobación. Una *clave* es un fragmento de datos variables que se introducen como entrada en un algoritmo criptográfico para realizar una de estas operaciones. En un esquema criptográfico bien diseñado, la seguridad del esquema depende solo de la seguridad de las claves usadas.

Las claves criptográficas se pueden clasificar en función de su uso dentro de un esquema criptográfico, como claves [simétricas](symmetric-keys.md) o [claves asimétricas.](public-private-key-pairs.md) Una [*clave simétrica*](../secgloss/s-gly.md) es una clave única que se usa para ambas [](../secgloss/e-gly.md) operaciones en un esquema criptográfico (por ejemplo, para cifrar y [*descifrar*](../secgloss/d-gly.md) los datos). Normalmente, la seguridad del esquema depende de garantizar que la clave solo la conozcan los participantes autorizados. Por otro lado, las claves asimétricas se usan en esquemas criptográficos donde se necesitan claves diferentes para cada operación. Ejemplos comunes de estos esquemas son los que usan pares de claves pública [](../secgloss/p-gly.md) y [*privada,*](../secgloss/p-gly.md)donde la seguridad del esquema depende de garantizar que solo una parte conozca la clave privada. Por ejemplo, los sistemas de cifrado de [](../secgloss/p-gly.md) claves pública y privada usan [](../secgloss/p-gly.md) dos claves, una clave pública que cualquiera puede usar para cifrar los datos y una clave privada que solo posee el destinatario autorizado y que se puede usar para descifrar los datos.

Las claves criptográficas se pueden clasificar aún más por el propósito para el que se usan. Estos usos incluyen la generación de firmas digitales, la verificación de firmas digitales, la autenticación de mensajes, el cifrado y descifrado de datos, el ajuste de claves y el transporte de claves. Para obtener una lista completa de [](../secgloss/n-gly.md) los tipos clave definidos por el Instituto Nacional de Estándares y Tecnología (NIST), vea la sección 5 GENERAL KEY MANAGEMENT GUIDANCE of [NIST Special Publication 800-57: Recommendation for Key Management – Part 1: General (Revised)](https://csrc.nist.gov/publications/nistpubs/800-57/sp800-57-Part1-revised2_Mar08-2007.pdf).

 

 
