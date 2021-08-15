---
title: Funciones intrínsecas del valor del sistema HLSL de Direct3D 12 Raytracing
description: Vea vínculos a artículos que describen funciones intrínsecas de valor del sistema de lenguaje de sombreador de alto nivel (HLSL) que admiten la canalización de rayos de Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b2a2cbd870da41df94ee0389757a1d1ec7cd5e4549a3abd32dbaaf6a7c8e8e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045563"
---
# <a name="direct3d-12-raytracing-hlsl-system-value-intrinsics"></a>Funciones intrínsecas del valor del sistema HLSL de Direct3D 12 Raytracing

Los valores del sistema se recuperan mediante funciones intrínsecas especiales, en lugar de incluir parámetros con semántica especial en la firma de la función de sombreador. 

## <a name="in-this-section"></a>En esta sección

### <a name="ray-dispatch-system-values"></a>Valores del sistema de distribución de rayos

| Tema | Descripción |
|-|-|
| [**DispatchRaysIndex**](dispatchraysindex.md) | Obtiene la ubicación x e y actual dentro del ancho y alto obtenidos con el valor intrínseco del sistema **DispatchRaysDimensions.** |
| [**DispatchRaysDimensions**](dispatchraysdimensions.md) | Los valores de ancho, alto y profundidad de la estructura **D3D12 \_ DISPATCH \_ RAYS \_ DESC** especificada en la **llamada a DispatchRays de** origen. |

### <a name="ray-system-values"></a>Valores del sistema ray

| Tema | Descripción |
|-|-|
| [**WorldRayOrigin**](worldrayorigin.md) | Origen del espacio mundial del rayo actual. |
| [**WorldRayDirection**](worldraydirection.md) | Dirección del espacio mundial para el rayo actual. |
| [**RayTMin**](raytmin.md) | Float que representa el punto inicial paramétrico actual del rayo. |
| [**RayTCurrent**](raytcurrent.md) | Float que representa el punto final paramétrico actual del rayo.  |
| [**RayFlags**](rayflags.md) | Entero sin signo que contiene las marcas **ray_flag** actuales. |

### <a name="primitiveobject-space-system-values"></a>Valores primitivos o del sistema de espacio de objetos

| Tema | Descripción |
|-|-|
| [**InstanceIndex**](instanceindex.md) | Índice generado automáticamente de la instancia actual en la estructura de aceleración de rayos de nivel superior. |
| [**InstanceID**](instanceid.md) | Identificador proporcionado por el usuario para la instancia en la instancia de la estructura de aceleración de nivel inferior dentro de la estructura de nivel superior. |
| [**PrimitiveIndex**](primitiveindex.md) | Índice generado automáticamente de la primitiva dentro de la geometría dentro de la instancia de estructura de aceleración de nivel inferior. |
| [**ObjectRayOrigin**](objectrayorigin.md) | Origen del espacio de objetos para el rayo actual. |
| [**ObjectRayDirection**](objectraydirection.md) | Dirección del espacio del objeto para el rayo actual. |
| [**ObjectToWorld3x4**](objecttoworld3x4.md) | Matriz para transformar del espacio de objetos al espacio del mundo. |
| [**ObjectToWorld4x3**](objecttoworld4x3.md) | Matriz para transformar del espacio de objetos al espacio del mundo. |
| [**WorldToObject3x4**](worldtoobject3x4.md) | Matriz para transformar del espacio del mundo al espacio de objetos |
| [**WorldToObject4x3**](worldtoobject4x3.md) | Matriz para transformar del espacio del mundo al espacio de objetos |
### <a name="hit-specific-system-values"></a>Valores del sistema específicos de las pulsaciones

| Tema | Descripción |
|-|-|
| [**HitKind**](hitkind.md) | Devuelve el valor pasado como parámetro **HitKind** a [**ReportHit.**](reporthit-function.md) |

## <a name="related-topics"></a>Temas relacionados

* [Referencia principal](direct3d-12-core-reference.md)
* [Referencia de Direct3D 12](direct3d-12-reference.md)
