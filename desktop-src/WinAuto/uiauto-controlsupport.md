---
title: Compatibilidad de UI Automation con controles estándar
description: En este tema se identifican los controles estándar de Windows compatibles con la automatización de la interfaz de usuario de Microsoft. La compatibilidad completa solo se proporciona para los controles de la versión 6 de ComCtrl32.dll (disponibles con Windows XP y versiones posteriores).
ms.assetid: 4821684c-8a90-413c-8ddc-699926e3bb09
keywords:
- clientes, compatibilidad de UI Automation con controles estándar
- clientes, compatibilidad con controles estándar
- clientes, controles Win32
- Automatización de la interfaz de usuario, compatibilidad con controles estándar
- Automatización de la interfaz de usuario, compatibilidad con controles estándar
- Automatización de la interfaz de usuario, controles Win32
- compatibilidad con controles estándar
- compatibilidad con controles estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6e384b9ee0fd72fd8a41aa3f791a5c996fe6d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531918"
---
# <a name="ui-automation-support-for-standard-controls"></a><span data-ttu-id="28195-112">Compatibilidad de UI Automation con controles estándar</span><span class="sxs-lookup"><span data-stu-id="28195-112">UI Automation Support for Standard Controls</span></span>

<span data-ttu-id="28195-113">En este tema se identifican los controles estándar de Windows compatibles con la automatización de la interfaz de usuario de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="28195-113">This topic identifies the standard Windows controls that are supported by Microsoft UI Automation.</span></span> <span data-ttu-id="28195-114">La compatibilidad completa solo se proporciona para los controles de la versión 6 de ComCtrl32.dll (disponibles con Windows XP y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="28195-114">Full support is provided only for controls from version 6 of ComCtrl32.dll (available with Windows XP and later).</span></span>

> [!Note]  
> <span data-ttu-id="28195-115">El control RichEdit solo se admite para las versiones incluidas con Windows Vista (en RichEd20.dll versión 3,1 y posteriores, y MsftEdit.dll versión 4,1 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="28195-115">The RichEdit control is supported only for versions shipped with Windows Vista (in RichEd20.dll version 3.1 and later, and MsftEdit.dll version 4.1 and later).</span></span>

 

<span data-ttu-id="28195-116">En la tabla siguiente se enumeran los nombres de clase de los controles estándar admitidos, junto con los tipos de control de automatización de la interfaz de usuario correspondientes.</span><span class="sxs-lookup"><span data-stu-id="28195-116">The following table lists the class names of the supported standard controls, along with the corresponding UI Automation control types.</span></span>



| <span data-ttu-id="28195-117">Class Name (Nombre de clase)</span><span class="sxs-lookup"><span data-stu-id="28195-117">Class Name</span></span>          | <span data-ttu-id="28195-118">Tipo de control</span><span class="sxs-lookup"><span data-stu-id="28195-118">Control Type</span></span>        |
|---------------------|---------------------|
| <span data-ttu-id="28195-119">Button</span><span class="sxs-lookup"><span data-stu-id="28195-119">Button</span></span>              | <span data-ttu-id="28195-120">Button</span><span class="sxs-lookup"><span data-stu-id="28195-120">Button</span></span>              |
| <span data-ttu-id="28195-121">Button</span><span class="sxs-lookup"><span data-stu-id="28195-121">Button</span></span>              | <span data-ttu-id="28195-122">RadioButton</span><span class="sxs-lookup"><span data-stu-id="28195-122">RadioButton</span></span>         |
| <span data-ttu-id="28195-123">Botón</span><span class="sxs-lookup"><span data-stu-id="28195-123">Button</span></span>              | <span data-ttu-id="28195-124">Grupo</span><span class="sxs-lookup"><span data-stu-id="28195-124">Group</span></span>               |
| <span data-ttu-id="28195-125">Botón</span><span class="sxs-lookup"><span data-stu-id="28195-125">Button</span></span>              | <span data-ttu-id="28195-126">CheckBox</span><span class="sxs-lookup"><span data-stu-id="28195-126">CheckBox</span></span>            |
| <span data-ttu-id="28195-127">Botón</span><span class="sxs-lookup"><span data-stu-id="28195-127">Button</span></span>              | <span data-ttu-id="28195-128">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="28195-128">Hyperlink</span></span>           |
| <span data-ttu-id="28195-129">Botón</span><span class="sxs-lookup"><span data-stu-id="28195-129">Button</span></span>              | <span data-ttu-id="28195-130">SplitButton</span><span class="sxs-lookup"><span data-stu-id="28195-130">SplitButton</span></span>         |
| <span data-ttu-id="28195-131">Botón</span><span class="sxs-lookup"><span data-stu-id="28195-131">Button</span></span>              | <span data-ttu-id="28195-132">CheckBox</span><span class="sxs-lookup"><span data-stu-id="28195-132">CheckBox</span></span>            |
| <span data-ttu-id="28195-133">ComboBoxEx32</span><span class="sxs-lookup"><span data-stu-id="28195-133">ComboBoxEx32</span></span>        | <span data-ttu-id="28195-134">ComboBox</span><span class="sxs-lookup"><span data-stu-id="28195-134">ComboBox</span></span>            |
| <span data-ttu-id="28195-135">ComboBox</span><span class="sxs-lookup"><span data-stu-id="28195-135">ComboBox</span></span>            | <span data-ttu-id="28195-136">ComboBox</span><span class="sxs-lookup"><span data-stu-id="28195-136">ComboBox</span></span>            |
| <span data-ttu-id="28195-137">Editar</span><span class="sxs-lookup"><span data-stu-id="28195-137">Edit</span></span>                | <span data-ttu-id="28195-138">Documento</span><span class="sxs-lookup"><span data-stu-id="28195-138">Document</span></span>            |
| <span data-ttu-id="28195-139">Editar</span><span class="sxs-lookup"><span data-stu-id="28195-139">Edit</span></span>                | <span data-ttu-id="28195-140">Editar</span><span class="sxs-lookup"><span data-stu-id="28195-140">Edit</span></span>                |
| <span data-ttu-id="28195-141">SysLink</span><span class="sxs-lookup"><span data-stu-id="28195-141">SysLink</span></span>             | <span data-ttu-id="28195-142">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="28195-142">Hyperlink</span></span>           |
| <span data-ttu-id="28195-143">estática</span><span class="sxs-lookup"><span data-stu-id="28195-143">Static</span></span>              | <span data-ttu-id="28195-144">Texto</span><span class="sxs-lookup"><span data-stu-id="28195-144">Text</span></span>                |
| <span data-ttu-id="28195-145">estática</span><span class="sxs-lookup"><span data-stu-id="28195-145">Static</span></span>              | <span data-ttu-id="28195-146">Imagen</span><span class="sxs-lookup"><span data-stu-id="28195-146">Image</span></span>               |
| <span data-ttu-id="28195-147">SysIPAddress32</span><span class="sxs-lookup"><span data-stu-id="28195-147">SysIPAddress32</span></span>      | <span data-ttu-id="28195-148">Personalizados</span><span class="sxs-lookup"><span data-stu-id="28195-148">Custom</span></span>              |
| <span data-ttu-id="28195-149">SysHeader32</span><span class="sxs-lookup"><span data-stu-id="28195-149">SysHeader32</span></span>         | <span data-ttu-id="28195-150">Header/HeaderItem</span><span class="sxs-lookup"><span data-stu-id="28195-150">Header/HeaderItem</span></span>   |
| <span data-ttu-id="28195-151">SysListView32</span><span class="sxs-lookup"><span data-stu-id="28195-151">SysListView32</span></span>       | <span data-ttu-id="28195-152">DataGrid</span><span class="sxs-lookup"><span data-stu-id="28195-152">DataGrid</span></span>            |
| <span data-ttu-id="28195-153">SysListView32</span><span class="sxs-lookup"><span data-stu-id="28195-153">SysListView32</span></span>       | <span data-ttu-id="28195-154">List</span><span class="sxs-lookup"><span data-stu-id="28195-154">List</span></span>                |
| <span data-ttu-id="28195-155">ListBox</span><span class="sxs-lookup"><span data-stu-id="28195-155">ListBox</span></span>             | <span data-ttu-id="28195-156">List</span><span class="sxs-lookup"><span data-stu-id="28195-156">List</span></span>                |
| <span data-ttu-id="28195-157">ListBox</span><span class="sxs-lookup"><span data-stu-id="28195-157">ListBox</span></span>             | <span data-ttu-id="28195-158">ListItem</span><span class="sxs-lookup"><span data-stu-id="28195-158">ListItem</span></span>            |
| <span data-ttu-id="28195-159">\#32768</span><span class="sxs-lookup"><span data-stu-id="28195-159">\#32768</span></span>             | <span data-ttu-id="28195-160">Menú</span><span class="sxs-lookup"><span data-stu-id="28195-160">Menu</span></span>                |
| <span data-ttu-id="28195-161">\#32768</span><span class="sxs-lookup"><span data-stu-id="28195-161">\#32768</span></span>             | <span data-ttu-id="28195-162">MenuItem</span><span class="sxs-lookup"><span data-stu-id="28195-162">MenuItem</span></span>            |
| <span data-ttu-id="28195-163">msctls \_ progress32</span><span class="sxs-lookup"><span data-stu-id="28195-163">msctls\_progress32</span></span>  | <span data-ttu-id="28195-164">ProgressBar</span><span class="sxs-lookup"><span data-stu-id="28195-164">ProgressBar</span></span>         |
| <span data-ttu-id="28195-165">RichEdit</span><span class="sxs-lookup"><span data-stu-id="28195-165">RichEdit</span></span>            | <span data-ttu-id="28195-166">Documentar.</span><span class="sxs-lookup"><span data-stu-id="28195-166">Document.</span></span> <span data-ttu-id="28195-167">Ver nota.</span><span class="sxs-lookup"><span data-stu-id="28195-167">See note.</span></span> |
| <span data-ttu-id="28195-168">RichEdit20A</span><span class="sxs-lookup"><span data-stu-id="28195-168">RichEdit20A</span></span>         | <span data-ttu-id="28195-169">Documento</span><span class="sxs-lookup"><span data-stu-id="28195-169">Document</span></span>            |
| <span data-ttu-id="28195-170">RichEdit20W</span><span class="sxs-lookup"><span data-stu-id="28195-170">RichEdit20W</span></span>         | <span data-ttu-id="28195-171">Documento</span><span class="sxs-lookup"><span data-stu-id="28195-171">Document</span></span>            |
| <span data-ttu-id="28195-172">RichEdit50W</span><span class="sxs-lookup"><span data-stu-id="28195-172">RichEdit50W</span></span>         | <span data-ttu-id="28195-173">Documento</span><span class="sxs-lookup"><span data-stu-id="28195-173">Document</span></span>            |
| <span data-ttu-id="28195-174">ScrollBar</span><span class="sxs-lookup"><span data-stu-id="28195-174">ScrollBar</span></span>           | <span data-ttu-id="28195-175">Control deslizante</span><span class="sxs-lookup"><span data-stu-id="28195-175">Slider</span></span>              |
| <span data-ttu-id="28195-176">msctls \_ trackbar32</span><span class="sxs-lookup"><span data-stu-id="28195-176">msctls\_trackbar32</span></span>  | <span data-ttu-id="28195-177">Control deslizante</span><span class="sxs-lookup"><span data-stu-id="28195-177">Slider</span></span>              |
| <span data-ttu-id="28195-178">msctls \_ updown32</span><span class="sxs-lookup"><span data-stu-id="28195-178">msctls\_updown32</span></span>    | <span data-ttu-id="28195-179">Spinner</span><span class="sxs-lookup"><span data-stu-id="28195-179">Spinner</span></span>             |
| <span data-ttu-id="28195-180">msctls \_ statusbar32</span><span class="sxs-lookup"><span data-stu-id="28195-180">msctls\_statusbar32</span></span> | <span data-ttu-id="28195-181">StatusBar</span><span class="sxs-lookup"><span data-stu-id="28195-181">StatusBar</span></span>           |
| <span data-ttu-id="28195-182">SysTabControl32</span><span class="sxs-lookup"><span data-stu-id="28195-182">SysTabControl32</span></span>     | <span data-ttu-id="28195-183">Pestaña</span><span class="sxs-lookup"><span data-stu-id="28195-183">Tab</span></span>                 |
| <span data-ttu-id="28195-184">SysTabControl32</span><span class="sxs-lookup"><span data-stu-id="28195-184">SysTabControl32</span></span>     | <span data-ttu-id="28195-185">TabItem</span><span class="sxs-lookup"><span data-stu-id="28195-185">TabItem</span></span>             |
| <span data-ttu-id="28195-186">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="28195-186">ToolbarWindow32</span></span>     | <span data-ttu-id="28195-187">ToolBar</span><span class="sxs-lookup"><span data-stu-id="28195-187">ToolBar</span></span>             |
| <span data-ttu-id="28195-188">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="28195-188">ToolbarWindow32</span></span>     | <span data-ttu-id="28195-189">MenuItem</span><span class="sxs-lookup"><span data-stu-id="28195-189">MenuItem</span></span>            |
| <span data-ttu-id="28195-190">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="28195-190">ToolbarWindow32</span></span>     | <span data-ttu-id="28195-191">Botón</span><span class="sxs-lookup"><span data-stu-id="28195-191">Button</span></span>              |
| <span data-ttu-id="28195-192">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="28195-192">ToolbarWindow32</span></span>     | <span data-ttu-id="28195-193">CheckBox</span><span class="sxs-lookup"><span data-stu-id="28195-193">CheckBox</span></span>            |
| <span data-ttu-id="28195-194">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="28195-194">ToolbarWindow32</span></span>     | <span data-ttu-id="28195-195">RadioButton</span><span class="sxs-lookup"><span data-stu-id="28195-195">RadioButton</span></span>         |
| <span data-ttu-id="28195-196">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="28195-196">ToolbarWindow32</span></span>     | <span data-ttu-id="28195-197">Separador</span><span class="sxs-lookup"><span data-stu-id="28195-197">Separator</span></span>           |
| <span data-ttu-id="28195-198">información sobre herramientas \_ Class32</span><span class="sxs-lookup"><span data-stu-id="28195-198">tooltips\_class32</span></span>   | <span data-ttu-id="28195-199">Información sobre herramientas</span><span class="sxs-lookup"><span data-stu-id="28195-199">ToolTip</span></span>             |
| <span data-ttu-id="28195-200">\#32774</span><span class="sxs-lookup"><span data-stu-id="28195-200">\#32774</span></span>             | <span data-ttu-id="28195-201">Información sobre herramientas</span><span class="sxs-lookup"><span data-stu-id="28195-201">ToolTip</span></span>             |
| <span data-ttu-id="28195-202">ReBarWindow32</span><span class="sxs-lookup"><span data-stu-id="28195-202">ReBarWindow32</span></span>       | <span data-ttu-id="28195-203">Barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="28195-203">Toolbar</span></span>             |
| <span data-ttu-id="28195-204">SysTreeView32</span><span class="sxs-lookup"><span data-stu-id="28195-204">SysTreeView32</span></span>       | <span data-ttu-id="28195-205">Árbol</span><span class="sxs-lookup"><span data-stu-id="28195-205">Tree</span></span>                |
| <span data-ttu-id="28195-206">SysTreeView32</span><span class="sxs-lookup"><span data-stu-id="28195-206">SysTreeView32</span></span>       | <span data-ttu-id="28195-207">TreeItem</span><span class="sxs-lookup"><span data-stu-id="28195-207">TreeItem</span></span>            |



 

<span data-ttu-id="28195-208">No se admiten los controles que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="28195-208">The controls listed in the following table are not supported.</span></span>



| <span data-ttu-id="28195-209">Class Name (Nombre de clase)</span><span class="sxs-lookup"><span data-stu-id="28195-209">Class Name</span></span>                                    | <span data-ttu-id="28195-210">Tipo de control</span><span class="sxs-lookup"><span data-stu-id="28195-210">Control Type</span></span> |
|-----------------------------------------------|--------------|
| <span data-ttu-id="28195-211">SysAnimate32</span><span class="sxs-lookup"><span data-stu-id="28195-211">SysAnimate32</span></span>                                  | <span data-ttu-id="28195-212">Imagen</span><span class="sxs-lookup"><span data-stu-id="28195-212">Image</span></span>        |
| <span data-ttu-id="28195-213">SysPager</span><span class="sxs-lookup"><span data-stu-id="28195-213">SysPager</span></span>                                      | <span data-ttu-id="28195-214">Spinner</span><span class="sxs-lookup"><span data-stu-id="28195-214">Spinner</span></span>      |
| <span data-ttu-id="28195-215">SysDateTimePick32</span><span class="sxs-lookup"><span data-stu-id="28195-215">SysDateTimePick32</span></span>                             | <span data-ttu-id="28195-216">Personalizados</span><span class="sxs-lookup"><span data-stu-id="28195-216">Custom</span></span>       |
| <span data-ttu-id="28195-217">SysMonthCal32</span><span class="sxs-lookup"><span data-stu-id="28195-217">SysMonthCal32</span></span>                                 | <span data-ttu-id="28195-218">Calendario</span><span class="sxs-lookup"><span data-stu-id="28195-218">Calendar</span></span>     |
| <span data-ttu-id="28195-219">MS \_ WINNOTE</span><span class="sxs-lookup"><span data-stu-id="28195-219">MS\_WINNOTE</span></span>                                   | <span data-ttu-id="28195-220">Información sobre herramientas</span><span class="sxs-lookup"><span data-stu-id="28195-220">Tooltip</span></span>      |
| <span data-ttu-id="28195-221">VBBubble</span><span class="sxs-lookup"><span data-stu-id="28195-221">VBBubble</span></span>                                      | <span data-ttu-id="28195-222">Información sobre herramientas</span><span class="sxs-lookup"><span data-stu-id="28195-222">Tooltip</span></span>      |
| <span data-ttu-id="28195-223">ScrollBar (cuando se usa como control independiente)</span><span class="sxs-lookup"><span data-stu-id="28195-223">ScrollBar (when used as a standalone control)</span></span> | <span data-ttu-id="28195-224">Control deslizante</span><span class="sxs-lookup"><span data-stu-id="28195-224">Slider</span></span>       |
| <span data-ttu-id="28195-225">SuperGrid</span><span class="sxs-lookup"><span data-stu-id="28195-225">SuperGrid</span></span>                                     | <span data-ttu-id="28195-226">Personalizados</span><span class="sxs-lookup"><span data-stu-id="28195-226">Custom</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="28195-227">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="28195-227">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28195-228">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="28195-228">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> </dl>

 

 




