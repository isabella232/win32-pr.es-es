---
title: cortar (SM4-ASM)
description: Instrucción del sombreador de geometría que completa la topología primitiva actual (si se ha emitido algún vértice) e inicia una nueva topología del tipo declarado por el sombreador de geometría.
ms.assetid: 9B28E33D-F518-4844-BE3F-BE61B5F08B4F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c462d2f4dc2e0c6b4076f577610c93794e890af
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983823"
---
# <a name="cut-sm4---asm"></a>cortar (SM4-ASM)

Instrucción del sombreador de geometría que completa la topología primitiva actual (si se ha emitido algún vértice) e inicia una nueva topología del tipo declarado por el sombreador de geometría.



| cut |
|-----|



 

## <a name="remarks"></a>Observaciones

Cuando se ejecuta **CUT** , lo primero que ocurre es que se completa cualquier topología emitida previamente por la invocación del sombreador de geometría. Si no se emitieron suficientes vértices para la topología primitiva anterior, se descartan. Dado que las únicas topologías de salida disponibles para el sombreador de geometría son PointList, linestrip y trianglestrip, nunca hay vértices sobrantes al **cortar**.

Una vez completada la topología anterior, si la hubiera, la instrucción **CUT** provoca que se inicie una nueva topología, utilizando la topología declarada como la salida del sombreador de geometría.

## <a name="restrictions"></a>Restricciones

-   La instrucción **CUT** solo se aplica al sombreador de geometría.
-   **CUT** puede aparecer cualquier número de veces en el sombreador de geometría, incluido en el control de flujo.
-   Si el sombreador de geometría finaliza y se emiten los vértices, se completa la topología que se está compilando, como si se ejecutara un **corte** como última instrucción.
-   Si se han declarado secuencias, se debe usar [Cut \_ Stream](cut-stream---sm5---asm-.md) en lugar de **CUT**.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
|               | x               |              |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




