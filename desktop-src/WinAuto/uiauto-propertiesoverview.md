---
title: Información general acerca de las propiedades de UI Automation
description: Los proveedores de automatización de la interfaz de usuario de Microsoft exponen propiedades en elementos de UI Automation Las propiedades permiten a las aplicaciones cliente recuperar información acerca de los controles.
ms.assetid: 35f017cb-f50a-4680-9f01-5079aa59da73
keywords:
- Automatización de la interfaz de usuario, información general sobre propiedades
- Automatización de la interfaz de usuario, propiedades frente a eventos
- Automatización de la interfaz de usuario, eventos frente a propiedades
- propiedades, acerca de
- propiedades, identificadores
- propiedades, valores
- propiedades, eventos
- eventos, propiedades
- propiedades, dinámicas
- propiedades dinámicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f4e5e1b29ae516059a531b17d50d0631282f82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268208"
---
# <a name="ui-automation-properties-overview"></a><span data-ttu-id="4652b-114">Información general acerca de las propiedades de UI Automation</span><span class="sxs-lookup"><span data-stu-id="4652b-114">UI Automation Properties Overview</span></span>

<span data-ttu-id="4652b-115">Los proveedores de automatización de la interfaz de usuario de Microsoft exponen propiedades en elementos de UI Automation</span><span class="sxs-lookup"><span data-stu-id="4652b-115">Microsoft UI Automation providers expose properties on UI Automation elements.</span></span> <span data-ttu-id="4652b-116">Las propiedades permiten a las aplicaciones cliente recuperar información acerca de los controles.</span><span class="sxs-lookup"><span data-stu-id="4652b-116">Properties enable client applications to retrieve information about controls.</span></span>

<span data-ttu-id="4652b-117">La automatización de la interfaz de usuario expone dos tipos diferentes de propiedades: *las propiedades de los elementos de automatización y las propiedades* de los patrones de *control*.</span><span class="sxs-lookup"><span data-stu-id="4652b-117">UI Automation exposes two different kinds of properties: *automation element properties*, and *control pattern propertes*.</span></span> <span data-ttu-id="4652b-118">Las propiedades del elemento de automatización se componen de un conjunto común de propiedades, como name, AcceleratorKey y ClassName, que exponen todos los elementos de automatización de la interfaz de usuario, independientemente del tipo de control.</span><span class="sxs-lookup"><span data-stu-id="4652b-118">The automation element properties consist of a common set of properties, such as Name, AcceleratorKey, and ClassName, that are exposed by all UI Automation elements, regardless of the control type.</span></span> <span data-ttu-id="4652b-119">La mayoría de las propiedades de elemento de automatización son valores estáticos.</span><span class="sxs-lookup"><span data-stu-id="4652b-119">Most automation element properties are static values.</span></span>

<span data-ttu-id="4652b-120">Las propiedades de patrón de control son las que expone un control que admite un patrón de control determinado.</span><span class="sxs-lookup"><span data-stu-id="4652b-120">Control pattern properties are those that are exposed by a control that supports a particular control pattern.</span></span> <span data-ttu-id="4652b-121">Cada patrón de control tiene un conjunto correspondiente de propiedades de patrón de control que debe exponer el control.</span><span class="sxs-lookup"><span data-stu-id="4652b-121">Each control pattern has a corresponding set of control pattern properties that the control must expose.</span></span> <span data-ttu-id="4652b-122">Por ejemplo, un control que admite el patrón de control [Grid](uiauto-implementinggrid.md) expone las propiedades ColumnCount y RowCount.</span><span class="sxs-lookup"><span data-stu-id="4652b-122">For example, a control that supports the [Grid](uiauto-implementinggrid.md) control pattern exposes the ColumnCount and RowCount properties.</span></span> <span data-ttu-id="4652b-123">La mayoría de las propiedades de patrón de control son valores dinámicos.</span><span class="sxs-lookup"><span data-stu-id="4652b-123">Most control pattern properties are dynamic values.</span></span>

