---
title: RaytracingAccelerationStructure
description: Tipo de recurso que se puede declarar en HLSL y pasarse a TraceRay para indicar el recurso de aceleración de nivel superior creado mediante BuildRaytracingAccelerationStructure.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: 4728e167fe9fbc353c51accaa92d9b9d4086a0bfff3f098f43b93523cd63a792
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123623"
---
# <a name="raytracingaccelerationstructure"></a>RaytracingAccelerationStructure

Tipo de recurso que se puede declarar en HLSL y pasarse a [**TraceRay**](traceray-function.md) para indicar el recurso de aceleración de nivel superior creado mediante **BuildRaytracingAccelerationStructure**. Se enlaza como un SRV de búfer sin formato en una tabla descriptora o un descriptor raíz SRV.  La declaración en HLSL es la siguiente:


```
RaytracingAccelerationStructure MyScene[] : register(t3,space1);
```

En este ejemplo se muestra una matriz de tamaño sin enlazar de estructuras de aceleración, lo que implica que viene de un montón de descriptores, ya que los descriptores raíz no se pueden indexar.

**RaytracingAccelerationStructure es** un recurso opaco sin métodos disponibles para los sombreadores.


 

 




