---
title: RaytracingAccelerationStructure
description: Tipo de recurso que se puede declarar en HLSL y pasarse a TraceRay para indicar el recurso de aceleración de nivel superior creado mediante BuildRaytracingAccelerationStructure.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: beb6f5e397126223e9c0e6959e16a6cca3145517
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072905"
---
# <a name="raytracingaccelerationstructure"></a>RaytracingAccelerationStructure

Tipo de recurso que se puede declarar en HLSL y pasarse a [**TraceRay**](traceray-function.md) para indicar el recurso de aceleración de nivel superior creado mediante **BuildRaytracingAccelerationStructure**. Se enlaza como un SRV de búfer sin formato en una tabla de descriptores o un descriptor raíz SRV.  La declaración en HLSL es la siguiente:


```
RaytracingAccelerationStructure MyScene[] : register(t3,space1);
```

En este ejemplo se muestra una matriz de tamaño sin enlazar de estructuras de aceleración, lo que implica que viene de un montón de descriptores, ya que los descriptores raíz no se pueden indexar.

**RaytracingAccelerationStructure** es un recurso opaco sin métodos disponibles para los sombreadores.


 

 




