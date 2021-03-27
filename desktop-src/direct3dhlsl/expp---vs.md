---
title: EXPP-vs
description: Proporciona el doble de precisión parcial exponencial.
ms.assetid: ac080ac9-5dfd-49e4-92ea-50bb26844ff6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0d57e2723c90eee8df728aa540baeab86932e773
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784942"
---
# <a name="expp---vs"></a>EXPP-vs

Proporciona una precisión parcial exponencial 2<sup>x</sup>.

## <a name="syntax"></a>Sintaxis



| EXPP DST, src. x1|sí|z|con |
|----------------------------|



 

Donde:

-   DST es el registro de destino.
-   src es un registro de origen. El registro de origen requiere el uso explícito de replicate swizzle, es decir, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes).
-   {x \| y \| z \| w} es el swizzle de replicación necesario en el registro de código fuente.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| expp                   | x    | x    | x    | x     | x    | x     |



 

### <a name="vs_1_1"></a>vs \_ 1 \_ 1

La instrucción [exp-vs](exp---vs.md) funciona de forma diferente en función de las versiones del sombreador de vértices.

En vs \_ 1 \_ 1, la instrucción EXPP proporciona los siguientes resultados:


```
v = the scalar value from the source register with a replicate swizzle

dest.x = pow(2, floor(v))
dest.y = v - floor(v)
dest.z = pow(2, v) (partial-precision)
dest.w = 1
```



En vs \_ 2 \_ 0 y up, la instrucción EXPP proporciona los siguientes resultados:


```
v = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow(2, v) (partial-precision)
```



### <a name="vs_2_0"></a>vs \_ 2 \_ 0

En vs \_ 2 \_ 0 y up, la instrucción funciona de la siguiente manera:


```
float V = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow( 2, V ) (partial-precision)
```



La instrucción proporciona al menos 10 bits de precisión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




