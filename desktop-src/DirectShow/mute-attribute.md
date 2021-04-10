---
description: El atributo MUTE especifica el estado de silencio del objeto.
ms.assetid: 9a6dccf5-ae00-4ee0-8df3-bf817fe1a164
title: silenciar atributo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f4e43feb16d75312cedd0caf5c217af2dd71332
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152462"
---
# <a name="mute-attribute"></a><span data-ttu-id="d16b8-103">silenciar atributo</span><span class="sxs-lookup"><span data-stu-id="d16b8-103">mute Attribute</span></span>

> [!Note]  
> <span data-ttu-id="d16b8-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="d16b8-104">\[Deprecated.</span></span> <span data-ttu-id="d16b8-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d16b8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d16b8-106">El `mute` atributo especifica el estado de silencio del objeto.</span><span class="sxs-lookup"><span data-stu-id="d16b8-106">The `mute` attribute specifies the object's mute state.</span></span> <span data-ttu-id="d16b8-107">Si el valor es **true**, no se representan el objeto ni sus elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="d16b8-107">If the value is **TRUE**, neither the object nor its children are rendered.</span></span> <span data-ttu-id="d16b8-108">Si el valor es **false**, el objeto se representa y sus elementos secundarios se representan según su propio estado de silencio.</span><span class="sxs-lookup"><span data-stu-id="d16b8-108">If the value is **FALSE**, the object is rendered, and its children are rendered according to their own mute state.</span></span> <span data-ttu-id="d16b8-109">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="d16b8-109">The default value is **FALSE**.</span></span>

## <a name="possible-values"></a><span data-ttu-id="d16b8-110">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="d16b8-110">Possible Values</span></span>

<span data-ttu-id="d16b8-111">Los siguientes valores se definen como TRUE: y, Y, t, T, 1.</span><span class="sxs-lookup"><span data-stu-id="d16b8-111">The following values are defined as TRUE: y, Y, t, T, 1.</span></span> <span data-ttu-id="d16b8-112">Los valores siguientes se definen como FALSE: n, N, f, F, 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="d16b8-112">The following values are defined as FALSE: n, N, f, F, 0 (zero).</span></span>

## <a name="applies-to"></a><span data-ttu-id="d16b8-113">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="d16b8-113">Applies To</span></span>

<span data-ttu-id="d16b8-114">[**clip**](clip-element.md), [**compuesto**](composite-element.md), [**efecto**](effect-element.md), [**Grupo**](group-element.md), [**escala de tiempo**](timeline-element.md), [**transición**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="d16b8-114">[**clip**](clip-element.md), [**composite**](composite-element.md), [**effect**](effect-element.md), [**group**](group-element.md), [**timeline**](timeline-element.md), [**transition**](transition-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="d16b8-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="d16b8-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d16b8-116">Atributos XTL</span><span class="sxs-lookup"><span data-stu-id="d16b8-116">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="d16b8-117">**IAMTimelineObj::SetMuted**</span><span class="sxs-lookup"><span data-stu-id="d16b8-117">**IAMTimelineObj::SetMuted**</span></span>](iamtimelineobj-setmuted.md)
</dt> </dl>

 

 



