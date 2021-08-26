---
title: dcl_uav_typed (sm5 - asm)
description: Declare una vista de acceso no ordenado (UAV) para que la use un sombreador. | dcl_uav_typed (sm5 - asm)
ms.assetid: F9F5583F-E3D0-447F-9227-BBB1B4E71934
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ec321389f8c8296bda8ccd1eba947b5ba38adc80c94b3c8c0685b069fcdafbf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950585"
---
# <a name="dcl_uav_typed-sm5---asm"></a>dcl \_ uav \_ con tipo (sm5 - asm)

Declare una vista de acceso no ordenado (UAV) para que la use un sombreador.



| dcl \_ uav \_ typed \[ \_ glc \] dstUAV, dimension, type |
|--------------------------------------------------|



 



| Elemento                                                                                           | Descripción                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[en \] el UAV.<br/>                                                                        |
| <span id="dimension"></span><span id="DIMENSION"></span>*Dimensión*<br/>                 | \[en \] Especifica cuántas dimensiones proporcionan las instrucciones que acceden al UAV.<br/> |
| <span id="type"></span><span id="TYPE"></span>*Tipo*<br/>                                | \[en \] El tipo del UAV.<br/>                                                            |



 

## <a name="remarks"></a>Comentarios

*dstUAV es* un registro u que se declara como una referencia a un unorderedAccessView que debe enlazarse a una ranura \# UAV \# en la API.

La dimensión debe ser buffer, Texture1D, Texture1DArray, Texture2D, Texture2DArray o Texture3D. Esto indica cuántas dimensiones proporcionan las instrucciones que acceden al UAV: 1 (Texture1D, Buffer), 2 (Texture1DArray, Texture2D) o 3 (Texture2DArray, Texture3D).

El tipo es {UNORM,SNORM,UINT,SINT,FLOAT}. Las operaciones realizadas con la u declarada deben ser compatibles con el tipo declarado aquí y el UAV enlazado a la ranura también debe \# \# tener el mismo tipo.

La \_ marca glc significa "globalmente coherente". La ausencia de glc significa que el UAV se declara solo como "coherente de grupo" en el sombreador de proceso o "coherente localmente" en una invocación de sombreador de un \_ solo píxel.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Dado que los UAV están disponibles en todas las fases del sombreador para Direct3D 11.1, esta instrucción se aplica a todas las fases del sombreador para el entorno de ejecución de Direct3D 11.1, que está disponible a partir de Windows 8.



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

> [!Note]  
> Esta instrucción no se admite en el sombreador de proceso 4.x.

 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





