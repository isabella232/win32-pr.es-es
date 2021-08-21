---
title: dmovc (sm5 - asm)
description: Movimiento condicional por componente. | dmovc (sm5 - asm)
ms.assetid: E376FE08-E251-4BE5-9F15-99B3B67A29C8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc0ed15d81a91d8a93ce99eda3fa17b91900e0045301f1c5b5d1f56e4448954a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792386"
---
# <a name="dmovc-sm5---asm"></a>dmovc (sm5 - asm)

Movimiento condicional por componente.



| dmovc \[ \_ sat \] dest \[ .mask \] , src0 \[ .swzzle, \] \[ - \] src1 \[ \_ abs \] \[ .sw swzzle, \] \[ - \] src2 \[ \_ abs \] \[ .swmovle \] , |
|-----------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                                              |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] El destino de movimiento.<br/> Si *src0*, *dest*  =  *src1* else *dest*  =  *src2*.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Los componentes con los que se probará la condición.<br/>                                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] Los componentes que se mueven si la condición es true.<br/>                                       |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[en \] Los componentes que se mueven si la condición es false.<br/>                                      |



 

## <a name="remarks"></a>Comentarios

En el ejemplo siguiente se muestra cómo usar esta instrucción.

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

Las máscaras válidas para dest son .xy, .zw, .xyzw.

Los swzzles válidos para *src0* son cualquier cosa. Los dos primeros componentes se usan después de la sangría para aplicar sangría a dos valores de condición de 32 bits.

Los swzzles válidos para *src1* y *src2* que contienen doubles son .xyzw, .xyxy, .zwxy, .zwzw. son .xy, .zw y .xyzw.

Las siguientes *asignaciones de src* son posteriores a swconfle:

-   *dest* es un vec2 doble entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).
-   *src0* es un vec2 de 32 bits/componente entre x e y (se omite zw).
-   *src1* es un vec2 doble entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).
-   *src2* es un vec2 doble entre (x 32LSB, y 32MSB) y (z 32LSB, w 32MSB).

Los modificadores de *src1* y *src2,* que no son swzzle, suponen que los datos son double. La ausencia de modificadores mueve los datos sin modificar los bits.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





