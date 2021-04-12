---
title: Elemento CUSTOMSLIDER
description: Elemento CUSTOMSLIDER
ms.assetid: 9cba9bdd-ea5b-4a4a-a61e-e6aff29fc3e0
keywords:
- Aspectos de Windows Media Player, elemento CUSTOMSLIDER
- aspectos, elemento CUSTOMSLIDER
- Elemento CUSTOMSLIDER
- referencia de las máscaras, elemento CUSTOMSLIDER
- elementos, CUSTOMSLIDER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f49fc6260df295e3266ae9ddf7b5b3eceee43d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357322"
---
# <a name="customslider-element"></a><span data-ttu-id="e164e-108">Elemento CUSTOMSLIDER</span><span class="sxs-lookup"><span data-stu-id="e164e-108">CUSTOMSLIDER Element</span></span>

<span data-ttu-id="e164e-109">El elemento **CUSTOMSLIDER** proporciona una manera de crear y manipular un control deslizante de cualquier forma, como un tirador circular.</span><span class="sxs-lookup"><span data-stu-id="e164e-109">The **CUSTOMSLIDER** element provides a way to create and manipulate a slider control of any shape, such as a circular knob.</span></span> <span data-ttu-id="e164e-110">En las tablas siguientes se enumeran los atributos y controladores de eventos admitidos por este elemento.</span><span class="sxs-lookup"><span data-stu-id="e164e-110">The following tables list the attributes and event handlers supported by this element.</span></span>

<span data-ttu-id="e164e-111">El elemento **CUSTOMSLIDER** admite los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="e164e-111">The **CUSTOMSLIDER** element supports the following attributes.</span></span>



| <span data-ttu-id="e164e-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="e164e-112">Attribute</span></span>                                               | <span data-ttu-id="e164e-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="e164e-113">Description</span></span>                                                                                                                 |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e164e-114">cursor</span><span class="sxs-lookup"><span data-stu-id="e164e-114">cursor</span></span>](customslider-cursor.md)                       | <span data-ttu-id="e164e-115">Especifica o recupera el valor del cursor de control deslizante que aparece cuando el mouse está encima del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="e164e-115">Specifies or retrieves the value of the slider control cursor that appears when the mouse is over the slider.</span></span>               |
| [<span data-ttu-id="e164e-116">disabledImage</span><span class="sxs-lookup"><span data-stu-id="e164e-116">disabledImage</span></span>](customslider-disabledimage.md)         | <span data-ttu-id="e164e-117">Especifica o recupera la imagen del control deslizante que se usa cuando se deshabilita el control deslizante.</span><span class="sxs-lookup"><span data-stu-id="e164e-117">Specifies or retrieves the image of the slider used when the slider is disabled.</span></span>                                            |
| [<span data-ttu-id="e164e-118">downImage</span><span class="sxs-lookup"><span data-stu-id="e164e-118">downImage</span></span>](customslider-downimage.md)                 | <span data-ttu-id="e164e-119">Especifica o recupera la imagen de estado hacia abajo del control deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="e164e-119">Specifies or retrieves the down state image of the custom slider.</span></span>                                                           |
| [<span data-ttu-id="e164e-120">hoverImage</span><span class="sxs-lookup"><span data-stu-id="e164e-120">hoverImage</span></span>](customslider-hoverimage.md)               | <span data-ttu-id="e164e-121">Especifica o recupera la imagen que se muestra cuando el mouse está encima del control deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="e164e-121">Specifies or retrieves the image that displays when the mouse is over the custom slider.</span></span>                                    |
| [<span data-ttu-id="e164e-122">image</span><span class="sxs-lookup"><span data-stu-id="e164e-122">image</span></span>](customslider-image.md)                         | <span data-ttu-id="e164e-123">Especifica o recupera el nombre del archivo que contiene las imágenes correspondientes a los distintos Estados del control deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="e164e-123">Specifies or retrieves the name of the file containing the images corresponding to the various states of the custom slider.</span></span> |
| [<span data-ttu-id="e164e-124">max</span><span class="sxs-lookup"><span data-stu-id="e164e-124">max</span></span>](customslider-max.md)                             | <span data-ttu-id="e164e-125">Especifica o recupera el valor máximo del intervalo definido por el control deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="e164e-125">Specifies or retrieves the maximum value of the range defined by the custom slider.</span></span>                                         |
| [<span data-ttu-id="e164e-126">min</span><span class="sxs-lookup"><span data-stu-id="e164e-126">min</span></span>](customslider-min.md)                             | <span data-ttu-id="e164e-127">Especifica o recupera el valor mínimo del intervalo definido por el control deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="e164e-127">Specifies or retrieves the minimum value of the range defined by the custom slider.</span></span>                                         |
| [<span data-ttu-id="e164e-128">positionImage</span><span class="sxs-lookup"><span data-stu-id="e164e-128">positionImage</span></span>](customslider-positionimage.md)         | <span data-ttu-id="e164e-129">Especifica o recupera el mapa de imágenes que se usa para determinar la imagen de posición del archivo de **imagen** que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="e164e-129">Specifies or retrieves the image map used to determine which position image from the **image** file to display.</span></span>             |
| [<span data-ttu-id="e164e-130">Herramienta</span><span class="sxs-lookup"><span data-stu-id="e164e-130">toolTip</span></span>](customslider-tooltip.md)                     | <span data-ttu-id="e164e-131">Especifica o recupera el texto de información sobre herramientas para el control deslizante.</span><span class="sxs-lookup"><span data-stu-id="e164e-131">Specifies or retrieves the ToolTip text for the slider.</span></span>                                                                     |
| [<span data-ttu-id="e164e-132">Property</span><span class="sxs-lookup"><span data-stu-id="e164e-132">transparencyColor</span></span>](customslider-transparencycolor.md) | <span data-ttu-id="e164e-133">Especifica o recupera el color de transparencia de las imágenes de control deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="e164e-133">Specifies or retrieves the transparency color of the custom slider images.</span></span>                                                  |
| [<span data-ttu-id="e164e-134">value</span><span class="sxs-lookup"><span data-stu-id="e164e-134">value</span></span>](customslider-value.md)                         | <span data-ttu-id="e164e-135">Especifica o recupera la posición actual del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="e164e-135">Specifies or retrieves the current position of the slider.</span></span>                                                                  |



 

