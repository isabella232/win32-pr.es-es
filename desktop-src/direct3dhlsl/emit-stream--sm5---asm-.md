---
title: emit_stream (sm5 - asm)
description: Emita un vértice a una secuencia determinada.
ms.assetid: 5DBB0BEC-6EA4-4C04-A3D2-853E48260226
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e7e90bfb72862abeccc8a9411904a7b42f77c933cc4c87af189d6557596389c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562707"
---
# <a name="emit_stream-sm5---asm"></a>emit \_ stream (sm5 - asm)

Emita un vértice a una secuencia determinada.



| emit \_ stream streamIndex |
|--------------------------|



 



| Elemento                                                                                                               | Descripción                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[en \] El índice de la secuencia.<br/> |



 

## <a name="remarks"></a>Comentarios

Esta instrucción hace que todos los registros o declarados de la secuencia dada se lean fuera del \# sombreador de geometría para generar un vértice. Aplazar la emisión, todos los datos de todos los registros de salida de todas las secuencias no se inicializan, no solo el flujo emitido a.

*streamIndex* debe ser un valor \[ inmediato 0..3 \] para una secuencia declarada.

A medida **que se \_ emiten** varias llamadas de secuencia de emisión, se generan primitivas.

### <a name="restrictions"></a>Restricciones

-   **emit \_ stream** puede aparecer cualquier número de veces en un sombreador de geometría, incluido el control de flujo.
-   Si no se han declarado secuencias, debe usar [emit](emit--sm4---asm-.md) en lugar de **emit \_ stream**.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Shader Model 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





