---
title: RWStructuredBuffer
description: Búfer de lectura/escritura que puede tomar un tipo T que es una estructura.
ms.assetid: 8dd93b81-135d-4f28-898f-38510dc39af1
keywords:
- RWStructuredBuffer HLSL
topic_type:
- apiref
api_name:
- RWStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f921ca795e761522828de14ede61894defe44f6e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359328"
---
# <a name="rwstructuredbuffer"></a>RWStructuredBuffer

Búfer de lectura/escritura que puede tomar un tipo T que es una estructura.



| Método                                                                     | Descripción                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [**DecrementCounter**](sm5-object-rwstructuredbuffer-decrementcounter.md) | Disminuye el contador oculto del objeto. |
| [**GetDimensions**](sm5-object-rwstructuredbuffer-getdimensions.md)       | Obtiene las dimensiones de recursos.           |
| [**IncrementCounter**](sm5-object-rwstructuredbuffer-incrementcounter.md) | Incrementa el contador oculto del objeto. |
| [**Carga**](rwstructuredbuffer-load.md)                                    | Lee los datos del búfer.                      |
| [**Operator\[\]**](sm5-object-rwstructuredbuffer-operatorindex.md)        | Devuelve una variable de recurso.            |



 

También se puede pasar una variable de recurso a cualquier operación desordenada o entrelazado.

Los objetos RWStructuredBuffer pueden tener como prefijo la clase de almacenamiento **globalmentecoherente**. Esta clase de almacenamiento hace que las barreras de memoria y las sincronizaciones vaciarán los datos en toda la GPU para que otros grupos puedan ver escrituras. Sin este especificador, una barrera o sincronización de memoria solo vaciará un UAV dentro del grupo actual.

El formato UAV enlazado a este recurso debe crearse con el formato DXGI \_ FORMAT \_ UNKNOWN.

Para más información sobre los [búferes estructurados,](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)consulte el material de información general.

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Este objeto se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Compatible |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| Modelo de sombreador [5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores Shader [Model 4](dx-graphics-hlsl-sm4.md) (disponible a través de la API de Direct3D 11 mediante el nivel de característica 10.0 o 10.1 [**(D3D \_ FEATURE \_ LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 X) en dispositivos que admiten sombreadores \_ de proceso. Para obtener más información sobre la compatibilidad del sombreador de proceso en hardware de nivel inferior, vea [Sombreadores de proceso en hardware de nivel inferior).](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders)<br/> | sí       |



 

Este objeto es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

