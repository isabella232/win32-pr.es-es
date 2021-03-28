---
title: cut_stream (SM5-ASM)
description: Instrucción del sombreador de geometría que completa la topología primitiva actual en la secuencia especificada, si se le ha emitido algún vértice, e inicia una nueva topología del tipo declarado por el sombreador de geometría en esa secuencia.
ms.assetid: CEFDD13B-34FD-4E9C-94A0-CB8879A7DBDE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4650628d7f6b66130568f885e008a5163a9ee44f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419901"
---
# <a name="cut_stream-sm5---asm"></a>cortar \_ flujo (SM5-ASM)

Instrucción del sombreador de geometría que completa la topología primitiva actual en la secuencia especificada, si se le ha emitido algún vértice, e inicia una nueva topología del tipo declarado por el sombreador de geometría en esa secuencia.



| cortar \_ flujo streamIndex |
|-------------------------|



 



| Elemento                                                                                                               | Descripción                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[en \] el índice de la secuencia.<br/> |



 

## <a name="remarks"></a>Observaciones

Cuando se ejecuta esta instrucción, se completa cualquier topología emitida previamente por la invocación del sombreador de geometría. Si no hay suficientes vértices emitidos para la topología primitiva anterior, se descartan. Dado que las únicas topologías de salida disponibles para el sombreador de geometría son PointList, linestrip y trianglestrip, nunca hay vértices sobrantes.

*streamIndex* debe ser un valor inmediato \[ 0.. 3 \] para una secuencia declarada.

Una vez completada la topología anterior, si la hubiera, esta instrucción provoca que se inicie una nueva topología con la topología declarada como la salida del sombreador de geometría.

### <a name="restrictions"></a>Restricciones

-   Esta instrucción solo se aplica al sombreador de geometría.
-   **el \_ flujo de corte** puede aparecer cualquier número de veces en el sombreador de geometría, incluido en el control de flujo.
-   Si el sombreador de geometría finaliza y se emiten los vértices, se completa la topología que se está compilando, como si se ejecutara una instrucción **Cut \_ Stream** como última instrucción.
-   Si no se han declarado secuencias, debe usar [CUT](cut--sm4---asm-.md) en lugar de **Cut \_ Stream**.

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

 

 





