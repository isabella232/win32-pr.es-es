---
title: Colocar y mover rectángulos de vídeo en el espacio de composición
description: Colocar y mover rectángulos de vídeo en el espacio de composición
ms.assetid: 97e7bb24-79f6-4638-a9c4-ac09dbd29be9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef766d1ae739e46a2c56bfab81b4243c9dcf6f10
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677111"
---
# <a name="position-and-move-video-rectangles-in-composition-space"></a><span data-ttu-id="a66f5-103">Colocar y mover rectángulos de vídeo en el espacio de composición</span><span class="sxs-lookup"><span data-stu-id="a66f5-103">Position and move video rectangles in composition space</span></span>

<span data-ttu-id="a66f5-104">Cuando el VMR mezcla varios flujos de entrada, coloca cada flujo dentro de un rectángulo normalizado, denominado "espacio de composición".</span><span class="sxs-lookup"><span data-stu-id="a66f5-104">When the VMR mixes multiple input streams, it positions each stream within a normalized rectangle, called "composition space."</span></span> <span data-ttu-id="a66f5-105">Dentro del espacio de composición, las coordenadas (0,0, 0,0) a (1,0, 1,0) forman el rectángulo de vídeo visible.</span><span class="sxs-lookup"><span data-stu-id="a66f5-105">Within composition space, the coordinates (0.0, 0.0) to (1.0, 1.0) form the visible video rectangle.</span></span> <span data-ttu-id="a66f5-106">Se recortan las coordenadas que se encuentran fuera de este rectángulo.</span><span class="sxs-lookup"><span data-stu-id="a66f5-106">Any coordinates that fall outside of this rectangle are clipped.</span></span>

<span data-ttu-id="a66f5-107">Una aplicación puede realizar efectos especiales con mover, ajustar y reducir el vídeo de un flujo de entrada, cambiando el rectángulo de destino en el espacio de composición de esa secuencia.</span><span class="sxs-lookup"><span data-stu-id="a66f5-107">An application can perform special effects with moving, stretching, and shrinking the video from an input stream, by changing the destination rectangle in composition space for that stream.</span></span> <span data-ttu-id="a66f5-108">Si el rectángulo especificado tiene un tamaño diferente que el del rectángulo de vídeo nativo, el vídeo nativo se reducirá o se ajustará para ajustarse.</span><span class="sxs-lookup"><span data-stu-id="a66f5-108">If the specified rectangle is a different size than the native video rectangle, the native video will be shrunk or stretched to fit.</span></span> <span data-ttu-id="a66f5-109">El rectángulo de destino se especifica mediante una llamada al método [**IVMRMixerControl:: SetOutputRect**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) .</span><span class="sxs-lookup"><span data-stu-id="a66f5-109">The destination rectangle is specified by calling the [**IVMRMixerControl::SetOutputRect**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) method.</span></span>

<span data-ttu-id="a66f5-110">Por ejemplo, supongamos que el flujo 0 (que corresponde a la patilla 0) contiene la secuencia de vídeo principal y que el flujo 1 (que corresponde a la patilla 1) contiene un vídeo secundario.</span><span class="sxs-lookup"><span data-stu-id="a66f5-110">For example, assume that stream 0 (which corresponds to pin 0) contains the main video stream, and stream 1 (which corresponds to pin 1) contains a secondary video.</span></span> <span data-ttu-id="a66f5-111">El flujo 1 se puede colocar completamente fuera de la cadena especificando un rectángulo normalizado de {-1,0 f, 0.0 f, 0.0 f, 1.0 f}.</span><span class="sxs-lookup"><span data-stu-id="a66f5-111">Stream 1 can be positioned completely offscreen by specifying a normalized rectangle of { -1.0f, 0.0f, 0.0f, 1.0f }.</span></span> <span data-ttu-id="a66f5-112">A continuación, el flujo 1 se puede pasar al área visible modificando los lados izquierdo y derecho del rectángulo en las sucesivas llamadas a **SetOutputRect**:</span><span class="sxs-lookup"><span data-stu-id="a66f5-112">Stream 1 can then be moved into the visible area by modifying the left and right sides of the rectangle on successive calls to **SetOutputRect**:</span></span>



