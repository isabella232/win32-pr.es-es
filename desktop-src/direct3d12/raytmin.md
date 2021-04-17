---
description: Un valor de tipo float que representa el punto inicial paramétrico actual del rayo.
ms.assetid: ''
title: RayTMin
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTMin
api_type:
- NA
ms.openlocfilehash: 00db0eb46e8c011e5b31f773679e19ca6dd4a7a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705339"
---
# <a name="raytmin"></a>RayTMin

Un valor de tipo float que representa el punto inicial paramétrico actual del rayo. 

## <a name="syntax"></a>Sintaxis

```
float RayTMin();

```

## <a name="remarks"></a>Observaciones

**RayTMin** define el punto inicial del rayo según la fórmula siguiente: Origin + (Direction * RayTMin).  El *origen* y la *Dirección* pueden estar en el espacio de objeto o en el mundo, lo que da como resultado un punto de partida de un mundo o un espacio de objeto.

**RayTMin** se especifica en la llamada a [**TraceRay**](traceray-function.md)y es constante mientras dure la llamada.




Se puede llamar a esta función desde los siguientes tipos de sombreador raytracing:

* [**Sombreador de cualquier acierto**](any-hit-shader.md)
* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de intersección**](intersection-shader.md)
* [**Sombreador de errores**](miss-shader.md)





## <a name="see-also"></a>Vea también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




