---
title: RWStructuredBuffer
description: Un búfer de lectura/escritura que puede tomar un tipo T que es una estructura.
ms.assetid: 8dd93b81-135d-4f28-898f-38510dc39af1
keywords:
- HLSL de RWStructuredBuffer
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
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420894"
---
# <a name="rwstructuredbuffer"></a>RWStructuredBuffer

Un búfer de lectura/escritura que puede tomar un tipo T que es una estructura.



| Método                                                                     | Descripción                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [**DecrementCounter**](sm5-object-rwstructuredbuffer-decrementcounter.md) | Disminuye el contador oculto del objeto. |
| [**GetDimensions**](sm5-object-rwstructuredbuffer-getdimensions.md)       | Obtiene las dimensiones de recursos.           |
| [**IncrementCounter**](sm5-object-rwstructuredbuffer-incrementcounter.md) | Incrementa el contador oculto del objeto. |
| [**Carga**](rwstructuredbuffer-load.md)                                    | Lee los datos del búfer.                      |
| [**Operador\[\]**](sm5-object-rwstructuredbuffer-operatorindex.md)        | Devuelve una variable de recurso.            |



 

También se puede pasar una variable de recurso a cualquier operación sin ordenar o interbloqueada.

Los objetos RWStructuredBuffer pueden ir precedidos de la clase de almacenamiento **globallycoherent**. Esta clase de almacenamiento provoca barreras de memoria y sincronizaciones para vaciar los datos en toda la GPU, de modo que otros grupos puedan ver escrituras. Sin este especificador, una barrera de memoria o una sincronización solo vaciará un UAV dentro del grupo actual.

El formato UAV enlazado a este recurso debe crearse con el formato de DXGI \_ \_ desconocido.

Para obtener más información sobre los [búferes estructurados](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), consulte el material de información general.

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Este objeto es compatible con los siguientes modelos de sombreador.



| Modelo de sombreador                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Compatible |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| Sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador superiores modelo de sombreador [4](dx-graphics-hlsl-sm4.md) (disponible a través de la API de Direct3D 11 mediante el nivel de características 10,0 o 10,1 ([**\_ \_ nivel de característica D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) en los dispositivos que admiten los sombreadores de cálculo. Para obtener más información sobre la compatibilidad del sombreador de cálculo en el hardware de nivel inferior, vea [sombreadores de cálculo en hardware de nivel inferior](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).<br/> | sí       |



 

Este objeto es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

