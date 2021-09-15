---
title: dcl_tgsm_structured (sm5 - asm)
description: Declare una referencia a una región de espacio de memoria compartida disponible para el grupo de subprocesos del sombreador de proceso. La memoria se ve como una matriz de estructuras.
ms.assetid: C42CD506-58EB-4740-8403-3F9BF29F0CAE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a639d31c4449a0dfeb152c06b35cfb86c5cc30a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573892"
---
# <a name="dcl_tgsm_structured-sm5---asm"></a>dcl \_ tgsm \_ structured (sm5 - asm)

Declare una referencia a una región de espacio de memoria compartida disponible para el grupo de subprocesos del sombreador de proceso. La memoria se ve como una matriz de estructuras.



| dcl \_ tgsm \_ structured g , \# structByteStride, structCount |
|----------------------------------------------------------|



 



| Elemento                                                                                                                                   | Descripción                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="g_"></span><span id="G_"></span>*G\#*<br/>                                                                             | \[en \] Una referencia a un bloque de memoria compartida de tamaño *structByteStride* \* *structCount* bytes. <br/> |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[en \] El paso de la estructura. Este valor es un uint en bytes y debe ser un múltiplo de 4. <br/>           |
| <span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*structCount*<br/>                     | \[en \] El número de estructuras.<br/>                                                                   |



 

## <a name="remarks"></a>Observaciones

El almacenamiento total de todos los g debe ser <= la cantidad de memoria compartida disponible por grupo de subprocesos, que es \# 32 kB o 8192 escalares de 32 bits.

En un caso extremo, puede declarar 8192 g s totales, si cada uno tiene un \# *structByteStride* de 4 y *un structCount* de 1.

En el extremo opuesto, puede declarar un solo g con un paso de estructura de 32 kB y un recuento \# de estructura de 1.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

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

 

 





