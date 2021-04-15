---
title: Recuperar propiedades de elementos de UI Automation
description: Las propiedades de los objetos IUIAutomationElement contienen información sobre los elementos de la interfaz de usuario, normalmente controles.
ms.assetid: e358fd67-22d0-4e43-a138-8afcc45f130e
keywords:
- clientes, obtener elementos de UI Automation
- clientes, elementos de UI Automation
- clientes, propiedades
- clientes, recuperar propiedades
- clientes, propiedades de UI Automation
- Automatización de la interfaz de usuario, obtener elementos
- Automatización de la interfaz de usuario, elementos
- Automatización de la interfaz de usuario, propiedades
- Automatización de la interfaz de usuario, recuperar propiedades
- recuperar propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e199522dbefaa2f722a67b0ede57fe910b8ed63b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695714"
---
# <a name="retrieving-properties-from-ui-automation-elements"></a><span data-ttu-id="a6a24-113">Recuperar propiedades de elementos de UI Automation</span><span class="sxs-lookup"><span data-stu-id="a6a24-113">Retrieving Properties from UI Automation Elements</span></span>

<span data-ttu-id="a6a24-114">Las propiedades de los objetos [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) contienen información sobre los elementos de la interfaz de usuario, normalmente controles.</span><span class="sxs-lookup"><span data-stu-id="a6a24-114">Properties on [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) objects contain information about UI elements, usually controls.</span></span> <span data-ttu-id="a6a24-115">Las propiedades de un elemento son genéricas; es decir, no es específico de un tipo de control.</span><span class="sxs-lookup"><span data-stu-id="a6a24-115">The properties of an element are generic; that is, not specific to a control type.</span></span> <span data-ttu-id="a6a24-116">Las propiedades específicas del control de un elemento se exponen mediante sus interfaces de patrón de control.</span><span class="sxs-lookup"><span data-stu-id="a6a24-116">Control-specific properties of an element are exposed by its control pattern interfaces.</span></span>

<span data-ttu-id="a6a24-117">Las propiedades de automatización de la interfaz de usuario de Microsoft son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a6a24-117">Microsoft UI Automation properties are read-only.</span></span> <span data-ttu-id="a6a24-118">Para establecer las propiedades de un control, debe utilizar los métodos del patrón de control adecuado.</span><span class="sxs-lookup"><span data-stu-id="a6a24-118">To set properties of a control, you must use the methods of the appropriate control pattern.</span></span> <span data-ttu-id="a6a24-119">Por ejemplo, utilice [**IUIAutomationScrollPattern:: scroll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollpattern-scroll) para cambiar los valores de posición de una ventana desplazable.</span><span class="sxs-lookup"><span data-stu-id="a6a24-119">For example, use [**IUIAutomationScrollPattern::Scroll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollpattern-scroll) to change the position values of a scrolling window.</span></span>

<span data-ttu-id="a6a24-120">Para mejorar el rendimiento, los valores de propiedad de los controles y los patrones de control se pueden almacenar en caché cuando se recuperan los elementos.</span><span class="sxs-lookup"><span data-stu-id="a6a24-120">To improve performance, property values of controls and control patterns can be cached when elements are retrieved.</span></span> <span data-ttu-id="a6a24-121">Para obtener más información, vea [caching UI Automation Properties and Control Patterns](uiauto-cachingforclients.md).</span><span class="sxs-lookup"><span data-stu-id="a6a24-121">For more information, see [Caching UI Automation Properties and Control Patterns](uiauto-cachingforclients.md).</span></span>

