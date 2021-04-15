---
description: Segmentos de sobre
ms.assetid: 1b59cd1c-7c37-4c70-a36c-2ee1f42b42c5
title: Segmentos de sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bac997667f52ef9bbf14760584889fa16cbbd04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537378"
---
# <a name="envelope-segments"></a><span data-ttu-id="e810e-103">Segmentos de sobre</span><span class="sxs-lookup"><span data-stu-id="e810e-103">Envelope Segments</span></span>

<span data-ttu-id="e810e-104">Una curva de parámetro se compone de uno o varios segmentos de sobre, definidos mediante la estructura de [**\_ \_ segmentos de sobres de MP**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_envelope_segment) .</span><span class="sxs-lookup"><span data-stu-id="e810e-104">A parameter curve consists of one or more envelope segments, defined using the [**MP\_ENVELOPE\_SEGMENT**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_envelope_segment) structure.</span></span> <span data-ttu-id="e810e-105">Esta estructura contiene la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="e810e-105">This structure contains the following information:</span></span>

-   <span data-ttu-id="e810e-106">Horas de inicio y finalización.</span><span class="sxs-lookup"><span data-stu-id="e810e-106">The start and end times.</span></span>
-   <span data-ttu-id="e810e-107">Los valores inicial y final.</span><span class="sxs-lookup"><span data-stu-id="e810e-107">The starting and ending values.</span></span>
-   <span data-ttu-id="e810e-108">El tipo de curva (lineal, cuadrada, etc.).</span><span class="sxs-lookup"><span data-stu-id="e810e-108">The curve type (linear, square, and so forth).</span></span>
-   <span data-ttu-id="e810e-109">Marcas opcionales, descritas en breve.</span><span class="sxs-lookup"><span data-stu-id="e810e-109">Optional flags, described shortly.</span></span>

<span data-ttu-id="e810e-110">El cliente agrega segmentos de sobre a un parámetro llamando al método [**IMediaParams:: AddEnvelope**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-addenvelope) y pasando una matriz de estructuras **de \_ \_ segmentos de sobre de MP** .</span><span class="sxs-lookup"><span data-stu-id="e810e-110">The client adds envelope segments to a parameter by calling the [**IMediaParams::AddEnvelope**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-addenvelope) method and passing in an array of **MP\_ENVELOPE\_SEGMENT** structures.</span></span> <span data-ttu-id="e810e-111">El cliente debe ordenar los segmentos en orden temporal ascendente antes de llamar al método.</span><span class="sxs-lookup"><span data-stu-id="e810e-111">The client should sort the segments into ascending time order before calling the method.</span></span> <span data-ttu-id="e810e-112">A medida que DMO procesa los datos, puede imaginarse el parámetro que viaja sobre cada segmento de sobre, como un automóvil que conduce a una serie de colinas.</span><span class="sxs-lookup"><span data-stu-id="e810e-112">As the DMO processes data, you can imagine the parameter traveling over each envelope segment, like a car driving over a series of hills.</span></span> <span data-ttu-id="e810e-113">El método [**IMediaParams:: GetParam**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-getparam) devuelve el valor más reciente.</span><span class="sxs-lookup"><span data-stu-id="e810e-113">The [**IMediaParams::GetParam**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-getparam) method returns the most recent value.</span></span>

<span data-ttu-id="e810e-114">Dos segmentos adyacentes pueden tener un espacio entre ellos.</span><span class="sxs-lookup"><span data-stu-id="e810e-114">Two adjacent segments can have a gap between them.</span></span> <span data-ttu-id="e810e-115">Durante los huecos, el parámetro conserva su valor anterior, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="e810e-115">During gaps, the parameter retains its previous value, as follows:</span></span>

-   <span data-ttu-id="e810e-116">Antes del primer segmento, el valor es el valor neutro.</span><span class="sxs-lookup"><span data-stu-id="e810e-116">Before the first segment, the value is the neutral value.</span></span>
-   <span data-ttu-id="e810e-117">Entre segmentos, el valor es el valor final del segmento anterior.</span><span class="sxs-lookup"><span data-stu-id="e810e-117">Between segments, the value is the ending value of the previous segment.</span></span>
-   <span data-ttu-id="e810e-118">Después del último segmento, el valor permanece en el valor final del segmento.</span><span class="sxs-lookup"><span data-stu-id="e810e-118">After the last segment, the value remains at the ending value of that segment.</span></span>
-   <span data-ttu-id="e810e-119">Si el cliente vacía DMO, el valor se revierte al valor neutro.</span><span class="sxs-lookup"><span data-stu-id="e810e-119">If the client flushes the DMO, the value reverts to the neutral value.</span></span>

<span data-ttu-id="e810e-120">Puede modificar un segmento estableciendo cualquiera de las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="e810e-120">You can alter a segment by setting either of the following flags:</span></span>

-   <span data-ttu-id="e810e-121">MPF \_ ENVLP \_ Begin \_ CURRENTVAL.</span><span class="sxs-lookup"><span data-stu-id="e810e-121">MPF\_ENVLP\_BEGIN\_CURRENTVAL.</span></span> <span data-ttu-id="e810e-122">DMO usa el valor más reciente del parámetro como el valor inicial del segmento.</span><span class="sxs-lookup"><span data-stu-id="e810e-122">The DMO uses the most recent value of the parameter as the starting value for the segment.</span></span> <span data-ttu-id="e810e-123">Podría ser el valor neutro o el valor final del segmento anterior.</span><span class="sxs-lookup"><span data-stu-id="e810e-123">This might be the neutral value, or the ending value from the previous segment.</span></span> <span data-ttu-id="e810e-124">DMO omite el miembro **valStart** de la estructura del **\_ \_ segmento de sobre de MP** .</span><span class="sxs-lookup"><span data-stu-id="e810e-124">The DMO ignores the **valStart** member of the **MP\_ENVELOPE\_SEGMENT** structure.</span></span>
-   <span data-ttu-id="e810e-125">MPF \_ ENVLP \_ Begin \_ NEUTRALVAL.</span><span class="sxs-lookup"><span data-stu-id="e810e-125">MPF\_ENVLP\_BEGIN\_NEUTRALVAL.</span></span> <span data-ttu-id="e810e-126">DMO usa el valor neutro del parámetro como el valor inicial para el segmento.</span><span class="sxs-lookup"><span data-stu-id="e810e-126">The DMO uses the neutral value of the parameter as the starting value for the segment.</span></span> <span data-ttu-id="e810e-127">Omite **valStart**.</span><span class="sxs-lookup"><span data-stu-id="e810e-127">It ignores **valStart**.</span></span>

<span data-ttu-id="e810e-128">Puede pensar en estas marcas como en la captación del punto inicial del segmento y en moverla hacia arriba o hacia abajo, mientras que el valor final permanece fijo.</span><span class="sxs-lookup"><span data-stu-id="e810e-128">You can think of these flags as grabbing the starting point of the segment and moving it up or down, while the ending value remains fixed.</span></span> <span data-ttu-id="e810e-129">El segmento se "ajustará" en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="e810e-129">The segment will "stretch" accordingly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e810e-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e810e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e810e-131">Parámetros multimedia</span><span class="sxs-lookup"><span data-stu-id="e810e-131">Media Parameters</span></span>](media-parameters.md)
</dt> </dl>

 

 



