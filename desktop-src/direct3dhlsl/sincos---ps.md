---
title: sincos (-PS
description: Calcula el seno y el coseno, en radianes. | sincos (-PS
ms.assetid: 639237ea-1b7a-4959-9093-78f134c11863
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1e7ccdca91af206862384ae14cf25a85d0817814
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998137"
---
# <a name="sincos---ps"></a>sincos (-PS

Calcula el seno y el coseno, en radianes.

## <a name="syntax"></a>Sintaxis

### <a name="ps_2_0-and-ps_2_x"></a>PS \_ 2 \_ 0 y PS \_ 2 \_ x



| sincos (DST. x1|sí|XY}, src0. x1|sí|z|w}, SRC1, src2 |
|------------------------------------------------------|



 

Donde:

-   DST es el registro de destino y tiene que ser un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ). El registro de destino debe tener exactamente una de las tres máscaras siguientes:. x \| . y \| . XY.
-   src0 es un registro de origen que proporciona el ángulo de entrada, que debe estar dentro \[ de-PI, + PI \] . {x \| y \| z \| w} es el swizzle de replicación necesario.
-   SRC1 y src2 son registros de origen y deben ser dos [registros Float constantes](dx9-graphics-reference-asm-ps-registers-constant-float.md)diferentes (c \# ). Los valores de SRC1 y src2 deben ser los de las macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) y [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) , respectivamente.

### <a name="ps_3_0"></a>PS \_ 3 \_ 0



| sincos (DST. x1|sí|XY}, src0. x1|sí|z|con |
|------------------------------------------|



 

Donde:

-   DST es un registro de destino y tiene que ser un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ). El registro de destino debe tener exactamente una de las tres máscaras siguientes:. x \| . y \| . XY.
-   src0 es un registro de origen que proporciona el ángulo de entrada, que debe estar dentro \[ de-PI, + PI \] . {x \| y \| z \| w} es el swizzle de replicación necesario.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| sincos (                |      |      |      |      | x    | x    | x     | x    | x     |



 

### <a name="ps_2_0-and-ps_2_x"></a>PS \_ 2 \_ 0 y PS \_ 2 \_ x

Para PS \_ 2 \_ 0 y PS \_ 2 \_ x, sincos (se puede usar con predication, pero con una restricción a swizzle del registro de [predicado](dx9-graphics-reference-asm-ps-registers-predicate.md) (P0): solo se permite replicar swizzle (. x \| . y \| . z \| . w).

Para PS \_ 2 \_ 0 y PS \_ 2 \_ x, la instrucción funciona de la siguiente manera (V = el valor escalar de src0 con un swizzle de replicación):

-   Si la máscara de escritura es. x:
    ```
    dest.x = cos(V)
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Si la máscara de escritura es. y:
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Si la máscara de escritura es. XY:
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="ps_3_0"></a>PS \_ 3 \_ 0

Para PS \_ 3 \_ 0, sincos (se puede usar con predication sin ninguna restricción. Vea [registro de predicados](dx9-graphics-reference-asm-ps-registers-predicate.md).

Para PS \_ 3 \_ 0, la instrucción funciona de la siguiente manera (V = el valor escalar de src0 con un swizzle de replicación):

-   Si la máscara de escritura es. x:
    ```
    dest.x = cos(V)
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Si la máscara de escritura es. y:
    ```
    dest.x is not touched by the instruction
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Si la máscara de escritura es. XY:
    ```
    dest.x = cos(V)
    dest.y = sin(V)
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

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
