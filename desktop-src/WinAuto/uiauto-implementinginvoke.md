---
title: Invocar patrón de control
description: Describe las directrices y convenciones para implementar IInvokeProvider, incluida información sobre los métodos.
ms.assetid: 6557a03c-fd1f-4e44-8393-fe367d7a17af
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control Invoke
- UI Automation, Invoke (patrón de control)
- Automatización de la interfaz de usuario, IInvokeProvider
- IInvokeProvider
- implementar patrones de control de invocación de UI Automation
- Invocar patrones de control
- patrones de control, IInvokeProvider
- patrones de control, implementar invocación de UI Automation
- patrones de control, Invoke
- interfaces, IInvokeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963f8d9ccd6ea2a50557ec26a655d5c7f43c6123
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903363"
---
# <a name="invoke-control-pattern"></a><span data-ttu-id="86e0a-113">Invocar patrón de control</span><span class="sxs-lookup"><span data-stu-id="86e0a-113">Invoke Control Pattern</span></span>

<span data-ttu-id="86e0a-114">Describe las directrices y convenciones para implementar [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider), incluida información sobre los métodos.</span><span class="sxs-lookup"><span data-stu-id="86e0a-114">Describes guidelines and conventions for implementing [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider), including information about methods.</span></span> <span data-ttu-id="86e0a-115">El patrón de control **Invoke** se usa para admitir controles que no mantienen el estado cuando se activan, sino que inician o realizan una única acción inequívoca.</span><span class="sxs-lookup"><span data-stu-id="86e0a-115">The **Invoke** control pattern is used to support controls that do not maintain state when activated but rather initiate or perform a single, unambiguous action.</span></span>

