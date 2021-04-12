---
title: Window (patrón de control)
description: Describe las directrices y convenciones para implementar IWindowProvider, incluida información sobre propiedades, métodos y eventos. El patrón de control window admite controles que proporcionan la funcionalidad fundamental basada en ventanas dentro de una interfaz gráfica de usuario tradicional.
ms.assetid: bfd37d27-fcec-4d25-841c-63e14e48c6c8
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control window
- Automatización de la interfaz de usuario, patrón de control window
- Automatización de la interfaz de usuario, IWindowProvider
- IWindowProvider
- implementar patrones de control de ventana de automatización de la interfaz de usuario
- Patrones de control de ventanas
- patrones de control, IWindowProvider
- patrones de control, implementar la ventana de automatización de la interfaz de usuario
- patrones de control, ventana
- interfaces, IWindowProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3c4f0d862a14fee35f8d1982c7870e2be031c61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357708"
---
# <a name="window-control-pattern"></a><span data-ttu-id="ac211-114">Window (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="ac211-114">Window Control Pattern</span></span>

<span data-ttu-id="ac211-115">Describe las directrices y convenciones para implementar [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider), incluida información sobre propiedades, métodos y eventos.</span><span class="sxs-lookup"><span data-stu-id="ac211-115">Describes guidelines and conventions for implementing [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider), including information about properties, methods, and events.</span></span> <span data-ttu-id="ac211-116">El patrón de control **Window** admite controles que proporcionan la funcionalidad fundamental basada en ventanas dentro de una interfaz gráfica de usuario tradicional.</span><span class="sxs-lookup"><span data-stu-id="ac211-116">The **Window** control pattern supports controls that provide fundamental window-based functionality within a traditional GUI.</span></span>

