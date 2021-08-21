---
title: AppendStructuredBuffer
description: Búfer de salida que aparece como una secuencia a la que el sombreador puede anexar. Solo los búferes estructurados pueden tomar tipos T que son estructuras.
ms.assetid: 377b0358-0f9d-4021-9140-19c3d1bfed38
keywords:
- AppendStructuredBuffer HLSL
topic_type:
- apiref
api_name:
- AppendStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 23efdb58b8effc0ccdaf32da31ad93dfaf8f6eae602c6769c947ffa0c0f505d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510114"
---
# <a name="appendstructuredbuffer"></a>AppendStructuredBuffer

Búfer de salida que aparece como una secuencia a la que el sombreador puede anexar. Solo los búferes estructurados pueden tomar tipos T que son estructuras.



| Método                                                                   | Descripción                               |
|--------------------------------------------------------------------------|-------------------------------------------|
| [**Append**](sm5-object-appendstructuredbuffer-append.md)               | Anexa un valor al final del búfer. |
| [**GetDimensions**](sm5-object-appendstructuredbuffer-getdimensions.md) | Obtiene las dimensiones de recursos.             |



 

El formato UAV enlazado a este recurso debe crearse con el formato DXGI \_ FORMAT \_ UNKNOWN.

El UAV enlazado a este recurso debe haber sido creado con [**D3D11 \_ BUFFER \_ UAV \_ FLAG \_ APPEND**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).

Para obtener más información sobre un búfer estructurado de anexos, vea ambas secciones: [anexar](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) y consumir búfer y [búfer estructurado.](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Este objeto se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores | Sí       |



 

Este objeto es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 