---
title: dcl_tgsm_structured (sm5 - asm)
description: Declare una referencia a una región de espacio de memoria compartida disponible para el grupo de subprocesos del sombreador de proceso. La memoria se ve como una matriz de estructuras.
ms.assetid: C42CD506-58EB-4740-8403-3F9BF29F0CAE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5bf6a6782c455a9bb51ad941a8b6cb42bd70806512a2eef2ed5bd301e57c77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673905"
---
# <a name="dcl_tgsm_structured-sm5---asm"></a>dcl \_ tgsm \_ structured (sm5 - asm)

Declare una referencia a una región de espacio de memoria compartida disponible para el grupo de subprocesos del sombreador de proceso. La memoria se ve como una matriz de estructuras.



| dcl \_ tgsm \_ structured g , \# structByteStride, structCount |
|----------------------------------------------------------|



 



| Elemento                                                                                                                                   | Descripción                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="g_"></span><span id="G_"></span>*G\#*<br/>                                                                             | \[en \] Una referencia a un bloque de memoria compartida de tamaño *structByteStride* \* *structCount* bytes. <br/> |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[en \] El paso de estructura. Este valor es un uint en bytes y debe ser un múltiplo de 4. <br/>           |
| <span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*structCount*<br/>                     | \[en \] El número de estructuras.<br/>                                                                   |



 

## <a name="remarks"></a>Comentarios

El almacenamiento total de todo g debe ser <= la cantidad de memoria compartida disponible por grupo de subprocesos, que es \# 32 kB o 8192 escalares de 32 bits.

En un caso extremo, puede declarar 8192 g s totales, si cada uno tiene un \# *structByteStride* de 4 y un *structCount* de 1.

En el extremo opuesto, puede declarar un solo g con un paso de estructura de 32 kB y un recuento \# de estructura de 1.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

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

 

 





