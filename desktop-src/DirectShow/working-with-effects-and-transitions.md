---
description: Trabajar con efectos y transiciones
ms.assetid: 00e97d02-ff43-4e1f-9806-abaeb9288058
title: Trabajar con efectos y transiciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99029269ac86e17246fd641341b071654582bc4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003150"
---
# <a name="working-with-effects-and-transitions"></a><span data-ttu-id="8a36d-103">Trabajar con efectos y transiciones</span><span class="sxs-lookup"><span data-stu-id="8a36d-103">Working with Effects and Transitions</span></span>

<span data-ttu-id="8a36d-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="8a36d-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="8a36d-105">Los efectos modifican un solo clip, una pista o una composición.</span><span class="sxs-lookup"><span data-stu-id="8a36d-105">Effects modify a single clip, track, or composition.</span></span> <span data-ttu-id="8a36d-106">Las transiciones crean seques a partir de una pista o se comparan con otra.</span><span class="sxs-lookup"><span data-stu-id="8a36d-106">Transitions create seques from one track or compositionsto another.</span></span>

<span data-ttu-id="8a36d-107">Los [servicios de edición de DirectShow](directshow-editing-services.md) usan objetos de transformación de DirectX para sus transiciones de vídeo y efectos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8a36d-107">[DirectShow Editing Services](directshow-editing-services.md) uses DirectX Transform objects for its video transitions and video effects.</span></span> <span data-ttu-id="8a36d-108">En el caso de las transiciones de vídeo, use cualquier objeto de transformación de DirectX de dos entradas 2D.</span><span class="sxs-lookup"><span data-stu-id="8a36d-108">For video transitions, use any 2-D two-input DirectX Transform object.</span></span> <span data-ttu-id="8a36d-109">Para los efectos de vídeo, use cualquier objeto de transformación de DirectX de una entrada 2D.</span><span class="sxs-lookup"><span data-stu-id="8a36d-109">For video effects, use any 2-D one-input DirectX Transform object.</span></span> <span data-ttu-id="8a36d-110">Microsoft ya no admite el desarrollo de objetos de transformación de DirectX de terceros.</span><span class="sxs-lookup"><span data-stu-id="8a36d-110">Microsoft no longer supports the development of third-party DirectX Transform objects.</span></span> <span data-ttu-id="8a36d-111">Sin embargo, se proporcionan varios con DirectShow y otros se proporcionan con Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="8a36d-111">However, several are provided with DirectShow and others are provided with Microsoft Internet Explorer.</span></span> <span data-ttu-id="8a36d-112">Para obtener más información acerca de las transiciones proporcionadas con Internet Explorer, consulte [referencia de filtros y transiciones visuales](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms532853(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8a36d-112">For more information about the transitions provided with Internet Explorer, see [Visual Filters and Transitions Reference](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms532853(v=vs.85)).</span></span>

<span data-ttu-id="8a36d-113">En el caso de los efectos de audio, puede usar cualquier filtro de efecto de audio de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="8a36d-113">For audio effects, you can use any DirectShow audio effect filter.</span></span> <span data-ttu-id="8a36d-114">DES también proporciona un [efecto de sobre de volumen](volume-envelope-effect.md) para establecer el volumen en un clip o pista.</span><span class="sxs-lookup"><span data-stu-id="8a36d-114">DES also provides a [Volume Envelope Effect](volume-envelope-effect.md) for setting the volume on a track or clip.</span></span> <span data-ttu-id="8a36d-115">DES no es compatible con las transiciones de audio.</span><span class="sxs-lookup"><span data-stu-id="8a36d-115">DES does not support audio transitions.</span></span>

<span data-ttu-id="8a36d-116">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="8a36d-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="8a36d-117">Agregar objetos Effect y Transition</span><span class="sxs-lookup"><span data-stu-id="8a36d-117">Adding Effect and Transition Objects</span></span>](adding-effect-and-transition-objects.md)
-   [<span data-ttu-id="8a36d-118">Vista previa de efectos y transiciones</span><span class="sxs-lookup"><span data-stu-id="8a36d-118">Previewing Effects and Transitions</span></span>](previewing-effects-and-transitions.md)
-   [<span data-ttu-id="8a36d-119">Enumerar efectos y transiciones</span><span class="sxs-lookup"><span data-stu-id="8a36d-119">Enumerating Effects and Transitions</span></span>](enumerating-effects-and-transitions.md)
-   [<span data-ttu-id="8a36d-120">Establecer propiedades en efectos y transiciones</span><span class="sxs-lookup"><span data-stu-id="8a36d-120">Setting Properties on Effects and Transitions</span></span>](setting-properties-on-effects-and-transitions.md)
-   [<span data-ttu-id="8a36d-121">Dirección de la transición</span><span class="sxs-lookup"><span data-stu-id="8a36d-121">Transition Direction</span></span>](transition-direction.md)

## <a name="related-topics"></a><span data-ttu-id="8a36d-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8a36d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a36d-123">Usar servicios de edición de DirectShow</span><span class="sxs-lookup"><span data-stu-id="8a36d-123">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 
