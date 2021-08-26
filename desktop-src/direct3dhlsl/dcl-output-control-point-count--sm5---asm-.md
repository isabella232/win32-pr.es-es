---
title: dcl_output_control_point_count (sm5 - asm)
description: Declara el recuento de puntos de control de salida del sombreador de casco.
ms.assetid: 51E8117F-1802-413B-9820-04D5CEBE2DB6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93dc28a2af3ac50c835fa7ec38d7d344029af76a11cb2b84945dbf5009d68473
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024705"
---
# <a name="dcl_output_control_point_count-sm5---asm"></a>dcl \_ output control point count \_ \_ \_ (sm5 - asm)

Declara el recuento de puntos de control de salida del sombreador de casco.



| dcl \_ output control point count \_ \_ \_ N |
|--------------------------------------|



 



| Elemento                                                   | Descripción                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N*<br/> | \[en \] Un valor entero de 0 a 32 que especifica el recuento de puntos de control de salida.<br/> |



 

## <a name="remarks"></a>Comentarios

El sombreador de casco puede generar 0 puntos de control si no son necesarios.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco                 | Domain | Geometría | Píxel | Compute |
|--------|----------------------|--------|----------|-------|---------|
|        | Sección Declaraciones |        |          |       |         |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





