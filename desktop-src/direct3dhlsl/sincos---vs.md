---
title: 'sincos: frente a'
description: 'Calcula el seno y el coseno, en radianes. | sincos: frente a'
ms.assetid: 733a3980-ceaf-43dc-a862-923c369e4a65
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca70a319852346c6e75ba544489d033a861d4c3b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263903"
---
# <a name="sincos---vs"></a>sincos: frente a

Calcula el seno y el coseno, en radianes.

## <a name="syntax"></a>Sintaxis

### <a name="vs_2_0-and-vs_2_x"></a>vs \_ 2 \_ 0 y vs \_ 2 \_ x



| sincos dst. {x\|y\|xy}, src0. {x\|y\|z\|w}, src1, src2 |
|------------------------------------------------------|



 

Donde:

-   dst es el registro de destino y debe ser [un registro temporal](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ). El registro de destino debe tener exactamente una de las tres máscaras siguientes: .x \| .y \| .xy.
-   src0 es un registro de origen que proporciona el ángulo de entrada, que debe estar dentro \[ de -pi, +pi \] . {x \| y \| z \| w} es la réplica necesaria swpliquen.
-   src1 y src2 son registros de origen y deben ser dos [registros flotantes](dx9-graphics-reference-asm-vs-registers-constant-float.md) constantes diferentes (c \# ). Los valores de src1 y src2 deben ser los de las macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) y [**D3DSINCOSCONST2,**](/windows/desktop/direct3d9/d3dsincosconst2) respectivamente.

### <a name="vs_3_0"></a>vs \_ 3 \_ 0



| sincos dst. {x\|y\|xy}, src0. {x\|y\|z\|w} |
|------------------------------------------|



 

Donde:

-   dst es un registro de destino y debe ser [un registro temporal](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ). El registro de destino debe tener exactamente una de las tres máscaras siguientes: .x \| .y \| .xy.
-   src0 es un registro de origen que proporciona el ángulo de entrada, que debe estar dentro \[ de -pi, +pi \] . {x \| y \| z \| w} es la réplica necesaria swpliquen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| sincos                 |      | x    | x    | x     | x    | x     |



 

### <a name="vs_2_0-and-vs_2_x-remarks"></a>vs \_ 2 \_ 0 y vs \_ 2 \_ x Comentarios

En el caso de vs 2 0 y vs 2 x, se pueden usar sincos con predicado, pero con una restricción para el swzzle del registro de predicado (p0): solo se permite replicar \_ \_ \_ \_ swique (.x [](dx9-graphics-reference-asm-vs-registers-predicate.md) \| \| .y .z \| .w).

En el caso de vs 2 0 y vs 2 x, la instrucción funciona de la siguiente manera: (V = el valor escalar de \_ \_ \_ src0 con un \_ swlino de replicación):

-   Si la máscara de escritura es .x:
    ```
    dest.x = cos( V )
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Si la máscara de escritura es .y:
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Si la máscara de escritura es .xy:
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="vs_3_0-remarks"></a>vs \_ 3 \_ 0 Comentarios

En comparación \_ con 3 \_ 0, los sincos se pueden usar con predicado sin ninguna restricción. Vea [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).

En el caso de vs 3 0, la instrucción funciona de la siguiente manera: (V = el valor escalar de \_ \_ src0 con un swlino de replicación)

-   Si la máscara de escritura es .x:
    ```
    dest.x = cos( V )
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Si la máscara de escritura es .y:
    ```
    dest.x is not touched by the instruction
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Si la máscara de escritura es .xy:
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

La aplicación puede asignar un ángulo arbitrario (en radianes) al intervalo \[ -pi, +pi mediante el \] siguiente pseudocódigo de sombreador:


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

 

 
