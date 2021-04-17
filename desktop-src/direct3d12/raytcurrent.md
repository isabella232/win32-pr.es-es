---
description: Un valor de tipo float que representa el punto final paramétrico actual del rayo.
ms.assetid: ''
title: RayTCurrent
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTCurrent
api_type:
- NA
ms.openlocfilehash: 4f090bab88c6be671ca0614255fd7bdebb0d1549
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705340"
---
# <a name="raytcurrent"></a>RayTCurrent

Un valor de tipo float que representa el punto final paramétrico actual del rayo.  

## <a name="syntax"></a>Sintaxis

```
float RayTCurrent();

```


## <a name="remarks"></a>Observaciones

**RayTCurrent** define el punto final actual del rayo según la siguiente fórmula: Origin + (Direction * RayTCurrent).  El *origen* y la *Dirección* pueden estar en el espacio de objeto o en el mundo, lo que da como resultado un punto de final de espacio de objeto o un mundo.

**RayTCurrent** se inicializa en la llamada a [**TraceRay**](traceray-function.md) de llamada con el valor [**RayDesc:: Tmax**](raydesc.md) y, a continuación, se actualiza durante la consulta de seguimiento, ya que las intersecciones se informan (en cualquier acierto) y se aceptan.

En el [sombreador de intersección](intersection-shader.md), representa la distancia a la intersección más cercana encontrada hasta el momento.  Se actualizará después de () al valor THit proporcionado si se aceptó el acierto.

En [cualquier sombreador de posicionamiento](any-hit-shader.md), representa la distancia a la intersección actual que se está informando.

En el [sombreador de posicionamiento más cercano](closest-hit-shader.md), representa la distancia a la intersección más cercana aceptada.

En el [sombreador de errores](miss-shader.md), es igual a *Tmax* pasado a la llamada a **TraceRay** .


Se puede llamar a esta función desde los siguientes tipos de sombreador raytracing:

* [**Sombreador de cualquier acierto**](any-hit-shader.md)
* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de intersección**](intersection-shader.md)
* [**Sombreador de errores**](miss-shader.md)





## <a name="see-also"></a>Vea también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




