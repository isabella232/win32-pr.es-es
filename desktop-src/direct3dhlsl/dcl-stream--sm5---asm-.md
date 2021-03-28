---
title: dcl_stream (SM5-ASM)
description: Declare un flujo de salida del sombreador de geometría.
ms.assetid: 0A8B8AB5-B7B0-46BB-91E8-B2E8E3D64B74
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f46903c3257c280788e91c25700743a23c146fe
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419986"
---
# <a name="dcl_stream-sm5---asm"></a>\_secuencia de DCL (SM5-ASM)

Declare un flujo de salida del sombreador de geometría.



| secuencia de DCL \_ m\# |
|-----------------|



 



| Elemento                                                       | Descripción                             |
|------------------------------------------------------------|-----------------------------------------|
| <span id="m_"></span><span id="M_"></span>*f\#*<br/> | \[en el \] flujo 0.. 3 (M0.. m3).<br/> |



 

## <a name="remarks"></a>Observaciones

Un flujo determinado solo puede declararse una vez.

Si no se declara ningún flujo, se supone que las declaraciones de topología de salida y salida son para el flujo 0.

La primera **\_ secuencia DCL** no puede aparecer después de las instrucciones **\_ Output** o **DCL \_ outputTopology** de DCL.

Las **instrucciones \_ Output** o **DCL \_ outputToplogy** de DCL después de cualquier instrucción **DCL \_ Stream** m \# definen las salidas de Stream m \# .

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

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

 

 





