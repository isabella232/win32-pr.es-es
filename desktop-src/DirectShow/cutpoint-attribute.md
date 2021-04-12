---
description: El atributo cutpoint especifica cuándo una transición corta de un origen al siguiente, si la transición se representa como un corte. El valor es relativo al inicio de la transición.
ms.assetid: bdb0b8cd-025f-4b56-9cd4-f71c58ee809a
title: Atributo cutpoint
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd516bd67577906a0a06d8da692ffbd7563ce32f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152361"
---
# <a name="cutpoint-attribute"></a><span data-ttu-id="910d0-104">Atributo cutpoint</span><span class="sxs-lookup"><span data-stu-id="910d0-104">cutpoint Attribute</span></span>

> [!Note]  
> <span data-ttu-id="910d0-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="910d0-105">\[Deprecated.</span></span> <span data-ttu-id="910d0-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="910d0-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="910d0-107">El `cutpoint` atributo especifica cuándo una transición corta de un origen al siguiente, si la transición se representa como un corte.</span><span class="sxs-lookup"><span data-stu-id="910d0-107">The `cutpoint` attribute specifies when a transition cuts from one source to the next, if the transition is rendered as a cut.</span></span> <span data-ttu-id="910d0-108">El valor es relativo al inicio de la transición.</span><span class="sxs-lookup"><span data-stu-id="910d0-108">The value is relative to the start of the transition.</span></span>

## <a name="possible-values"></a><span data-ttu-id="910d0-109">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="910d0-109">Possible Values</span></span>

<span data-ttu-id="910d0-110">Debe ser una cadena con el formato *HH: mm: SS. FF* , donde *HH* = hours, *mm* = minutes, *SS* = seconds y *FF* = fracciones de segundo.</span><span class="sxs-lookup"><span data-stu-id="910d0-110">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="910d0-111">Ejemplo: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="910d0-111">Example: 1:04:30.512.</span></span> <span data-ttu-id="910d0-112">Se pueden omitir las unidades iniciales.</span><span class="sxs-lookup"><span data-stu-id="910d0-112">Leading units can be omitted.</span></span> <span data-ttu-id="910d0-113">Por ejemplo, 3:00 (tres minutos) y 45 (45 segundos) son válidos.</span><span class="sxs-lookup"><span data-stu-id="910d0-113">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="910d0-114">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="910d0-114">Applies To</span></span>

[<span data-ttu-id="910d0-115">**transitorio**</span><span class="sxs-lookup"><span data-stu-id="910d0-115">**transition**</span></span>](transition-element.md)

## <a name="see-also"></a><span data-ttu-id="910d0-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="910d0-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="910d0-117">Atributos XTL</span><span class="sxs-lookup"><span data-stu-id="910d0-117">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="910d0-118">**IAMTimelineTrans::SetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="910d0-118">**IAMTimelineTrans::SetCutPoint**</span></span>](iamtimelinetrans-setcutpoint.md)
</dt> </dl>

 

 



