---
description: 'ObjectToWorld3x4: matriz para transformar de espacio de objeto a espacio mundial.'
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
ms.openlocfilehash: d58737e50fb7d173c84c4b38f6b91b9b6bfbc9d3b5a88c498344dadd5e94e73a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123754"
---
# <a name="objecttoworld3x4"></a>ObjectToWorld3x4

Matriz para transformar del espacio de objetos al espacio del mundo. Espacio de objeto hace referencia al espacio de la estructura de aceleración de nivel inferior actual.

## <a name="syntax"></a>Sintaxis

```
void ObjectToWorld3x4();

```




## <a name="remarks"></a>Comentarios

La matriz es una transformación de **la matriz ObjectToWorld4x3.**

Se puede llamar a esta función desde los siguientes tipos de sombreador:

* [**Sombreador de cualquier acierto**](any-hit-shader.md)
* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de intersección**](intersection-shader.md)





## <a name="see-also"></a>Vea también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




