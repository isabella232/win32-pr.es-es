---
title: dcl_resource sin procesar (sm5 - asm)
description: 'Declare una entrada de recurso de sombreador y asígnela a t\: un registro de marcador de posición para el recurso. | dcl_resource sin procesar (sm5 - asm)'
ms.assetid: ECBA9DAB-F217-47FB-9588-F35866004E72
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd6ccc5990e34990772a072086d9e080cde67b4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264260"
---
# <a name="dcl_resource-raw-sm5---asm"></a>dcl \_ resource raw (sm5 - asm)

Declare una entrada de recurso de sombreador y asígnela a \# t: un registro de marcador de posición para el recurso.



| dcl \_ resource \_ raw dstSRV |
|---------------------------|



 



| Elemento                                                                                           | Descripción                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*<br/> | \[en \] un registro t declarado como una referencia a \# ShaderResourceView de un búfer sin formato.<br/> |



 

## <a name="remarks"></a>Observaciones

El contenido de la estructura no tiene ningún tipo; Las operaciones realizadas en la memoria pueden interpretar implícitamente que los datos tienen un tipo .

Las instrucciones que hacen referencia a un t sin formato toman una dirección 1D, un valor de 32 bits sin signo que especifica el desplazamiento de bytes a una ubicación alineada de 32 bits en el \# búfer. La dirección debe ser un múltiplo de 4 (bytes).

Las vistas enlazadas a t declaradas como sin formato deben tener RAW especificado en su creación; de lo contrario, el comportamiento cuando se accede \# desde un sombreador es indefinido.

cs \_ 4 \_ 0 y cs \_ 4 \_ 1 admiten esta instrucción.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
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

 

 





