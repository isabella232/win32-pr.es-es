---
title: ConsumeStructuredBuffer
description: Un búfer de entrada que aparece como un flujo del que el sombreador puede extraer valores. Solo los búferes estructurados pueden tomar tipos T que son estructuras.
ms.assetid: 373bdd97-6186-4bce-99bf-738a153234f6
keywords:
- HLSL de ConsumeStructuredBuffer
topic_type:
- apiref
api_name:
- ConsumeStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af7a670713dc5b63839702a04a632dda61ebfa43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997165"
---
# <a name="consumestructuredbuffer"></a>ConsumeStructuredBuffer

Un búfer de entrada que aparece como un flujo del que el sombreador puede extraer valores. Solo los búferes estructurados pueden tomar tipos T que son estructuras.



| Método                                                                    | Descripción                                 |
|---------------------------------------------------------------------------|---------------------------------------------|
| [**Consumo**](sm5-object-consumestructuredbuffer-consume.md)             | Quita un valor del final del búfer. |
| [**GetDimensions**](sm5-object-consumestructuredbuffer-getdimensions.md) | Obtiene las dimensiones de recursos.               |



 

El formato UAV enlazado a este recurso debe crearse con el formato de DXGI \_ \_ desconocido.

El UAV enlazado a este recurso se debe haber creado con la [**marca de D3D11 del \_ búfer \_ UAV \_ \_ Append**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).

Para obtener más información sobre el uso de búferes estructurados, vea ambas secciones: [Append y consume](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) buffer y [buffer estructurado](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources).

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

 

 