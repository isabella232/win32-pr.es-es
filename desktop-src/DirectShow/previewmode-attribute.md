---
description: El atributo previewmode especifica el modo de vista previa para el grupo. Si el valor es TRUE, los fotogramas podrían quitarse durante la vista previa. De lo contrario, no se quita ningún fotograma durante la vista previa. El valor predeterminado es TRUE.
ms.assetid: 5e4f4407-b43e-4b31-8676-1e12b6b70034
title: Atributo previewmode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3b589b279a11b8ec329641ea2522a6a46dfa0e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422888"
---
# <a name="previewmode-attribute"></a><span data-ttu-id="4f3fb-106">Atributo previewmode</span><span class="sxs-lookup"><span data-stu-id="4f3fb-106">previewmode Attribute</span></span>

> [!Note]  
> <span data-ttu-id="4f3fb-107">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-107">\[Deprecated.</span></span> <span data-ttu-id="4f3fb-108">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4f3fb-108">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4f3fb-109">El `previewmode` atributo especifica el modo de vista previa para el grupo.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-109">The `previewmode` attribute specifies the preview mode for the group.</span></span> <span data-ttu-id="4f3fb-110">Si el valor es **true**, los fotogramas podrían quitarse durante la vista previa.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-110">If the value is **TRUE**, frames might be dropped during preview.</span></span> <span data-ttu-id="4f3fb-111">De lo contrario, no se quita ningún fotograma durante la vista previa.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-111">Otherwise, no frames are dropped during preview.</span></span> <span data-ttu-id="4f3fb-112">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-112">The default value is **TRUE**.</span></span>

## <a name="possible-values"></a><span data-ttu-id="4f3fb-113">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="4f3fb-113">Possible Values</span></span>

<span data-ttu-id="4f3fb-114">Los siguientes valores se definen como TRUE: y, Y, t, T, 1.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-114">The following values are defined as TRUE: y, Y, t, T, 1.</span></span> <span data-ttu-id="4f3fb-115">Los valores siguientes se definen como FALSE: n, N, f, F, 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="4f3fb-115">The following values are defined as FALSE: n, N, f, F, 0 (zero).</span></span>

## <a name="applies-to"></a><span data-ttu-id="4f3fb-116">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="4f3fb-116">Applies To</span></span>

[<span data-ttu-id="4f3fb-117">**agrupamiento**</span><span class="sxs-lookup"><span data-stu-id="4f3fb-117">**group**</span></span>](group-element.md)

## <a name="remarks"></a><span data-ttu-id="4f3fb-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f3fb-118">Remarks</span></span>

<span data-ttu-id="4f3fb-119">En la configuración predeterminada, se quitan los fotogramas mientras se realiza una vista previa de los efectos o las transiciones lentas para mantener el vídeo sincronizado con el audio.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-119">Under the default setting, frames are dropped while previewing slow effects or transitions, to keep the video synchronized with the audio.</span></span> <span data-ttu-id="4f3fb-120">Es posible que el vídeo parezca entrecortado como resultado.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-120">The video might look choppy as a result.</span></span> <span data-ttu-id="4f3fb-121">Si se establece este atributo en **false** , cada fotograma se representará durante la versión preliminar, lo que podría dar lugar a que el vídeo deje de estar sincronizado con el audio.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-121">Setting this attribute to **FALSE** forces every frame to render during preview, possibly resulting in the video becoming out of sync with the audio.</span></span> <span data-ttu-id="4f3fb-122">Los fotogramas nunca se quitan cuando se escribe en un archivo.</span><span class="sxs-lookup"><span data-stu-id="4f3fb-122">Frames are never dropped when writing to a file.</span></span>

## <a name="see-also"></a><span data-ttu-id="4f3fb-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f3fb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f3fb-124">Atributos XTL</span><span class="sxs-lookup"><span data-stu-id="4f3fb-124">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="4f3fb-125">**IAMTimelineGroup::SetPreviewMode**</span><span class="sxs-lookup"><span data-stu-id="4f3fb-125">**IAMTimelineGroup::SetPreviewMode**</span></span>](iamtimelinegroup-setpreviewmode.md)
</dt> </dl>

 

 



