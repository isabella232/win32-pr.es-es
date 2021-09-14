---
description: Obtiene la ubicación actual dentro del ancho, alto y profundidad obtenidos con el valor intrínseco del sistema [**DispatchRaysDimensions.**](dispatchraysdimensions.md)
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
ms.openlocfilehash: aa26400c26aba4ee9e647bcd0a79bad3f3d52f7c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253029"
---
# <a name="dispatchraysindex"></a>DispatchRaysIndex 

Obtiene la ubicación actual dentro del ancho, alto y profundidad obtenidos con el valor intrínseco del sistema [**DispatchRaysDimensions.**](dispatchraysdimensions.md)

## <a name="syntax"></a>Sintaxis

```syntax
uint3 DispatchRaysIndex();
```

## <a name="remarks"></a>Observaciones

Se puede llamar a esta función desde los siguientes tipos de sombreador de rayos.

* [**Sombreador de cualquier acierto**](any-hit-shader.md)
* [**Sombreador al que se puede llamar**](callable-shader.md)
* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de intersección**](intersection-shader.md)
* [**Sombreador de errores**](miss-shader.md)
* [**Sombreador de generación de rayos**](ray-generation-shader.md)

## <a name="see-also"></a>Consulte también

* [Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
