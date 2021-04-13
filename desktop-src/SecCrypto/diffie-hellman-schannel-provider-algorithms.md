---
description: El propósito del algoritmo Diffie-Hellman es hacer posible que dos o más hosts creen y compartan una clave de cifrado secreta idéntica, simplemente compartiendo información a través de una red que no es segura.
ms.assetid: f89a1268-e364-41ec-a6a8-1f6331dbb787
title: Algoritmos de proveedor Diffie-Hellman/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4fb88e3a50e15a6690340ab3fbcee91da1193a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361627"
---
# <a name="diffie-hellmanschannel-provider-algorithms"></a>Algoritmos de proveedor Diffie-Hellman/Schannel

El propósito del algoritmo Diffie-Hellman es hacer posible que dos o más hosts creen y compartan una clave de cifrado secreta idéntica, simplemente compartiendo información a través de una red que no es segura. La información que se comparte a través de la red está en forma de un par de valores constantes y una clave pública D-H.

El proveedor de servicios criptográficos [*de Microsoft Diffie-Hellman*](../secgloss/d-gly.md) / [*Schannel*](../secgloss/s-gly.md) admite los siguientes algoritmos.



| IDENTIFICADOR de algoritmo                  | Descripción                                                                                                                                           | Comentarios                                                                                                   |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| CALG \_ DH \_ SF                  | Algoritmo de intercambio de [ *claves* de almacenamiento y reenvío Diffie-Hellman](../secgloss/k-gly.md) | Longitud de clave: se puede establecer, de 384 bits a 512 bits en incrementos de 8 bits. Longitud de clave predeterminada: 512 bits.<br/> |
| CALG \_ MD5                     | Algoritmo de hash MD5.                                                                                                                                | Solo se proporciona para el hash.                                                                                 |
| CALG \_ DH \_ EPHEM               | Intercambio de claves en D-H efímero.                                                                                                                           | Longitud de clave: se puede establecer, de 384 bits a 512 bits en incrementos de 8 bits. Longitud de clave predeterminada: 512 bits.<br/> |
| CALG \_ Sha                     | Algoritmo de hash SHA.                                                                                                                                | Debe usarse para las firmas de DSS.                                                                           |
| CALG \_ RC2                     | Algoritmo de cifrado de bloques RC2                                                                                                                        | Longitud de clave: de 40 a 88 bits.                                                                                 |
| CALG \_ RC4                     | Algoritmo de cifrado de flujo RC4                                                                                                                       | Longitud de clave: de 40 a 88 bits.                                                                                 |
| CALG \_ CYLINK \_ clave MEK<br/> | Algoritmo de cifrado DES variante                                                                                                                      | Longitud de clave: 40 bits.                                                                                       |



 

 

 
