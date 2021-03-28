---
title: deriv_rtx_coarse (SM5-ASM)
description: Calcula la tasa de cambio de los componentes. | deriv_rtx_coarse (SM5-ASM)
ms.assetid: 57743BB2-251C-4EA7-BDA9-70B2ECEE3B3F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2355b6db6aef9e85959d6359053fea76b48af0a5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998065"
---
# <a name="deriv_rtx_coarse-sm5---asm"></a>derivar \_ RTX \_ grueso (SM5-ASM)

Calcula la tasa de cambio de los componentes.



| derive \_ RTX \_ General \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , |
|----------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] la dirección de los resultados de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] los componentes de la operación.<br/>             |



 

## <a name="remarks"></a>Observaciones

Esta instrucción calcula la tasa de cambio de contenido de cada componente float32 de *src0* (post-swizzle), con respecto a la dirección rendertarget x Direction (RTX) o a la dirección de rendertarget y (vea [derive \_ propiedad \_ gruesa](deriv-rty-coarse--sm5---asm-.md)). Solo se calcula un par derivado de x, y para cada sello de 2x2 de píxeles.

Los datos de la invocación del sombreador de píxeles actual pueden participar o no en el cálculo del derivado solicitado, porque el derivado solo se calculará una vez por 2x2 cuádruple. Por ejemplo, el derivado x podría ser un delta de la fila superior de píxeles y la dirección y ([derivar \_ propiedad \_ gruesa](deriv-rty-coarse--sm5---asm-.md)) podría ser una diferencia de la columna izquierda de píxeles. El cálculo exacto depende del proveedor de hardware. Tampoco hay ninguna especificación que indique cómo se alinearán o colocarán en mosaico las cuatro cuádruples en un primitivo.

Los derivados se calculan en un nivel aproximado, una vez por cada 2x2 píxeles cuádruple. Esta instrucción y [derive \_ propiedad \_ grueso](deriv-rty-coarse--sm5---asm-.md) son alternativas para [derivar \_ RTX \_ Fine](deriv-rtx-fine--sm5---asm-.md) y [derivar \_ propiedad \_ Fine](deriv-rty-fine--sm5---asm-.md). Estas \_ instrucciones aproximadas y \_ precisas son un reemplazo **de \_ rtxderiv \_ propiedad derivado** de modelos de sombreador anteriores.

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

 

 





