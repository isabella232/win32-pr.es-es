---
title: dmovc (SM5-ASM)
description: Movimiento condicional por componente. | dmovc (SM5-ASM)
ms.assetid: E376FE08-E251-4BE5-9F15-99B3B67A29C8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e364e6340733c42ae69412db726851329eb2809d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104424199"
---
# <a name="dmovc-sm5---asm"></a>dmovc (SM5-ASM)

Movimiento condicional por componente.



| dmovc \[ \_ SAT \] dest \[ . Mask \] , src0 \[ . swizzle \] , \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . swizzle \] , |
|-----------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                                              |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] el destino de movimiento.<br/> Si *src0*, *dest*  =  *SRC1* else *dest*  =  *src2*.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] los componentes de los que se va a probar la condición.<br/>                                          |
| <span id="src1"></span><span id="SRC1"></span>*SRC1*<br/> | \[en \] los componentes que se van a desplace si la condición es true.<br/>                                       |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[en \] los componentes que se van a desplace si la condición es falsa.<br/>                                      |



 

## <a name="remarks"></a>Observaciones

En el ejemplo siguiente se muestra cómo utilizar esta instrucción.

``` syntax
                if(the dest mask contains .xy)
                {
                    if(the first 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the first double from src1 (post swizzle)
                        into dest.xy
                    }
                    else
                    {
                        copy the first double from src2 (post swizzle)
                        into dest.xy
                    }
                }
                if(the dest mask contains .zw)
                {
                    if(the second 32-bit component of src0, post-swizzle, 
                       has any bit set)
                    {
                        copy the second double from src1 (post swizzle)
                        into dest.zw
                    }
                    else
                    {
                        copy the second double from src2 (post swizzle)
                        into dest.zw
                    }
                }
```

Las máscaras válidas para dest son. XY,. ZW,. xyzw.

El valor de swizzles válido para *src0* es cualquier cosa. Los dos primeros componentes posteriores a swizzle se usan para facilite los valores de condición de 2 32 bits.

El valor de swizzles válido para *SRC1* y *src2* que contienen valores double es. xyzw,. xyxy,. zwxy,. zwzw. son. XY,. ZW y. xyzw.

Las siguientes asignaciones de *src* son posteriores a swizzle:

-   *dest* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).
-   *src0* es un vec2 de 32 bits/componente en x e y (ZW omitido).
-   *SRC1* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).
-   *src2* es un doble vec2 entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).

Los modificadores de *SRC1* y *src2*, excepto swizzle, suponen que los datos son Double. La ausencia de modificadores mueve los datos sin modificar los bits.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta instrucción es compatible con los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblador modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





