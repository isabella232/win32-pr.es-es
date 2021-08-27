---
title: dcl_stream (sm5 - asm)
description: Declare un flujo de salida del sombreador de geometría.
ms.assetid: 0A8B8AB5-B7B0-46BB-91E8-B2E8E3D64B74
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f53b8226cc9a4d8d2bd980cd26371f9e7b46a5168ec61ff39e425f73a4d7193c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793046"
---
# <a name="dcl_stream-sm5---asm"></a>flujo dcl \_ (sm5 - asm)

Declare un flujo de salida del sombreador de geometría.



| dcl \_ stream m\# |
|-----------------|



 



| Elemento                                                       | Descripción                             |
|------------------------------------------------------------|-----------------------------------------|
| <span id="m_"></span><span id="M_"></span>*M\#*<br/> | \[en \] Stream 0..3 (m0.. m3).<br/> |



 

## <a name="remarks"></a>Comentarios

Una secuencia determinada solo se puede declarar una vez.

Si no se declara ninguna secuencia, se supone que las declaraciones de topología de salida y salida son para la secuencia 0.

La primera **secuencia dcl \_** no puede aparecer después de las instrucciones **dcl output \_ o** **\_ dcl outputTopology.**

Cualquier **instrucción dcl \_ output o** **dcl \_ outputToplogy** después de cualquier **instrucción dcl \_ stream** m define las \# salidas de la secuencia m \# .

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

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

 

 





