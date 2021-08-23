---
title: deriv_rtx_coarse (sm5 - asm)
description: Calcula la velocidad de cambio de los componentes. | deriv_rtx_coarse (sm5 - asm)
ms.assetid: 57743BB2-251C-4EA7-BDA9-70B2ECEE3B3F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50066fe58c3d0a0cdd903de9fbb479a8fbab2c3a20c622ebca138c0937aaf0dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986645"
---
# <a name="deriv_rtx_coarse-sm5---asm"></a>deriv \_ rtx \_ coarse (sm5 - asm)

Calcula la velocidad de cambio de los componentes.



| deriv \_ rtx \_ coarse \[ \_ sat \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swzzle \] , |
|----------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección de los resultados de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Los componentes de la operación.<br/>             |



 

## <a name="remarks"></a>Comentarios

Esta instrucción calcula la velocidad de cambio de contenido de cada componente float32 de *src0* (posterior al swconflé), con respecto a la dirección x de RenderTarget (rtx) o renderTarget y (vea [deriv \_ rty \_ coarse).](deriv-rty-coarse--sm5---asm-.md) Solo se calcula un par derivado x,y único para cada marca de 2 x 2 píxeles de píxeles.

Los datos de la invocación del sombreador de píxeles actual pueden o no participar en el cálculo del derivado solicitado, ya que el derivado se calculará solo una vez por 2x2 quad. Por ejemplo, el derivado x podría ser un delta de la fila superior de píxeles, y la dirección y[(deriv \_ rty \_ coarse)](deriv-rty-coarse--sm5---asm-.md)podría ser una diferencia de la columna izquierda de píxeles. El cálculo exacto es del proveedor de hardware. Tampoco hay ninguna especificación que dictara cómo se alinearán los cuatros de 2x2 o se pondrán en mosaico sobre una primitiva.

Los derivados se calculan en un nivel general, una vez por cada cuatro píxeles de 2 x 2 píxeles. Esta instrucción y [deriv \_ rty \_ coarse](deriv-rty-coarse--sm5---asm-.md) son alternativas a [deriv \_ rtx \_ fine](deriv-rtx-fine--sm5---asm-.md) y [deriv \_ rty \_ fine](deriv-rty-fine--sm5---asm-.md). Estas instrucciones derivadas gruesas y finas \_ \_ sustituyen **a deriv \_ rtxderiv \_ rty** de modelos de sombreador anteriores.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     |         |



 

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

 

 





