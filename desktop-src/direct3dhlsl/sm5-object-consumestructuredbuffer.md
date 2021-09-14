---
title: ConsumeStructuredBuffer
description: Búfer de entrada que aparece como un flujo del que el sombreador puede extraer valores. Solo los búferes estructurados pueden tomar tipos T que son estructuras.
ms.assetid: 373bdd97-6186-4bce-99bf-738a153234f6
keywords:
- ConsumeStructuredBuffer HLSL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963607"
---
# <a name="consumestructuredbuffer"></a>ConsumeStructuredBuffer

Búfer de entrada que aparece como un flujo del que el sombreador puede extraer valores. Solo los búferes estructurados pueden tomar tipos T que son estructuras.



| Método                                                                    | Descripción                                 |
|---------------------------------------------------------------------------|---------------------------------------------|
| [**Consumo**](sm5-object-consumestructuredbuffer-consume.md)             | Quita un valor del final del búfer. |
| [**GetDimensions**](sm5-object-consumestructuredbuffer-getdimensions.md) | Obtiene las dimensiones de recursos.               |



 

El formato UAV enlazado a este recurso debe crearse con el formato DXGI \_ FORMAT \_ UNKNOWN.

El UAV enlazado a este recurso debe haber sido creado con [**D3D11 \_ BUFFER \_ UAV \_ FLAG \_ APPEND**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).

Para obtener más información sobre el consumo de búferes estructurados, vea ambas secciones: [anexar](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) y consumir búfer y [búfer estructurado.](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Este objeto se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores | sí       |



 

Este objeto es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 