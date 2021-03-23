---
title: Contadores, consultas y predication
description: Los contadores de salida de flujo y UAV funcionan en Direct3D 12 en un método similar a Direct3D 11, aunque ahora la aplicación debe asignar la memoria para los contadores, el controlador no lo hace.
ms.assetid: 8BDDAFEF-57D4-4EF5-BB0C-6C96AF557A45
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314c01b05ac31e5d5f8348b775c8955ae382f5ed
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104549170"
---
# <a name="counters-queries-and-predication"></a><span data-ttu-id="19a4f-103">Contadores, consultas y predication</span><span class="sxs-lookup"><span data-stu-id="19a4f-103">Counters, queries, and predication</span></span>

<span data-ttu-id="19a4f-104">En este tema se describen los contadores de salida de flujo, los contadores de UAV, las consultas y predication.</span><span class="sxs-lookup"><span data-stu-id="19a4f-104">This topic covers stream-output counters, UAV counters, queries, and predication.</span></span>

<span data-ttu-id="19a4f-105">Los contadores de salida de flujo y UAV funcionan en Direct3D 12 en un método similar a Direct3D 11, aunque ahora la aplicación debe asignar la memoria para los contadores, el controlador no lo hace.</span><span class="sxs-lookup"><span data-stu-id="19a4f-105">Stream output and UAV counters operate in Direct3D 12 in a similar method to Direct3D 11, although now memory for the counters must be allocated by the app, the driver does not do it.</span></span> <span data-ttu-id="19a4f-106">Las consultas en Direct3D 12 son más diferentes de las de Direct3D 11, con la adición de barreras y otros procesos que eliminan la necesidad de algunos tipos de consulta.</span><span class="sxs-lookup"><span data-stu-id="19a4f-106">Queries in Direct3D 12 are more different from those in Direct3D 11, with the addition of fences and other processes that remove the need for some query types.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="19a4f-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="19a4f-107">In this section</span></span>



| <span data-ttu-id="19a4f-108">Tema</span><span class="sxs-lookup"><span data-stu-id="19a4f-108">Topic</span></span>                                                           | <span data-ttu-id="19a4f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="19a4f-109">Description</span></span>                                                                                                                                                                                  |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19a4f-110">Contadores de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="19a4f-110">Stream Output Counters</span></span>](stream-output-counters.md)<br/> | <span data-ttu-id="19a4f-111">La salida de flujo es la capacidad de la GPU de escribir vértices en un búfer.</span><span class="sxs-lookup"><span data-stu-id="19a4f-111">Stream output is the ability of the GPU to write vertices to a buffer.</span></span> <span data-ttu-id="19a4f-112">Los contadores de salida de flujo supervisan el progreso.</span><span class="sxs-lookup"><span data-stu-id="19a4f-112">The stream output counters monitor progress.</span></span><br/>                                                               |
| [<span data-ttu-id="19a4f-113">Contadores de UAV</span><span class="sxs-lookup"><span data-stu-id="19a4f-113">UAV Counters</span></span>](uav-counters.md)<br/>                     | <span data-ttu-id="19a4f-114">Los contadores de UAV se pueden usar para asociar un contador atómico de 32 bits con un desordenado-Access-View (UAV).</span><span class="sxs-lookup"><span data-stu-id="19a4f-114">UAV counters can be used to associate a 32-bit atomic counter with an unordered-access-view (UAV).</span></span><br/>                                                                                |
| [<span data-ttu-id="19a4f-115">Consultas</span><span class="sxs-lookup"><span data-stu-id="19a4f-115">Queries</span></span>](queries.md)<br/>                               | <span data-ttu-id="19a4f-116">En Direct3D 12, las consultas se agrupan en matrices de consultas llamadas un montón de consultas.</span><span class="sxs-lookup"><span data-stu-id="19a4f-116">In Direct3D 12, queries are grouped into arrays of queries called a query heap.</span></span> <span data-ttu-id="19a4f-117">Un montón de consulta tiene un tipo que define los tipos válidos de consultas que se pueden usar con ese montón.</span><span class="sxs-lookup"><span data-stu-id="19a4f-117">A query heap has a type which defines the valid types of queries that can be used with that heap.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="19a4f-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="19a4f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19a4f-119">Medición del rendimiento</span><span class="sxs-lookup"><span data-stu-id="19a4f-119">Performance Measurement</span></span>](performance-measurement.md)
</dt> </dl>

 

 





