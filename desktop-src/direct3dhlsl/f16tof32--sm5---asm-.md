---
title: f16tof32 (sm5 - asm)
description: Conversión de float16 a float32 por componente. | f16tof32 (sm5 - asm)
ms.assetid: CFAA1350-DA7F-4105-A90A-72052C5E2FB3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc4456737d5ddaaed351ae2a1cc76418c33af9c498e725099e1912d8fabe7ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562661"
---
# <a name="f16tof32-sm5---asm"></a>f16tof32 (sm5 - asm)

Conversión de float16 a float32 por componente.



| f16tof32 dest \[ .mask \] , \[ - \] src \[ .sw maskle\] |
|----------------------------------------------|



 



| Elemento                                                            | Descripción                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección del resultado float32.<br/> |
| <span id="src"></span><span id="SRC"></span>*Fuente*<br/>    | \[en \] el valor float16 que se debe convertir.<br/>      |



 

## <a name="remarks"></a>Comentarios

Esta operación realiza una conversión por componente de un valor float16 de bits LSB a un resultado float32.

Esta operación sigue las reglas D3D para la conversión de punto flotante.

Use esta instrucción para la descompresión de datos controlada por sombreadores.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
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

 

 





