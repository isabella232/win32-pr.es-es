---
description: 'ObjectToWorld3x4: matriz para la transformación del espacio de objetos al espacio del mundo.'
ms.assetid: ''
title: ObjectToWorld3x4
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectToWorld3x4
api_type:
- NA
ms.openlocfilehash: 947676c25bd5cac50749c737afd7e4ff75426c0a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107743"
---
# <a name="objecttoworld3x4"></a>ObjectToWorld3x4

Matriz para transformar del espacio de objetos al espacio del mundo. Espacio de objeto hace referencia al espacio de la estructura de aceleración de nivel inferior actual.

## <a name="syntax"></a>Sintaxis

```
void ObjectToWorld3x4();

```




## <a name="remarks"></a>Comentarios

La matriz es una retorsión de **la matriz ObjectToWorld4x3.**

Se puede llamar a esta función desde los siguientes tipos de sombreador de raytracción:

* [**Sombreador de cualquier acierto**](any-hit-shader.md)
* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de intersección**](intersection-shader.md)





## <a name="see-also"></a>Consulte también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




