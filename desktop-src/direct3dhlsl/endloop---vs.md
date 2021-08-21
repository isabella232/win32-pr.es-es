---
title: endloop- vs
description: Final de un bucle... bloque endloop.
ms.assetid: fd7df120-a927-4a66-b152-6ce5247446e4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cdd9158d12ecc29073526833a7a4ca5eec03100558a9ebdc711822c7ca74c9bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949895"
---
# <a name="endloop---vs"></a>endloop- vs

Final de un [bucle](loop---vs.md)... bloque endloop.

## <a name="syntax"></a>Syntax



| endloop |
|---------|



 

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| endloop                |      | x    | x    | x     | x    | x     |



 

Esta instrucción funciona como se muestra aquí.


```
LoopCounter += LoopStep;
LoopInterationCount = LoopIterationCount - 1;
if (LoopIterationCount > 0)
    Continue execution at the StartLoopOffset
```



endloop debe seguir la última instrucción de un [bucle: vs](loop---vs.md) block.

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

 

 




