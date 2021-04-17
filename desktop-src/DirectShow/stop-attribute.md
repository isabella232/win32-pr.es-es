---
description: El atributo STOP especifica la hora de detención de un objeto, relativa al objeto primario.
ms.assetid: 1bda3472-abda-4672-9b82-311163e56fe0
title: detener atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6deb3f2a422cb8100da32c0427caf6436e72fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688215"
---
# <a name="stop-attribute"></a><span data-ttu-id="82872-103">detener atributo</span><span class="sxs-lookup"><span data-stu-id="82872-103">stop Attribute</span></span>

> [!Note]  
> <span data-ttu-id="82872-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="82872-104">\[Deprecated.</span></span> <span data-ttu-id="82872-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="82872-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="82872-106">El `stop` atributo especifica la hora de detención de un objeto, relativa al objeto primario.</span><span class="sxs-lookup"><span data-stu-id="82872-106">The `stop` attribute specifies the stop time of an object, relative to the parent object.</span></span>

## <a name="possible-values"></a><span data-ttu-id="82872-107">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="82872-107">Possible Values</span></span>

<span data-ttu-id="82872-108">Debe ser una cadena con el formato *HH: mm: SS. FF* , donde *HH* = hours, *mm* = minutes, *SS* = seconds y *FF* = fracciones de segundo.</span><span class="sxs-lookup"><span data-stu-id="82872-108">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="82872-109">Ejemplo: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="82872-109">Example: 1:04:30.512.</span></span> <span data-ttu-id="82872-110">Se pueden omitir las unidades iniciales.</span><span class="sxs-lookup"><span data-stu-id="82872-110">Leading units can be omitted.</span></span> <span data-ttu-id="82872-111">Por ejemplo, 3:00 (tres minutos) y 45 (45 segundos) son válidos.</span><span class="sxs-lookup"><span data-stu-id="82872-111">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="82872-112">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="82872-112">Applies To</span></span>

<span data-ttu-id="82872-113">[**clip**](clip-element.md), [**efecto**](effect-element.md), [**transición**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="82872-113">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="82872-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="82872-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82872-115">Atributos XTL</span><span class="sxs-lookup"><span data-stu-id="82872-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="82872-116">**IAMTimelineObj::SetStartStop**</span><span class="sxs-lookup"><span data-stu-id="82872-116">**IAMTimelineObj::SetStartStop**</span></span>](iamtimelineobj-setstartstop.md)
</dt> </dl>

 

 



