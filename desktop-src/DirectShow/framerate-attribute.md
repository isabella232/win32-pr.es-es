---
description: El atributo de velocidad de fotogramas especifica una velocidad de fotogramas por segundo.
ms.assetid: 541a86e3-7736-4de4-b509-f8d61ef9bc58
title: velocidad de fotogramas (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1af5deb8ae2a851b328fcd6d9ffa3923328708
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997828"
---
# <a name="framerate-attribute-directshow"></a><span data-ttu-id="075aa-103">velocidad de fotogramas (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="075aa-103">framerate Attribute (DirectShow)</span></span>

> [!Note]  
> <span data-ttu-id="075aa-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="075aa-104">\[Deprecated.</span></span> <span data-ttu-id="075aa-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="075aa-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="075aa-106">El `framerate` atributo especifica una velocidad de fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="075aa-106">The `framerate` attribute specifies a framerate, in frames per second.</span></span>

## <a name="possible-values"></a><span data-ttu-id="075aa-107">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="075aa-107">Possible Values</span></span>

<span data-ttu-id="075aa-108">Valor de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="075aa-108">Floating-point value.</span></span> <span data-ttu-id="075aa-109">El valor debe incluir el cero inicial delante de la posición decimal.</span><span class="sxs-lookup"><span data-stu-id="075aa-109">The value must include the leading zero before the decimal place.</span></span> <span data-ttu-id="075aa-110">Por ejemplo, 0,3, no. 3.</span><span class="sxs-lookup"><span data-stu-id="075aa-110">For example, 0.3, not .3.</span></span> <span data-ttu-id="075aa-111">No use más de siete dígitos decimales.</span><span class="sxs-lookup"><span data-stu-id="075aa-111">Do not use more than seven decimal digits.</span></span>

## <a name="applies-to"></a><span data-ttu-id="075aa-112">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="075aa-112">Applies To</span></span>

<span data-ttu-id="075aa-113">[**clip**](clip-element.md), [**Grupo**](group-element.md), [**escala de tiempo**](timeline-element.md)</span><span class="sxs-lookup"><span data-stu-id="075aa-113">[**clip**](clip-element.md), [**group**](group-element.md), [**timeline**](timeline-element.md)</span></span>

## <a name="remarks"></a><span data-ttu-id="075aa-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="075aa-114">Remarks</span></span>

<span data-ttu-id="075aa-115">En el caso del elemento **clip** , este atributo especifica la velocidad de fotogramas predeterminada del origen.</span><span class="sxs-lookup"><span data-stu-id="075aa-115">For the **clip** element, this attribute specifies the default frame rate of the source.</span></span> <span data-ttu-id="075aa-116">Especifique el atributo para las secuencias de andDIB de imágenes fijas.</span><span class="sxs-lookup"><span data-stu-id="075aa-116">Specify the attribute for still images andDIB sequences.</span></span> <span data-ttu-id="075aa-117">En el caso de una imagen fija, establezca el valor en cero.</span><span class="sxs-lookup"><span data-stu-id="075aa-117">For a still image, set the value to zero.</span></span> <span data-ttu-id="075aa-118">En el caso de una secuencia DIB, use un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="075aa-118">For a DIB sequence, use a nonzero value.</span></span> <span data-ttu-id="075aa-119">El valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="075aa-119">The default value is zero.</span></span>

<span data-ttu-id="075aa-120">En el caso del elemento **Group** , este atributo especifica la velocidad de fotogramas de salida para el grupo.</span><span class="sxs-lookup"><span data-stu-id="075aa-120">For the **group** element, this attribute specifies the output frame rate for the group.</span></span>

<span data-ttu-id="075aa-121">En el caso del elemento **Timeline** , este atributo especifica la velocidad de fotogramas predeterminada para todos los grupos.</span><span class="sxs-lookup"><span data-stu-id="075aa-121">For the **timeline** element, this attribute specifies the default frame rate for all groups.</span></span>

## <a name="see-also"></a><span data-ttu-id="075aa-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="075aa-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="075aa-123">Atributos XTL</span><span class="sxs-lookup"><span data-stu-id="075aa-123">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="075aa-124">**IAMTimelineSrc::SetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="075aa-124">**IAMTimelineSrc::SetDefaultFPS**</span></span>](iamtimelinesrc-setdefaultfps.md)
</dt> <dt>

[<span data-ttu-id="075aa-125">**IAMTimelineGroup::SetOutputFPS**</span><span class="sxs-lookup"><span data-stu-id="075aa-125">**IAMTimelineGroup::SetOutputFPS**</span></span>](iamtimelinegroup-setoutputfps.md)
</dt> <dt>

[<span data-ttu-id="075aa-126">**IAMTimeline::SetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="075aa-126">**IAMTimeline::SetDefaultFPS**</span></span>](iamtimeline-setdefaultfps.md)
</dt> </dl>

 

 



