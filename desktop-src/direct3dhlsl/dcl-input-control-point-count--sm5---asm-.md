---
title: dcl_input_control_point_count (SM5-ASM)
description: Declare el recuento de puntos de control de entrada del sombreador de casco en la sección declaración del sombreador de casco.
ms.assetid: 2E524BF0-3DD0-446A-8437-0CF17B348D83
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f0a674a05bfd66b4c1d94da73958dc68f00fe21
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419995"
---
# <a name="dcl_input_control_point_count-sm5---asm"></a>\_recuento \_ \_ de puntos \_ de control de entrada de DCL (SM5-ASM)

Declare el recuento de puntos de control de entrada del sombreador de casco en la sección declaración del sombreador de casco.



| recuento de puntos de control de entrada de DCL \_ \_ \_ \_ {1.. 32} |
|-------------------------------------------|



 



| Elemento                                                   | Descripción                                      |
|--------------------------------------------------------|--------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N*<br/> | \[en \] el recuento de puntos de control de entrada.<br/> |



 

## <a name="remarks"></a>Observaciones

Se requiere al menos un punto de control de entrada; puede estar vacío si no es necesario.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        | X    |        |          |       |         |



 

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

 

 





