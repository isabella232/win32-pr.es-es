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
ms.openlocfilehash: 00db0eb46e8c011e5b31f773679e19ca6dd4a7a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072906"
---
# <a name="raytmin"></a>RayTMin

Un valor float que representa el punto inicial paramétrico actual para el rayo. 

## <a name="syntax"></a>Sintaxis

```
float RayTMin();

```

## <a name="remarks"></a>Observaciones

**RayTMin define** el punto inicial del rayo según la fórmula siguiente: Origin + (Direction * RayTMin).  *El* origen *y la* dirección pueden estar en el espacio del mundo o del objeto, lo que da como resultado un mundo o un punto de partida del espacio de objetos.

**RayTMin se** especifica en la llamada a [**TraceRay**](traceray-function.md)y es constante mientras dura esa llamada.




Se puede llamar a esta función desde los siguientes tipos de sombreador de raytracción:

* [**Sombreador de cualquier acierto**](any-hit-shader.md)
* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de intersección**](intersection-shader.md)
* [**Sombreador de errores**](miss-shader.md)





## <a name="see-also"></a>Consulte también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




