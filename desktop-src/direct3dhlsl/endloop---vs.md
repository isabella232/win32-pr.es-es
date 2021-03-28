---
title: ENDLOOP-vs
description: Fin de un bucle... bloque ENDLOOP.
ms.assetid: fd7df120-a927-4a66-b152-6ce5247446e4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a9aec4d1b2c5237a87fae2c0beab4e8d995db97
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419879"
---
# <a name="endloop---vs"></a>ENDLOOP-vs

Fin de un [bucle](loop---vs.md)... bloque ENDLOOP.

## <a name="syntax"></a>Sintaxis



| ENDLOOP |
|---------|



 

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| ENDLOOP                |      | x    | x    | x     | x    | x     |



 

Esta instrucción funciona como se muestra aquí.


```
LoopCounter += LoopStep;
LoopInterationCount = LoopIterationCount - 1;
if (LoopIterationCount > 0)
    Continue execution at the StartLoopOffset
```



ENDLOOP debe seguir la última instrucción de un bloque [Loop-vs](loop---vs.md) .

## <a name="example"></a>Ejemplo


```
loop aL, i3
    add r1, r0, c2[ aL ]
endloop
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




