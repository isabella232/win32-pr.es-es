---
title: f32tof16 (SM5-ASM)
description: Conversión de componentes float16 a float32. | f32tof16 (SM5-ASM)
ms.assetid: 36BCCFC5-722A-45EB-8A66-7544833BBBA5
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54a101f370f9c53d1d3f43f9e1cf6c4da82933d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986706"
---
# <a name="f32tof16-sm5---asm"></a>f32tof16 (SM5-ASM)

Conversión de componentes float16 a float32.



| f32tof16 dest \[ . Mask \] , \[ - \] src \[ . swizzle\] |
|----------------------------------------------|



 



| Elemento                                                            | Descripción                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] la dirección del resultado de float16.<br/> |
| <span id="src"></span><span id="SRC"></span>*diez*<br/>    | \[en \] el valor float32 que se va a convertir.<br/>  |



 

## <a name="remarks"></a>Observaciones

Esta instrucción realiza una conversión de componentes de un valor float32 en un resultado de valor float16 colocado en LSB 16 bits.

Esta instrucción sigue las reglas D3D para la conversión de punto flotante.

Use esta instrucción para la compresión de datos controlada por el sombreador.

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

 

 