<span data-ttu-id="4652b-124">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="4652b-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="4652b-125">Identificadores de propiedad</span><span class="sxs-lookup"><span data-stu-id="4652b-125">Property Identifiers</span></span>](#property-identifiers)
-   [<span data-ttu-id="4652b-126">Valores de propiedad</span><span class="sxs-lookup"><span data-stu-id="4652b-126">Property Values</span></span>](#property-values)
-   [<span data-ttu-id="4652b-127">Propiedades y eventos</span><span class="sxs-lookup"><span data-stu-id="4652b-127">Properties and Events</span></span>](#properties-and-events)
-   [<span data-ttu-id="4652b-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4652b-128">Related topics</span></span>](#related-topics)

## <a name="property-identifiers"></a><span data-ttu-id="4652b-129">Identificadores de propiedad</span><span class="sxs-lookup"><span data-stu-id="4652b-129">Property Identifiers</span></span>

<span data-ttu-id="4652b-130">Cada propiedad se identifica mediante un valor numérico de **PROPERTYID** denominado *identificador de propiedad* (ID).</span><span class="sxs-lookup"><span data-stu-id="4652b-130">Every property is identified by a **PROPERTYID** numeric value called a *property identifier* (ID).</span></span> <span data-ttu-id="4652b-131">Los proveedores y los clientes usan los identificadores numéricos en llamadas a métodos como [**IRawElementProviderAdviseEvents:: AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) y [**IUIAutomationElement:: GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue) para identificar las solicitudes de propiedad.</span><span class="sxs-lookup"><span data-stu-id="4652b-131">Providers and clients use the numeric IDs in method calls such as [**IRawElementProviderAdviseEvents::AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) and [**IUIAutomationElement::GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue) to identify property requests.</span></span> <span data-ttu-id="4652b-132">Para obtener una descripción detallada de cada identificador de propiedad de automatización de la interfaz de usuario, incluido el tipo de datos y el valor predeterminado de cada propiedad, vea [identificadores de propiedad](uiauto-entry-propids.md).</span><span class="sxs-lookup"><span data-stu-id="4652b-132">For a detailed description of each UI Automation property identifier, including the data type and default value of each property, see [Property Identifiers](uiauto-entry-propids.md).</span></span>

## <a name="property-values"></a><span data-ttu-id="4652b-133">Valores de propiedad</span><span class="sxs-lookup"><span data-stu-id="4652b-133">Property Values</span></span>

<span data-ttu-id="4652b-134">Todas las propiedades son de solo lectura, aunque algunas se pueden cambiar mediante métodos que actúan sobre el control, como [**IDockProvider:: SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) (Provider) o [**IUIAutomationDockPattern:: SetDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition) (Client).</span><span class="sxs-lookup"><span data-stu-id="4652b-134">All properties are read-only, although some can be changed by using methods that act on the control, such as [**IDockProvider::SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) (provider) or [**IUIAutomationDockPattern::SetDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition) (client).</span></span>

<span data-ttu-id="4652b-135">Para obtener información sobre cómo recuperar los valores de propiedad, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="4652b-135">For information about retrieving property values, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>

## <a name="properties-and-events"></a><span data-ttu-id="4652b-136">Propiedades y eventos</span><span class="sxs-lookup"><span data-stu-id="4652b-136">Properties and Events</span></span>

<span data-ttu-id="4652b-137">Estrechamente asociados a las propiedades de la automatización de la interfaz de usuario es el concepto de *eventos de cambio de propiedad*.</span><span class="sxs-lookup"><span data-stu-id="4652b-137">Closely associated with the properties in UI Automation is the concept of *property-changed events*.</span></span> <span data-ttu-id="4652b-138">En el caso de las propiedades dinámicas, una aplicación cliente necesita una manera de saber que un valor de propiedad ha cambiado, de modo que puede actualizar su caché de información o reaccionar a la nueva información de alguna otra manera.</span><span class="sxs-lookup"><span data-stu-id="4652b-138">For dynamic properties, a client application needs a way to know that a property value has changed, so that it can update its cache of information or react to the new information in some other way.</span></span> <span data-ttu-id="4652b-139">Los clientes se pueden registrar para escuchar eventos de cambio de propiedad en cualquier propiedad.</span><span class="sxs-lookup"><span data-stu-id="4652b-139">Clients can register to listen for property-changed events on any property.</span></span>

<span data-ttu-id="4652b-140">Los proveedores generan eventos cuando cambia algo en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4652b-140">Providers raise events when something in the UI changes.</span></span> <span data-ttu-id="4652b-141">Por ejemplo, si una casilla está activada o desactivada, la implementación del proveedor del patrón de control [Toggle](uiauto-implementingtoggle.md) genera un evento de cambio de propiedad.</span><span class="sxs-lookup"><span data-stu-id="4652b-141">For example, if a check box is selected or cleared, a property-changed event is raised by the provider implementation of the [Toggle](uiauto-implementingtoggle.md) control pattern.</span></span> <span data-ttu-id="4652b-142">Los proveedores pueden generar eventos de forma selectiva, dependiendo de si hay clientes en escucha de eventos o en escucha de eventos específicos.</span><span class="sxs-lookup"><span data-stu-id="4652b-142">Providers can raise events selectively, depending on whether any clients are listening for events, or listening for specific events.</span></span>

<span data-ttu-id="4652b-143">No todos los cambios de propiedades generan eventos; esto depende totalmente de la implementación del proveedor de Automatización de la interfaz de usuario del elemento.</span><span class="sxs-lookup"><span data-stu-id="4652b-143">Not all property changes raise events; that is entirely up to the implementation of the UI Automation provider for the element.</span></span> <span data-ttu-id="4652b-144">Por ejemplo, los proveedores de proxy estándar para los cuadros de lista no generan un evento de cambio de propiedad cuando cambia la propiedad de selección.</span><span class="sxs-lookup"><span data-stu-id="4652b-144">For example, the standard proxy providers for list boxes do not raise a property-changed event when the Selection property changes.</span></span> <span data-ttu-id="4652b-145">En este caso, la aplicación debe escuchar el evento que se genera cuando cambia la selección ([**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="4652b-145">In this case, the application must listen for the event raised when the selection changes ([**UIA\_SelectionItem\_ElementSelectedEventId**](uiauto-event-ids.md)).</span></span>

<span data-ttu-id="4652b-146">Los clientes escuchan eventos mediante su suscripción, como se describe en [suscribirse a eventos de automatización de la interfaz de usuario](uiauto-eventsforclients.md).</span><span class="sxs-lookup"><span data-stu-id="4652b-146">Clients listen for events by subscribing to them, as described at [Subscribing to UI Automation Events](uiauto-eventsforclients.md).</span></span> <span data-ttu-id="4652b-147">En el caso de los eventos de cambio de propiedad en concreto, los clientes deben implementar [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) y pasar la interfaz a [**IUIAutomation:: AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) o [**IUIAutomation:: AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray).</span><span class="sxs-lookup"><span data-stu-id="4652b-147">For property-changed events in particular, clients must implement [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) and pass the interface to [**IUIAutomation::AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) or [**IUIAutomation::AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4652b-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4652b-148">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4652b-149">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="4652b-149">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4652b-150">**GetCurrentPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="4652b-150">**GetCurrentPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
</dt> <dt>

[<span data-ttu-id="4652b-151">**GetCurrentPropertyValueEx**</span><span class="sxs-lookup"><span data-stu-id="4652b-151">**GetCurrentPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
</dt> <dt>

[<span data-ttu-id="4652b-152">**GetCachedPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="4652b-152">**GetCachedPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
</dt> <dt>

[<span data-ttu-id="4652b-153">**GetCachedPropertyValueEx**</span><span class="sxs-lookup"><span data-stu-id="4652b-153">**GetCachedPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)
</dt> <dt>

<span data-ttu-id="4652b-154">**Vista**</span><span class="sxs-lookup"><span data-stu-id="4652b-154">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4652b-155">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="4652b-155">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="4652b-156">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="4652b-156">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="4652b-157">Información general sobre eventos de UI Automation</span><span class="sxs-lookup"><span data-stu-id="4652b-157">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> </dl>

 

 




