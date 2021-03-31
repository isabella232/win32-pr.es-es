---
title: Elemento de vídeo
description: Elemento de vídeo
ms.assetid: 817e0d2e-cbc3-4b61-81c0-876104125f39
keywords:
- Aspectos de Windows Media Player, elemento de vídeo
- aspectos, elemento de vídeo
- Elemento de vídeo
- referencia de las máscaras, elemento de vídeo
- elementos, vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd8ab6bd014d2968483120fd1dd98804905faa4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776639"
---
# <a name="video-element"></a><span data-ttu-id="a268c-108">Elemento de vídeo</span><span class="sxs-lookup"><span data-stu-id="a268c-108">VIDEO Element</span></span>

<span data-ttu-id="a268c-109">El elemento de **vídeo** proporciona una manera de manipular una ventana de vídeo en una máscara, mediante los siguientes atributos y eventos.</span><span class="sxs-lookup"><span data-stu-id="a268c-109">The **VIDEO** element provides a way to manipulate a video window in a skin, using the following attributes and events.</span></span> <span data-ttu-id="a268c-110">También se proporciona un elemento de **vídeo** predefinido para mayor comodidad.</span><span class="sxs-lookup"><span data-stu-id="a268c-110">A predefined **VIDEO** element is also provided for convenience.</span></span>

<span data-ttu-id="a268c-111">El elemento de **vídeo** admite los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="a268c-111">The **VIDEO** element supports the following attributes.</span></span>



| <span data-ttu-id="a268c-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="a268c-112">Attribute</span></span>                                            | <span data-ttu-id="a268c-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="a268c-113">Description</span></span>                                                                                                                                                                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a268c-114">backgroundColor</span><span class="sxs-lookup"><span data-stu-id="a268c-114">backgroundColor</span></span>](video-backgroundcolor.md)         | <span data-ttu-id="a268c-115">Especifica o recupera el color de fondo del control de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a268c-115">Specifies or retrieves the background color of the Video control.</span></span>                                                                                                                                                                        |
| [<span data-ttu-id="a268c-116">cursor</span><span class="sxs-lookup"><span data-stu-id="a268c-116">cursor</span></span>](video-cursor.md)                           | <span data-ttu-id="a268c-117">Especifica o recupera el valor del cursor que se utiliza cuando el mouse está sobre un área en la que se hace clic del vídeo.</span><span class="sxs-lookup"><span data-stu-id="a268c-117">Specifies or retrieves the cursor value that is used when the mouse is over a clickable area of the video.</span></span>                                                                                                                               |
| [<span data-ttu-id="a268c-118">Completa</span><span class="sxs-lookup"><span data-stu-id="a268c-118">fullScreen</span></span>](video-fullscreen.md)                   | <span data-ttu-id="a268c-119">Especifica o recupera un valor que indica si el vídeo se muestra en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="a268c-119">Specifies or retrieves a value indicating whether the video is displayed in full-screen mode.</span></span> <span data-ttu-id="a268c-120">Solo se puede establecer en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="a268c-120">Can only be set at run time.</span></span>                                                                                                               |
| [<span data-ttu-id="a268c-121">maintainAspectRatio</span><span class="sxs-lookup"><span data-stu-id="a268c-121">maintainAspectRatio</span></span>](video-maintainaspectratio.md) | <span data-ttu-id="a268c-122">Especifica o recupera un valor que indica si el vídeo mantendrá la relación de aspecto cuando se intenta ajustar el ancho y el alto definidos para el control.</span><span class="sxs-lookup"><span data-stu-id="a268c-122">Specifies or retrieves a value indicating whether the video will maintain the aspect ratio when trying to fit within the width and height defined for the control.</span></span>                                                                       |
| [<span data-ttu-id="a268c-123">shrinkToFit</span><span class="sxs-lookup"><span data-stu-id="a268c-123">shrinkToFit</span></span>](video-shrinktofit.md)                 | <span data-ttu-id="a268c-124">Especifica o recupera un valor que indica si el vídeo se reducirá al ancho y al alto definidos para el control de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a268c-124">Specifies or retrieves a value indicating whether the video will shrink to the width and height defined for the Video control.</span></span>                                                                                                           |
| [<span data-ttu-id="a268c-125">stretchToFit</span><span class="sxs-lookup"><span data-stu-id="a268c-125">stretchToFit</span></span>](video-stretchtofit.md)               | <span data-ttu-id="a268c-126">Especifica o recupera un valor que indica si el vídeo se ajustará al ancho y al alto definidos para el control de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a268c-126">Specifies or retrieves a value indicating whether the video will stretch itself to the width and height defined for the Video control.</span></span>                                                                                                   |
| [<span data-ttu-id="a268c-127">Herramienta</span><span class="sxs-lookup"><span data-stu-id="a268c-127">toolTip</span></span>](video-tooltip.md)                         | <span data-ttu-id="a268c-128">Especifica o recupera el texto de información sobre herramientas para la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a268c-128">Specifies or retrieves the ToolTip text for the video window.</span></span>                                                                                                                                                                            |
| [<span data-ttu-id="a268c-129">sin ventana</span><span class="sxs-lookup"><span data-stu-id="a268c-129">windowless</span></span>](video-windowless.md)                   | <span data-ttu-id="a268c-130">Especifica o recupera un valor que indica si el control de vídeo se va a mostrar o no en ventanas; es decir, si todo el rectángulo del control será visible en todo momento o se puede recortar.</span><span class="sxs-lookup"><span data-stu-id="a268c-130">Specifies or retrieves a value indicating whether the Video control will be windowed or windowless; that is, whether the entire rectangle of the control will be visible at all times or can be clipped.</span></span> <span data-ttu-id="a268c-131">Solo se puede establecer en tiempo de diseño.</span><span class="sxs-lookup"><span data-stu-id="a268c-131">Can only be set at design time.</span></span> |
| [<span data-ttu-id="a268c-132">General</span><span class="sxs-lookup"><span data-stu-id="a268c-132">zoom</span></span>](video-zoom.md)                               | <span data-ttu-id="a268c-133">Especifica el porcentaje por el que se va a escalar el vídeo.</span><span class="sxs-lookup"><span data-stu-id="a268c-133">Specifies the percentage by which to scale the video.</span></span>                                                                                                                                                                                    |



 

