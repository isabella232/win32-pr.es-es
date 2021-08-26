---
title: expp - vs
description: Proporciona una precisión parcial exponencial de 2x.
ms.assetid: ac080ac9-5dfd-49e4-92ea-50bb26844ff6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e8717edc045f50cc572d675dbec405b01fda49503349e9716210dfcae23fb277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982455"
---
# <a name="expp---vs"></a>expp - vs

Proporciona una precisión parcial exponencial de 2<sup>x</sup>.

## <a name="syntax"></a>Syntax



| expp dst, src. {x\|y\|z\|w} |
|----------------------------|



 

Donde:

-   dst es el registro de destino.
-   src es un registro de origen. El registro de origen requiere el uso explícito de replicar swzzle, es decir, debe especificarse exactamente uno de los componentes .x, .y, .z, .w swzzle (o .r, .g, .b, .a equivalentes).
-   {x \| y \| z \| w} es la réplica necesaria en el registro de origen.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| expp                   | x    | x    | x    | x     | x    | x     |



 

### <a name="vs_1_1"></a>vs \_ 1 \_ 1

La [instrucción exp - vs](exp---vs.md) funciona de forma diferente en función de las versiones del sombreador de vértices.

En comparación \_ con \_ 1 1, la instrucción expp proporciona los siguientes resultados:


```
v = the scalar value from the source register with a replicate swizzle

dest.x = pow(2, floor(v))
dest.y = v - floor(v)
dest.z = pow(2, v) (partial-precision)
dest.w = 1
```



En comparación \_ con 2 \_ 0 y versiones 2 y 2, la instrucción expp proporciona los siguientes resultados:


```
v = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow(2, v) (partial-precision)
```



### <a name="vs_2_0"></a>vs \_ 2 \_ 0

En comparación \_ con 2 \_ 0 y 0, la instrucción funciona de la siguiente forma:


```
float V = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow( 2, V ) (partial-precision)
```



La instrucción proporciona al menos 10 bits de precisión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