<span data-ttu-id="86e0a-116">Los controles que mantienen el estado, como las casillas y los botones de radio, deben implementar [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) y [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="86e0a-116">Controls that do maintain state, such as check boxes and radio buttons, must instead implement [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) and [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) respectively.</span></span> <span data-ttu-id="86e0a-117">Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="86e0a-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="86e0a-118">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="86e0a-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="86e0a-119">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="86e0a-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="86e0a-120">Miembros requeridos para **IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="86e0a-120">Required Members for **IInvokeProvider**</span></span>](#required-members-for-iinvokeprovider)
-   [<span data-ttu-id="86e0a-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="86e0a-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="86e0a-122">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="86e0a-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="86e0a-123">Al implementar el patrón de control **Invoke** , tenga en cuenta las siguientes directrices y convenciones:</span><span class="sxs-lookup"><span data-stu-id="86e0a-123">When implementing the **Invoke** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="86e0a-124">Los controles implementan [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) si el mismo comportamiento no se expone a través de otro proveedor de patrones de control.</span><span class="sxs-lookup"><span data-stu-id="86e0a-124">Controls implement [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) if the same behavior is not exposed through another control pattern provider.</span></span> <span data-ttu-id="86e0a-125">Por ejemplo, si el método [**IUIAutomationInvokePattern:: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) de un control realiza la misma acción que el método [**IUIAutomationExpandCollapsePattern:: Expand**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-expand) o [**Collapse**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-collapse) , el control no debe implementar **IInvokeProvider**.</span><span class="sxs-lookup"><span data-stu-id="86e0a-125">For example, if the [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) method on a control performs the same action as the [**IUIAutomationExpandCollapsePattern::Expand**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-expand) or [**Collapse**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-collapse) method, the control should not implement **IInvokeProvider**.</span></span>
-   <span data-ttu-id="86e0a-126">Generalmente, la invocación de un control se realiza con un clic, un doble clic, presionando la tecla ENTRAR, usando un método abreviado de teclado predefinido o alguna combinación alternativa de pulsaciones de teclas.</span><span class="sxs-lookup"><span data-stu-id="86e0a-126">Invoking a control is generally performed by clicking or double-clicking or pressing ENTER, a predefined keyboard shortcut, or some alternate combination of keystrokes.</span></span>
-   <span data-ttu-id="86e0a-127">El evento **invocado** Event ([**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)) se genera en un control que se ha activado (como respuesta a un control que lleva a cabo su acción asociada).</span><span class="sxs-lookup"><span data-stu-id="86e0a-127">The **Invoked** event ([**UIA\_Invoke\_InvokedEventId**](uiauto-event-ids.md)) event is raised on a control that has been activated (as a response to a control carrying out its associated action).</span></span> <span data-ttu-id="86e0a-128">Si es posible, se debe generar el evento después de que el control haya completado la acción y haya hecho la devolución sin bloquearse.</span><span class="sxs-lookup"><span data-stu-id="86e0a-128">If possible, the event should be raised after the control has completed the action and returned without blocking.</span></span> <span data-ttu-id="86e0a-129">El evento **invocado** (**InvokedEventId de la \_ invocación \_ de UIA**) debe generarse antes de atender la solicitud de **invocación** en los escenarios siguientes:</span><span class="sxs-lookup"><span data-stu-id="86e0a-129">The **Invoked** event (**UIA\_Invoke\_InvokedEventId**) should be raised before servicing the **Invoke** request in the following scenarios:</span></span>
    -   <span data-ttu-id="86e0a-130">No es posible ni práctico esperar hasta que se complete la acción.</span><span class="sxs-lookup"><span data-stu-id="86e0a-130">It is not possible or practical to wait until the action is complete.</span></span>
    -   <span data-ttu-id="86e0a-131">La acción requiere la interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="86e0a-131">The action requires user interaction.</span></span>
    -   <span data-ttu-id="86e0a-132">La acción requiere mucho tiempo y provocará que el cliente que llama se bloquee durante un tiempo considerable.</span><span class="sxs-lookup"><span data-stu-id="86e0a-132">The action is time-consuming and will cause the calling client to block for a significant amount of time.</span></span>
-   <span data-ttu-id="86e0a-133">Si la invocación del control tiene efectos secundarios significativos, esos efectos secundarios se deben exponer a través de la propiedad **HelpText** .</span><span class="sxs-lookup"><span data-stu-id="86e0a-133">If invoking the control has significant side-effects, those side-effects should be exposed through the **HelpText** property.</span></span> <span data-ttu-id="86e0a-134">Por ejemplo, aunque [**IUIAutomationInvokePattern:: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) no esté asociado a la selección, **Invoke** puede hacer que se seleccione otro control.</span><span class="sxs-lookup"><span data-stu-id="86e0a-134">For example, even though [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) is not associated with selection, **Invoke** may cause another control to become selected.</span></span>
-   <span data-ttu-id="86e0a-135">Normalmente, los efectos de mantener el puntero (o pasar el mouse por encima) no constituyen un evento **invocado** .</span><span class="sxs-lookup"><span data-stu-id="86e0a-135">Hover (or mouse-over) effects generally do not constitute an **Invoked** event.</span></span> <span data-ttu-id="86e0a-136">Sin embargo, los controles que realizan una acción (en lugar de producir un efecto visual) basados en el estado de desplazamiento deben admitir el patrón de control **Invoke** .</span><span class="sxs-lookup"><span data-stu-id="86e0a-136">However, controls that perform an action (as opposed to cause a visual effect) based on the hover state should support the **Invoke** control pattern.</span></span>
    > [!Note]  
    > <span data-ttu-id="86e0a-137">Esta implementación se considera un problema de accesibilidad si el control solo se puede invocar como resultado de un efecto secundario relacionado con el mouse.</span><span class="sxs-lookup"><span data-stu-id="86e0a-137">This implementation is considered an accessibility issue if the control can be invoked only as a result of a mouse-related side effect.</span></span>

     

-   <span data-ttu-id="86e0a-138">La invocación de un control es diferente de la selección de un elemento.</span><span class="sxs-lookup"><span data-stu-id="86e0a-138">Invoking a control is different from selecting an item.</span></span> <span data-ttu-id="86e0a-139">No obstante, dependiendo del control, su invocación puede provocar que el elemento se seleccione como un efecto secundario.</span><span class="sxs-lookup"><span data-stu-id="86e0a-139">However, depending on the control, invoking it may cause the item to become selected as a side-effect.</span></span> <span data-ttu-id="86e0a-140">Por ejemplo, la invocación de un elemento de lista de documentos de Microsoft Word en la carpeta Mis documentos selecciona el elemento y abre el documento.</span><span class="sxs-lookup"><span data-stu-id="86e0a-140">For example, invoking a Microsoft Word document list item in the My Documents folder both selects the item and opens the document.</span></span>
-   <span data-ttu-id="86e0a-141">Un elemento puede desaparecer del árbol de automatización de la interfaz de usuario de Microsoft inmediatamente después de que se invoque.</span><span class="sxs-lookup"><span data-stu-id="86e0a-141">An element can disappear from the Microsoft UI Automation tree immediately upon being invoked.</span></span> <span data-ttu-id="86e0a-142">La solicitud de información del elemento que proporciona la devolución de llamada de evento puede producir un error como resultado.</span><span class="sxs-lookup"><span data-stu-id="86e0a-142">Requesting information from the element provided by the event callback may fail as a result.</span></span> <span data-ttu-id="86e0a-143">La solución recomendada es la captura previa de la información almacenada en caché.</span><span class="sxs-lookup"><span data-stu-id="86e0a-143">Pre-fetching cached information is the recommended workaround.</span></span>
-   <span data-ttu-id="86e0a-144">Los controles pueden implementar varios patrones de control.</span><span class="sxs-lookup"><span data-stu-id="86e0a-144">Controls can implement multiple control patterns.</span></span> <span data-ttu-id="86e0a-145">Por ejemplo, el control **color de relleno** de la barra de herramientas de Microsoft Excel implementa los patrones de control Invoke y [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="86e0a-145">For example, the **Fill Color** control on the Microsoft Excel toolbar implements both the Invoke and the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control patterns.</span></span> <span data-ttu-id="86e0a-146">El patrón de control ExpandCollapse expone el menú y el patrón de control **Invoke** rellena la selección activa con el color elegido.</span><span class="sxs-lookup"><span data-stu-id="86e0a-146">The ExpandCollapse control pattern exposes the menu and the **Invoke** control pattern fills the active selection with the chosen color.</span></span>

## <a name="required-members-for-iinvokeprovider"></a><span data-ttu-id="86e0a-147">Miembros requeridos para **IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="86e0a-147">Required Members for **IInvokeProvider**</span></span>

<span data-ttu-id="86e0a-148">El método siguiente es necesario para implementar la interfaz [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) .</span><span class="sxs-lookup"><span data-stu-id="86e0a-148">The following method is required for implementing the [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) interface.</span></span>



| <span data-ttu-id="86e0a-149">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="86e0a-149">Required members</span></span>                                | <span data-ttu-id="86e0a-150">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="86e0a-150">Member type</span></span> | <span data-ttu-id="86e0a-151">Notas</span><span class="sxs-lookup"><span data-stu-id="86e0a-151">Notes</span></span>                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="86e0a-152">**Invocar**</span><span class="sxs-lookup"><span data-stu-id="86e0a-152">**Invoke**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) | <span data-ttu-id="86e0a-153">Método</span><span class="sxs-lookup"><span data-stu-id="86e0a-153">Method</span></span>      | <span data-ttu-id="86e0a-154">**Invoke** es una llamada asincrónica y debe volver inmediatamente sin bloquearse.</span><span class="sxs-lookup"><span data-stu-id="86e0a-154">**Invoke** is an asynchronous call and must return immediately without blocking.</span></span><br/> <span data-ttu-id="86e0a-155">Este comportamiento es especialmente importante para los controles que, directa o indirectamente, inician un cuadro de diálogo modal cuando se invocan.</span><span class="sxs-lookup"><span data-stu-id="86e0a-155">This behavior is particularly critical for controls that, directly or indirectly, launch a modal dialog when invoked.</span></span> <span data-ttu-id="86e0a-156">Cualquier cliente de Automatización de la interfaz de usuario que haya provocado que el evento permanezca bloqueado hasta que se cierre el cuadro de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="86e0a-156">Any UI Automation client that instigated the event will remain blocked until the modal dialog is closed.</span></span> <br/> |



 

<span data-ttu-id="86e0a-157">Este patrón de control no tiene eventos o propiedades asociados.</span><span class="sxs-lookup"><span data-stu-id="86e0a-157">This control pattern has no associated properties or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86e0a-158">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="86e0a-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86e0a-159">Tipos de control y sus patrones de control admitidos</span><span class="sxs-lookup"><span data-stu-id="86e0a-159">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="86e0a-160">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="86e0a-160">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="86e0a-161">Información general sobre el árbol de la UI Automation</span><span class="sxs-lookup"><span data-stu-id="86e0a-161">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="86e0a-162">**\_InvokedEventId de invocación de UIA \_**</span><span class="sxs-lookup"><span data-stu-id="86e0a-162">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)
</dt> </dl>

 

 





