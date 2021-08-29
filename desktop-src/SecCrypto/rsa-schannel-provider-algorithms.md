---
description: Los algoritmos pueden ser compatibles con el proveedor criptográfico RSA/Schannel de Microsoft.
ms.assetid: 8793f0e8-a368-42be-8351-c60d99c34fb9
title: Algoritmos de proveedor RSA/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688dd7f22e6353544690c14091d29af50fec94dc3b65d6733aefc2a9fa8387bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900529"
---
# <a name="rsaschannel-provider-algorithms"></a>Algoritmos de proveedor RSA/Schannel

Los siguientes algoritmos pueden ser compatibles con el proveedor [*criptográfico*](../secgloss/r-gly.md) / [*Schannel de*](../secgloss/s-gly.md) Microsoft RSA.



| Id. de algoritmo    | Descripción                                                                                                                         | Comentarios                                                                                                        |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| CALG \_ RSA \_ KEYX | Algoritmo de intercambio de [ *claves públicas* RSA](../secgloss/k-gly.md) | Longitud de clave: se puede establecer de 384 bits a 16 384 bits en incrementos de 8 bits. Longitud de clave predeterminada: 1024 bits.<br/> |
| CALG \_ MD5       | Algoritmo de hash MD5.                                                                                                              | Solo se proporciona para el hash.                                                                                      |
| CALG \_ SHA       | Algoritmo de hash SHA.                                                                                                              | Debe usarse para las firmas de DSS.                                                                                |
| CALG \_ RC2       | Algoritmo de cifrado de bloques RC2.                                                                                                     | Longitud de clave: de 40 a 88 bits                                                                                       |
| CALG \_ RC4       | Algoritmo de cifrado de secuencia RC4.                                                                                                    | Longitud de clave: de 40 a 88 bits                                                                                       |



 

 

 
