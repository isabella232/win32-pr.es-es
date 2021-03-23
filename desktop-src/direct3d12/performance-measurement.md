---
title: Contadores, consultas y medición de rendimiento
description: En las secciones siguientes se describen las características que se usan en las pruebas y mejoras de rendimiento, como consultas, contadores, temporización y predication.
ms.assetid: C7AEF1A0-36FB-4026-9CCF-ED0206961A58
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf316978f3dd0928692f378dd8d72b8453ad0aae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105034"
---
# <a name="counters-queries-and-performance-measurement"></a><span data-ttu-id="bd298-103">Contadores, consultas y medición de rendimiento</span><span class="sxs-lookup"><span data-stu-id="bd298-103">Counters, Queries and Performance Measurement</span></span>

<span data-ttu-id="bd298-104">En las secciones siguientes se describen las características que se usan en las pruebas y mejoras de rendimiento, como consultas, contadores, temporización y predication.</span><span class="sxs-lookup"><span data-stu-id="bd298-104">The following sections describe features for use in performance testing and improvement, such as queries, counters, timing, and predication.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bd298-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="bd298-105">In this section</span></span>



| <span data-ttu-id="bd298-106">Tema</span><span class="sxs-lookup"><span data-stu-id="bd298-106">Topic</span></span>                                                                                                 | <span data-ttu-id="bd298-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd298-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd298-108">Contadores de salida de streaming, contadores UAV, consultas y Predication</span><span class="sxs-lookup"><span data-stu-id="bd298-108">Stream-Output Counters, UAV Counters, Queries, and Predication</span></span>](counters-and-queries.md)<br/> | <span data-ttu-id="bd298-109">Los contadores de salida de flujo y UAV funcionan en Direct3D 12 en un método similar a Direct3D 11, aunque ahora la aplicación debe asignar la memoria para los contadores, el controlador no lo hace.</span><span class="sxs-lookup"><span data-stu-id="bd298-109">Stream output and UAV counters operate in Direct3D 12 in a similar method to Direct3D 11, although now memory for the counters must be allocated by the app, the driver does not do it.</span></span> <span data-ttu-id="bd298-110">Las consultas en Direct3D 12 son más diferentes de las de Direct3D 11, con la adición de barreras y otros procesos que eliminan la necesidad de algunos tipos de consulta.</span><span class="sxs-lookup"><span data-stu-id="bd298-110">Queries in Direct3D 12 are more different from those in Direct3D 11, with the addition of fences and other processes that remove the need for some query types.</span></span><br/> |
| [<span data-ttu-id="bd298-111">Control de tiempo</span><span class="sxs-lookup"><span data-stu-id="bd298-111">Timing</span></span>](timing.md)<br/>                                                                       | <span data-ttu-id="bd298-112">En esta sección se explica cómo consultar las marcas de tiempo y calibrar los contadores de GPU y de marca de tiempo de la CPU.</span><span class="sxs-lookup"><span data-stu-id="bd298-112">This section covers querying timestamps, and calibrating the GPU and CPU timestamp counters.</span></span><br/>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="bd298-113">Predication</span><span class="sxs-lookup"><span data-stu-id="bd298-113">Predication</span></span>](predication.md)<br/>                                                             | <span data-ttu-id="bd298-114">Predication es una característica que permite que la GPU en lugar de la CPU determine no dibujar, copiar o enviar un objeto.</span><span class="sxs-lookup"><span data-stu-id="bd298-114">Predication is a feature that enables the GPU rather than the CPU to determine to not draw, copy or dispatch an object.</span></span><br/>                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="bd298-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bd298-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd298-116">Guía de programación de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="bd298-116">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> </dl>

 

 





