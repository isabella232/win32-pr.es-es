---
description: Composición
ms.assetid: b5f607b2-9cca-4eef-9c63-d2015bd10469
title: Composición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e030e02ab77ec54e1e340d72db7210665d649bfb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677075"
---
# <a name="composition"></a><span data-ttu-id="79597-103">Composición</span><span class="sxs-lookup"><span data-stu-id="79597-103">Composition</span></span>

> [!Note]  
> <span data-ttu-id="79597-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="79597-104">\[Deprecated.</span></span> <span data-ttu-id="79597-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="79597-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="79597-106">El objeto de composición es un contenedor para las pistas.</span><span class="sxs-lookup"><span data-stu-id="79597-106">The composition object is a container for tracks.</span></span> <span data-ttu-id="79597-107">También puede contener otras composiciones (para el anidamiento de pistas), efectos y transiciones.</span><span class="sxs-lookup"><span data-stu-id="79597-107">It can also hold other compositions (for nesting of tracks), effects, and transitions.</span></span> <span data-ttu-id="79597-108">Para crear este objeto, llame al método [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) .</span><span class="sxs-lookup"><span data-stu-id="79597-108">To create this object, call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span>

<span data-ttu-id="79597-109">El objeto de composición expone las siguientes interfaces:</span><span class="sxs-lookup"><span data-stu-id="79597-109">The composition object exposes the following interfaces:</span></span>

-   [<span data-ttu-id="79597-110">**IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="79597-110">**IAMTimelineComp**</span></span>](iamtimelinecomp.md)
-   [<span data-ttu-id="79597-111">**IAMTimelineEffectable**</span><span class="sxs-lookup"><span data-stu-id="79597-111">**IAMTimelineEffectable**</span></span>](iamtimelineeffectable.md)
-   [<span data-ttu-id="79597-112">**IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="79597-112">**IAMTimelineObj**</span></span>](iamtimelineobj.md)
-   [<span data-ttu-id="79597-113">**IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="79597-113">**IAMTimelineTransable**</span></span>](iamtimelinetransable.md)
-   [<span data-ttu-id="79597-114">**IAMTimelineVirtualTrack**</span><span class="sxs-lookup"><span data-stu-id="79597-114">**IAMTimelineVirtualTrack**</span></span>](iamtimelinevirtualtrack.md)

## <a name="related-topics"></a><span data-ttu-id="79597-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="79597-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79597-116">Modelo de escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="79597-116">The Timeline Model</span></span>](the-timeline-model.md)
</dt> <dt>

[<span data-ttu-id="79597-117">Construir una escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="79597-117">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