<span data-ttu-id="ac211-117">Entre los ejemplos de controles que deben implementar este patrón de control se incluyen las ventanas de aplicación de nivel superior, las ventanas secundarias de interfaz de múltiples documentos (MDI), los controles de panel de división de tamaño ajustable, los cuadros de diálogo modales y las ventanas de ayuda de globo.</span><span class="sxs-lookup"><span data-stu-id="ac211-117">Examples of controls that must implement this control pattern include top-level application windows, multiple-document interface (MDI) child windows, resizable split pane controls, modal dialogs and balloon help windows.</span></span> <span data-ttu-id="ac211-118">Para obtener ejemplos de controles que implementan este patrón de control, vea [Control Pattern Mapping for UI Automation Clients](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="ac211-118">For examples of controls that implement this control pattern, see [Control Pattern Mapping for UI Automation Clients](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="ac211-119">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="ac211-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ac211-120">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="ac211-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="ac211-121">Miembros requeridos para **IWindowProvider**</span><span class="sxs-lookup"><span data-stu-id="ac211-121">Required Members for **IWindowProvider**</span></span>](#required-members-for-iwindowprovider)
-   [<span data-ttu-id="ac211-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ac211-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="ac211-123">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="ac211-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="ac211-124">Al implementar el patrón de control **Window** , tenga en cuenta las siguientes directrices y convenciones:</span><span class="sxs-lookup"><span data-stu-id="ac211-124">When implementing the **Window** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="ac211-125">Para admitir la capacidad de modificar el tamaño de la ventana y la posición de la pantalla mediante la automatización de la interfaz de usuario de Microsoft, un control debe implementar [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) además de [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span><span class="sxs-lookup"><span data-stu-id="ac211-125">To support the ability to modify both window size and screen position using Microsoft UI Automation, a control must implement [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) in addition to [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span></span>
-   <span data-ttu-id="ac211-126">Normalmente, los controles que contienen barras de título y elementos de barra de título que permiten que el control se mueva, cambie de tamaño, se maximice, se minimice o se cierren, por lo general, para implementar [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span><span class="sxs-lookup"><span data-stu-id="ac211-126">Controls that contain title bars, and title bar elements that enable the control to be moved, resized, maximized, minimized, or closed, are typically required to implement [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span></span>
-   <span data-ttu-id="ac211-127">Los controles como los elementos emergentes de información sobre herramientas y las listas desplegables de menús o cuadros combinados no implementan normalmente [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span><span class="sxs-lookup"><span data-stu-id="ac211-127">Controls such as tooltip pop-ups and combo-box or menu drop-downs do not typically implement [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span></span>
-   <span data-ttu-id="ac211-128">Las ventanas de ayuda de globo se diferencian de los elementos emergentes de información sobre herramientas básicos por el aprovisionamiento de un botón de **cierre** de tipo ventana.</span><span class="sxs-lookup"><span data-stu-id="ac211-128">Balloon help windows are differentiated from basic tooltip pop-ups by the provision of a window-like **Close** button.</span></span>
-   <span data-ttu-id="ac211-129">El modo de pantalla completa no es compatible con [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) , ya que es específico de la característica de una aplicación y no es un comportamiento de ventana típico.</span><span class="sxs-lookup"><span data-stu-id="ac211-129">Full-screen mode is not supported by [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) as it is feature-specific to an application and is not typical window behavior.</span></span>

## <a name="required-members-for-iwindowprovider"></a><span data-ttu-id="ac211-130">Miembros requeridos para **IWindowProvider**</span><span class="sxs-lookup"><span data-stu-id="ac211-130">Required Members for **IWindowProvider**</span></span>

<span data-ttu-id="ac211-131">Se requieren las siguientes propiedades, métodos y eventos para implementar la interfaz [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) .</span><span class="sxs-lookup"><span data-stu-id="ac211-131">The following properties, methods, and events are required for implementing the [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) interface.</span></span>



| <span data-ttu-id="ac211-132">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="ac211-132">Required members</span></span>                                                                            | <span data-ttu-id="ac211-133">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="ac211-133">Member type</span></span> | <span data-ttu-id="ac211-134">Notas</span><span class="sxs-lookup"><span data-stu-id="ac211-134">Notes</span></span>                                                                       |
|---------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="ac211-135">**WindowInteractionState**</span><span class="sxs-lookup"><span data-stu-id="ac211-135">**WindowInteractionState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowinteractionstate)             | <span data-ttu-id="ac211-136">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ac211-136">Property</span></span>    | <span data-ttu-id="ac211-137">No se garantiza que sea **WindowInteractionState \_ ReadyForUserInteraction**</span><span class="sxs-lookup"><span data-stu-id="ac211-137">Is not guaranteed to be **WindowInteractionState\_ReadyForUserInteraction**</span></span> |
| [<span data-ttu-id="ac211-138">**IsModal**</span><span class="sxs-lookup"><span data-stu-id="ac211-138">**IsModal**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_ismodal)                                           | <span data-ttu-id="ac211-139">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ac211-139">Property</span></span>    | <span data-ttu-id="ac211-140">None</span><span class="sxs-lookup"><span data-stu-id="ac211-140">None</span></span>                                                                        |
| [<span data-ttu-id="ac211-141">**IsTopmost**</span><span class="sxs-lookup"><span data-stu-id="ac211-141">**IsTopmost**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_istopmost)                                       | <span data-ttu-id="ac211-142">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ac211-142">Property</span></span>    | <span data-ttu-id="ac211-143">None</span><span class="sxs-lookup"><span data-stu-id="ac211-143">None</span></span>                                                                        |
| [<span data-ttu-id="ac211-144">**CanMaximize**</span><span class="sxs-lookup"><span data-stu-id="ac211-144">**CanMaximize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canmaximize)                                   | <span data-ttu-id="ac211-145">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ac211-145">Property</span></span>    | <span data-ttu-id="ac211-146">None</span><span class="sxs-lookup"><span data-stu-id="ac211-146">None</span></span>                                                                        |
| [<span data-ttu-id="ac211-147">**CanMinimize**</span><span class="sxs-lookup"><span data-stu-id="ac211-147">**CanMinimize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canminimize)                                   | <span data-ttu-id="ac211-148">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ac211-148">Property</span></span>    | <span data-ttu-id="ac211-149">None</span><span class="sxs-lookup"><span data-stu-id="ac211-149">None</span></span>                                                                        |
| [<span data-ttu-id="ac211-150">**WindowVisualState**</span><span class="sxs-lookup"><span data-stu-id="ac211-150">**WindowVisualState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowvisualstate)                       | <span data-ttu-id="ac211-151">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ac211-151">Property</span></span>    | <span data-ttu-id="ac211-152">None</span><span class="sxs-lookup"><span data-stu-id="ac211-152">None</span></span>                                                                        |
| [<span data-ttu-id="ac211-153">**Cercanos**</span><span class="sxs-lookup"><span data-stu-id="ac211-153">**Close**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-close)                                               | <span data-ttu-id="ac211-154">Método</span><span class="sxs-lookup"><span data-stu-id="ac211-154">Method</span></span>      | <span data-ttu-id="ac211-155">None</span><span class="sxs-lookup"><span data-stu-id="ac211-155">None</span></span>                                                                        |
| [<span data-ttu-id="ac211-156">**SetVisualState**</span><span class="sxs-lookup"><span data-stu-id="ac211-156">**SetVisualState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-setvisualstate)                             | <span data-ttu-id="ac211-157">Método</span><span class="sxs-lookup"><span data-stu-id="ac211-157">Method</span></span>      | <span data-ttu-id="ac211-158">None</span><span class="sxs-lookup"><span data-stu-id="ac211-158">None</span></span>                                                                        |
| [<span data-ttu-id="ac211-159">**WaitForInputIdle**</span><span class="sxs-lookup"><span data-stu-id="ac211-159">**WaitForInputIdle**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-waitforinputidle)                         | <span data-ttu-id="ac211-160">Método</span><span class="sxs-lookup"><span data-stu-id="ac211-160">Method</span></span>      | <span data-ttu-id="ac211-161">None</span><span class="sxs-lookup"><span data-stu-id="ac211-161">None</span></span>                                                                        |
| [<span data-ttu-id="ac211-162">**Ventana de UIA \_ \_ WindowClosedEventId**</span><span class="sxs-lookup"><span data-stu-id="ac211-162">**UIA\_Window\_WindowClosedEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="ac211-163">Evento</span><span class="sxs-lookup"><span data-stu-id="ac211-163">Event</span></span>       | <span data-ttu-id="ac211-164">None</span><span class="sxs-lookup"><span data-stu-id="ac211-164">None</span></span>                                                                        |
| [<span data-ttu-id="ac211-165">**Ventana de UIA \_ \_ WindowOpenedEventId**</span><span class="sxs-lookup"><span data-stu-id="ac211-165">**UIA\_Window\_WindowOpenedEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="ac211-166">Evento</span><span class="sxs-lookup"><span data-stu-id="ac211-166">Event</span></span>       | <span data-ttu-id="ac211-167">None</span><span class="sxs-lookup"><span data-stu-id="ac211-167">None</span></span>                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="ac211-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ac211-168">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ac211-169">**Vista**</span><span class="sxs-lookup"><span data-stu-id="ac211-169">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ac211-170">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="ac211-170">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="ac211-171">Asignación de patrones de controles para clientes de UI Automation</span><span class="sxs-lookup"><span data-stu-id="ac211-171">Control Pattern Mapping for UI Automation Clients</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="ac211-172">Información general sobre el árbol de la UI Automation</span><span class="sxs-lookup"><span data-stu-id="ac211-172">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




