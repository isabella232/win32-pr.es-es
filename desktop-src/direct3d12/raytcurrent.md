---
description: Float que representa el punto final paramétrico actual del rayo.
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
ms.openlocfilehash: 5db5e01fc4af6c3d9304f7f8cf72893029ea34a54cf815310fd1fb3b4c13cbe4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028155"
---
# <a name="raytcurrent"></a>RayTCurrent

Float que representa el punto final paramétrico actual del rayo.  

## <a name="syntax"></a>Sintaxis

```
float RayTCurrent();

```


## <a name="remarks"></a>Comentarios

**RayTCurrent** define el punto final actual del rayo según la fórmula siguiente: Origin + (Direction * RayTCurrent).  *El* origen *y la* dirección pueden estar en el espacio del mundo o del objeto, lo que da lugar a un mundo o un punto final del espacio de objetos.

**RayTCurrent** se inicializa en la llamada [**a TraceRay**](traceray-function.md) con el valor [**RayDesc::TMax**](raydesc.md) y, a continuación, se actualiza durante la consulta de seguimiento a medida que se notifican las intersecciones (en cualquier caso) y se aceptan.

En el [sombreador de](intersection-shader.md)intersección , representa la distancia a la intersección más cercana encontrada hasta ahora.  Se actualizará después de () al valor THit proporcionado si se aceptó la pulsación.

En cualquier [sombreador de impacto,](any-hit-shader.md)representa la distancia a la intersección actual que se notifica.

En el [sombreador de pulsaciones más](closest-hit-shader.md)cercano, representa la distancia a la intersección más cercana aceptada.

En el [sombreador de errores](miss-shader.md), es igual a *TMax* pasado a la **llamada TraceRay.**


Se puede llamar a esta función desde los siguientes tipos de sombreador de raytracción:

* [**Sombreador de cualquier acierto**](any-hit-shader.md)
* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de intersección**](intersection-shader.md)
* [**Sombreador de errores**](miss-shader.md)





## <a name="see-also"></a>Vea también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




