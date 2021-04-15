---
title: Elemento de vista
description: Elemento de vista
ms.assetid: e1dfde08-33a0-4f12-8db0-ad62e4a1d467
keywords:
- Aspectos de Windows Media Player, elemento VIEW
- aspectos, elemento de vista
- Elemento de vista
- referencia de las máscaras, elemento de vista
- elementos, vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e907cced22b4d1cd498054df06ac8677a7488b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418828"
---
# <a name="view-element"></a><span data-ttu-id="542d1-108">Elemento de vista</span><span class="sxs-lookup"><span data-stu-id="542d1-108">VIEW Element</span></span>

<span data-ttu-id="542d1-109">El elemento de **vista** contiene los detalles de la interfaz de usuario de una máscara y usa los atributos, métodos y controladores de eventos que se muestran en las tablas siguientes.</span><span class="sxs-lookup"><span data-stu-id="542d1-109">The **VIEW** element contains the user interface details of a skin, and uses the attributes, methods, and event handlers shown in the following tables.</span></span>

<span data-ttu-id="542d1-110">Se pueden definir varios elementos de **vista** como elementos secundarios del elemento de **tema** de una máscara para proporcionar diferentes interfaces para diferentes situaciones.</span><span class="sxs-lookup"><span data-stu-id="542d1-110">Multiple **VIEW** elements can be defined as children of the **THEME** element of a skin to provide different interfaces for different situations.</span></span> <span data-ttu-id="542d1-111">Los elementos de **vista** no se pueden especificar como elementos secundarios de ningún otro elemento y contienen todos los demás elementos de máscara.</span><span class="sxs-lookup"><span data-stu-id="542d1-111">**VIEW** elements cannot be specified as children of any other element, and they contain all other skin elements.</span></span> <span data-ttu-id="542d1-112">Tenga en cuenta que cada vista tiene su propio ámbito de variable, lo que significa que no puede compartir valores de atributo con otras vistas.</span><span class="sxs-lookup"><span data-stu-id="542d1-112">Note that each view has its own variable scope, which means it cannot share attribute values with other views.</span></span>

<span data-ttu-id="542d1-113">El atributo de **vista** global se puede usar para hacer referencia a un elemento de **vista** específico desde cualquier lugar dentro de él.</span><span class="sxs-lookup"><span data-stu-id="542d1-113">The **view** global attribute can be used to reference a specific **VIEW** element from anywhere within it.</span></span> <span data-ttu-id="542d1-114">Se trata de una alternativa al uso del atributo **ID** , que debe usarse desde otros elementos de **vista** o desde dentro del elemento **Theme** .</span><span class="sxs-lookup"><span data-stu-id="542d1-114">This is an alternative to using its **id** attribute, which must be used from within other **VIEW** elements or from within the **THEME** element.</span></span>

<span data-ttu-id="542d1-115">El elemento **View** admite los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="542d1-115">The **VIEW** element supports the following attributes.</span></span> <span data-ttu-id="542d1-116">Los atributos marcados con un asterisco ( \* ) también se admiten en el elemento de la **subvista** .</span><span class="sxs-lookup"><span data-stu-id="542d1-116">Attributes marked with an asterisk (\*) are also supported by the **SUBVIEW** element.</span></span>



