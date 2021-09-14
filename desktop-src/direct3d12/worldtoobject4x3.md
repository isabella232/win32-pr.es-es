---
description: 'WorldToObject4x3: matriz para la transformación del espacio del mundo al espacio de objetos.'
ms.assetid: ''
title: WorldToObject4x3
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WorldToObject4x3
api_type:
- NA
ms.openlocfilehash: 334a79352345fb35fbbafe68248a221bdaab9f6d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160448"
---
# <a name="worldtoobject4x3"></a>WorldToObject4x3

Matriz para la transformación del espacio del mundo al espacio de objetos. Espacio de objeto hace referencia al espacio de la estructura de aceleración de nivel inferior actual.

## <a name="syntax"></a>Sintaxis

```
void WorldToObject4x3();

```




## <a name="remarks"></a>Observaciones

La matriz es una contracción de **la matriz WorldToObject3x4.**

Se puede llamar a esta función desde los siguientes tipos de sombreador de raytracción:

* [**Sombreador de cualquier acierto**](any-hit-shader.md)
* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de intersección**](intersection-shader.md)





## <a name="see-also"></a>Consulte también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




