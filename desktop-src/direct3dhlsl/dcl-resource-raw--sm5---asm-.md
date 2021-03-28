---
title: dcl_resource RAW (SM5-ASM)
description: Declare una entrada de recurso de sombreador y asígnela a un registro de marcador de posición t \-a para el recurso. | dcl_resource RAW (SM5-ASM)
ms.assetid: ECBA9DAB-F217-47FB-9588-F35866004E72
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd6ccc5990e34990772a072086d9e080cde67b4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280050"
---
# <a name="dcl_resource-raw-sm5---asm"></a>\_recurso de DCL sin formato (SM5-ASM)

Declare una entrada de recurso de sombreador y asígnela a un \# registro de marcador de posición t-a para el recurso.



| \_ \_ dstSRV sin formato de recursos de DCL |
|---------------------------|



 



| Elemento                                                                                           | Descripción                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*<br/> | \[en \] un \# registro t declarado como una referencia a un ShaderResourceView de un búfer sin formato.<br/> |



 

## <a name="remarks"></a>Observaciones

El contenido de la estructura no tiene ningún tipo; las operaciones realizadas en la memoria pueden interpretar implícitamente los datos como si tuvieran un tipo.

Las instrucciones que hacen referencia a una t sin formato \# toman una dirección 1D, un valor de bit 32 sin signo que especifica el desplazamiento de bytes a una ubicación alineada de 32 bits en el búfer. La dirección debe ser un múltiplo de 4 (bytes).

Las vistas enlazadas a t \# declaradas como RAW deben tener los sin procesar especificados en su creación; de lo contrario, el comportamiento cuando se tiene acceso desde un sombreador no está definido.

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

 

 





