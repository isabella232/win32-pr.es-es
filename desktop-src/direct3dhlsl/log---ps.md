---
title: 'log: ps'
description: 'Registro de precisión completa( x). | log: ps'
ms.assetid: e540a082-5916-4111-b908-bb229c9e7dc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4be7061b6e2e0bfa4fd86ffaeef1651cd114996bb9252192582f4c447aac09ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854155"
---
# <a name="log---ps"></a>log: ps

Registro de precisión completa( x).

## <a name="syntax"></a>Syntax



| log dst, src |
|--------------|



 

where

-   dst es el registro de destino.
-   src es un registro de origen. El registro de origen requiere el uso explícito de replicate swzzle; Es decir, se debe especificar exactamente uno de los componentes .x, .y, .z, .w swzzle (o .r, .g, .b, .a equivalentes).

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| log                   |      |      |      |      | x    | x    | x     | x    | x     |



 

El siguiente fragmento de código muestra las operaciones realizadas.


```
float v = abs(src);
if (v != 0)
{
    dest.x = dest.y = dest.z = dest.w = 
        (float)(log(v)/log(2));  
}
else
{
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;
}
```



Esta instrucción acepta un origen escalar cuyo bit de signo se omite. El resultado se replica en los cuatro canales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