| <span data-ttu-id="542d1-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="542d1-117">Attribute</span></span>                                                       | <span data-ttu-id="542d1-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="542d1-118">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="542d1-119">[BackgroundColor](view-backgroundcolor.md)\*</span><span class="sxs-lookup"><span data-stu-id="542d1-119">[backgroundColor](view-backgroundcolor.md) \*</span></span>                  | <span data-ttu-id="542d1-120">Especifica o recupera el color de fondo de la **vista** o la **subvista**.</span><span class="sxs-lookup"><span data-stu-id="542d1-120">Specifies or retrieves the background color of the **VIEW** or **SUBVIEW**.</span></span>                                             |
| <span data-ttu-id="542d1-121">[backgroundImage](view-backgroundimage.md) \*</span><span class="sxs-lookup"><span data-stu-id="542d1-121">[backgroundImage](view-backgroundimage.md) \*</span></span>                  | <span data-ttu-id="542d1-122">Especifica o recupera la imagen de fondo de la **vista** o la **subvista**.</span><span class="sxs-lookup"><span data-stu-id="542d1-122">Specifies or retrieves the background image of the **VIEW** or **SUBVIEW**.</span></span>                                             |
| [<span data-ttu-id="542d1-123">backgroundImageHueShift</span><span class="sxs-lookup"><span data-stu-id="542d1-123">backgroundImageHueShift</span></span>](view-backgroundimagehueshift.md)     | <span data-ttu-id="542d1-124">Especifica o recupera la cantidad por la que se desplaza el matiz de la imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="542d1-124">Specifies or retrieves the amount by which the hue of the background image is shifted.</span></span>                                  |
| [<span data-ttu-id="542d1-125">backgroundImageSaturation</span><span class="sxs-lookup"><span data-stu-id="542d1-125">backgroundImageSaturation</span></span>](view-backgroundimagesaturation.md) | <span data-ttu-id="542d1-126">Especifica o recupera el valor de saturación de la imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="542d1-126">Specifies or retrieves the saturation value of the background image.</span></span>                                                    |
| <span data-ttu-id="542d1-127">[backgroundTiled](view-backgroundtiled.md)\*</span><span class="sxs-lookup"><span data-stu-id="542d1-127">[backgroundTiled](view-backgroundtiled.md) \*</span></span>                  | <span data-ttu-id="542d1-128">Especifica o recupera un valor que indica si la imagen de fondo de la **vista** o la **subvista** está en mosaico.</span><span class="sxs-lookup"><span data-stu-id="542d1-128">Specifies or retrieves a value indicating whether the background image of the **VIEW** or **SUBVIEW** is tiled.</span></span>         |
| [<span data-ttu-id="542d1-129">category</span><span class="sxs-lookup"><span data-stu-id="542d1-129">category</span></span>](view-category.md)                                   | <span data-ttu-id="542d1-130">Especifica o recupera la categoría para la que aparecerá la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="542d1-130">Specifies or retrieves the category for which the user interface will appear.</span></span>                                           |
| [<span data-ttu-id="542d1-131">focusObjectID</span><span class="sxs-lookup"><span data-stu-id="542d1-131">focusObjectID</span></span>](view-focusobjectid.md)                         | <span data-ttu-id="542d1-132">Especifica o recupera un valor que indica qué elemento tiene el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="542d1-132">Specifies or retrieves a value indicating which element has keyboard focus.</span></span>                                             |
| [<span data-ttu-id="542d1-133">maxHeight</span><span class="sxs-lookup"><span data-stu-id="542d1-133">maxHeight</span></span>](view-maxheight.md)                                 | <span data-ttu-id="542d1-134">Especifica o recupera el alto máximo de la **vista** al cambiar el tamaño.</span><span class="sxs-lookup"><span data-stu-id="542d1-134">Specifies or retrieves the maximum height of the **VIEW** when resizing.</span></span>                                                |
| [<span data-ttu-id="542d1-135">maxWidth</span><span class="sxs-lookup"><span data-stu-id="542d1-135">maxWidth</span></span>](view-maxwidth.md)                                   | <span data-ttu-id="542d1-136">Especifica o recupera el ancho máximo de la **vista** al cambiar el tamaño.</span><span class="sxs-lookup"><span data-stu-id="542d1-136">Specifies or retrieves the maximum width of the **VIEW** when resizing.</span></span>                                                 |
| [<span data-ttu-id="542d1-137">minHeight</span><span class="sxs-lookup"><span data-stu-id="542d1-137">minHeight</span></span>](view-minheight.md)                                 | <span data-ttu-id="542d1-138">Especifica o recupera el alto mínimo de la **vista** al cambiar el tamaño.</span><span class="sxs-lookup"><span data-stu-id="542d1-138">Specifies or retrieves the minimum height of the **VIEW** when resizing.</span></span>                                                |
| [<span data-ttu-id="542d1-139">minWidth</span><span class="sxs-lookup"><span data-stu-id="542d1-139">minWidth</span></span>](view-minwidth.md)                                   | <span data-ttu-id="542d1-140">Especifica o recupera el ancho mínimo de la **vista** al cambiar el tamaño.</span><span class="sxs-lookup"><span data-stu-id="542d1-140">Specifies or retrieves the minimum width of the **VIEW** when resizing.</span></span>                                                 |
| [<span data-ttu-id="542d1-141">tamaño</span><span class="sxs-lookup"><span data-stu-id="542d1-141">resizable</span></span>](view-resizable.md)                                 | <span data-ttu-id="542d1-142">Especifica o recupera un valor que indica si se puede cambiar el tamaño de la **vista** .</span><span class="sxs-lookup"><span data-stu-id="542d1-142">Specifies or retrieves a value indicating whether the **VIEW** can be resized.</span></span>                                          |
| [<span data-ttu-id="542d1-143">resizeBackgroundImage</span><span class="sxs-lookup"><span data-stu-id="542d1-143">resizeBackgroundImage</span></span>](view-resizebackgroundimage.md)         | <span data-ttu-id="542d1-144">Especifica o recupera un valor que indica si se puede cambiar el tamaño de la imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="542d1-144">Specifies or retrieves a value indicating whether the background image can be resized.</span></span>                                  |
| [<span data-ttu-id="542d1-145">scriptFile</span><span class="sxs-lookup"><span data-stu-id="542d1-145">scriptFile</span></span>](view-scriptfile.md)                               | <span data-ttu-id="542d1-146">Especifica los nombres de archivo de los archivos JScript que lo acompañan.</span><span class="sxs-lookup"><span data-stu-id="542d1-146">Specifies the file names of accompanying JScript files.</span></span>                                                                 |
| [<span data-ttu-id="542d1-147">timerInterval</span><span class="sxs-lookup"><span data-stu-id="542d1-147">timerInterval</span></span>](view-timerinterval.md)                         | <span data-ttu-id="542d1-148">Especifica o recupera el intervalo, en milisegundos, en el que el temporizador activa eventos al controlador de eventos de **tiempo de actividad** .</span><span class="sxs-lookup"><span data-stu-id="542d1-148">Specifies or retrieves the interval, in milliseconds, at which the timer fires events to the **ontimer** event handler.</span></span> |
| [<span data-ttu-id="542d1-149">title</span><span class="sxs-lookup"><span data-stu-id="542d1-149">title</span></span>](view-title.md)                                         | <span data-ttu-id="542d1-150">Especifica o recupera el título de la **vista**.</span><span class="sxs-lookup"><span data-stu-id="542d1-150">Specifies or retrieves the title of the **VIEW**.</span></span> <span data-ttu-id="542d1-151">Solo se puede establecer en tiempo de diseño.</span><span class="sxs-lookup"><span data-stu-id="542d1-151">Can only be set at design time.</span></span>                                       |
| [<span data-ttu-id="542d1-152">titleBar</span><span class="sxs-lookup"><span data-stu-id="542d1-152">titleBar</span></span>](view-titlebar.md)                                   | <span data-ttu-id="542d1-153">Especifica o recupera un valor que indica si se muestra la barra de título de la ventana.</span><span class="sxs-lookup"><span data-stu-id="542d1-153">Specifies or retrieves a value indicating whether the window title bar is shown.</span></span>                                        |
| <span data-ttu-id="542d1-154">[transparencyColor](view-transparencycolor.md)\*</span><span class="sxs-lookup"><span data-stu-id="542d1-154">[transparencyColor](view-transparencycolor.md) \*</span></span>              | <span data-ttu-id="542d1-155">Especifica o recupera el color de transparencia de la imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="542d1-155">Specifies or retrieves the transparency color of the background image.</span></span>                                                  |



 

