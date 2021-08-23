---
description: Obtiene la ubicación actual dentro del ancho, alto y profundidad obtenidos con el valor intrínseco del [**sistema DispatchRaysDimensions.**](dispatchraysdimensions.md)
title: 'DispatchRaysIndex '
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysIndex
api_type:
- NA
ms.openlocfilehash: 1b40987c76f42d41d74b7cb3d41f35cc20bd5a6ac1414ae9b010cedcfa7ef9fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124173"
---
# <a name="dispatchraysindex"></a>DispatchRaysIndex 

Obtiene la ubicación actual dentro del ancho, alto y profundidad obtenidos con el valor intrínseco del [**sistema DispatchRaysDimensions.**](dispatchraysdimensions.md)

## <a name="syntax"></a>Sintaxis

```syntax
uint3 DispatchRaysIndex();
```

## <a name="remarks"></a>Comentarios

Se puede llamar a esta función desde los siguientes tipos de sombreador de raytracing.

* [**Sombreador de cualquier acierto**](any-hit-shader.md)
* [**Sombreador al que se puede llamar**](callable-shader.md)
* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de intersección**](intersection-shader.md)
* [**Sombreador de errores**](miss-shader.md)
* [**Sombreador de generación de rayos**](ray-generation-shader.md)

## <a name="see-also"></a>Vea también

* [Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
