---
title: countbits ((SM5-ASM)
description: Cuenta el número de bits establecidos en un número.
ms.assetid: ED75487F-46FF-45F5-BEAA-7A32BEFB0571
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d46fe9c750790d65630a743dd9ddc347fea50e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103904288"
---
# <a name="countbits-sm5---asm"></a>countbits ((SM5-ASM)

Cuenta el número de bits establecidos en un número.



| countbits (DEST \[ . Mask \] , src0 \[ . swizzle\] |
|-------------------------------------------|



 



| Elemento                                                            | Descripción                                   |
|-----------------------------------------------------------------|-----------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] la dirección de los resultados.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] el número de bits 32 de entrada.<br/>    |



 

## <a name="remarks"></a>Observaciones

Esta instrucción se puede usar para calcular el porcentaje de cobertura de entrada del sombreador.

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

 

 





