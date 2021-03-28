---
title: dcl_tessellator_partitioning (SM5-ASM)
description: Declare la creación de particiones del teselador en una sección de declaración del sombreador de casco.
ms.assetid: 6EA00C6B-A0DE-4CE4-8B52-1337CA92CA5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6f6091301f95dd2364debec2bf54c0966c0e64
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419983"
---
# <a name="dcl_tessellator_partitioning-sm5---asm"></a>creación \_ \_ de particiones de DCL del teselador (SM5-ASM)

Declare la creación de particiones del teselador en una sección de declaración del sombreador de casco.



| DCL \_ del teselador creación de \_ particiones {entero de particionamiento \_ \| creación de particiones \_ pow2 \|crear particiones de las \_ fracciones \_ impares| dividir las particiones \_ \_ pares} |
|---------------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Descripción                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="partitioning_integer__________________________________partitioning_pow2_partitioning_fractional_odd__________________________________partitioning_fractional_even"></span><span id="PARTITIONING_INTEGER__________________________________PARTITIONING_POW2_PARTITIONING_FRACTIONAL_ODD__________________________________PARTITIONING_FRACTIONAL_EVEN"></span>*creación de particiones de entero de particionamiento \_ \| \_ pow2 \| particionamiento \_ fraccionario \_ \| \_ \_*<br/> | \[en \] la partición del teselador.<br/> |



 

## <a name="remarks"></a>Observaciones

Desde el punto de vista del hardware, \_ pow2 se comporta como un \_ entero. Es el autor del sombreador de HLSL y/o compilercode para redondear TessFactors a potencias de 2.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco                 | Dominio | Geometría | Píxel | Compute |
|--------|----------------------|--------|----------|-------|---------|
|        | Sección declaraciones |        |          |       |         |



 

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

 

 





