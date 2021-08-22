---
description: 'WorldToObject4x3: matriz para transformar del espacio del mundo al espacio de objetos.'
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
ms.openlocfilehash: 26775e10723a768aa5b526fadfae55414dafa2311b020b1683a99e2b2139dc30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565565"
---
# <a name="worldtoobject4x3"></a>WorldToObject4x3

Matriz para transformar del espacio del mundo al espacio de objetos. Espacio de objeto hace referencia al espacio de la estructura de aceleración de nivel inferior actual.

## <a name="syntax"></a>Sintaxis

```
void WorldToObject4x3();

```




## <a name="remarks"></a>Comentarios

La matriz es una transformación de **la matriz WorldToObject3x4.**

Se puede llamar a esta función desde los siguientes tipos de sombreador de raytracción:

* [**Sombreador de cualquier acierto**](any-hit-shader.md)
* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de intersección**](intersection-shader.md)





## <a name="see-also"></a>Vea también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




