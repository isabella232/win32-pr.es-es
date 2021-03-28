---
title: Pow-vs
description: SRC1 de precisión completa ABS (src0). | Pow-vs
ms.assetid: 51da86c6-bafa-42e0-90a5-d1545e39e600
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3263fa19015bc32c94ae714891c3bbb2128c9463
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279980"
---
# <a name="pow---vs"></a>Pow-vs

<sup>SRC1</sup>de precisión completa ABS (src0).

## <a name="syntax"></a>Sintaxis



| Pow DST, src0, SRC1 |
|---------------------|



 

, donde

-   DST es el registro de destino.
-   src0 es un registro de origen de entrada. El registro de origen requiere el uso explícito de replicate swizzle, es decir, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes).
-   SRC1 es un registro de origen de entrada. El registro de origen requiere el uso explícito de replicate swizzle, es decir, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes).

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| pow                    |      | x    | x    | x     | x    | x     |



 

Esta instrucción funciona como se muestra aquí.


```
dest = pow(abs(src0), src1);
```



Se trata de una instrucción escalar, por lo que los registros de origen deben tener replicar swizzles para indicar qué canales se usan.

El resultado escalar se replica en los cuatro canales de salida.

Esta instrucción se puede expandir como exp (SRC1 \* log (src0)).

La precisión no es inferior a 15 bits.

El registro de destino debe ser un registro temporal y no debe ser el mismo registro que SRC1.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