<span data-ttu-id="e164e-136">El elemento **CUSTOMSLIDER** puede implementar los controladores de eventos siguientes.</span><span class="sxs-lookup"><span data-stu-id="e164e-136">The **CUSTOMSLIDER** element can implement the following event handlers.</span></span>



| <span data-ttu-id="e164e-137">Controlador de eventos</span><span class="sxs-lookup"><span data-stu-id="e164e-137">Event handler</span></span>                                         | <span data-ttu-id="e164e-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="e164e-138">Description</span></span>                                                                                                          |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e164e-139">onDragBegin</span><span class="sxs-lookup"><span data-stu-id="e164e-139">onDragBegin</span></span>](customslider-ondragbegin.md)           | <span data-ttu-id="e164e-140">Controla un evento que se produce cuando el usuario hace clic y mantiene presionado el botón primario del mouse y comienza a arrastrar el mouse.</span><span class="sxs-lookup"><span data-stu-id="e164e-140">Handles an event that occurs when the user clicks and holds the left mouse button down and begins to drag the mouse.</span></span> |
| [<span data-ttu-id="e164e-141">onDragEnd</span><span class="sxs-lookup"><span data-stu-id="e164e-141">onDragEnd</span></span>](customslider-ondragend.md)               | <span data-ttu-id="e164e-142">Controla un evento que se produce cuando se suelta el botón primario del mouse después de una operación de arrastre.</span><span class="sxs-lookup"><span data-stu-id="e164e-142">Handles an event that occurs when the left mouse button is released after a dragging operation.</span></span>                      |
| [<span data-ttu-id="e164e-143">onPositionChange</span><span class="sxs-lookup"><span data-stu-id="e164e-143">onPositionChange</span></span>](customslider-onpositionchange.md) | <span data-ttu-id="e164e-144">Controla un evento que se produce cuando cambia la posición del control deslizante a medida que el usuario hace clic o arrastra.</span><span class="sxs-lookup"><span data-stu-id="e164e-144">Handles an event that occurs when the position of the slider changes as a result of the user clicking or dragging.</span></span>   |



 

<span data-ttu-id="e164e-145">El elemento **CUSTOMSLIDER** admite los atributos de ambiente y puede implementar los controladores de eventos de ambiente.</span><span class="sxs-lookup"><span data-stu-id="e164e-145">The **CUSTOMSLIDER** element supports the ambient attributes and can implement the ambient event handlers.</span></span> <span data-ttu-id="e164e-146">Para obtener más información, vea [atributos de ambiente](ambient-attributes.md) y controladores de eventos de [ambiente](ambient-event-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="e164e-146">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e164e-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e164e-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e164e-148">**Referencia de programación de máscara**</span><span class="sxs-lookup"><span data-stu-id="e164e-148">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




