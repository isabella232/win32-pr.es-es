---
title: Funciones intrínsecas del valor del sistema HLSL de Direct3D 12 Raytracing
description: Los siguientes sombreadores HLSL admiten la canalización raytracing de Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a20282e7bc0e9e4898fd361b0959cd6b6f32253
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2020
ms.locfileid: "105714493"
---
# <a name="direct3d-12-raytracing-hlsl-system-value-intrinsics"></a>Funciones intrínsecas del valor del sistema HLSL de Direct3D 12 Raytracing

Los valores del sistema se recuperan mediante funciones intrínsecas especiales, en lugar de incluir parámetros con semántica especial en la firma de la función de sombreador. 

## <a name="in-this-section"></a>En esta sección

### <a name="ray-dispatch-system-values"></a>Valores del sistema de distribución de Ray

| Tema | Descripción |
|-|-|
| [**DispatchRaysIndex**](dispatchraysindex.md) | Obtiene la ubicación x e y actual en el ancho y el alto obtenidos con el valor intrínseco del sistema **DispatchRaysDimensions** . |
| [**DispatchRaysDimensions**](dispatchraysdimensions.md) | Los valores de ancho, alto y profundidad de la estructura de D3D12 de los **\_ \_ rayos \_ de distribución** de la serie especificada en la llamada de **DispatchRays** de origen. |

### <a name="ray-system-values"></a>Valores del sistema Ray

| Tema | Descripción |
|-|-|
| [**WorldRayOrigin**](worldrayorigin.md) | El origen de espacio mundial del rayo actual. |
| [**WorldRayDirection**](worldraydirection.md) | Dirección de espacio mundial del rayo actual. |
| [**RayTMin**](raytmin.md) | Un valor de tipo float que representa el punto inicial paramétrico actual del rayo. |
| [**RayTCurrent**](raytcurrent.md) | Un valor de tipo float que representa el punto final paramétrico actual del rayo.  |
| [**RayFlags**](rayflags.md) | Entero sin signo que contiene las marcas de **ray_flag** actuales. |

### <a name="primitiveobject-space-system-values"></a>Valores del sistema de espacio de objetos primitivos

| Tema | Descripción |
|-|-|
| [**InstanceIndex**](instanceindex.md) | Índice generado automáticamente de la instancia actual en la estructura de nivel superior raytracing de aceleración. |
| [**ID**](instanceid.md) | El identificador proporcionado por el usuario para la instancia en la instancia de la estructura de aceleración de nivel inferior dentro de la estructura de nivel superior. |
| [**PrimitiveIndex**](primitiveindex.md) | Índice generado automáticamente de la primitiva dentro de la geometría dentro de la instancia de la estructura de aceleración de nivel inferior. |
| [**ObjectRayOrigin**](objectrayorigin.md) | El origen del espacio de objeto del rayo actual. |
| [**ObjectRayDirection**](objectraydirection.md) | Dirección del espacio de objeto del rayo actual. |
| [**ObjectToWorld3x4**](objecttoworld3x4.md) | Matriz que se va a transformar del espacio de objeto a espacio universal. |
| [**ObjectToWorld4x3**](objecttoworld4x3.md) | Matriz que se va a transformar del espacio de objeto a espacio universal. |
| [**WorldToObject3x4**](worldtoobject3x4.md) | Matriz para transformar de espacio universal a objeto-espacio |
| [**WorldToObject4x3**](worldtoobject4x3.md) | Matriz para transformar de espacio universal a objeto-espacio |
### <a name="hit-specific-system-values"></a>Valores del sistema específicos de la visita

| Tema | Descripción |
|-|-|
| [**HitKind**](hitkind.md) | Devuelve el valor que se pasa como parámetro **HitKind** a [**ReportHit**](reporthit-function.md). |

## <a name="related-topics"></a>Temas relacionados

* [Referencia básica](direct3d-12-core-reference.md)
* [Referencia de Direct3D 12](direct3d-12-reference.md)
