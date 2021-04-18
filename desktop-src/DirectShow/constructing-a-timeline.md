---
description: Construir una escala de tiempo
ms.assetid: 4909f797-d296-4c9f-83fb-543e48bbe75d
title: Construir una escala de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c16b1134eb92b3e3ac5a0f1919d7c4a2736b206
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422991"
---
# <a name="constructing-a-timeline"></a><span data-ttu-id="33b75-103">Construir una escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="33b75-103">Constructing a Timeline</span></span>

<span data-ttu-id="33b75-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="33b75-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="33b75-105">En este artículo se describe cómo construir una escala de tiempo en los [servicios de edición de DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="33b75-105">This article describes how to construct a timeline in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="33b75-106">Presenta una aplicación de consola de ejemplo que crea una escala de tiempo y la representa.</span><span class="sxs-lookup"><span data-stu-id="33b75-106">It presents an example console application that creates a timeline and renders it.</span></span> <span data-ttu-id="33b75-107">La escala de tiempo es mínima y consta de un único grupo de vídeos con un clip de origen, pero muestra la mayoría de los conceptos necesarios para crear escalas de tiempo más complejas.</span><span class="sxs-lookup"><span data-stu-id="33b75-107">The timeline is minimal, consisting of a single video group with one source clip, but it demonstrates most of the concepts needed to create more complex timelines.</span></span>

<span data-ttu-id="33b75-108">Este artículo contiene los siguientes temas.</span><span class="sxs-lookup"><span data-stu-id="33b75-108">This article contains the following topics.</span></span>

-   [<span data-ttu-id="33b75-109">Crear objetos Timeline</span><span class="sxs-lookup"><span data-stu-id="33b75-109">Creating Timeline Objects</span></span>](creating-timeline-objects.md)
-   [<span data-ttu-id="33b75-110">Crear grupos, composiciones y pistas</span><span class="sxs-lookup"><span data-stu-id="33b75-110">Creating Groups, Compositions, and Tracks</span></span>](creating-groups-compositions-and-tracks.md)
-   [<span data-ttu-id="33b75-111">Establecer el tipo de medio de grupo</span><span class="sxs-lookup"><span data-stu-id="33b75-111">Setting the Group Media Type</span></span>](setting-the-group-media-type.md)
-   [<span data-ttu-id="33b75-112">Agregar un origen</span><span class="sxs-lookup"><span data-stu-id="33b75-112">Adding a Source</span></span>](adding-a-source.md)
-   [<span data-ttu-id="33b75-113">Crear una escala de tiempo: código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="33b75-113">Creating a Timeline: Example Code</span></span>](creating-a-timeline--example-code.md)

## <a name="related-topics"></a><span data-ttu-id="33b75-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="33b75-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33b75-115">Usar servicios de edición de DirectShow</span><span class="sxs-lookup"><span data-stu-id="33b75-115">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



