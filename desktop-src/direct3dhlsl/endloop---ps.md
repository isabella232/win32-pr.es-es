---
title: ENDLOOP-PS
description: Final de un bucle-PS... bloque ENDLOOP.
ms.assetid: 8d05d0b3-88d2-44e3-a22d-54d8a8ceb5f4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee1a7eb10146e40a39c05bcecb99d3a7667dee2c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103994825"
---
# <a name="endloop---ps"></a>ENDLOOP-PS

Final de un [bucle-PS](loop---ps.md)... bloque ENDLOOP.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| ENDLOOP               |      |      |      |      |      |      |       | x    | x     |



 

ENDLOOP debe seguir la última instrucción de un bloque [de bucle-PS](loop---ps.md) .

## <a name="example"></a>Ejemplo


```
loop aL, i3
    add r1, r0, c2[ aL ]
endloop
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




