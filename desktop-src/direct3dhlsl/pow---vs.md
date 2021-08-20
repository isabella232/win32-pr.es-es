---
title: pow - vs
description: Abs(src0)src1 de precisión completa. | pow - vs
ms.assetid: 51da86c6-bafa-42e0-90a5-d1545e39e600
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3fd6c40ef133782990cc8f10517d51a723a21e0730bfabd83feca4c7e294cb7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118088671"
---
# <a name="pow---vs"></a>pow - vs

Abs(src0)<sup>src1</sup>de precisión completa.

## <a name="syntax"></a>Syntax



| pow dst, src0, src1 |
|---------------------|



 

where

-   dst es el registro de destino.
-   src0 es un registro de origen de entrada. El registro de origen requiere el uso explícito de replicar swzzle, es decir, exactamente uno de los componentes .x, .y, .z, .w swzzle (o los componentes .r, .g, .b, .a equivalentes).
-   src1 es un registro de origen de entrada. El registro de origen requiere el uso explícito de replicar swzzle, es decir, exactamente uno de los componentes .x, .y, .z, .w swzzle (o los componentes .r, .g, .b, .a equivalentes).

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| pow                    |      | x    | x    | x     | x    | x     |



 

Esta instrucción funciona como se muestra aquí.


```
dest = pow(abs(src0), src1);
```



Se trata de una instrucción escalar, por lo que los registros de origen deben tener swzzles de replicación para indicar qué canales se usan.

El resultado escalar se replica en los cuatro canales de salida.

Esta instrucción se podría expandir como exp(src1 \* log(src0)).

La precisión no es inferior a 15 bits.

El registro dest debe ser un registro temporal y no debe ser el mismo registro que src1.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