<span data-ttu-id="542d1-156">El elemento **View** admite los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="542d1-156">The **VIEW** element supports the following methods.</span></span>



| <span data-ttu-id="542d1-157">Método</span><span class="sxs-lookup"><span data-stu-id="542d1-157">Method</span></span>                                              | <span data-ttu-id="542d1-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="542d1-158">Description</span></span>                                                |
|-----------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="542d1-159">close</span><span class="sxs-lookup"><span data-stu-id="542d1-159">close</span></span>](view-close.md)                             | <span data-ttu-id="542d1-160">Cierra la **vista**.</span><span class="sxs-lookup"><span data-stu-id="542d1-160">Closes the **VIEW**.</span></span>                                       |
| [<span data-ttu-id="542d1-161">maximizar</span><span class="sxs-lookup"><span data-stu-id="542d1-161">maximize</span></span>](view-maximize.md)                       | <span data-ttu-id="542d1-162">Maximiza la **vista**.</span><span class="sxs-lookup"><span data-stu-id="542d1-162">Maximizes the **VIEW**.</span></span>                                    |
| [<span data-ttu-id="542d1-163">miniMIZE</span><span class="sxs-lookup"><span data-stu-id="542d1-163">minimize</span></span>](view-minimize.md)                       | <span data-ttu-id="542d1-164">Minimiza la **vista**.</span><span class="sxs-lookup"><span data-stu-id="542d1-164">Minimizes the **VIEW**.</span></span>                                    |
| [<span data-ttu-id="542d1-165">restore</span><span class="sxs-lookup"><span data-stu-id="542d1-165">restore</span></span>](view-restore.md)                         | <span data-ttu-id="542d1-166">Restaura la **vista**.</span><span class="sxs-lookup"><span data-stu-id="542d1-166">Restores the **VIEW**.</span></span>                                     |
| [<span data-ttu-id="542d1-167">returnToMediaCenter</span><span class="sxs-lookup"><span data-stu-id="542d1-167">returnToMediaCenter</span></span>](view-returntomediacenter.md) | <span data-ttu-id="542d1-168">Devuelve el usuario al modo completo de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="542d1-168">Returns the user to the full mode of Windows Media Player.</span></span> |
| [<span data-ttu-id="542d1-169">size</span><span class="sxs-lookup"><span data-stu-id="542d1-169">size</span></span>](view-size.md)                               | <span data-ttu-id="542d1-170">Cambia el tamaño de la **vista** en un borde especificado.</span><span class="sxs-lookup"><span data-stu-id="542d1-170">Resizes the **VIEW** on a specified edge.</span></span>                  |



 

