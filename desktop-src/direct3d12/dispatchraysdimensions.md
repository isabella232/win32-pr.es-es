---
description: Los valores de ancho, alto y profundidad de la D3D12_DISPATCH_RAYS_DESC especificada en la llamada de DispatchRays de origen.
ms.assetid: ''
title: DispatchRaysDimensions
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysDimensions
api_type:
- NA
ms.openlocfilehash: 4f68b7bdd5f5ea92074b366b9f981f490a9801079b29def17ba66770abd3c5f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989495"
---
# <a name="dispatchraysdimensions"></a>DispatchRaysDimensions

Los valores de ancho, alto y profundidad de la estructura **D3D12 \_ DISPATCH \_ RAYS \_ DESC** especificada en la llamada [**a DispatchRays de**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) origen.

## <a name="syntax"></a>Sintaxis

```
uint3 DispatchRaysDimensions();
```

## <a name="remarks"></a>Comentarios

Se puede llamar a esta función desde los siguientes tipos de sombreador de raytracción:

* [**Sombreador de cualquier acierto**](any-hit-shader.md)
* [**Sombreador al que se puede llamar**](callable-shader.md)
* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de intersección**](intersection-shader.md)
* [**Sombreador de errores**](miss-shader.md)
* [**Sombreador de generación de rayos**](ray-generation-shader.md)

## <a name="see-also"></a>Vea también

* [Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
