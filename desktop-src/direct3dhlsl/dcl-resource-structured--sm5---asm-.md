---
title: dcl_resource estructurado (sm5 - asm)
description: 'Declare una entrada de recurso de sombreador y asígnela a t\: un registro de marcador de posición para el recurso. | dcl_resource estructurado (sm5 - asm)'
ms.assetid: 87FC8A56-9DB2-424B-889C-2AB59885DA13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79ec0bc0b818b345c62bb48ae6f5db68671127110ed06a85c988f8a0449fd490
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285898"
---
# <a name="dcl_resource-structured-sm5---asm"></a>dcl \_ resource structured (sm5 - asm)

Declare una entrada de recurso de sombreador y asígnela a \# t: un registro de marcador de posición para el recurso.



| dcl \_ resource \_ structured dstSRV, structByteStride |
|----------------------------------------------------|



 



| Elemento                                                                                                                                   | Descripción                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*<br/>                                         | \[en un registro t declarado como referencia a ShaderResourceView de un búfer estructurado con el intervalo especificado que debe enlazarse a la ranura SRV en \] \# la \# API. <br/> |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[en \] uint que especifica el tamaño de la estructura en bytes en el búfer que se declara. Este valor debe ser mayor que cero.<br/>                                   |



 

## <a name="remarks"></a>Comentarios

El contenido de la estructura no tiene ningún tipo; Las operaciones realizadas en la memoria pueden interpretar implícitamente que los datos tienen un tipo.

Las instrucciones que hacen referencia a una estructura t toman una dirección 2D, donde el primer componente elige struct y el segundo componente elige el desplazamiento dentro de struct, múltiplo de \# \[ \] \[ 32 bits \] .

cs \_ 4 \_ 0 y cs \_ 4 \_ 1 admiten esta instrucción.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





