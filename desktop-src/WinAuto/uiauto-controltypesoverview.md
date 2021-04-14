---
title: Información general sobre tipos de control de UI Automation
description: Los tipos de control de automatización de la interfaz de usuario de Microsoft son propiedades que sirven como identificadores conocidos que indican el tipo de control que representa un determinado elemento de la interfaz de usuario, como un cuadro combinado o un botón.
ms.assetid: 61818b64-09cb-4443-acca-4743941c48d3
keywords:
- Automatización de la interfaz de usuario, información general sobre tipos de control
- UI Automation, UIA_LocalizedControlTypePropertyId propiedad
- tipos de controles, acerca de
- tipos de control, requisitos
- tipos de control, requisitos previos
- tipos de control, predefinidos
- tipos de control, propiedad UIA_LocalizedControlTypePropertyId
- tipos de controles predefinidos
- Propiedad UIA_LocalizedControlTypePropertyId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b504de2c8f0ae660a27b3b16fa4537630a468f5c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533208"
---
# <a name="ui-automation-control-types-overview"></a><span data-ttu-id="63581-112">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="63581-112">UI Automation Control Types Overview</span></span>

<span data-ttu-id="63581-113">Los tipos de control de automatización de la interfaz de usuario de Microsoft son propiedades que sirven como identificadores conocidos que indican el tipo de control que representa un determinado elemento de la interfaz de usuario, como un cuadro combinado o un botón.</span><span class="sxs-lookup"><span data-stu-id="63581-113">Microsoft UI Automation control types are properties that serve as well-known identifiers that indicate the kind of control that a particular UI element represents, such as a combo box or a button.</span></span> <span data-ttu-id="63581-114">Las aplicaciones cliente utilizan el tipo para identificar las capacidades de un control y para determinar cómo interactuar con él.</span><span class="sxs-lookup"><span data-stu-id="63581-114">Client applications use the type to identify the capabilities of a control and to determine how to interact with it.</span></span>

