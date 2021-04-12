---
description: El atributo swapinputs especifica si se deben intercambiar las entradas de la transición. Si el valor es TRUE, se intercambian las entradas. El valor predeterminado es FALSE.
ms.assetid: 2b8d95ec-2c6c-4bd8-83e9-7f72770449b5
title: Atributo swapinputs
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27e2f02c642283e90b994bcd1bfa9e05076a7bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361412"
---
# <a name="swapinputs-attribute"></a><span data-ttu-id="6c623-105">Atributo swapinputs</span><span class="sxs-lookup"><span data-stu-id="6c623-105">swapinputs Attribute</span></span>

> [!Note]  
> <span data-ttu-id="6c623-106">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="6c623-106">\[Deprecated.</span></span> <span data-ttu-id="6c623-107">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6c623-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6c623-108">El `swapinputs` atributo especifica si se deben intercambiar las entradas de la transición.</span><span class="sxs-lookup"><span data-stu-id="6c623-108">The `swapinputs` attribute specifies whether to swap transition inputs.</span></span> <span data-ttu-id="6c623-109">Si el valor es **true**, se intercambian las entradas.</span><span class="sxs-lookup"><span data-stu-id="6c623-109">If the value is **TRUE**, the inputs are swapped.</span></span> <span data-ttu-id="6c623-110">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="6c623-110">The default value is **FALSE**.</span></span>

## <a name="possible-values"></a><span data-ttu-id="6c623-111">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="6c623-111">Possible Values</span></span>

<span data-ttu-id="6c623-112">Los siguientes valores se definen como TRUE: y, Y, t, T, 1.</span><span class="sxs-lookup"><span data-stu-id="6c623-112">The following values are defined as TRUE: y, Y, t, T, 1.</span></span> <span data-ttu-id="6c623-113">Los valores siguientes se definen como FALSE: n, N, f, F, 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="6c623-113">The following values are defined as FALSE: n, N, f, F, 0 (zero).</span></span>

## <a name="applies-to"></a><span data-ttu-id="6c623-114">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="6c623-114">Applies To</span></span>

[<span data-ttu-id="6c623-115">**transitorio**</span><span class="sxs-lookup"><span data-stu-id="6c623-115">**transition**</span></span>](transition-element.md)

## <a name="remarks"></a><span data-ttu-id="6c623-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c623-116">Remarks</span></span>

<span data-ttu-id="6c623-117">De forma predeterminada, una transición continúa desde el compuesto de todas las capas de prioridad más baja hasta la capa en la que reside la transición.</span><span class="sxs-lookup"><span data-stu-id="6c623-117">By default, a transition proceeds from the composite of all lower-priority layers to the layer on which the transition resides.</span></span> <span data-ttu-id="6c623-118">Si el `swapinputs` atributo es 1, esta dirección se invierte.</span><span class="sxs-lookup"><span data-stu-id="6c623-118">If the `swapinputs` attribute is 1, this direction is reversed.</span></span> <span data-ttu-id="6c623-119">Para obtener más información sobre el modelo de capas que usa DES, vea [el modelo Timeline](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="6c623-119">For more information about the layering model used by DES, see [The Timeline Model](the-timeline-model.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6c623-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c623-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c623-121">Atributos XTL</span><span class="sxs-lookup"><span data-stu-id="6c623-121">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="6c623-122">**IAMTimelineTrans::SetSwapInputs**</span><span class="sxs-lookup"><span data-stu-id="6c623-122">**IAMTimelineTrans::SetSwapInputs**</span></span>](iamtimelinetrans-setswapinputs.md)
</dt> </dl>

 

 



