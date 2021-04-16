---
description: Composición y disposición en capas
ms.assetid: c1aefd92-b47f-4af1-8299-9ba401ad5fe8
title: Composición y disposición en capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7dce1e1df87b5ffc5c65e9090c6fb7266b972d3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677076"
---
# <a name="composition-and-layering"></a><span data-ttu-id="76ccf-103">Composición y disposición en capas</span><span class="sxs-lookup"><span data-stu-id="76ccf-103">Composition and Layering</span></span>

<span data-ttu-id="76ccf-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="76ccf-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="76ccf-105">En una colección de pistas, la primera pista tiene la prioridad más baja (prioridad 0) y cada pista subsiguiente tiene una prioridad un nivel superior.</span><span class="sxs-lookup"><span data-stu-id="76ccf-105">In a collection of tracks, the first track has the lowest priority (priority 0) and each subsequent track has a priority one level higher.</span></span> <span data-ttu-id="76ccf-106">En cada nivel de prioridad, los clips de origen de esa pista ocultan los clips de origen en las pistas situadas debajo, a menos que esa capa también contenga una transición.</span><span class="sxs-lookup"><span data-stu-id="76ccf-106">At each priority level, the source clips in that track hide the source clips in the tracks below it, unless that layer also contains a transition.</span></span> <span data-ttu-id="76ccf-107">Por lo tanto, puede imaginar que DES realiza varios pasos cuando se representa.</span><span class="sxs-lookup"><span data-stu-id="76ccf-107">Thus you can imagine DES making several passes when it renders.</span></span>

<span data-ttu-id="76ccf-108">En primer lugar, representa la pista 0.</span><span class="sxs-lookup"><span data-stu-id="76ccf-108">First, it renders track 0.</span></span> <span data-ttu-id="76ccf-109">No hay nada "bajo" pista 0, por lo que las regiones vacías se representan como una imagen en negro sólido.</span><span class="sxs-lookup"><span data-stu-id="76ccf-109">There is nothing "under" Track 0, so empty regions are rendered as a solid black image.</span></span> <span data-ttu-id="76ccf-110">Las transiciones de este nivel se producen entre la imagen negra y la pista 0, o viceversa.</span><span class="sxs-lookup"><span data-stu-id="76ccf-110">Transitions in this layer occur between the black image and track 0 or vice versa.</span></span> <span data-ttu-id="76ccf-111">DES coloca la pista 1 encima de la pista 0, lo que genera cualquier transición entre las dos pistas.</span><span class="sxs-lookup"><span data-stu-id="76ccf-111">DES lays track 1 on top of track 0, generating any transitions between the two tracks.</span></span> <span data-ttu-id="76ccf-112">El resultado es el compuesto de las dos pistas.</span><span class="sxs-lookup"><span data-stu-id="76ccf-112">The result is the composite of the two tracks.</span></span> <span data-ttu-id="76ccf-113">Después, coloca el seguimiento 2 en esta composición.</span><span class="sxs-lookup"><span data-stu-id="76ccf-113">Next, it places track 2 onto this composite.</span></span> <span data-ttu-id="76ccf-114">Las transiciones en este nivel se producen entre el compuesto y el seguimiento 2.</span><span class="sxs-lookup"><span data-stu-id="76ccf-114">Transitions at this layer occur between the composite and track 2.</span></span> <span data-ttu-id="76ccf-115">El proceso continúa hasta que se coloca la última pista (prioridad más alta).</span><span class="sxs-lookup"><span data-stu-id="76ccf-115">The process continues until the last (highest-priority) track is put down.</span></span>

<span data-ttu-id="76ccf-116">Cuando varias pistas están compuestas juntas, se comportan como una sola pista (denominada pista virtual).</span><span class="sxs-lookup"><span data-stu-id="76ccf-116">When several tracks are composited together, they behave like a single track (called a virtual track).</span></span> <span data-ttu-id="76ccf-117">El objeto de composición encapsula este comportamiento, lo que permite realizar transiciones complejas.</span><span class="sxs-lookup"><span data-stu-id="76ccf-117">The composition object encapsulates this behavior, making complex transitions possible.</span></span> <span data-ttu-id="76ccf-118">Por ejemplo, un clip de vídeo puede borrarse en un segundo clip, mientras que el compuesto (ambos clips más el barrido) se atenúa hasta un tercer clip.</span><span class="sxs-lookup"><span data-stu-id="76ccf-118">For example, one video clip can wipe to a second clip, while the composite (both clips plus the wipe) fades to a third clip.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76ccf-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="76ccf-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76ccf-120">Introducción con servicios de edición de DirectShow</span><span class="sxs-lookup"><span data-stu-id="76ccf-120">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