<span data-ttu-id="63581-115">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="63581-115">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="63581-116">Requisitos de los tipos de control de la automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="63581-116">UI Automation Control Type Requisites</span></span>](#ui-automation-control-type-requisites)
-   [<span data-ttu-id="63581-117">La propiedad LocalizedControlType</span><span class="sxs-lookup"><span data-stu-id="63581-117">The LocalizedControlType Property</span></span>](#the-localizedcontroltype-property)
-   [<span data-ttu-id="63581-118">Tipos actuales de control de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="63581-118">Current UI Automation Control Types</span></span>](#current-ui-automation-control-types)
-   [<span data-ttu-id="63581-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="63581-119">Related topics</span></span>](#related-topics)

## <a name="ui-automation-control-type-requisites"></a><span data-ttu-id="63581-120">Requisitos de los tipos de control de la automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="63581-120">UI Automation Control Type Requisites</span></span>

<span data-ttu-id="63581-121">Cada tipo de control de automatización de la interfaz de usuario tiene un conjunto de condiciones asociadas a él.</span><span class="sxs-lookup"><span data-stu-id="63581-121">Each UI Automation control type has a set of conditions associated with it.</span></span> <span data-ttu-id="63581-122">Cuando un proveedor asigna un tipo de control a un control, el proveedor debe asegurarse de que el control cumpla todas las condiciones asociadas a ese tipo de control.</span><span class="sxs-lookup"><span data-stu-id="63581-122">When a provider assigns a control type to a control, the provider must ensure that the control meets all of the conditions associated with that control type.</span></span> <span data-ttu-id="63581-123">Entre las condiciones se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="63581-123">The conditions include the following:</span></span>

-   <span data-ttu-id="63581-124">Patrones de control de UI Automation: cada tipo de control tiene un conjunto de patrones de control que el control debe admitir, un conjunto que es opcional y un conjunto que el control no debe admitir.</span><span class="sxs-lookup"><span data-stu-id="63581-124">UI Automation control patterns: Each control type has a set of control patterns that the control must support, a set that is optional, and a set that the control must not support.</span></span>
-   <span data-ttu-id="63581-125">Valores de propiedad de la automatización de la interfaz de usuario: cada tipo de control tiene un conjunto de propiedades que el control debe admitir.</span><span class="sxs-lookup"><span data-stu-id="63581-125">UI Automation property values: Each control type has a set of properties that the control must support.</span></span>
-   <span data-ttu-id="63581-126">Eventos de automatización de la interfaz de usuario: cada tipo de control tiene un conjunto de eventos que el control debe admitir.</span><span class="sxs-lookup"><span data-stu-id="63581-126">UI Automation events: Each control type has a set of events that the control must support.</span></span>
-   <span data-ttu-id="63581-127">Estructura de árbol de automatización de la interfaz de usuario: cada tipo de control define el modo en que debe aparecer el control en la estructura de árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="63581-127">UI Automation tree structure: Each control type defines how the control must appear in the UI Automation tree structure.</span></span>

<span data-ttu-id="63581-128">Cuando un control cumple las condiciones de un tipo de control determinado, el valor de la propiedad [**IUIAutomationElement:: CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (o [**IUIAutomationElement:: CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)) indicará ese tipo de control.</span><span class="sxs-lookup"><span data-stu-id="63581-128">When a control meets the conditions for a particular control type, the [**IUIAutomationElement::CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (or [**IUIAutomationElement::CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)) property value will indicate that control type.</span></span>

<span data-ttu-id="63581-129">Si el control no cumple las especificaciones para un tipo de control determinado, use [**UIA \_ CUSTOMCONTROLTYPEID**](uiauto-controltype-ids.md) como identificador de tipo de control y describa por completo el control mediante las propiedades y los patrones de control pertinentes.</span><span class="sxs-lookup"><span data-stu-id="63581-129">If your control does not meet the specifications for a particular control type, use [**UIA\_CustomControlTypeId**](uiauto-controltype-ids.md) as the control type ID, and completely describe the control by using the relevant control patterns and properties.</span></span> <span data-ttu-id="63581-130">También puede establecer la propiedad [**\_ LocalizedControlTypePropertyId de UIA**](uiauto-automation-element-propids.md) en una cadena que describa mejor el tipo del control.</span><span class="sxs-lookup"><span data-stu-id="63581-130">You can also set the [**UIA\_LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) property to a string that best describes the type of your control.</span></span>

## <a name="the-localizedcontroltype-property"></a><span data-ttu-id="63581-131">La propiedad LocalizedControlType</span><span class="sxs-lookup"><span data-stu-id="63581-131">The LocalizedControlType Property</span></span>

<span data-ttu-id="63581-132">Si usa un tipo de control predefinido para describir el control, use el valor predeterminado de la [**propiedad \_ LocalizedControlTypePropertyId de UIA**](uiauto-automation-element-propids.md) y permita que la automatización de la interfaz de usuario proporcione una cadena localizada para que los proveedores se expongan correctamente.</span><span class="sxs-lookup"><span data-stu-id="63581-132">If you use a predefined control type to describe your control, use the default value for the [**UIA\_LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) property and allow UI Automation to provide a localized string for providers to expose properly.</span></span> <span data-ttu-id="63581-133">Si no puede usar un tipo de control predefinido para describir el control, establezca la propiedad **\_ LocalizedControlTypePropertyId de UIA** en una cadena traducida que describa con precisión el tipo de control.</span><span class="sxs-lookup"><span data-stu-id="63581-133">If you cannot use a predefined control type to describe your control, set the **UIA\_LocalizedControlTypePropertyId** property to a localized string that accurately describes the type of your control.</span></span> <span data-ttu-id="63581-134">La cadena debe ser concisa, pero lo suficiente como para que una tecnología de asistencia, como un lector de pantalla, pueda utilizarla en la interfaz de usuario para informar al usuario del tipo del control.</span><span class="sxs-lookup"><span data-stu-id="63581-134">The string should be concise, yet accurate enough that an assistive technology such as a screen reader can use it in the UI to inform the user of the control's type.</span></span>

## <a name="current-ui-automation-control-types"></a><span data-ttu-id="63581-135">Tipos actuales de control de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="63581-135">Current UI Automation Control Types</span></span>

<span data-ttu-id="63581-136">En los temas siguientes se describen los tipos de control de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="63581-136">The following topics describe the UI Automation control types.</span></span> <span data-ttu-id="63581-137">Para cada tipo de control, la descripción incluye el conjunto de condiciones que un control del tipo especificado debe admitir:</span><span class="sxs-lookup"><span data-stu-id="63581-137">For each control type, the description includes the set of conditions that a control of the given type must support:</span></span>

-   <span data-ttu-id="63581-138">AppBar (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-138">AppBar Control Type</span></span>
-   [<span data-ttu-id="63581-139">Button (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-139">Button Control Type</span></span>](uiauto-supportbuttoncontroltype.md)
-   [<span data-ttu-id="63581-140">Calendar (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-140">Calendar Control Type</span></span>](uiauto-supportcalendarcontroltype.md)
-   [<span data-ttu-id="63581-141">CheckBox (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-141">CheckBox Control Type</span></span>](uiauto-supportcheckboxcontroltype.md)
-   [<span data-ttu-id="63581-142">ComboBox (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-142">ComboBox Control Type</span></span>](uiauto-supportcomboboxcontroltype.md)
-   [<span data-ttu-id="63581-143">DataGrid (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-143">DataGrid Control Type</span></span>](uiauto-supportdatagridcontroltype.md)
-   [<span data-ttu-id="63581-144">DataItem (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-144">DataItem Control Type</span></span>](uiauto-supportdataitemcontroltype.md)
-   [<span data-ttu-id="63581-145">Document (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-145">Document Control Type</span></span>](uiauto-supportdocumentcontroltype.md)
-   [<span data-ttu-id="63581-146">Editar tipo de control</span><span class="sxs-lookup"><span data-stu-id="63581-146">Edit Control Type</span></span>](uiauto-supporteditcontroltype.md)
-   [<span data-ttu-id="63581-147">Group (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-147">Group Control Type</span></span>](uiauto-supportgroupcontroltype.md)
-   [<span data-ttu-id="63581-148">Header (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-148">Header Control Type</span></span>](uiauto-supportheadercontroltype.md)
-   [<span data-ttu-id="63581-149">HeaderItem (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-149">HeaderItem Control Type</span></span>](uiauto-supportheaderitemcontroltype.md)
-   [<span data-ttu-id="63581-150">HYPERLINK (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-150">Hyperlink Control Type</span></span>](uiauto-supporthyperlinkcontroltype.md)
-   [<span data-ttu-id="63581-151">Image (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-151">Image Control Type</span></span>](uiauto-supportimagecontroltype.md)
-   [<span data-ttu-id="63581-152">List (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-152">List Control Type</span></span>](uiauto-supportlistcontroltype.md)
-   [<span data-ttu-id="63581-153">ListItem (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-153">ListItem Control Type</span></span>](uiauto-supportlistitemcontroltype.md)
-   [<span data-ttu-id="63581-154">Menu (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-154">Menu Control Type</span></span>](uiauto-supportmenucontroltype.md)
-   [<span data-ttu-id="63581-155">MenuBar (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-155">MenuBar Control Type</span></span>](uiauto-supportmenubarcontroltype.md)
-   [<span data-ttu-id="63581-156">MenuItem (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-156">MenuItem Control Type</span></span>](uiauto-supportmenuitemcontroltype.md)
-   [<span data-ttu-id="63581-157">Pane (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-157">Pane Control Type</span></span>](uiauto-supportpanecontroltype.md)
-   [<span data-ttu-id="63581-158">ProgressBar (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-158">ProgressBar Control Type</span></span>](uiauto-supportprogressbarcontroltype.md)
-   [<span data-ttu-id="63581-159">RadioButton (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-159">RadioButton Control Type</span></span>](uiauto-supportradiobuttoncontroltype.md)
-   [<span data-ttu-id="63581-160">ScrollBar (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-160">ScrollBar Control Type</span></span>](uiauto-supportscrollbarcontroltype.md)
-   [<span data-ttu-id="63581-161">SemanticZoom (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-161">SemanticZoom Control Type</span></span>](/windows/desktop/WinAuto/uiauto-supportsemanticzoomcontroltype)
-   [<span data-ttu-id="63581-162">Separator (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-162">Separator Control Type</span></span>](uiauto-supportseparatorcontroltype.md)
-   [<span data-ttu-id="63581-163">Slide (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-163">Slider Control Type</span></span>](uiauto-supportslidercontroltype.md)
-   [<span data-ttu-id="63581-164">Spinner (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-164">Spinner Control Type</span></span>](uiauto-supportspinnercontroltype.md)
-   [<span data-ttu-id="63581-165">SplitButton (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-165">SplitButton Control Type</span></span>](uiauto-supportsplitbuttoncontroltype.md)
-   [<span data-ttu-id="63581-166">StatusBar (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-166">StatusBar Control Type</span></span>](uiauto-supportstatusbarcontroltype.md)
-   [<span data-ttu-id="63581-167">Tab (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-167">Tab Control Type</span></span>](uiauto-supporttabcontroltype.md)
-   [<span data-ttu-id="63581-168">TabItem (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-168">TabItem Control Type</span></span>](uiauto-supporttabitemcontroltype.md)
-   [<span data-ttu-id="63581-169">Table (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-169">Table Control Type</span></span>](uiauto-supporttablecontroltype.md)
-   [<span data-ttu-id="63581-170">Text (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-170">Text Control Type</span></span>](uiauto-supporttextcontroltype.md)
-   [<span data-ttu-id="63581-171">Thumb (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-171">Thumb Control Type</span></span>](uiauto-supportthumbcontroltype.md)
-   [<span data-ttu-id="63581-172">TitleBar (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-172">TitleBar Control Type</span></span>](uiauto-supporttitlebarcontroltype.md)
-   [<span data-ttu-id="63581-173">ToolBar (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-173">ToolBar Control Type</span></span>](uiauto-supporttoolbarcontroltype.md)
-   [<span data-ttu-id="63581-174">ToolTip (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-174">ToolTip Control Type</span></span>](uiauto-supporttooltipcontroltype.md)
-   [<span data-ttu-id="63581-175">Tree (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-175">Tree Control Type</span></span>](uiauto-supporttreecontroltype.md)
-   [<span data-ttu-id="63581-176">Tipo de control TreeItem</span><span class="sxs-lookup"><span data-stu-id="63581-176">TreeItem Control Type</span></span>](uiauto-supporttreeitemcontroltype.md)
-   [<span data-ttu-id="63581-177">Window (tipo de control)</span><span class="sxs-lookup"><span data-stu-id="63581-177">Window Control Type</span></span>](uiauto-supportwindowcontroltype.md)

## <a name="related-topics"></a><span data-ttu-id="63581-178">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="63581-178">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="63581-179">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="63581-179">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="63581-180">Identificadores de tipo de control</span><span class="sxs-lookup"><span data-stu-id="63581-180">Control Type Identifiers</span></span>](uiauto-controltype-ids.md)
</dt> <dt>

<span data-ttu-id="63581-181">**Vista**</span><span class="sxs-lookup"><span data-stu-id="63581-181">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="63581-182">Compatibilidad con tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="63581-182">Supporting UI Automation Control Types</span></span>](uiauto-supportinguiautocontroltypes.md)
</dt> <dt>

[<span data-ttu-id="63581-183">Compatibilidad de UI Automation con controles estándar</span><span class="sxs-lookup"><span data-stu-id="63581-183">UI Automation Support for Standard Controls</span></span>](uiauto-controlsupport.md)
</dt> <dt>

[<span data-ttu-id="63581-184">Fundamentos de UI Automation</span><span class="sxs-lookup"><span data-stu-id="63581-184">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
</dt> </dl>

 

 