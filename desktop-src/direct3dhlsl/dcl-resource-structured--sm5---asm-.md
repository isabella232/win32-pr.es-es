---
title: dcl_resource estructurado (SM5-ASM)
description: Declare una entrada de recurso de sombreador y asígnela a un registro de marcador de posición t \-a para el recurso. | dcl_resource estructurado (SM5-ASM)
ms.assetid: 87FC8A56-9DB2-424B-889C-2AB59885DA13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ab993e0cb260529c3419210c33f5d735a625bce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279987"
---
# <a name="dcl_resource-structured-sm5---asm"></a>\_recurso de DCL estructurado (SM5-ASM)

Declare una entrada de recurso de sombreador y asígnela a un \# registro de marcador de posición t-a para el recurso.



| \_recurso \_ de DCL estructurado DstSRV, structByteStride |
|----------------------------------------------------|



 



| Elemento                                                                                                                                   | Descripción                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*<br/>                                         | \[en \] un \# registro t declarado como una referencia a un ShaderResourceView de un búfer estructurado con el intervalo especificado que se debe enlazar a la ranura SRV \# en la API. <br/> |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[en \] un uint que especifica el tamaño de la estructura en bytes del búfer que se está declarando. Este valor debe ser mayor que cero.<br/>                                   |



 

## <a name="remarks"></a>Observaciones

El contenido de la estructura no tiene ningún tipo; las operaciones realizadas en la memoria pueden interpretar implícitamente los datos como si tuvieran un tipo.

Las instrucciones que hacen referencia a un t estructurado \# toman una dirección 2D, donde el primer componente selecciona \[ struct \] , y el segundo componente elige \[ offset en struct, múltiplo de 32 bits \] .

CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten esta instrucción.

Esta instrucción se aplica a las siguientes fases del sombreador:



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



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblador modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





