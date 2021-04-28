---
description: 'ObjectToWorld4x3: matriz para transformar del espacio de objetos al espacio del mundo.'
ms.assetid: ''
title: ObjectToWorld4x3
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectToWorld4x3
api_type:
- NA
ms.openlocfilehash: bc91c6e98aceb13af3f589f873a4b96c2b1843c4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098303"
---
# <a name="objecttoworld4x3"></a>ObjectToWorld4x3

Matriz para transformar del espacio del objeto al espacio del mundo. Espacio de objeto hace referencia al espacio de la estructura de aceleración de nivel inferior actual.

## <a name="syntax"></a>Sintaxis

```
void ObjectToWorld4x3();

```




## <a name="remarks"></a>Comentarios

La matriz es una transformación de **la matriz ObjectToWorld3x4.**

Se puede llamar a esta función desde los siguientes tipos de sombreador:

* [**Sombreador de cualquier acierto**](any-hit-shader.md)
* [**Sombreador del acierto más cercano**](closest-hit-shader.md)
* [**Sombreador de intersección**](intersection-shader.md)





## <a name="see-also"></a>Consulte también

<dl> <dt>

[Reference de HLSL de Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




