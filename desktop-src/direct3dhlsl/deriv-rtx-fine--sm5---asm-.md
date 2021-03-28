---
title: deriv_rtx_fine (SM5-ASM)
description: Calcula la tasa de cambio de los componentes. | deriv_rtx_fine (SM5-ASM)
ms.assetid: 5752C85B-2965-489C-BF27-968FAF5EAA52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73061e3220704cf2c19e28b4d6d434fda43fb941
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998172"
---
# <a name="deriv_rtx_fine-sm5---asm"></a>derive \_ RTX \_ Fine (SM5-ASM)

Calcula la tasa de cambio de los componentes.



| derive \_ RTX \_ Fine \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , |
|--------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] la dirección de los resultados de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] los componentes de la operación.<br/>             |



 

## <a name="remarks"></a>Observaciones

Esta instrucción calcula la tasa de cambio de contenido de cada componente float32 de *src0* (post-swizzle), con respecto a la dirección rendertarget x Direction (RTX) o a la dirección de rendertarget y (vea [derive \_ propiedad \_ Fine](deriv-rty-fine--sm5---asm-.md)). Cada píxel de la marca de 2x2 obtiene un par único de cálculos derivados x/y.

Los datos de la invocación del sombreador de píxeles actual siempre participan en el cálculo del derivado solicitado. En el píxel de 2x2 píxeles en el que se encuentra el píxel actual, el derivado x es el delta de la fila de 2 píxeles, incluido el píxel actual. El derivado y es el delta de la columna de 2 píxeles, incluido el píxel actual. No hay ninguna especificación que indique cómo se alinearán o se colocarán en mosaico las cuatro cuádruples en un primitivo.

Los derivados se calculan en un nivel más fino (cálculo único del par derivado x/y para cada píxel de un cuádruple 2x2). Esta instrucción y [derive \_ propiedad \_ Fine](deriv-rty-fine--sm5---asm-.md) son alternativas para [derivar \_ RTX \_ gruesa](deriv-rtx-coarse--sm5---asm-.md) y [derivar \_ propiedad \_ grueso](deriv-rty-coarse--sm5---asm-.md). Estas \_ instrucciones aproximadas y \_ precisas son un reemplazo de **derive \_ RTX** estas \_ instrucciones aproximadas y \_ precisas son un sustituto de **derive \_ RTX** y **derive \_ propiedad** de modelos de sombreador anteriores.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     |         |



 

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

 

 





