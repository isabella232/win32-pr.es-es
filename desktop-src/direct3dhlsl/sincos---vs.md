---
title: sincos (-vs
description: Calcula el seno y el coseno, en radianes. | sincos (-vs
ms.assetid: 733a3980-ceaf-43dc-a862-923c369e4a65
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca70a319852346c6e75ba544489d033a861d4c3b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003698"
---
# <a name="sincos---vs"></a>sincos (-vs

Calcula el seno y el coseno, en radianes.

## <a name="syntax"></a>Sintaxis

### <a name="vs_2_0-and-vs_2_x"></a>vs \_ 2 \_ 0 y vs \_ 2 \_ x



| sincos (DST. x1|sí|XY}, src0. x1|sí|z|w}, SRC1, src2 |
|------------------------------------------------------|



 

Donde:

-   DST es el registro de destino y tiene que ser un [registro temporal](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ). El registro de destino debe tener exactamente una de las tres máscaras siguientes:. x \| . y \| . XY.
-   src0 es un registro de origen que proporciona el ángulo de entrada, que debe estar dentro \[ de-PI, + PI \] . {x \| y \| z \| w} es el swizzle de replicación necesario.
-   SRC1 y src2 son registros de origen y deben ser dos [registros Float constantes](dx9-graphics-reference-asm-vs-registers-constant-float.md) diferentes (c \# ). Los valores de SRC1 y src2 deben ser los de las macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) y [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) , respectivamente.

### <a name="vs_3_0"></a>vs \_ 3 \_ 0



| sincos (DST. x1|sí|XY}, src0. x1|sí|z|con |
|------------------------------------------|



 

Donde:

-   DST es un registro de destino y tiene que ser un [registro temporal](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ). El registro de destino debe tener exactamente una de las tres máscaras siguientes:. x \| . y \| . XY.
-   src0 es un registro de origen que proporciona el ángulo de entrada, que debe estar dentro \[ de-PI, + PI \] . {x \| y \| z \| w} es el swizzle de replicación necesario.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| sincos (                 |      | x    | x    | x     | x    | x     |



 

### <a name="vs_2_0-and-vs_2_x-remarks"></a>vs \_ 2 \_ 0 y vs \_ 2 \_ x comentarios

Para vs \_ 2 \_ 0 y vs \_ 2 \_ x, sincos (se puede usar con predication, pero con una restricción a swizzle del registro de [predicado](dx9-graphics-reference-asm-vs-registers-predicate.md) (P0): solo se permite replicar swizzle (. x \| . y \| . z \| . w).

Para vs \_ 2 \_ 0 y vs \_ 2 \_ x, la instrucción funciona de la siguiente manera: (V = el valor escalar de src0 con un swizzle de replicación):

-   Si la máscara de escritura es. x:
    ```
    dest.x = cos( V )
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Si la máscara de escritura es. y:
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Si la máscara de escritura es. XY:
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="vs_3_0-remarks"></a>vs \_ 3 \_ 0 comentarios

Para vs \_ 3 \_ 0, sincos (se puede usar con predication sin ninguna restricción. Vea [registro de predicados](dx9-graphics-reference-asm-vs-registers-predicate.md).

En el caso de vs \_ 3 \_ 0, la instrucción funciona de la siguiente manera: (V = el valor escalar de src0 con un swizzle de replicación)

-   Si la máscara de escritura es. x:
    ```
    dest.x = cos( V )
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Si la máscara de escritura es. y:
    ```
    dest.x is not touched by the instruction
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Si la máscara de escritura es. XY:
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

La aplicación puede asignar un ángulo arbitrario (en radianes) al intervalo \[ -PI, + PI \] con el siguiente pseudocódigo del sombreador:


```
def c0, pi, 0.5, 2*pi, 1/(2*pi)
mad r0.x, input_angle, c0.w, c0.y
frc r0.x, r0.x
mad r0.x, r0.x, c0.z, -c0.x
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