<span data-ttu-id="a268c-134">El elemento de **vídeo** puede implementar los controladores de eventos siguientes.</span><span class="sxs-lookup"><span data-stu-id="a268c-134">The **VIDEO** element can implement the following event handlers.</span></span>



| <span data-ttu-id="a268c-135">Controlador de eventos</span><span class="sxs-lookup"><span data-stu-id="a268c-135">Event handler</span></span>                          | <span data-ttu-id="a268c-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="a268c-136">Description</span></span>                                                                  |
|----------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="a268c-137">onvideoend</span><span class="sxs-lookup"><span data-stu-id="a268c-137">onvideoend</span></span>](video-onvideoend.md)     | <span data-ttu-id="a268c-138">Controla un evento que se produce cuando el vídeo detiene la representación y se descarga.</span><span class="sxs-lookup"><span data-stu-id="a268c-138">Handles an event that occurs when the video stops rendering and is unloaded.</span></span> |
| [<span data-ttu-id="a268c-139">onvideostart</span><span class="sxs-lookup"><span data-stu-id="a268c-139">onvideostart</span></span>](video-onvideostart.md) | <span data-ttu-id="a268c-140">Controla un evento que se produce cuando el vídeo se carga y comienza a representarse.</span><span class="sxs-lookup"><span data-stu-id="a268c-140">Handles an event that occurs when the video is loaded and begins to render.</span></span>  |



 

<span data-ttu-id="a268c-141">El elemento de **vídeo** admite los atributos de ambiente y puede implementar los controladores de eventos de ambiente, excepto donde se indique.</span><span class="sxs-lookup"><span data-stu-id="a268c-141">The **VIDEO** element supports the ambient attributes and can implement the ambient event handlers, except where noted.</span></span> <span data-ttu-id="a268c-142">Para obtener más información, vea [atributos de ambiente](ambient-attributes.md) y controladores de eventos de [ambiente](ambient-event-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="a268c-142">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md).</span></span>

<span data-ttu-id="a268c-143">Los elementos de vídeo predefinidos son elementos de **vídeo** normales con varios valores de atributos comunes especificados de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a268c-143">Predefined video elements are normal **VIDEO** elements with various common attribute settings specified by default.</span></span> <span data-ttu-id="a268c-144">Están disponibles los siguientes elementos de vídeo predefinidos.</span><span class="sxs-lookup"><span data-stu-id="a268c-144">The following predefined video elements are available.</span></span>



| <span data-ttu-id="a268c-145">VÍDEO predefinido</span><span class="sxs-lookup"><span data-stu-id="a268c-145">Predefined VIDEO</span></span>         | <span data-ttu-id="a268c-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="a268c-146">Description</span></span>                                                |
|--------------------------|------------------------------------------------------------|
| [<span data-ttu-id="a268c-147">WMPVIDEO</span><span class="sxs-lookup"><span data-stu-id="a268c-147">WMPVIDEO</span></span>](wmpvideo.md) | <span data-ttu-id="a268c-148">Un elemento de **vídeo** que estira el vídeo cuando se cambia el tamaño.</span><span class="sxs-lookup"><span data-stu-id="a268c-148">A **VIDEO** element that stretches the video when resized.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a268c-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a268c-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a268c-150">**Referencia de programación de máscara**</span><span class="sxs-lookup"><span data-stu-id="a268c-150">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




