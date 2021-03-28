---
title: dcl_uav_typed (SM5-ASM)
description: Declare una vista de acceso desordenado (UAV) para su uso por parte de un sombreador. | dcl_uav_typed (SM5-ASM)
ms.assetid: F9F5583F-E3D0-447F-9227-BBB1B4E71934
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b789714c7ec825620b73e387fa8a4dd73e1a590d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998257"
---
# <a name="dcl_uav_typed-sm5---asm"></a>DCL \_ UAV \_ con tipo (SM5-ASM)

Declare una vista de acceso desordenado (UAV) para su uso por parte de un sombreador.



| DCL \_ UAV \_ con tipo \[ \_ GLC \] dstUAV, Dimension, tipo |
|--------------------------------------------------|



 



| Elemento                                                                                           | Descripción                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[en \] UAV.<br/>                                                                        |
| <span id="dimension"></span><span id="DIMENSION"></span>*Galería*<br/>                 | \[en \] especifica el número de dimensiones que proporcionan las instrucciones de acceso a UAV.<br/> |
| <span id="type"></span><span id="TYPE"></span>*automáticamente*<br/>                                | \[en \] el tipo de UAV.<br/>                                                            |



 

## <a name="remarks"></a>Observaciones

*dstUAV* es un registro u que \# se declara como una referencia a un UnorderedAccessView que se debe enlazar a \# la ranura UAV de la API.

La dimensión debe ser buffer, Texture1D, Texture1DArray, Texture2D, Texture2DArray o Texture3D. Esto indica el número de dimensiones que tienen las instrucciones de acceso a UAV: 1 (Texture1D, buffer), 2 (Texture1DArray, Texture2D) o 3 (Texture2DArray, Texture3D).

El tipo es {UNORM, SNORM, UINT, SINT, FLOAT}. Las operaciones realizadas con la u declarada \# deben ser compatibles con el tipo declarado aquí, y la UAV enlazada a la ranura \# también debe tener el mismo tipo.

La \_ marca GLC significa "Globally coherente". La ausencia de \_ GLC significa que el UAV se declara solo como "coherente con el grupo" en el sombreador de cálculo o "localmente coherente" en una invocación del sombreador de un solo píxel.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

> [!Note]  
> Esta instrucción no se admite en el sombreador de cálculo 4. x.

 

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

 

 





