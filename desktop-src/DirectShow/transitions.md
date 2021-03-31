---
description: Transiciones
ms.assetid: 432db77f-c3fa-4234-bbce-cf17d8878b99
title: Transiciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01fef1cd888293ad83ab1ba9f05ab4bb83ddafa9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912881"
---
# <a name="transitions"></a><span data-ttu-id="7bc25-103">Transiciones</span><span class="sxs-lookup"><span data-stu-id="7bc25-103">Transitions</span></span>

<span data-ttu-id="7bc25-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="7bc25-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="7bc25-105">Una transición es una forma de segue de una pista de vídeo a otra, con un efecto visual como un fundido o un barrido.</span><span class="sxs-lookup"><span data-stu-id="7bc25-105">A transition is a way to segue from one video track to another, using a visual effect such as a fade or a wipe.</span></span> <span data-ttu-id="7bc25-106">En la ilustración siguiente se muestra una escala de tiempo con una transición:</span><span class="sxs-lookup"><span data-stu-id="7bc25-106">The following illustration shows a timeline with a transition:</span></span>

![escala de tiempo con transición](images/timeline3.png)

<span data-ttu-id="7bc25-108">El objeto de transición está en el seguimiento 1 y representa una transición de la pista 0 a la del seguimiento 1.</span><span class="sxs-lookup"><span data-stu-id="7bc25-108">The transition object is on track 1, and it represents a transition from track 0 to track 1.</span></span> <span data-ttu-id="7bc25-109">Al inicio de la transición, el vídeo representado está completo de la pista 0 (origen A).</span><span class="sxs-lookup"><span data-stu-id="7bc25-109">At the start of the transition, the rendered video is entirely from Track 0 (source A).</span></span> <span data-ttu-id="7bc25-110">Al final, el vídeo está por completo de la pista 1 (origen C).</span><span class="sxs-lookup"><span data-stu-id="7bc25-110">At the end, the video is entirely from Track 1 (source C).</span></span> <span data-ttu-id="7bc25-111">En, la salida pasa del origen a al origen C. Por ejemplo, en una transición de atenuación, un origen se atenúa progresivamente hasta el otro.</span><span class="sxs-lookup"><span data-stu-id="7bc25-111">In between, the output transitions from source A to source C. For example, in a fade transition, one source progressively fades to the other.</span></span> <span data-ttu-id="7bc25-112">El resultado final es esquematizados a lo largo de la parte inferior de la ilustración.</span><span class="sxs-lookup"><span data-stu-id="7bc25-112">The final output is schematized along the bottom of the illustration.</span></span>

<span data-ttu-id="7bc25-113">Las transiciones no se pueden superponer en el tiempo dentro de la misma pista, pero puede crear transiciones que se superpongan mediante el objeto de composición, como se describe en [composición y disposición en capas](composition-and-layering.md).</span><span class="sxs-lookup"><span data-stu-id="7bc25-113">Transitions cannot overlap in time within the same track, but you can create overlapping transitions by using the composition object, as described in [Composition and Layering](composition-and-layering.md).</span></span>

<span data-ttu-id="7bc25-114">Una transición tiene una dirección.</span><span class="sxs-lookup"><span data-stu-id="7bc25-114">A transition has a direction.</span></span> <span data-ttu-id="7bc25-115">De forma predeterminada, se inicia a partir de la pista de menor prioridad (origen A, en el ejemplo anterior) y termina en la pista de prioridad más alta (origen C).</span><span class="sxs-lookup"><span data-stu-id="7bc25-115">By default, it starts from the lower priority track (source A, in the previous example.) and ends at the higher-priority track (source C).</span></span> <span data-ttu-id="7bc25-116">Entre, el vídeo es una combinación de los dos orígenes.</span><span class="sxs-lookup"><span data-stu-id="7bc25-116">In between, the video is a mixture of the two sources.</span></span> <span data-ttu-id="7bc25-117">Sin embargo, puede especificar el comportamiento opuesto, tal como se muestra en la siguiente ilustración:</span><span class="sxs-lookup"><span data-stu-id="7bc25-117">However, you can specify the opposite behavior, as shown in the following illustration:</span></span>

![ntrack con dos transiciones](images/fade.png)

<span data-ttu-id="7bc25-119">En este caso, la primera transición de la pista 0 atenúa el seguimiento 1, que es el comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7bc25-119">Here, the first transition fades from track 0 fades track 1, which is the default behavior.</span></span> <span data-ttu-id="7bc25-120">La segunda transición vuelve de la pista 1 a la pista 0.</span><span class="sxs-lookup"><span data-stu-id="7bc25-120">The second transition fades from track 1 back to Track 0.</span></span> <span data-ttu-id="7bc25-121">Tenga en cuenta que ambas transiciones se encuentran en el seguimiento 1.</span><span class="sxs-lookup"><span data-stu-id="7bc25-121">Note that both transitions are located on track 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bc25-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7bc25-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bc25-123">Introducción con servicios de edición de DirectShow</span><span class="sxs-lookup"><span data-stu-id="7bc25-123">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[<span data-ttu-id="7bc25-124">Transiciones y efectos</span><span class="sxs-lookup"><span data-stu-id="7bc25-124">Transitions and Effects</span></span>](transitions-and-effects.md)
</dt> <dt>

[<span data-ttu-id="7bc25-125">Trabajar con efectos y transiciones</span><span class="sxs-lookup"><span data-stu-id="7bc25-125">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



