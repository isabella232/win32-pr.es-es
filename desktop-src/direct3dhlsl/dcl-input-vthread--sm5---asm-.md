---
title: dcl_input vThread (SM5-ASM)
description: Declare los identificadores de entrada del sombreador de cálculo.
ms.assetid: C041863A-32B0-4588-A1A9-E416AF9B723C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf6a7bb19feef95eae9cc153911407b206fde16
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103785020"
---
# <a name="dcl_input-vthread-sm5---asm"></a>\_vThread de entrada de DCL (SM5-ASM)

Declare los identificadores de entrada del sombreador de cálculo.



| entrada de DCL \_ {vThreadID.XYZ \|vThreadGroupID.xyz \| vThreadIDInGroup.xyz \|vThreadIDInGroupFlattened} |
|--------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                                                                                                                                                                                                                                                                          | Descripción                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="vThreadID___vThreadGroupID___vThreadIDInGroup___vThreadIDInGroupFlattened"></span><span id="vthreadid___vthreadgroupid___vthreadidingroup___vthreadidingroupflattened"></span><span id="VTHREADID___VTHREADGROUPID___VTHREADIDINGROUP___VTHREADIDINGROUPFLATTENED"></span>*vThreadID \| vThreadGroupID \| vThreadIDInGroup \| vThreadIDInGroupFlattened*<br/> | \[en \] el valor de identificador entero de 32 bits sin signo de 3 componentes.<br/> |



 

**la \_ entrada de DCL** es una declaración existente en otras fases del sombreador. Se usa en el sombreador de cálculo para declarar los distintos valores de identificador entero de 32 bits sin signo de tres componentes exclusivos del sombreador de cálculo. Son las siguientes:

-   vThreadID.xyz
-   vGroupID.xyz
-   vThreadIDInGroup.xyz
-   vThreadIDInGroupFlattened (componente único)

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

 

 