|        |                             |
|--------|-----------------------------|
| <span data-ttu-id="a66f5-113">Hora</span><span class="sxs-lookup"><span data-stu-id="a66f5-113">Time</span></span>   | <span data-ttu-id="a66f5-114">Rectángulo</span><span class="sxs-lookup"><span data-stu-id="a66f5-114">Rectangle</span></span>                   |
| <span data-ttu-id="a66f5-115">t + 0</span><span class="sxs-lookup"><span data-stu-id="a66f5-115">t + 0</span></span>  | <span data-ttu-id="a66f5-116">{-1,0 f, 0.0 f, 0.0 f, 1,0 f}</span><span class="sxs-lookup"><span data-stu-id="a66f5-116">{ -1.0f, 0.0f, 0.0f, 1.0f }</span></span> |
| <span data-ttu-id="a66f5-117">t + 1</span><span class="sxs-lookup"><span data-stu-id="a66f5-117">t + 1</span></span>  | <span data-ttu-id="a66f5-118">{-0.9 f, 0.0 f, 0.1 f, 1,0 f}</span><span class="sxs-lookup"><span data-stu-id="a66f5-118">{ -0.9f, 0.0f, 0.1f, 1.0f }</span></span> |
| <span data-ttu-id="a66f5-119">t + 2</span><span class="sxs-lookup"><span data-stu-id="a66f5-119">t + 2</span></span>  | <span data-ttu-id="a66f5-120">{-0,8 f, 0.0 f, 0,2 f, 1,0 f}</span><span class="sxs-lookup"><span data-stu-id="a66f5-120">{ -0.8f, 0.0f, 0.2f, 1.0f }</span></span> |
| <span data-ttu-id="a66f5-121">...</span><span class="sxs-lookup"><span data-stu-id="a66f5-121">...</span></span>    | <span data-ttu-id="a66f5-122">...</span><span class="sxs-lookup"><span data-stu-id="a66f5-122">...</span></span>                         |
| <span data-ttu-id="a66f5-123">t + 10</span><span class="sxs-lookup"><span data-stu-id="a66f5-123">t + 10</span></span> | <span data-ttu-id="a66f5-124">{0.0 f, 0.0 f, 1.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="a66f5-124">{ 0.0f, 0.0f, 1.0f, 1.0f }</span></span>  |



 

![mover una secuencia de vídeo en el espacio de composición](images/composition-space.png)

<span data-ttu-id="a66f5-126">En el momento t + 10, el vídeo de la secuencia 1 está completamente visible.</span><span class="sxs-lookup"><span data-stu-id="a66f5-126">At time t+10, the video from stream 1 is completely visible.</span></span> <span data-ttu-id="a66f5-127">En este ejemplo, el tamaño nativo de la secuencia 1 se mantuvo mientras se estaba moviendo.</span><span class="sxs-lookup"><span data-stu-id="a66f5-127">In this example, the native size of stream 1 was maintained while it was moving.</span></span> <span data-ttu-id="a66f5-128">También puede ampliar o reducir el rectángulo para producir efectos interesantes.</span><span class="sxs-lookup"><span data-stu-id="a66f5-128">You could also stretch or shrink the rectangle to produce interesting effects.</span></span> <span data-ttu-id="a66f5-129">También puede voltear el vídeo verticalmente; para ello, especifique un valor mayor en la parte superior a la parte inferior, o bien refleje el vídeo horizontalmente; para ello, especifique un valor mayor para el lado izquierdo.</span><span class="sxs-lookup"><span data-stu-id="a66f5-129">You can also flip the video vertically, by specifying a greater value for the top than the bottom, or mirror the video horizontally, by specifying a greater value for the left than the right.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a66f5-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a66f5-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a66f5-131">Usar el modo de mezcla de VMR</span><span class="sxs-lookup"><span data-stu-id="a66f5-131">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



