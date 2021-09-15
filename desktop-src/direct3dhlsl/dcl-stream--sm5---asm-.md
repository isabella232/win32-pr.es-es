---
title: dcl_stream (sm5 - asm)
description: Declare un flujo de salida del sombreador de geometría.
ms.assetid: 0A8B8AB5-B7B0-46BB-91E8-B2E8E3D64B74
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f46903c3257c280788e91c25700743a23c146fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573897"
---
# <a name="dcl_stream-sm5---asm"></a>flujo dcl \_ (sm5 - asm)

Declare un flujo de salida del sombreador de geometría.



| dcl \_ stream m\# |
|-----------------|



 



| Elemento                                                       | Descripción                             |
|------------------------------------------------------------|-----------------------------------------|
| <span id="m_"></span><span id="M_"></span>*M\#*<br/> | \[en \] Stream 0..3 (m0.. m3).<br/> |



 

## <a name="remarks"></a>Observaciones

Una secuencia determinada solo se puede declarar una vez.

Si no se declara ninguna secuencia, se supone que las declaraciones de topología de salida y salida son para el flujo 0.

La primera **secuencia dcl \_** no puede aparecer después de ninguna **instrucción dcl \_ outputTopology** o **\_ dcl outputTopology.**

Las **instrucciones dcl \_ output o** **dcl \_ outputToplogy** después de cualquier instrucción **dcl \_ stream** m definen las \# salidas para el flujo m \# .

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

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

 

 





