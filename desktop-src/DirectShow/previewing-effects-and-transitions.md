---
description: Vista previa de efectos y transiciones
ms.assetid: aa13bd57-69c1-462c-86e3-64026a03bfc4
title: Vista previa de efectos y transiciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25506b7e50fe83c2e4fca7bb4166748ec43d33dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152522"
---
# <a name="previewing-effects-and-transitions"></a><span data-ttu-id="0564c-103">Vista previa de efectos y transiciones</span><span class="sxs-lookup"><span data-stu-id="0564c-103">Previewing Effects and Transitions</span></span>

<span data-ttu-id="0564c-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="0564c-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="0564c-105">Algunos efectos y transiciones tardan mucho tiempo en representarse.</span><span class="sxs-lookup"><span data-stu-id="0564c-105">Some effects and transitions take a relatively long time to render.</span></span> <span data-ttu-id="0564c-106">Durante la versión preliminar, esto puede hacer que el vídeo sea entrecortado o no sincronizado con el audio.</span><span class="sxs-lookup"><span data-stu-id="0564c-106">During preview this can cause the video to become choppy or out of sync with the audio.</span></span> <span data-ttu-id="0564c-107">Puede aumentar la velocidad de la versión preliminar deshabilitando los efectos o las transiciones:</span><span class="sxs-lookup"><span data-stu-id="0564c-107">You can increase preview speed by disabling effects or transitions:</span></span>

-   <span data-ttu-id="0564c-108">Para deshabilitar todos los efectos, llame a [**IAMTimeline:: EnableEffects**](iamtimeline-enableeffects.md).</span><span class="sxs-lookup"><span data-stu-id="0564c-108">To disable all effects, call [**IAMTimeline::EnableEffects**](iamtimeline-enableeffects.md).</span></span>
-   <span data-ttu-id="0564c-109">Para deshabilitar todas las transiciones, llame a [**IAMTimeline:: EnableTransitions**](iamtimeline-enabletransitions.md).</span><span class="sxs-lookup"><span data-stu-id="0564c-109">To disable all transitions, call [**IAMTimeline::EnableTransitions**](iamtimeline-enabletransitions.md).</span></span>
-   <span data-ttu-id="0564c-110">Para deshabilitar una transición determinada, llame a [**IAMTimelineTrans:: SetCutsOnly**](iamtimelinetrans-setcutsonly.md).</span><span class="sxs-lookup"><span data-stu-id="0564c-110">To disable a particular transition, call [**IAMTimelineTrans::SetCutsOnly**](iamtimelinetrans-setcutsonly.md).</span></span>

<span data-ttu-id="0564c-111">Cuando se deshabilitan los efectos, no se representan durante la vista previa.</span><span class="sxs-lookup"><span data-stu-id="0564c-111">When effects are disabled, they are not rendered during preview.</span></span> <span data-ttu-id="0564c-112">Cuando se deshabilita una transición, se representa como un corte de salto.</span><span class="sxs-lookup"><span data-stu-id="0564c-112">When a transition is disabled, it is rendered as a jump cut.</span></span> <span data-ttu-id="0564c-113">Todavía se produce el segue entre pistas, pero el efecto visual no se representa.</span><span class="sxs-lookup"><span data-stu-id="0564c-113">The segue between tracks still occurs, but the visual effect is not rendered.</span></span>

<span data-ttu-id="0564c-114">Si no se puede representar un efecto o una transición, el motor de representación sustituye a un efecto o transición predeterminados.</span><span class="sxs-lookup"><span data-stu-id="0564c-114">If an effect or transition cannot be rendered, the render engine substitutes a default effect or transition.</span></span> <span data-ttu-id="0564c-115">Llame al método [**IAMTimeline:: SetDefaultEffect**](iamtimeline-setdefaulteffect.md) para establecer el efecto predeterminado y el método [**IAMTimeline:: SetDefaultTransition**](iamtimeline-setdefaulttransition.md) para establecer la transición predeterminada.</span><span class="sxs-lookup"><span data-stu-id="0564c-115">Call the [**IAMTimeline::SetDefaultEffect**](iamtimeline-setdefaulteffect.md) method to set the default effect, and the [**IAMTimeline::SetDefaultTransition**](iamtimeline-setdefaulttransition.md) method to set the default transition.</span></span> <span data-ttu-id="0564c-116">Si no especifica un valor predeterminado, o si el que especifica también produce un error, DES utiliza su propio valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0564c-116">If you do not specify a default, or if the one you specify also causes an error, DES uses its own default.</span></span>

> [!Note]  
> <span data-ttu-id="0564c-117">También puede mejorar la calidad de la vista previa aumentando la cantidad de almacenamiento en búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="0564c-117">You can also improve preview quality by increasing the amount of frame buffering.</span></span> <span data-ttu-id="0564c-118">Vea [**IAMTimelineGroup:: SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md).</span><span class="sxs-lookup"><span data-stu-id="0564c-118">See [**IAMTimelineGroup::SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0564c-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0564c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0564c-120">Trabajar con efectos y transiciones</span><span class="sxs-lookup"><span data-stu-id="0564c-120">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



