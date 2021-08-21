---
title: deriv_rtx_fine (sm5 - asm)
description: Calcula la velocidad de cambio de los componentes. | deriv_rtx_fine (sm5 - asm)
ms.assetid: 5752C85B-2965-489C-BF27-968FAF5EAA52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6666750be76d673ddc6c5f0d66d23131096812c93b71be52eb7e0f6ebb403ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792661"
---
# <a name="deriv_rtx_fine-sm5---asm"></a>deriv \_ rtx \_ fine (sm5 - asm)

Calcula la velocidad de cambio de los componentes.



| deriv \_ rtx \_ fine sat \[ \_ \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swzzle \] , |
|--------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección de los resultados de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Los componentes de la operación.<br/>             |



 

## <a name="remarks"></a>Comentarios

Esta instrucción calcula la tasa de cambio de contenido de cada componente float32 de *src0* (posterior a swzzle), con respecto a renderTarget x direction (rtx) o RenderTarget y direction (ver [deriv \_ rty \_ fine](deriv-rty-fine--sm5---asm-.md)). Cada píxel de la marca 2x2 obtiene un par único de cálculos derivados x/y

Los datos de la invocación del sombreador de píxeles actual siempre participan en el cálculo del derivado solicitado. En el cuadránxel de 2 x 2 píxeles en el que se encuentra el píxel actual, el derivado de x es el delta de la fila de 2 píxeles, incluido el píxel actual. El derivado de y es la diferencia de la columna de 2 píxeles, incluido el píxel actual. No hay ninguna especificación que dictara cómo se alinearán los cuatros de 2x2 o se pondrán en mosaico sobre una primitiva.

Los derivados se calculan en un nivel fino (cálculo único del par derivado x/y para cada píxel de un cuadránxel de 2x2). Esta instrucción y [deriv \_ rty \_ fine](deriv-rty-fine--sm5---asm-.md) son alternativas a [deriv \_ rtx \_ coarse](deriv-rtx-coarse--sm5---asm-.md) y [deriv \_ rty \_ coarse.](deriv-rty-coarse--sm5---asm-.md) Estas instrucciones derivadas gruesas y finas son un reemplazo de deriv rtx Estas instrucciones derivadas gruesas y finas son un reemplazo de \_ \_ **\_** \_ \_ **deriv \_ rtx** y **deriv \_ rty** de modelos de sombreador anteriores.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     |         |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





