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
# <a name="raytracingaccelerationstructure"></a><span data-ttu-id="809f1-103">RaytracingAccelerationStructure</span><span class="sxs-lookup"><span data-stu-id="809f1-103">RaytracingAccelerationStructure</span></span>

<span data-ttu-id="809f1-104">Un tipo de recurso que se puede declarar en HLSL y pasarse a [**TraceRay**](traceray-function.md) para indicar el recurso de aceleración de nivel superior creado con **BuildRaytracingAccelerationStructure**.</span><span class="sxs-lookup"><span data-stu-id="809f1-104">A resource type that can be declared in HLSL and passed into [**TraceRay**](traceray-function.md) to indicate the top-level acceleration resource built using **BuildRaytracingAccelerationStructure**.</span></span> <span data-ttu-id="809f1-105">Se enlaza como un SRV de búfer sin procesar en una tabla de descriptores o en un descriptor de raíz SRV.</span><span class="sxs-lookup"><span data-stu-id="809f1-105">It is bound as a raw buffer SRV in a descriptor table or root descriptor SRV.</span></span>  <span data-ttu-id="809f1-106">La declaración en HLSL es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="809f1-106">The declaration in HLSL is as follows:</span></span>


```
RaytracingAccelerationStructure MyScene[] : register(t3,space1);
```

<span data-ttu-id="809f1-107">En este ejemplo se muestra una matriz de tamaño sin límite de estructuras de aceleración, lo que implica que procede de un montón de descriptores, ya que los descriptores raíz no se pueden indizar.</span><span class="sxs-lookup"><span data-stu-id="809f1-107">This example shows an unbounded size array of acceleration structures, which implies coming from a descriptor heap since root descriptors can’t be indexed.</span></span>

<span data-ttu-id="809f1-108">**RaytracingAccelerationStructure** es un recurso opaco sin métodos disponibles para los sombreadores.</span><span class="sxs-lookup"><span data-stu-id="809f1-108">**RaytracingAccelerationStructure** is an opaque resource with no methods available to shaders.</span></span>


 

 




