---
description: Dirección de la transición
ms.assetid: d18525de-bb75-4c5e-b387-cfec7ba03df7
title: Dirección de la transición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01d43ec4258d2f23c8b8961e3e1b8fd3d554b057
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104550246"
---
# <a name="transition-direction"></a><span data-ttu-id="a900c-103">Dirección de la transición</span><span class="sxs-lookup"><span data-stu-id="a900c-103">Transition Direction</span></span>

<span data-ttu-id="a900c-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="a900c-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="a900c-105">Una transición va desde la entrada a a la entrada B y desde el tiempo t ₀ hasta t ₁.</span><span class="sxs-lookup"><span data-stu-id="a900c-105">A transition goes from input A to input B, and from time t₀ to t₁.</span></span> <span data-ttu-id="a900c-106">Por lo tanto, la *Dirección* de una transición puede significar una de estas dos cosas:</span><span class="sxs-lookup"><span data-stu-id="a900c-106">Therefore, the *direction* of a transition can mean one of two things:</span></span>

-   <span data-ttu-id="a900c-107">Asignación de las capas de la escala de tiempo a las entradas.</span><span class="sxs-lookup"><span data-stu-id="a900c-107">The mapping of timeline layers to inputs.</span></span>
-   <span data-ttu-id="a900c-108">La progresión a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="a900c-108">The progression over time.</span></span>

<span data-ttu-id="a900c-109">El primero es la *dirección de entrada* y el segundo es la *dirección de progreso*.</span><span class="sxs-lookup"><span data-stu-id="a900c-109">The first is the *input direction*, and the second is the *progress direction*.</span></span> <span data-ttu-id="a900c-110">Puede controlar ambas direcciones.</span><span class="sxs-lookup"><span data-stu-id="a900c-110">You can control both directions.</span></span>

-   <span data-ttu-id="a900c-111">Dirección de entrada: de forma predeterminada, una transición va del compuesto de los niveles de prioridad inferior a la capa que contiene la transición.</span><span class="sxs-lookup"><span data-stu-id="a900c-111">Input direction: By default, a transition goes from the composite of the lower-priority layers to the layer that contains the transition.</span></span> <span data-ttu-id="a900c-112">Para invertir esta dirección, llame al método [**IAMTimelineTrans:: SetSwapInputs**](iamtimelinetrans-setswapinputs.md) .</span><span class="sxs-lookup"><span data-stu-id="a900c-112">To reverse this direction, call the [**IAMTimelineTrans::SetSwapInputs**](iamtimelinetrans-setswapinputs.md) method.</span></span>
-   <span data-ttu-id="a900c-113">Dirección del progreso: la mayoría de las transiciones admiten una propiedad de **progreso** estándar, que especifica qué porcentaje de la transición se refleja en la salida en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="a900c-113">Progress direction: Most transitions support a standard **Progress** property, which specifies what percentage of the transition is reflected in the output at a given moment.</span></span> <span data-ttu-id="a900c-114">De forma predeterminada, el valor de la propiedad **Progress** va de 0,0 a 1,0 durante la transición.</span><span class="sxs-lookup"><span data-stu-id="a900c-114">By default, the value of the **Progress** property goes from 0.0 to 1.0 over the duration of the transition.</span></span> <span data-ttu-id="a900c-115">Para invertir el progreso, establezca la propiedad **Progress** en go de 1,0 a 0,0.</span><span class="sxs-lookup"><span data-stu-id="a900c-115">To reverse the progress, set the **Progress** property to go from 1.0 to 0.0.</span></span>

<span data-ttu-id="a900c-116">En el diagrama siguiente se ilustra la diferencia entre la dirección de entrada y la dirección de progreso.</span><span class="sxs-lookup"><span data-stu-id="a900c-116">The following diagram illustrates the difference between input direction and progress direction.</span></span> <span data-ttu-id="a900c-117">Muestra cuatro variaciones en una transición de [borrado de SMPTE](smpte-wipe-transition.md) estándar.</span><span class="sxs-lookup"><span data-stu-id="a900c-117">It shows four variations on a standard [SMPTE Wipe](smpte-wipe-transition.md) transition.</span></span>

![instrucciones de borrado](images/wipedirections.png)

<span data-ttu-id="a900c-119">La transición reside en el seguimiento 1.</span><span class="sxs-lookup"><span data-stu-id="a900c-119">The transition resides on track 1.</span></span> <span data-ttu-id="a900c-120">De forma predeterminada, el borrado se realiza de izquierda a derecha y de seguimiento de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="a900c-120">By default, the wipe goes from left to right and from track 0 to track 1.</span></span> <span data-ttu-id="a900c-121">El intercambio de entradas hace que el barrido pase de la pista 1 a la pista 0, pero de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="a900c-121">Swapping inputs causes the wipe to go from track 1 to track 0, but still from left to right.</span></span> <span data-ttu-id="a900c-122">Invertir el progreso hace que la transición pase de derecha a izquierda.</span><span class="sxs-lookup"><span data-stu-id="a900c-122">Reversing the progress makes the transition go from right to left.</span></span> <span data-ttu-id="a900c-123">Puede combinar ambos, tal como se muestra en el extremo izquierdo.</span><span class="sxs-lookup"><span data-stu-id="a900c-123">You can combine both, as shown on the far left.</span></span>

<span data-ttu-id="a900c-124">Para obtener más información sobre el modo en que DES representa las transiciones, consulte [el modelo de escala de tiempo](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="a900c-124">For more information about how DES renders transitions, see [The Timeline Model](the-timeline-model.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a900c-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a900c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a900c-126">Trabajar con efectos y transiciones</span><span class="sxs-lookup"><span data-stu-id="a900c-126">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



