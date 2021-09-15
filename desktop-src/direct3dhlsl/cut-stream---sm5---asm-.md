---
title: cut_stream (sm5 - asm)
description: Instrucción del sombreador de geometría que completa la topología primitiva actual en la secuencia especificada, si se le ha emitido algún vértice, e inicia una nueva topología del tipo declarado por el sombreador de geometría en esa secuencia.
ms.assetid: CEFDD13B-34FD-4E9C-94A0-CB8879A7DBDE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4650628d7f6b66130568f885e008a5163a9ee44f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466965"
---
# <a name="cut_stream-sm5---asm"></a>secuencia \_ de corte (sm5 - asm)

Instrucción del sombreador de geometría que completa la topología primitiva actual en la secuencia especificada, si se le ha emitido algún vértice, e inicia una nueva topología del tipo declarado por el sombreador de geometría en esa secuencia.



| cut \_ stream streamIndex |
|-------------------------|



 



| Elemento                                                                                                               | Descripción                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[en \] El índice de secuencia.<br/> |



 

## <a name="remarks"></a>Observaciones

Cuando se ejecuta esta instrucción, se completa cualquier topología emitida previamente por la invocación del sombreador de geometría. Si no hay suficientes vértices emitidos para la topología primitiva anterior, se descartan. Dado que las únicas topologías de salida disponibles para el sombreador de geometría son pointlist, linestrip y trianglestrip, nunca hay vértices sobrados.

*streamIndex* debe ser un valor \[ inmediato 0..3 \] para una secuencia declarada.

Una vez completada la topología anterior, si existe, esta instrucción hace que se inicie una nueva topología, utilizando la topología declarada como salida del sombreador de geometría.

### <a name="restrictions"></a>Restricciones

-   Esta instrucción solo se aplica al sombreador de geometría.
-   **La \_ secuencia de** corte puede aparecer varias veces en el sombreador de geometría, incluido el control de flujo.
-   Si el sombreador de geometría finaliza y se han emitido vértices, se **\_** completa la topología que están compilando, como si se ejecutara una instrucción de secuencia de corte como última instrucción.
-   Si no se han declarado secuencias, debe usar [cortar](cut--sm4---asm-.md) en lugar de **cortar \_ secuencia**.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





