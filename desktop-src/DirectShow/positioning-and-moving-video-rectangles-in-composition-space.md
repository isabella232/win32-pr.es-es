---
title: Posición y movimiento de rectángulos de vídeo en el espacio de composición
description: Colocación y movimiento de rectángulos de vídeo en el espacio de composición
ms.assetid: 97e7bb24-79f6-4638-a9c4-ac09dbd29be9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96955fc2107036299ab6f530eeda76374a0a0315
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909633"
---
# <a name="position-and-move-video-rectangles-in-composition-space"></a><span data-ttu-id="b86d9-103">Posición y movimiento de rectángulos de vídeo en el espacio de composición</span><span class="sxs-lookup"><span data-stu-id="b86d9-103">Position and move video rectangles in composition space</span></span>

<span data-ttu-id="b86d9-104">Cuando vmr mezcla varios flujos de entrada, coloca cada secuencia dentro de un rectángulo normalizado, denominado "espacio de composición".</span><span class="sxs-lookup"><span data-stu-id="b86d9-104">When the VMR mixes multiple input streams, it positions each stream within a normalized rectangle, called "composition space."</span></span> <span data-ttu-id="b86d9-105">Dentro del espacio de composición, las coordenadas (0.0, 0.0) a (1.0, 1.0) forman el rectángulo de vídeo visible.</span><span class="sxs-lookup"><span data-stu-id="b86d9-105">Within composition space, the coordinates (0.0, 0.0) to (1.0, 1.0) form the visible video rectangle.</span></span> <span data-ttu-id="b86d9-106">Las coordenadas que se encuentran fuera de este rectángulo se recortan.</span><span class="sxs-lookup"><span data-stu-id="b86d9-106">Any coordinates that fall outside of this rectangle are clipped.</span></span>

<span data-ttu-id="b86d9-107">Una aplicación puede realizar efectos especiales al mover, extender y reducir el vídeo de un flujo de entrada, cambiando el rectángulo de destino en el espacio de composición de esa secuencia.</span><span class="sxs-lookup"><span data-stu-id="b86d9-107">An application can perform special effects with moving, stretching, and shrinking the video from an input stream, by changing the destination rectangle in composition space for that stream.</span></span> <span data-ttu-id="b86d9-108">Si el rectángulo especificado tiene un tamaño diferente al del rectángulo de vídeo nativo, el vídeo nativo se verá reducido o se ajustará para ajustarse.</span><span class="sxs-lookup"><span data-stu-id="b86d9-108">If the specified rectangle is a different size than the native video rectangle, the native video will be shrunk or stretched to fit.</span></span> <span data-ttu-id="b86d9-109">El rectángulo de destino se especifica mediante una llamada [**al método IVMRMixerControl::SetOutputRect.**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs)</span><span class="sxs-lookup"><span data-stu-id="b86d9-109">The destination rectangle is specified by calling the [**IVMRMixerControl::SetOutputRect**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) method.</span></span>

<span data-ttu-id="b86d9-110">Por ejemplo, suponga que la secuencia 0 (que corresponde a la patilla 0) contiene la secuencia de vídeo principal y la secuencia 1 (que corresponde a la patilla 1) contiene un vídeo secundario.</span><span class="sxs-lookup"><span data-stu-id="b86d9-110">For example, assume that stream 0 (which corresponds to pin 0) contains the main video stream, and stream 1 (which corresponds to pin 1) contains a secondary video.</span></span> <span data-ttu-id="b86d9-111">La secuencia 1 se puede colocar completamente fuera de la pantalla especificando un rectángulo normalizado de { -1.0f, 0.0f, 0.0f, 1.0f }.</span><span class="sxs-lookup"><span data-stu-id="b86d9-111">Stream 1 can be positioned completely offscreen by specifying a normalized rectangle of { -1.0f, 0.0f, 0.0f, 1.0f }.</span></span> <span data-ttu-id="b86d9-112">A continuación, el flujo 1 se puede mover al área visible modificando los lados izquierdo y derecho del rectángulo en llamadas sucesivas a **SetOutputRect**:</span><span class="sxs-lookup"><span data-stu-id="b86d9-112">Stream 1 can then be moved into the visible area by modifying the left and right sides of the rectangle on successive calls to **SetOutputRect**:</span></span>



