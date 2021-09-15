---
title: deriv_rtx_coarse (sm5 - asm)
description: Calcula la velocidad de cambio de los componentes. | deriv_rtx_coarse (sm5 - asm)
ms.assetid: 57743BB2-251C-4EA7-BDA9-70B2ECEE3B3F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2355b6db6aef9e85959d6359053fea76b48af0a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573868"
---
# <a name="deriv_rtx_coarse-sm5---asm"></a>deriv \_ rtx \_ general (sm5 - asm)

Calcula la velocidad de cambio de los componentes.



| deriv \_ rtx \_ coarse \[ \_ sat \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swzzle \] , |
|----------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección de los resultados de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Los componentes de la operación.<br/>             |



 

## <a name="remarks"></a>Observaciones

Esta instrucción calcula la velocidad de cambio de contenido de cada componente float32 de *src0* (posterior al swconflé), con respecto a la dirección x de RenderTarget (rtx) o renderTarget y (vea [deriv \_ rty \_ coarse).](deriv-rty-coarse--sm5---asm-.md) Solo se calcula un par derivado x,y único para cada marca de 2 x 2 píxeles de píxeles.

Los datos de la invocación del sombreador de píxeles actual pueden o no participar en el cálculo del derivado solicitado, ya que el derivado se calculará solo una vez por 2x2 quad. Por ejemplo, el derivado x podría ser un delta de la fila superior de píxeles, y la dirección y[(deriv \_ rty \_ coarse)](deriv-rty-coarse--sm5---asm-.md)podría ser un delta de la columna izquierda de píxeles. El cálculo exacto es del proveedor de hardware. Tampoco hay ninguna especificación que dictara cómo se alinearán los cuatros de 2x2 o se pondrán en mosaico sobre una primitiva.

Los derivados se calculan en un nivel general, una vez por cada cuatro píxeles de 2 x 2 píxeles. Esta instrucción y [deriv \_ rty \_ coarse](deriv-rty-coarse--sm5---asm-.md) son alternativas a [deriv \_ rtx \_ fine](deriv-rtx-fine--sm5---asm-.md) y [deriv \_ rty \_ fine](deriv-rty-fine--sm5---asm-.md). Estas instrucciones derivadas gruesas y finas \_ \_ sustituyen **a deriv \_ rtxderiv \_ rty** de modelos de sombreador anteriores.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     |         |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





