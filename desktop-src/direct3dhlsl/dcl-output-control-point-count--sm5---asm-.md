---
title: dcl_output_control_point_count (SM5-ASM)
description: Declara el recuento de puntos de control de salida del sombreador de casco.
ms.assetid: 51E8117F-1802-413B-9820-04D5CEBE2DB6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 147f8f7021252f07cdb6dd0f225555ff0f23d54b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077132"
---
# <a name="dcl_output_control_point_count-sm5---asm"></a>\_recuento \_ \_ de puntos \_ de control de salida de DCL (SM5-ASM)

Declara el recuento de puntos de control de salida del sombreador de casco.



| número de puntos de control de salida de DCL \_ \_ \_ \_ N |
|--------------------------------------|



 



| Elemento                                                   | Descripción                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N*<br/> | \[en \] un valor entero comprendido entre 0 y 32 que especifica el recuento de puntos de control de salida.<br/> |



 

## <a name="remarks"></a>Observaciones

El sombreador de casco puede producir 0 puntos de control si no son necesarios.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco                 | Dominio | Geometría | Píxel | Compute |
|--------|----------------------|--------|----------|-------|---------|
|        | Sección declaraciones |        |          |       |         |



 

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

 

 





