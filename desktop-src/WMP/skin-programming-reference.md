---
title: Referencia de programación de máscara
description: Referencia de programación de máscara
ms.assetid: 914f6045-7252-4a06-a514-d31ef6d2d03b
keywords:
- Media Player de Windows, máscaras
- Máscaras de Windows Media Player, referencia de programación
- máscaras, referencia de programación
- referencia para máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30194f0048f4ef66cf32b7c5f3f94c2bd4e190ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773723"
---
# <a name="skin-programming-reference"></a><span data-ttu-id="e8923-107">Referencia de programación de máscara</span><span class="sxs-lookup"><span data-stu-id="e8923-107">Skin Programming Reference</span></span>

<span data-ttu-id="e8923-108">La referencia de programación de la máscara documenta los siguientes elementos y sus atributos, métodos y eventos asociados.</span><span class="sxs-lookup"><span data-stu-id="e8923-108">The Skin Programming Reference documents the following elements and their associated attributes, methods, and events.</span></span>

<span data-ttu-id="e8923-109">Los elementos y atributos de esta sección requieren Windows Media Player 7,0 o posterior, a menos que se indique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="e8923-109">The elements and attributes in this section require Windows Media Player 7.0 or later unless otherwise noted.</span></span>



| <span data-ttu-id="e8923-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="e8923-110">Element</span></span>                                                  | <span data-ttu-id="e8923-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8923-111">Description</span></span>                                                                         |
|----------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="e8923-112">Atributos de ambiente</span><span class="sxs-lookup"><span data-stu-id="e8923-112">Ambient Attributes</span></span>](ambient-attributes.md)             | <span data-ttu-id="e8923-113">Atributos que se aplican a todos los elementos de máscara con excepciones indicadas.</span><span class="sxs-lookup"><span data-stu-id="e8923-113">Attributes that apply to all skin elements with exceptions noted.</span></span>                   |
| [<span data-ttu-id="e8923-114">Controladores de eventos de ambiente</span><span class="sxs-lookup"><span data-stu-id="e8923-114">Ambient Event Handlers</span></span>](ambient-event-handlers.md)     | <span data-ttu-id="e8923-115">Controladores de eventos que pueden ser implementados por la mayoría de los elementos de máscara.</span><span class="sxs-lookup"><span data-stu-id="e8923-115">Event handlers that can be implemented by most skin elements.</span></span>                       |
| [<span data-ttu-id="e8923-116">Atributos de evento de ambiente</span><span class="sxs-lookup"><span data-stu-id="e8923-116">Ambient Event Attributes</span></span>](ambient-event-attributes.md) | <span data-ttu-id="e8923-117">Atributos que detallan el estado de Windows Media Player cuando se desencadena un evento.</span><span class="sxs-lookup"><span data-stu-id="e8923-117">Attributes detailing the state of Windows Media Player when an event is fired.</span></span>      |
| [<span data-ttu-id="e8923-118">Automenú</span><span class="sxs-lookup"><span data-stu-id="e8923-118">AUTOMENU</span></span>](automenu-element.md)                         | <span data-ttu-id="e8923-119">Proporciona una manera de mostrar el panel de acceso rápido en una máscara.</span><span class="sxs-lookup"><span data-stu-id="e8923-119">Provides a way to display the Quick Access Panel in a skin.</span></span>                         |
| [<span data-ttu-id="e8923-120">BOTÓN</span><span class="sxs-lookup"><span data-stu-id="e8923-120">BUTTON</span></span>](button-element.md)                             | <span data-ttu-id="e8923-121">Botón independiente.</span><span class="sxs-lookup"><span data-stu-id="e8923-121">A standalone button.</span></span>                                                                |
| [<span data-ttu-id="e8923-122">BUTTONELEMENT</span><span class="sxs-lookup"><span data-stu-id="e8923-122">BUTTONELEMENT</span></span>](buttonelement-element.md)               | <span data-ttu-id="e8923-123">Un botón dentro de un grupo de botones.</span><span class="sxs-lookup"><span data-stu-id="e8923-123">A button within a button group.</span></span>                                                     |
| [<span data-ttu-id="e8923-124">BUTTONGROUP</span><span class="sxs-lookup"><span data-stu-id="e8923-124">BUTTONGROUP</span></span>](buttongroup-element.md)                   | <span data-ttu-id="e8923-125">Grupo de elementos Button.</span><span class="sxs-lookup"><span data-stu-id="e8923-125">A group of button elements.</span></span>                                                         |
| [<span data-ttu-id="e8923-126">COLUMN</span><span class="sxs-lookup"><span data-stu-id="e8923-126">COLUMN</span></span>](column-element.md)                             | <span data-ttu-id="e8923-127">Representa una columna dentro de un control de lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="e8923-127">Represents a column within a playlist control.</span></span>                                      |
| [<span data-ttu-id="e8923-128">PERMITE</span><span class="sxs-lookup"><span data-stu-id="e8923-128">CONTROLS</span></span>](controls-element.md)                         | <span data-ttu-id="e8923-129">Proporciona acceso al objeto de [controles](controls-object.md) desde dentro de una máscara.</span><span class="sxs-lookup"><span data-stu-id="e8923-129">Provides access to the [Controls](controls-object.md) object from within a skin.</span></span>   |
| [<span data-ttu-id="e8923-130">CUSTOMSLIDER</span><span class="sxs-lookup"><span data-stu-id="e8923-130">CUSTOMSLIDER</span></span>](customslider-element.md)                 | <span data-ttu-id="e8923-131">Control deslizante personalizable.</span><span class="sxs-lookup"><span data-stu-id="e8923-131">A customizable slider control.</span></span>                                                      |
| [<span data-ttu-id="e8923-132">EDITBOX</span><span class="sxs-lookup"><span data-stu-id="e8923-132">EDITBOX</span></span>](editbox-element.md)                           | <span data-ttu-id="e8923-133">Proporciona una manera para que los usuarios escriban texto dentro de una máscara.</span><span class="sxs-lookup"><span data-stu-id="e8923-133">Provides a way for users to enter text within a skin.</span></span>                               |
| [<span data-ttu-id="e8923-134">EFECTOS</span><span class="sxs-lookup"><span data-stu-id="e8923-134">EFFECTS</span></span>](effects-element.md)                           | <span data-ttu-id="e8923-135">Un elemento que contiene y controla una colección de efectos.</span><span class="sxs-lookup"><span data-stu-id="e8923-135">An element that contains and controls a collection of effects.</span></span>                      |
| [<span data-ttu-id="e8923-136">EQUALIZERSETTINGS</span><span class="sxs-lookup"><span data-stu-id="e8923-136">EQUALIZERSETTINGS</span></span>](equalizersettings-element.md)       | <span data-ttu-id="e8923-137">Un elemento que permite la manipulación del ecualizador gráfico.</span><span class="sxs-lookup"><span data-stu-id="e8923-137">An element allowing manipulation of the graphic equalizer.</span></span>                          |
| [<span data-ttu-id="e8923-138">MOVS</span><span class="sxs-lookup"><span data-stu-id="e8923-138">ITEM</span></span>](item-element.md)                                 | <span data-ttu-id="e8923-139">Representa un elemento en un cuadro de lista o control emergente.</span><span class="sxs-lookup"><span data-stu-id="e8923-139">Represents an item in a list box or pop-up control.</span></span>                                 |
| [<span data-ttu-id="e8923-140">IDENTIFICACIÓN</span><span class="sxs-lookup"><span data-stu-id="e8923-140">LISTBOX</span></span>](listbox-element.md)                           | <span data-ttu-id="e8923-141">Proporciona a los usuarios una manera de seleccionar elementos de una lista.</span><span class="sxs-lookup"><span data-stu-id="e8923-141">Provides a way for users to select items from a list.</span></span>                               |
| [<span data-ttu-id="e8923-142">ENCARGADO</span><span class="sxs-lookup"><span data-stu-id="e8923-142">PLAYER</span></span>](player-element.md)                             | <span data-ttu-id="e8923-143">Proporciona acceso al objeto de [reproductor](player-object.md) desde dentro de una máscara.</span><span class="sxs-lookup"><span data-stu-id="e8923-143">Provides access to the [Player](player-object.md) object from within a skin.</span></span>       |
| [<span data-ttu-id="e8923-144">AUTOMÁTICAS</span><span class="sxs-lookup"><span data-stu-id="e8923-144">PLAYLIST</span></span>](playlist-element.md)                         | <span data-ttu-id="e8923-145">Un elemento para controlar la apariencia de una lista de reproducción dentro de una máscara.</span><span class="sxs-lookup"><span data-stu-id="e8923-145">An element for controlling the appearance of a playlist within a skin.</span></span>              |
| [<span data-ttu-id="e8923-146">EMERGENTE</span><span class="sxs-lookup"><span data-stu-id="e8923-146">POPUP</span></span>](popup-element.md)                               | <span data-ttu-id="e8923-147">Proporciona a los usuarios una manera de seleccionar elementos de una lista.</span><span class="sxs-lookup"><span data-stu-id="e8923-147">Provides a way for users to select items from a list.</span></span>                               |
| [<span data-ttu-id="e8923-148">PROGRESSBAR</span><span class="sxs-lookup"><span data-stu-id="e8923-148">PROGRESSBAR</span></span>](progressbar-element.md)                   | <span data-ttu-id="e8923-149">Proporciona una manera de Mostrar información de progreso en un control horizontal o vertical.</span><span class="sxs-lookup"><span data-stu-id="e8923-149">Provides a way to display progress information in a horizontal or vertical control.</span></span> |
| [<span data-ttu-id="e8923-150">CONFIGURACIÓN</span><span class="sxs-lookup"><span data-stu-id="e8923-150">SETTINGS</span></span>](settings-element.md)                         | <span data-ttu-id="e8923-151">Proporciona acceso al objeto de [configuración](settings-object.md) desde dentro de una máscara.</span><span class="sxs-lookup"><span data-stu-id="e8923-151">Provides access to the [Settings](settings-object.md) object from within a skin.</span></span>   |
| [<span data-ttu-id="e8923-152">HASTA</span><span class="sxs-lookup"><span data-stu-id="e8923-152">SLIDER</span></span>](slider-element.md)                             | <span data-ttu-id="e8923-153">Control deslizante.</span><span class="sxs-lookup"><span data-stu-id="e8923-153">A slider control.</span></span>                                                                   |
| [<span data-ttu-id="e8923-154">VISTA secundaria</span><span class="sxs-lookup"><span data-stu-id="e8923-154">SUBVIEW</span></span>](subview-element.md)                           | <span data-ttu-id="e8923-155">Subsecciones de una vista que pueden moverse u ocultarse.</span><span class="sxs-lookup"><span data-stu-id="e8923-155">Subsections within a view that can be moved or hidden.</span></span>                              |
| [<span data-ttu-id="e8923-156">NEGRITA</span><span class="sxs-lookup"><span data-stu-id="e8923-156">TEXT</span></span>](text-element.md)                                 | <span data-ttu-id="e8923-157">Un control que contiene texto.</span><span class="sxs-lookup"><span data-stu-id="e8923-157">A control containing text.</span></span>                                                          |
| [<span data-ttu-id="e8923-158">DICCIONARIOS</span><span class="sxs-lookup"><span data-stu-id="e8923-158">THEME</span></span>](theme-element.md)                               | <span data-ttu-id="e8923-159">Elemento principal que identifica un archivo de máscara.</span><span class="sxs-lookup"><span data-stu-id="e8923-159">The main element identifying a skin file.</span></span>                                           |
| [<span data-ttu-id="e8923-160">CÁMARA</span><span class="sxs-lookup"><span data-stu-id="e8923-160">VIDEO</span></span>](video-element.md)                               | <span data-ttu-id="e8923-161">Un elemento para especificar la apariencia de una ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e8923-161">An element for specifying the appearance of a video window.</span></span>                         |
| [<span data-ttu-id="e8923-162">Opciones de videoconfiguración</span><span class="sxs-lookup"><span data-stu-id="e8923-162">VIDEOSETTINGS</span></span>](videosettings-element.md)               | <span data-ttu-id="e8923-163">Un elemento que permite el control de varias configuraciones de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e8923-163">An element allowing control of various video settings.</span></span>                              |
| [<span data-ttu-id="e8923-164">VIEW</span><span class="sxs-lookup"><span data-stu-id="e8923-164">VIEW</span></span>](view-element.md)                                 | <span data-ttu-id="e8923-165">Especifica el aspecto de la interfaz de usuario (UI) para cada categoría de elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="e8923-165">Specifies what the user interface (UI) looks like for each category of media.</span></span>       |
| [<span data-ttu-id="e8923-166">Varios</span><span class="sxs-lookup"><span data-stu-id="e8923-166">Miscellaneous</span></span>](miscellaneous.md)                       | <span data-ttu-id="e8923-167">Atributos especializados y otros temas variados para su uso en la creación de máscaras.</span><span class="sxs-lookup"><span data-stu-id="e8923-167">Specialized attributes and other miscellaneous topics for use in creating skins.</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="e8923-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e8923-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8923-169">**Máscaras de Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="e8923-169">**Windows Media Player Skins**</span></span>](windows-media-player-skins.md)
</dt> </dl>

 

 




