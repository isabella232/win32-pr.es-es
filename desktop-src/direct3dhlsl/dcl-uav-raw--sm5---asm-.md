---
title: dcl_uav_raw (sm5 - asm)
description: Declare una vista de acceso no ordenado (UAV) para que la use un sombreador. | dcl_uav_raw (sm5 - asm)
ms.assetid: D0F43FF8-FF1C-4E42-AF42-F528C98FD680
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f47614d5a9327f2d686a36db6bfe4afeb653788
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573889"
---
# <a name="dcl_uav_raw-sm5---asm"></a>dcl \_ uav \_ raw (sm5 - asm)

Declare una vista de acceso no ordenado (UAV) para que la use un sombreador.



| dcl \_ uav \_ raw \[ \_ glc \] dstUAV |
|-------------------------------|



 



| Elemento                                                                                           | Descripción                |
|------------------------------------------------------------------------------------------------|----------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[en \] el UAV.<br/> |



 

## <a name="remarks"></a>Observaciones

*dstUAV* es un registro u declarado como referencia a un unorderedAccessView de un búfer, donde el búfer aparece como una matriz 1D simple de entradas de 32 bits sin \# tipo.

Las operaciones realizadas en la memoria pueden interpretar implícitamente que los datos tienen un tipo.

La \_ marca glc significa "globalmente coherente". La ausencia de glc significa que el UAV se declara solo como "coherente de grupo" en el sombreador de proceso o "coherente localmente" en una invocación de sombreador de \_ píxeles único.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Dado que los UAV están disponibles en todas las fases del sombreador para Direct3D 11.1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11.1, que está disponible a partir de Windows 8.



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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



 

> [!Note]  
> Esta instrucción se admite en cs \_ 4 \_ 0 y cs \_ 4 \_ 1.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





