---
description: Los valores de ancho, alto y profundidad de la D3D12_DISPATCH_RAYS_DESC estructura especificada en la llamada de DispatchRays de origen.
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
ms.openlocfilehash: e35c967ad831c82912d2962da72d9ad17eab1c15
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359786"
---
# <a name="dispatchraysdimensions"></a>DispatchRaysDimensions

Los valores de ancho, alto y profundidad de la estructura **D3D12 \_ DISPATCH \_ RAYS \_ DESC** especificada en la [**llamada a DispatchRays de**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) origen.

## <a name="syntax"></a>Sintaxis

```
uint3 DispatchRaysDimensions();
```

## <a name="remarks"></a>Observaciones

Se puede llamar a esta función desde los siguientes tipos de sombreador:

* [**Sombreador de cualquier acierto**](any-hit-shader.md)
* [**Sombreador al que se puede llamar**](callable-shader.md)
* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de intersección**](intersection-shader.md)
* [**Sombreador de errores**](miss-shader.md)
* [**Sombreador de generación de rayos**](ray-generation-shader.md)

## <a name="see-also"></a>Consulte también

* [Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
