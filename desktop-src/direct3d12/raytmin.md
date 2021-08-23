---
description: Un valor float que representa el punto inicial paramétrico actual para el rayo.
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
ms.openlocfilehash: 5429574480cfda071dfec93cea771211bab578bdaecb4513c76f43c4d820b22b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989485"
---
# <a name="raytmin"></a>RayTMin

Un valor float que representa el punto inicial paramétrico actual para el rayo. 

## <a name="syntax"></a>Sintaxis

```
float RayTMin();

```

## <a name="remarks"></a>Comentarios

**RayTMin define** el punto inicial del rayo según la fórmula siguiente: Origin + (Direction * RayTMin).  *El* origen *y la* dirección pueden estar en el espacio del mundo o del objeto, lo que da como resultado un mundo o un punto de partida del espacio de objetos.

**RayTMin se** especifica en la llamada a [**TraceRay**](traceray-function.md)y es constante mientras dura esa llamada.




Se puede llamar a esta función desde los siguientes tipos de sombreador de raytracción:

* [**Sombreador de cualquier acierto**](any-hit-shader.md)
* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de intersección**](intersection-shader.md)
* [**Sombreador de errores**](miss-shader.md)





## <a name="see-also"></a>Vea también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




