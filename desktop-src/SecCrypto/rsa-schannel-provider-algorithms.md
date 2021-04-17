---
description: Es posible que el proveedor de servicios criptográficos de Microsoft RSA/Schannel admita los algoritmos.
ms.assetid: 8793f0e8-a368-42be-8351-c60d99c34fb9
title: Algoritmos de proveedor RSA/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9dc3293b0938e9c9e89e955b26eac2a40ac198b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666521"
---
# <a name="rsaschannel-provider-algorithms"></a>Algoritmos de proveedor RSA/Schannel

Es posible que el proveedor de servicios criptográficos de Microsoft [*RSA*](../secgloss/r-gly.md)Schannel admita los siguientes algoritmos / [](../secgloss/s-gly.md) .



| IDENTIFICADOR de algoritmo    | Descripción                                                                                                                         | Comentarios                                                                                                        |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| CALG \_ RSA \_ KEYX | [ *Algoritmo de intercambio de claves* de clave pública RSA](../secgloss/k-gly.md) | Longitud de clave: se puede establecer, de 384 bits a 16.384 bits en incrementos de 8 bits. Longitud de clave predeterminada: 1.024 bits.<br/> |
| CALG \_ MD5       | Algoritmo de hash MD5.                                                                                                              | Solo se proporciona para el hash.                                                                                      |
| CALG \_ Sha       | Algoritmo de hash SHA.                                                                                                              | Debe usarse para las firmas de DSS.                                                                                |
| CALG \_ RC2       | Algoritmo de cifrado de bloques RC2.                                                                                                     | Longitud de clave: de 40 a 88 bits                                                                                       |
| CALG \_ RC4       | Algoritmo de cifrado de flujo RC4.                                                                                                    | Longitud de clave: de 40 a 88 bits                                                                                       |



 

 

 
