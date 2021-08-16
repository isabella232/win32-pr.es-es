---
title: cut (sm4 - asm)
description: Instrucción del sombreador de geometría que completa la topología primitiva actual (si se han emitido vértices) e inicia una nueva topología del tipo declarado por el sombreador de geometría.
ms.assetid: 9B28E33D-F518-4844-BE3F-BE61B5F08B4F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34357c05cdd9506ec480d5021db5b330971de9fce7fd70ce9909658be9bb8c4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117908829"
---
# <a name="cut-sm4---asm"></a>cut (sm4 - asm)

Instrucción del sombreador de geometría que completa la topología primitiva actual (si se han emitido vértices) e inicia una nueva topología del tipo declarado por el sombreador de geometría.



| Cortar |
|-----|



 

## <a name="remarks"></a>Comentarios

Cuando **se** ejecuta el corte, lo primero que ocurre es que se completa cualquier topología emitida previamente por la invocación del sombreador de geometría. Si no se emitieron suficientes vértices para la topología primitiva anterior, se descartan. Dado que las únicas topologías de salida disponibles para el sombreador de geometría son pointlist, linestrip y trianglestrip, nunca hay ningún vértice de resto al **cortar**.

Una vez completada la topología anterior, si existe, **cortar** hace que se inicie una nueva topología, utilizando la topología declarada como salida del sombreador de geometría.

## <a name="restrictions"></a>Restricciones

-   La **instrucción de** corte solo se aplica al sombreador de geometría.
-   **El** corte puede aparecer varias veces en el sombreador de geometría, incluido el control de flujo.
-   Si finaliza el Sombreador de geometría y se han emitido vértices, se  completa la topología que están compilando, como si se ejecutara un corte como última instrucción.
-   Si se han declarado secuencias, se debe usar la secuencia [ \_ de](cut-stream---sm5---asm-.md) corte en lugar de **cortar**.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
|               | x               |              |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | Sí       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