| <span data-ttu-id="b86d9-113">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="b86d9-113">Label</span></span> | <span data-ttu-id="b86d9-114">Value</span><span class="sxs-lookup"><span data-stu-id="b86d9-114">Value</span></span> |
|--------|-----------------------------|
| <span data-ttu-id="b86d9-115">Time</span><span class="sxs-lookup"><span data-stu-id="b86d9-115">Time</span></span>   | <span data-ttu-id="b86d9-116">Rectángulo</span><span class="sxs-lookup"><span data-stu-id="b86d9-116">Rectangle</span></span>                   |
| <span data-ttu-id="b86d9-117">t + 0</span><span class="sxs-lookup"><span data-stu-id="b86d9-117">t + 0</span></span>  | <span data-ttu-id="b86d9-118">{ -1.0f, 0.0f, 0.0f, 1.0f }</span><span class="sxs-lookup"><span data-stu-id="b86d9-118">{ -1.0f, 0.0f, 0.0f, 1.0f }</span></span> |
| <span data-ttu-id="b86d9-119">t + 1</span><span class="sxs-lookup"><span data-stu-id="b86d9-119">t + 1</span></span>  | <span data-ttu-id="b86d9-120">{ -0.9f, 0.0f, 0.1f, 1.0f }</span><span class="sxs-lookup"><span data-stu-id="b86d9-120">{ -0.9f, 0.0f, 0.1f, 1.0f }</span></span> |
| <span data-ttu-id="b86d9-121">t + 2</span><span class="sxs-lookup"><span data-stu-id="b86d9-121">t + 2</span></span>  | <span data-ttu-id="b86d9-122">{ -0.8f, 0.0f, 0.2f, 1.0f }</span><span class="sxs-lookup"><span data-stu-id="b86d9-122">{ -0.8f, 0.0f, 0.2f, 1.0f }</span></span> |
| <span data-ttu-id="b86d9-123">...</span><span class="sxs-lookup"><span data-stu-id="b86d9-123">...</span></span>    | <span data-ttu-id="b86d9-124">...</span><span class="sxs-lookup"><span data-stu-id="b86d9-124">...</span></span>                         |
| <span data-ttu-id="b86d9-125">t + 10</span><span class="sxs-lookup"><span data-stu-id="b86d9-125">t + 10</span></span> | <span data-ttu-id="b86d9-126">{ 0.0f, 0.0f, 1.0f, 1.0f }</span><span class="sxs-lookup"><span data-stu-id="b86d9-126">{ 0.0f, 0.0f, 1.0f, 1.0f }</span></span>  |



 

![mover una secuencia de vídeo en el espacio de composición](images/composition-space.png)

<span data-ttu-id="b86d9-128">En el momento t+10, el vídeo de la secuencia 1 es completamente visible.</span><span class="sxs-lookup"><span data-stu-id="b86d9-128">At time t+10, the video from stream 1 is completely visible.</span></span> <span data-ttu-id="b86d9-129">En este ejemplo, el tamaño nativo del flujo 1 se mantiene mientras se movía.</span><span class="sxs-lookup"><span data-stu-id="b86d9-129">In this example, the native size of stream 1 was maintained while it was moving.</span></span> <span data-ttu-id="b86d9-130">También podría extender o reducir el rectángulo para producir efectos interesantes.</span><span class="sxs-lookup"><span data-stu-id="b86d9-130">You could also stretch or shrink the rectangle to produce interesting effects.</span></span> <span data-ttu-id="b86d9-131">También puede voltear el vídeo verticalmente, especificando un valor mayor para la parte superior que la parte inferior, o reflejar el vídeo horizontalmente, especificando un valor mayor para la izquierda que para la derecha.</span><span class="sxs-lookup"><span data-stu-id="b86d9-131">You can also flip the video vertically, by specifying a greater value for the top than the bottom, or mirror the video horizontally, by specifying a greater value for the left than the right.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b86d9-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b86d9-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b86d9-133">Uso del modo de combinación de VMR</span><span class="sxs-lookup"><span data-stu-id="b86d9-133">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



