---
title: RaytracingAccelerationStructure
description: Un tipo de recurso que se puede declarar en HLSL y pasarse a TraceRay para indicar el recurso de aceleración de nivel superior creado con BuildRaytracingAccelerationStructure.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: beb6f5e397126223e9c0e6959e16a6cca3145517
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "105707519"
---
# <a name="raytracingaccelerationstructure"></a>RaytracingAccelerationStructure

Un tipo de recurso que se puede declarar en HLSL y pasarse a [**TraceRay**](traceray-function.md) para indicar el recurso de aceleración de nivel superior creado con **BuildRaytracingAccelerationStructure**. Se enlaza como un SRV de búfer sin procesar en una tabla de descriptores o en un descriptor de raíz SRV.  La declaración en HLSL es la siguiente:


```
RaytracingAccelerationStructure MyScene[] : register(t3,space1);
```

En este ejemplo se muestra una matriz de tamaño sin límite de estructuras de aceleración, lo que implica que procede de un montón de descriptores, ya que los descriptores raíz no se pueden indizar.

**RaytracingAccelerationStructure** es un recurso opaco sin métodos disponibles para los sombreadores.


 

 




