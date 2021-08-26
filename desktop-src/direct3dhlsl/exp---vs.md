---
title: 'exp : frente a'
description: 'Proporciona una precisión total exponencial de 2x. | exp : frente a'
ms.assetid: 3644046b-3257-4257-9880-146ca50f6b0b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2b5b27067e83cbfd7604165ec1191d3371634aac15781a719377c92c69e29e6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067955"
---
# <a name="exp---vs"></a>exp : frente a

Proporciona una precisión total exponencial de 2<sup>x</sup>.

## <a name="syntax"></a>Syntax



| exp dst, src |
|--------------|



 

where

-   dst es el registro de destino.
-   src es un registro de origen. El registro de origen requiere el uso explícito de replicar swzzle, es decir, debe especificarse exactamente uno de los componentes .x, .y, .z, .w swzzle (o .r, .g, .b, .a equivalentes). Consulte [Source Register Swlingling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md).

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| exp                    | x    | x    | x    | x     | x    | x     |



 

Esta instrucción proporciona al menos 21 bits de precisión.

El fragmento de código siguiente muestra las operaciones realizadas:


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




