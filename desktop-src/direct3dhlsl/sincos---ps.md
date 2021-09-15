---
title: 'sincos: ps'
description: 'Calcula el seno y el coseno, en radianes. | sincos: ps'
ms.assetid: 639237ea-1b7a-4959-9093-78f134c11863
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1e7ccdca91af206862384ae14cf25a85d0817814
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573653"
---
# <a name="sincos---ps"></a>sincos: ps

Calcula el seno y el coseno, en radianes.

## <a name="syntax"></a>Sintaxis

### <a name="ps_2_0-and-ps_2_x"></a>ps \_ 2 \_ 0 y ps \_ 2 \_ x



| sincos dst. {x\|y\|xy}, src0. {x\|y\|z\|w}, src1, src2 |
|------------------------------------------------------|



 

Donde:

-   dst es el registro de destino y debe ser [un registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ). El registro de destino debe tener exactamente una de las tres máscaras siguientes: .x \| .y \| .xy.
-   src0 es un registro de origen que proporciona el ángulo de entrada, que debe estar dentro \[ de -pi, +pi \] . {x \| y \| z \| w} es la réplica necesaria swpliquen.
-   src1 y src2 son registros de origen y deben ser dos [registros flotantes constantes](dx9-graphics-reference-asm-ps-registers-constant-float.md)diferentes (c \# ). Los valores de src1 y src2 deben ser los de las macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) y [**D3DSINCOSCONST2,**](/windows/desktop/direct3d9/d3dsincosconst2) respectivamente.

### <a name="ps_3_0"></a>ps \_ 3 \_ 0



| sincos dst. {x\|y\|xy}, src0. {x\|y\|z\|w} |
|------------------------------------------|



 

Donde:

-   dst es un registro de destino y debe ser [un registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ). El registro de destino debe tener exactamente una de las tres máscaras siguientes: .x \| .y \| .xy.
-   src0 es un registro de origen que proporciona el ángulo de entrada, que debe estar dentro \[ de -pi, +pi \] . {x \| y \| z \| w} es la réplica necesaria swpliquen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| sincos                |      |      |      |      | x    | x    | x     | x    | x     |



 

### <a name="ps_2_0-and-ps_2_x"></a>ps \_ 2 \_ 0 y ps \_ 2 \_ x

Para ps 2 0 y ps 2 x, los sincos se pueden usar con predicado, pero con una restricción para el swzzle del registro de predicado (p0): solo se permite replicar \_ \_ \_ \_ swique (.x [](dx9-graphics-reference-asm-ps-registers-predicate.md) \| \| .y .z \| .w).

Para ps 2 0 y ps 2 x, la instrucción funciona de la siguiente manera (V = el valor escalar de src0 con un sw \_ \_ hoja de \_ \_ replicación):

-   Si la máscara de escritura es .x:
    ```
    dest.x = cos(V)
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Si la máscara de escritura es .y:
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Si la máscara de escritura es .xy:
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="ps_3_0"></a>ps \_ 3 \_ 0

Para ps \_ 3 \_ 0, sincos se puede usar con predicado sin ninguna restricción. Vea [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).

Para ps 3 0, la instrucción funciona de la siguiente manera (V = el valor escalar de \_ \_ src0 con un swlino de replicación):

-   Si la máscara de escritura es .x:
    ```
    dest.x = cos(V)
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Si la máscara de escritura es .y:
    ```
    dest.x is not touched by the instruction
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Si la máscara de escritura es .xy:
    ```
    dest.x = cos(V)
    dest.y = sin(V)
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

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
