---
title: Funciones intrínsecas del valor del sistema HLSL de Direct3D 12 Raytracing
description: Vea vínculos a artículos que describen funciones intrínsecas de valor del sistema de lenguaje de sombreador de alto nivel (HLSL) que admiten la canalización de rayos de Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2790cf5df42f64071db3ca51a35e58ee9afcd5
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396440"
---
# <a name="direct3d-12-raytracing-hlsl-system-value-intrinsics"></a>Funciones intrínsecas del valor del sistema HLSL de Direct3D 12 Raytracing

Los valores del sistema se recuperan mediante funciones intrínsecas especiales, en lugar de incluir parámetros con semántica especial en la firma de la función de sombreador. 

## <a name="in-this-section"></a>En esta sección

### <a name="ray-dispatch-system-values"></a>Valores del sistema de distribución de Ray

| Tema | Descripción |
|-|-|
| [**DispatchRaysIndex**](dispatchraysindex.md) | Obtiene la ubicación x e y actual dentro del ancho y alto obtenidos con el valor intrínseco del sistema **DispatchRaysDimensions.** |
| [**DispatchRaysDimensions**](dispatchraysdimensions.md) | Los valores de ancho, alto y profundidad de la estructura **D3D12 \_ DISPATCH \_ RAYS \_ DESC** especificada en la **llamada dispatchRays de** origen. |

### <a name="ray-system-values"></a>Valores del sistema ray

| Tema | Descripción |
|-|-|
| [**WorldRayOrigin**](worldrayorigin.md) | Origen del espacio mundial del rayo actual. |
| [**WorldRayDirection**](worldraydirection.md) | Dirección del espacio del mundo para el rayo actual. |
| [**RayTMin**](raytmin.md) | Un valor float que representa el punto inicial paramétrico actual para el rayo. |
| [**RayTCurrent**](raytcurrent.md) | Float que representa el punto final paramétrico actual del rayo.  |
| [**RayFlags**](rayflags.md) | Entero sin signo que contiene las marcas **ray_flag** actuales. |

### <a name="primitiveobject-space-system-values"></a>Valores primitivos o del sistema de espacio de objetos

| Tema | Descripción |
|-|-|
| [**InstanceIndex**](instanceindex.md) | Índice generado automáticamente de la instancia actual en la estructura de aceleración de rayos de nivel superior. |
| [**InstanceID**](instanceid.md) | Identificador proporcionado por el usuario para la instancia de en la instancia de la estructura de aceleración de nivel inferior dentro de la estructura de nivel superior. |
| [**PrimitiveIndex**](primitiveindex.md) | Índice generado automáticamente de la primitiva dentro de la geometría dentro de la instancia de la estructura de aceleración de nivel inferior. |
| [**ObjectRayOrigin**](objectrayorigin.md) | Origen del espacio de objetos para el rayo actual. |
| [**ObjectRayDirection**](objectraydirection.md) | Dirección del espacio del objeto para el rayo actual. |
| [**ObjectToWorld3x4**](objecttoworld3x4.md) | Matriz para transformar del espacio de objetos al espacio del mundo. |
| [**ObjectToWorld4x3**](objecttoworld4x3.md) | Matriz para transformar del espacio de objetos al espacio del mundo. |
| [**WorldToObject3x4**](worldtoobject3x4.md) | Matriz para la transformación del espacio del mundo al espacio de objetos |
| [**WorldToObject4x3**](worldtoobject4x3.md) | Matriz para la transformación del espacio del mundo al espacio de objetos |
### <a name="hit-specific-system-values"></a>Valores del sistema específicos de la aplicación

| Tema | Descripción |
|-|-|
| [**HitKind**](hitkind.md) | Devuelve el valor pasado como parámetro **HitKind** a [**ReportHit.**](reporthit-function.md) |

## <a name="related-topics"></a>Temas relacionados

* [Referencia principal](direct3d-12-core-reference.md)
* [Referencia de Direct3D 12](direct3d-12-reference.md)
