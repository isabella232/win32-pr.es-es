---
title: dcl_tgsm_structured (SM5-ASM)
description: Declare una referencia a una región del espacio de memoria compartido disponible para el grupo de subprocesos del sombreador de cálculo. La memoria se ve como una matriz de estructuras.
ms.assetid: C42CD506-58EB-4740-8403-3F9BF29F0CAE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a639d31c4449a0dfeb152c06b35cfb86c5cc30a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996888"
---
# <a name="dcl_tgsm_structured-sm5---asm"></a>DCL \_ TGSM \_ estructurado (SM5-ASM)

Declare una referencia a una región del espacio de memoria compartido disponible para el grupo de subprocesos del sombreador de cálculo. La memoria se ve como una matriz de estructuras.



| DCL \_ TGSM \_ estructurado g \# , structByteStride, structCount |
|----------------------------------------------------------|



 



| Elemento                                                                                                                                   | Descripción                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="g_"></span><span id="G_"></span>*i\#*<br/>                                                                             | \[en \] una referencia a un bloque de memoria compartida de tamaño *structByteStride* \* *structCount* bytes. <br/> |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[en \] el intervalo de la estructura. Este valor es un uint en bytes y debe ser un múltiplo de 4. <br/>           |
| <span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*structCount*<br/>                     | \[en \] el número de estructuras.<br/>                                                                   |



 

## <a name="remarks"></a>Observaciones

El almacenamiento total de todos los g \# debe ser <= la cantidad de memoria compartida disponible por grupo de subprocesos, que es de 32 KB o escalares de 8192 32 bits.

En un caso extremo, puede declarar 8192 g s totales \# , si cada una tiene un *structByteStride* de 4 y un *structCount* de 1.

En el extremo opuesto, puede declarar una sola g \# con un paso de estructura de 32 KB y un recuento de estructura de 1.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

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

 

 





