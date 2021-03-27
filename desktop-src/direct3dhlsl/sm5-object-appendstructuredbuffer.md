---
title: AppendStructuredBuffer
description: Búfer de salida que aparece como un flujo al que el sombreador puede anexar. Solo los búferes estructurados pueden tomar tipos T que son estructuras.
ms.assetid: 377b0358-0f9d-4021-9140-19c3d1bfed38
keywords:
- HLSL de AppendStructuredBuffer
topic_type:
- apiref
api_name:
- AppendStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c140052c861c8da3df6378fc3bc49816998c130
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792291"
---
# <a name="appendstructuredbuffer"></a>AppendStructuredBuffer

Búfer de salida que aparece como un flujo al que el sombreador puede anexar. Solo los búferes estructurados pueden tomar tipos T que son estructuras.



| Método                                                                   | Descripción                               |
|--------------------------------------------------------------------------|-------------------------------------------|
| [**Append**](sm5-object-appendstructuredbuffer-append.md)               | Anexa un valor al final del búfer. |
| [**GetDimensions**](sm5-object-appendstructuredbuffer-getdimensions.md) | Obtiene las dimensiones de recursos.             |



 

El formato UAV enlazado a este recurso debe crearse con el formato de DXGI \_ \_ desconocido.

El UAV enlazado a este recurso se debe haber creado con la [**marca de D3D11 del \_ búfer \_ UAV \_ \_ Append**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).

Para obtener más información sobre un búfer estructurado append, vea ambas secciones: [Append y consume](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) buffer y [buffer estructurado](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Este objeto es compatible con los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores | sí       |



 

Este objeto es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 