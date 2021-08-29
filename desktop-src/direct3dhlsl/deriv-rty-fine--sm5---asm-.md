---
title: deriv_rty_fine (sm5 - asm)
description: Calcula la velocidad de cambio de los componentes. | deriv_rty_fine (sm5 - asm)
ms.assetid: 7C5769A6-443C-4208-BD09-3DF3C5902624
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 331ec5c887b221533f7d7d420530d009f32b203151b681b8c187bfb950462e65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625925"
---
# <a name="deriv_rty_fine-sm5---asm"></a>deriv \_ rty \_ fine (sm5 - asm)

Calcula la velocidad de cambio de los componentes.



| deriv \_ rty \_ fine sat \[ \_ \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swzzle \] , |
|--------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección de los resultados de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Los componentes de la operación.<br/>             |



 

## <a name="remarks"></a>Comentarios

Para obtener más información, [vea deriv \_ rtx \_ fine.](deriv-rtx-fine--sm5---asm-.md)

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
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

 

 





