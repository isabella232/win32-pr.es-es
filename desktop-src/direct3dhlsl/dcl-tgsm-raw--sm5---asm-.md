---
title: dcl_tgsm_raw (SM5-ASM)
description: Declare una referencia a una región del espacio de memoria compartido disponible para el grupo de subprocesos del sombreador de cálculo.
ms.assetid: 8EA6931C-5B13-431F-A886-04F8C73CD22D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd20d8a0d8d2309b9b895a5cb5439877bb10d31a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103785002"
---
# <a name="dcl_tgsm_raw-sm5---asm"></a>DCL \_ TGSM \_ raw (SM5-ASM)

Declare una referencia a una región del espacio de memoria compartido disponible para el grupo de subprocesos del sombreador de cálculo.



| \_TGSM \_ de DCL RAW g \# , byteCount |
|-------------------------------|



 



| Elemento                                                                                                       | Descripción                                                                             |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="g_"></span><span id="G_"></span>*i\#*<br/>                                                 | \[en \] una referencia a un bloque de tamaño *byteCount* de memoria compartida sin tipo. <br/> |
| <span id="byteCount"></span><span id="bytecount"></span><span id="BYTECOUNT"></span>*byteCount*<br/> | \[en \] debe ser un múltiplo de 4. <br/>                                             |



 

## <a name="remarks"></a>Observaciones

El almacenamiento total de todos los g \# debe ser <= la cantidad de memoria compartida disponible por grupo de subprocesos, que es de 32 KB.

En un caso extremo, puede declarar 8192 g s en total \# , cada uno con un *byteCount* de 4.

En el extremo opuesto, puede declarar una sola g \# con un *byteCount* de 32768.

> [!Note]  
> CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten la [ \_ TGSM \_ de DCL](dcl-tgsm-structured--sm5---asm-.md), pero no la de **DCL \_ TGSM \_ raw**.

 

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

 

 





