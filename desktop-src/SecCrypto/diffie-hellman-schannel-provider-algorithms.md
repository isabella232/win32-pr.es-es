---
description: El propósito del algoritmo Diffie-Hellman es hacer posible que dos o más hosts creen y compartan una clave de cifrado secreta idéntica, simplemente compartiendo información a través de una red que no es segura.
ms.assetid: f89a1268-e364-41ec-a6a8-1f6331dbb787
title: Algoritmos de proveedor Diffie-Hellman/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d432a533c1f863aa9f3495f0f38147800246812b1f10bb8a728a650548b4a89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100845"
---
# <a name="diffie-hellmanschannel-provider-algorithms"></a>Algoritmos de proveedor Diffie-Hellman/Schannel

El propósito del algoritmo Diffie-Hellman es hacer posible que dos o más hosts creen y compartan una clave de cifrado secreta idéntica, simplemente compartiendo información a través de una red que no es segura. La información que se comparte a través de la red tiene el formato de un par de valores constantes y una clave pública D-H.

El proveedor [*criptográfico Schannel De Microsoft Diffie-Hellman*](../secgloss/d-gly.md) / [](../secgloss/s-gly.md) admite los algoritmos siguientes.



| Id. de algoritmo                  | Descripción                                                                                                                                           | Comentarios                                                                                                   |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| CALG \_ DH \_ SF                  | Diffie-Hellman de intercambio de claves de almacenamiento y [ *reenvío*](../secgloss/k-gly.md) | Longitud de clave: se puede establecer, de 384 bits a 512 bits en incrementos de 8 bits. Longitud de clave predeterminada: 512 bits.<br/> |
| CALG \_ MD5                     | Algoritmo de hash MD5.                                                                                                                                | Solo se proporciona para el hash.                                                                                 |
| CALG \_ DH \_ EPHEM               | Intercambio de claves D-H efímero.                                                                                                                           | Longitud de clave: se puede establecer, de 384 bits a 512 bits en incrementos de 8 bits. Longitud de clave predeterminada: 512 bits.<br/> |
| CALG \_ SHA                     | Algoritmo de hash SHA.                                                                                                                                | Debe usarse para las firmas de DSS.                                                                           |
| CALG \_ RC2                     | Algoritmo de cifrado de bloques RC2                                                                                                                        | Longitud de clave: de 40 a 88 bits.                                                                                 |
| CALG \_ RC4                     | Algoritmo de cifrado de secuencias RC4                                                                                                                       | Longitud de clave: de 40 a 88 bits.                                                                                 |
| CALG \_ CYLINK \_ MEK<br/> | Algoritmo de cifrado de variantes DES                                                                                                                      | Longitud de clave: 40 bits.                                                                                       |



 

 

 
