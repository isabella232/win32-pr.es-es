---
title: dcl_uav_raw (SM5-ASM)
description: Declare una vista de acceso desordenado (UAV) para su uso por parte de un sombreador. | dcl_uav_raw (SM5-ASM)
ms.assetid: D0F43FF8-FF1C-4E42-AF42-F528C98FD680
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f47614d5a9327f2d686a36db6bfe4afeb653788
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998093"
---
# <a name="dcl_uav_raw-sm5---asm"></a>DCL \_ UAV \_ raw (SM5-ASM)

Declare una vista de acceso desordenado (UAV) para su uso por parte de un sombreador.



| DCL \_ UAV \_ raw \[ \_ GLC \] dstUAV |
|-------------------------------|



 



| Elemento                                                                                           | Descripción                |
|------------------------------------------------------------------------------------------------|----------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[en \] UAV.<br/> |



 

## <a name="remarks"></a>Observaciones

*dstUAV* es un \# registro u declarado como una referencia a un UnorderedAccessView de un búfer, donde el búfer aparece como una matriz 1D simple de entradas sin tipo de 32 bits.

Las operaciones realizadas en la memoria pueden interpretar implícitamente los datos como si tuvieran un tipo.

La \_ marca GLC significa "globalmente coherente". La ausencia de \_ GLC significa que el UAV se declara solo como "coherente con el grupo" en el sombreador de cálculo o "localmente coherente" en una invocación del sombreador de un solo píxel.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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



 

> [!Note]  
> Esta instrucción es compatible con CS \_ 4 \_ 0 y CS \_ 4 \_ 1.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblador modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