<span data-ttu-id="542d1-171">El elemento de **vista** puede implementar los controladores de eventos siguientes.</span><span class="sxs-lookup"><span data-stu-id="542d1-171">The **VIEW** element can implement the following event handlers.</span></span>



| <span data-ttu-id="542d1-172">Controlador de eventos</span><span class="sxs-lookup"><span data-stu-id="542d1-172">Event handler</span></span>               | <span data-ttu-id="542d1-173">Descripción</span><span class="sxs-lookup"><span data-stu-id="542d1-173">Description</span></span>                                                                |
|-----------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="542d1-174">OnClose</span><span class="sxs-lookup"><span data-stu-id="542d1-174">onclose</span></span>](view-onclose.md) | <span data-ttu-id="542d1-175">Controla un evento que se produce cuando la **vista** está a punto de cerrarse.</span><span class="sxs-lookup"><span data-stu-id="542d1-175">Handles an event that occurs when the **VIEW** is about to be closed.</span></span>      |
| [<span data-ttu-id="542d1-176">OnError</span><span class="sxs-lookup"><span data-stu-id="542d1-176">onerror</span></span>](view-onerror.md) | <span data-ttu-id="542d1-177">Controla un evento de error si **Settings. enableErrorDialogs** está establecido en false.</span><span class="sxs-lookup"><span data-stu-id="542d1-177">Handles an error event if **Settings.enableErrorDialogs** is set to false.</span></span> |
| [<span data-ttu-id="542d1-178">carga</span><span class="sxs-lookup"><span data-stu-id="542d1-178">onload</span></span>](view-onload.md)   | <span data-ttu-id="542d1-179">Controla un evento que se produce cuando se muestra la **vista** por primera vez.</span><span class="sxs-lookup"><span data-stu-id="542d1-179">Handles an event that occurs when the **VIEW** is first displayed.</span></span>         |
| [<span data-ttu-id="542d1-180">tiempo de espera</span><span class="sxs-lookup"><span data-stu-id="542d1-180">ontimer</span></span>](view-ontimer.md) | <span data-ttu-id="542d1-181">Controla los eventos del temporizador.</span><span class="sxs-lookup"><span data-stu-id="542d1-181">Handles timer events.</span></span>                                                      |



 

<span data-ttu-id="542d1-182">El elemento **View** admite los atributos de ambiente y puede implementar los controladores de eventos ambiente, excepto donde se indique.</span><span class="sxs-lookup"><span data-stu-id="542d1-182">The **VIEW** element supports the ambient attributes and can implement the ambient event handlers, except where noted.</span></span> <span data-ttu-id="542d1-183">Para obtener más información, vea [atributos de ambiente](ambient-attributes.md) y controladores de eventos de [ambiente](ambient-event-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="542d1-183">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md),</span></span>

## <a name="related-topics"></a><span data-ttu-id="542d1-184">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="542d1-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="542d1-185">**Referencia de programación de máscara**</span><span class="sxs-lookup"><span data-stu-id="542d1-185">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




