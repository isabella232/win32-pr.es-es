---
description: El atributo Start especifica la hora de inicio de un objeto, relativa al objeto primario.
ms.assetid: 971de88e-c1ee-4e07-bf8e-3153e4fd11f3
title: Atributo de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b377d0d83c86b981400a784904cf0423f0cca20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688227"
---
# <a name="start-attribute"></a><span data-ttu-id="a232e-103">Atributo de inicio</span><span class="sxs-lookup"><span data-stu-id="a232e-103">start Attribute</span></span>

> [!Note]  
> <span data-ttu-id="a232e-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="a232e-104">\[Deprecated.</span></span> <span data-ttu-id="a232e-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a232e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a232e-106">El `start` atributo especifica la hora de inicio de un objeto, relativa al objeto primario.</span><span class="sxs-lookup"><span data-stu-id="a232e-106">The `start` attribute specifies the start time of an object, relative to the parent object.</span></span>

## <a name="possible-values"></a><span data-ttu-id="a232e-107">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="a232e-107">Possible Values</span></span>

<span data-ttu-id="a232e-108">Debe ser una cadena con el formato *HH: mm: SS. FF* , donde *HH* = hours, *mm* = minutes, *SS* = seconds y *FF* = fracciones de segundo.</span><span class="sxs-lookup"><span data-stu-id="a232e-108">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="a232e-109">Ejemplo: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="a232e-109">Example: 1:04:30.512.</span></span> <span data-ttu-id="a232e-110">Se pueden omitir las unidades iniciales.</span><span class="sxs-lookup"><span data-stu-id="a232e-110">Leading units can be omitted.</span></span> <span data-ttu-id="a232e-111">Por ejemplo, 3:00 (tres minutos) y 45 (45 segundos) son válidos.</span><span class="sxs-lookup"><span data-stu-id="a232e-111">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="a232e-112">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="a232e-112">Applies To</span></span>

<span data-ttu-id="a232e-113">[**clip**](clip-element.md), [**efecto**](effect-element.md), [**transición**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="a232e-113">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="a232e-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="a232e-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a232e-115">Atributos XTL</span><span class="sxs-lookup"><span data-stu-id="a232e-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="a232e-116">**IAMTimelineObj::SetStartStop**</span><span class="sxs-lookup"><span data-stu-id="a232e-116">**IAMTimelineObj::SetStartStop**</span></span>](iamtimelineobj-setstartstop.md)
</dt> </dl>

 

 