<span data-ttu-id="a6a24-122">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="a6a24-122">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a6a24-123">Identificadores de propiedad</span><span class="sxs-lookup"><span data-stu-id="a6a24-123">Property IDs</span></span>](#property-ids)
-   [<span data-ttu-id="a6a24-124">Condiciones de propiedad</span><span class="sxs-lookup"><span data-stu-id="a6a24-124">Property Conditions</span></span>](#property-conditions)
-   [<span data-ttu-id="a6a24-125">Recuperación de propiedades</span><span class="sxs-lookup"><span data-stu-id="a6a24-125">Retrieving Properties</span></span>](#retrieving-properties)
-   [<span data-ttu-id="a6a24-126">Valores de propiedad predeterminados</span><span class="sxs-lookup"><span data-stu-id="a6a24-126">Default Property Values</span></span>](#default-property-values)
-   [<span data-ttu-id="a6a24-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a6a24-127">Related topics</span></span>](#related-topics)

## <a name="property-ids"></a><span data-ttu-id="a6a24-128">Identificadores de propiedad</span><span class="sxs-lookup"><span data-stu-id="a6a24-128">Property IDs</span></span>

<span data-ttu-id="a6a24-129">Los identificadores de propiedad se definen en Uiautomationclient. h.</span><span class="sxs-lookup"><span data-stu-id="a6a24-129">Property identifiers are defined in Uiautomationclient.h.</span></span> <span data-ttu-id="a6a24-130">Se usan para especificar propiedades al suscribirse a eventos de cambio de propiedad, recuperar valores de propiedad y construir condiciones de propiedad.</span><span class="sxs-lookup"><span data-stu-id="a6a24-130">They are used to specify properties when you subscribe to property-changed events, retrieve property values, and construct property conditions.</span></span> <span data-ttu-id="a6a24-131">Los identificadores de propiedad también identifican la propiedad que ha cambiado cuando se llama a [**IUIAutomationPropertyChangedEventHandler:: HandlePropertyChangedEvent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationpropertychangedeventhandler-handlepropertychangedevent) .</span><span class="sxs-lookup"><span data-stu-id="a6a24-131">Property identifiers also identify the property that has changed when [**IUIAutomationPropertyChangedEventHandler::HandlePropertyChangedEvent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationpropertychangedeventhandler-handlepropertychangedevent) is called.</span></span>

<span data-ttu-id="a6a24-132">Para obtener una lista de los identificadores de propiedad de automatización de la interfaz de usuario, vea [identificadores de propiedad](uiauto-entry-propids.md).</span><span class="sxs-lookup"><span data-stu-id="a6a24-132">For a list of UI Automation property identifiers, see [Property Identifiers](uiauto-entry-propids.md).</span></span>

## <a name="property-conditions"></a><span data-ttu-id="a6a24-133">Condiciones de propiedad</span><span class="sxs-lookup"><span data-stu-id="a6a24-133">Property Conditions</span></span>

<span data-ttu-id="a6a24-134">Los identificadores de propiedad se utilizan para construir objetos [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition) que se usan para buscar elementos de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="a6a24-134">The property IDs are used in constructing [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition) objects that are used to find UI Automation elements.</span></span> <span data-ttu-id="a6a24-135">Por ejemplo, puede que desee buscar un elemento que tenga un nombre determinado o todos los controles que están habilitados.</span><span class="sxs-lookup"><span data-stu-id="a6a24-135">For example, you might want to find an element that has a certain name, or all controls that are enabled.</span></span> <span data-ttu-id="a6a24-136">Cada condición de propiedad especifica un identificador de propiedad y el valor que debe coincidir con la propiedad.</span><span class="sxs-lookup"><span data-stu-id="a6a24-136">Each property condition specifies a property identifier and the value that the property must match.</span></span>

<span data-ttu-id="a6a24-137">Para más información, consulte los temas de referencia siguientes:</span><span class="sxs-lookup"><span data-stu-id="a6a24-137">For more information, see the following reference topics:</span></span>

-   [<span data-ttu-id="a6a24-138">**IUIAutomation::CreatePropertyCondition**</span><span class="sxs-lookup"><span data-stu-id="a6a24-138">**IUIAutomation::CreatePropertyCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition)
-   [<span data-ttu-id="a6a24-139">**IUIAutomation::CreatePropertyConditionEx**</span><span class="sxs-lookup"><span data-stu-id="a6a24-139">**IUIAutomation::CreatePropertyConditionEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertyconditionex)
-   [<span data-ttu-id="a6a24-140">**IUIAutomationElement:: FindFirst**</span><span class="sxs-lookup"><span data-stu-id="a6a24-140">**IUIAutomationElement::FindFirst**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst)
-   [<span data-ttu-id="a6a24-141">**IUIAutomationElement:: FindAll**</span><span class="sxs-lookup"><span data-stu-id="a6a24-141">**IUIAutomationElement::FindAll**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)

## <a name="retrieving-properties"></a><span data-ttu-id="a6a24-142">Recuperación de propiedades</span><span class="sxs-lookup"><span data-stu-id="a6a24-142">Retrieving Properties</span></span>

<span data-ttu-id="a6a24-143">Algunas propiedades genéricas, y todas las propiedades de patrón de control, están disponibles como propiedades en la interfaz de patrón de control o [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) , y se pueden recuperar con un descriptor de acceso, como [**IUIAutomationElement:: CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) o [**CachedDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-get_cacheddockposition).</span><span class="sxs-lookup"><span data-stu-id="a6a24-143">Some generic properties, and all control pattern properties, are available as properties on the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) or control pattern interface and can be retrieved by using an accessor, such as [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) or [**CachedDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-get_cacheddockposition).</span></span>

<span data-ttu-id="a6a24-144">Además, cualquier propiedad actual o almacenada en caché (que no sea propiedades de patrón de control) se puede recuperar utilizando uno de los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a6a24-144">In addition, any current or cached property (other than control pattern properties) can be retrieved by using one of the following methods:</span></span>

-   [<span data-ttu-id="a6a24-145">**GetCurrentPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="a6a24-145">**GetCurrentPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
-   [<span data-ttu-id="a6a24-146">**GetCurrentPropertyValueEx**</span><span class="sxs-lookup"><span data-stu-id="a6a24-146">**GetCurrentPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
-   [<span data-ttu-id="a6a24-147">**GetCachedPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="a6a24-147">**GetCachedPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
-   [<span data-ttu-id="a6a24-148">**GetCachedPropertyValueEx**</span><span class="sxs-lookup"><span data-stu-id="a6a24-148">**GetCachedPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)

<span data-ttu-id="a6a24-149">Estos métodos ofrecen un rendimiento ligeramente mejor y acceso a toda la gama de propiedades.</span><span class="sxs-lookup"><span data-stu-id="a6a24-149">These methods offer slightly better performance and access to the full range of properties.</span></span> <span data-ttu-id="a6a24-150">Sin embargo, los valores se devuelven en estructuras [**variantes**](/windows/win32/api/oaidl/ns-oaidl-variant) , mientras que los descriptores de acceso de propiedad individuales convierten el valor al tipo adecuado.</span><span class="sxs-lookup"><span data-stu-id="a6a24-150">However, values are returned in [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structures, whereas the individual property accessors cast the value to the appropriate type.</span></span>

## <a name="default-property-values"></a><span data-ttu-id="a6a24-151">Valores de propiedad predeterminados</span><span class="sxs-lookup"><span data-stu-id="a6a24-151">Default Property Values</span></span>

<span data-ttu-id="a6a24-152">Si un proveedor de automatización de la interfaz de usuario no implementa una propiedad, la automatización de la interfaz de usuario puede proporcionar un valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a6a24-152">If a UI Automation provider does not implement a property, UI Automation can supply a default value.</span></span> <span data-ttu-id="a6a24-153">Por ejemplo, si el proveedor de un control no admite la propiedad identificada por [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md), la automatización de la interfaz de usuario devuelve una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="a6a24-153">For example, if the provider for a control does not support the property identified by [**UIA\_HelpTextPropertyId**](uiauto-automation-element-propids.md), UI Automation returns an empty string.</span></span> <span data-ttu-id="a6a24-154">Del mismo modo, si el proveedor no admite la propiedad identificada por [**UIA \_ IsDockPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md), la automatización de la interfaz de usuario devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="a6a24-154">Similarly, if the provider does not support the property identified by [**UIA\_IsDockPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md), UI Automation returns **FALSE**.</span></span>

<span data-ttu-id="a6a24-155">La diferencia entre [**IUIAutomationElement:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) y [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex) (y entre pares similares de métodos) es que el método "ex" puede especificar que no se devuelva ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a6a24-155">The difference between [**IUIAutomationElement::GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) and [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex) (and between similar pairs of methods) is that the "Ex" method can specify that no default value is to be returned.</span></span> <span data-ttu-id="a6a24-156">En este caso, el valor devuelto es una constante única especial, que indica que no se admite la propiedad.</span><span class="sxs-lookup"><span data-stu-id="a6a24-156">In this case, the return value is a special unique constant, indicating that the property is not supported.</span></span> <span data-ttu-id="a6a24-157">Al recibir este valor, la aplicación puede proporcionar su propio valor o simplemente omitir la propiedad.</span><span class="sxs-lookup"><span data-stu-id="a6a24-157">On receiving this value, the application can supply its own value or simply ignore the property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6a24-158">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a6a24-158">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a6a24-159">**Vista**</span><span class="sxs-lookup"><span data-stu-id="a6a24-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a6a24-160">Información general acerca de las propiedades de UI Automation</span><span class="sxs-lookup"><span data-stu-id="a6a24-160">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="a6a24-161">Identificadores de propiedad</span><span class="sxs-lookup"><span data-stu-id="a6a24-161">Property Identifiers</span></span>](uiauto-entry-propids.md)
</dt> </dl>

 

 