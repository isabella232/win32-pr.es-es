---
title: emit_stream (SM5-ASM)
description: Emite un vértice a un flujo determinado.
ms.assetid: 5DBB0BEC-6EA4-4C04-A3D2-853E48260226
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f56c2582453d18120e3e95b27af9c7613728fa62
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419918"
---
# <a name="emit_stream-sm5---asm"></a>emisión \_ de flujo (SM5-ASM)

Emite un vértice a un flujo determinado.



| emitir \_ streamIndex de flujo |
|--------------------------|



 



| Elemento                                                                                                               | Descripción                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[en \] el índice de la secuencia.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta instrucción hace que todos los registros o declarados \# de la secuencia especificada se lean fuera del sombreador de geometría para generar un vértice. Tras la emisión, no se inicializan todos los datos de todos los registros de salida de todas las secuencias, no solo la secuencia que se emite a.

*streamIndex* debe ser un valor inmediato \[ 0.. 3 \] para una secuencia declarada.

Cuando se emiten varias llamadas a la **\_ secuencia de emisión** , se generan primitivas.

### <a name="restrictions"></a>Restricciones

-   **Emit \_ Stream** puede aparecer cualquier número de veces en un sombreador de geometría, incluido en el control de flujo.
-   Si no se han declarado secuencias, debe usar [Emit](emit--sm4---asm-.md) en lugar de **emitir \_ Stream**.

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

 

 





