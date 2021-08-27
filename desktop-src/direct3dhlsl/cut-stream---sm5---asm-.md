---
title: cut_stream (sm5 - asm)
description: Instrucción del sombreador de geometría que completa la topología primitiva actual en la secuencia especificada, si se le ha emitido algún vértice, e inicia una nueva topología del tipo declarado por el sombreador de geometría en esa secuencia.
ms.assetid: CEFDD13B-34FD-4E9C-94A0-CB8879A7DBDE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c019785d121bfb504b447456ad2376deb9c9c63357621513f42dcdf09351f465
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025025"
---
# <a name="cut_stream-sm5---asm"></a>secuencia \_ de corte (sm5 - asm)

Instrucción del sombreador de geometría que completa la topología primitiva actual en la secuencia especificada, si se le ha emitido algún vértice, e inicia una nueva topología del tipo declarado por el sombreador de geometría en esa secuencia.



| cut \_ stream streamIndex |
|-------------------------|



 



| Elemento                                                                                                               | Descripción                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[en \] El índice de la secuencia.<br/> |



 

## <a name="remarks"></a>Comentarios

Cuando se ejecuta esta instrucción, se completa cualquier topología emitida previamente por la invocación del sombreador de geometría. Si no hay suficientes vértices emitidos para la topología primitiva anterior, se descartan. Dado que las únicas topologías de salida disponibles para el sombreador de geometría son pointlist, linestrip y trianglestrip, nunca hay vértices de resto.

*streamIndex* debe ser un valor \[ inmediato 0..3 \] para una secuencia declarada.

Una vez completada la topología anterior, si existe, esta instrucción hace que se inicie una nueva topología, utilizando la topología declarada como salida para el sombreador de geometría.

### <a name="restrictions"></a>Restricciones

-   Esta instrucción solo se aplica al sombreador de geometría.
-   **La \_ secuencia de** corte puede aparecer varias veces en el sombreador de geometría, incluido el control de flujo.
-   Si finaliza el sombreador de geometría y se han emitido vértices, se **\_** completa la topología que están compilando, como si se ejecutara una instrucción de secuencia de corte como última instrucción.
-   Si no se han declarado secuencias, debe usar [cut](cut--sm4---asm-.md) en lugar de **cut \_ stream**.

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

 

 





