---
title: dcl_input vThread (sm5 - asm)
description: Declare los IDs de entrada del sombreador de proceso.
ms.assetid: C041863A-32B0-4588-A1A9-E416AF9B723C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07c7eef8fe85ae39fb61d9e34b600805d38f7b92d5dbceb7dc2218b1515b6d36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286203"
---
# <a name="dcl_input-vthread-sm5---asm"></a>dcl \_ input vThread (sm5 - asm)

Declare los IDs de entrada del sombreador de proceso.



| dcl \_ input {vThreadID.xyz\|vThreadGroupID.xyz\| vThreadIDInGroup.xyz\|vThreadIDInGroupFlattened} |
|--------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                                                                                                                                                                                                                                                                          | Descripción                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="vThreadID___vThreadGroupID___vThreadIDInGroup___vThreadIDInGroupFlattened"></span><span id="vthreadid___vthreadgroupid___vthreadidingroup___vthreadidingroupflattened"></span><span id="VTHREADID___VTHREADGROUPID___VTHREADIDINGROUP___VTHREADIDINGROUPFLATTENED"></span>*vThreadID \| vThreadGroupID \| vThreadIDInGroup \| vThreadIDInGroupFlattened*<br/> | \[en El valor de identificador entero \] de 32 bits sin signo de 3 componentes.<br/> |



 

**La \_ entrada dcl** es una declaración existente en otras fases del sombreador. Se usa en el sombreador de proceso para declarar los distintos valores de identificador entero de 32 bits sin signo de 3 componentes únicos para el sombreador de proceso. Son las siguientes:

-   vThreadID.xyz
-   vGroupID.xyz
-   vThreadIDInGroup.xyz
-   vThreadIDInGroupFlattened (componente único)

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible. |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





