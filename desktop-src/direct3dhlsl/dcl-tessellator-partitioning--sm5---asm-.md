---
title: dcl_tessellator_partitioning (sm5 - asm)
description: Declare la creación de particiones del teselador en una sección de declaración del sombreador de casco.
ms.assetid: 6EA00C6B-A0DE-4CE4-8B52-1337CA92CA5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6f6091301f95dd2364debec2bf54c0966c0e64
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573893"
---
# <a name="dcl_tessellator_partitioning-sm5---asm"></a>Creación de \_ particiones de tessellator \_ dcl (sm5 - asm)

Declare la creación de particiones del teselador en una sección de declaración del sombreador de casco.



| dcl \_ tessellator \_ partitioning {partitioning \_ integer\| particionamiento \_ pow2\|particionamiento \_ de fracciones \_ impares\| particionamiento \_ de \_ fracciones incluso} |
|---------------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Descripción                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="partitioning_integer__________________________________partitioning_pow2_partitioning_fractional_odd__________________________________partitioning_fractional_even"></span><span id="PARTITIONING_INTEGER__________________________________PARTITIONING_POW2_PARTITIONING_FRACTIONAL_ODD__________________________________PARTITIONING_FRACTIONAL_EVEN"></span>*\_particionamiento de \| particiones de \_ enteros pow2 \| \_ particionamiento fraccionamiento fraccionamiento \_ impar \| \_ incluso \_*<br/> | \[en \] La creación de particiones del teselador.<br/> |



 

## <a name="remarks"></a>Observaciones

Desde el punto de vista del hardware, \_ pow2 se comporta como \_ un entero. Es el autor del sombreador HLSL o el código del compilador redondear TessFactors a potencias de 2.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco                 | Domain | Geometría | Píxel | Compute |
|--------|----------------------|--------|----------|-------|---------|
|        | Sección Declaraciones |        |          |       |         |



 

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

 

 





