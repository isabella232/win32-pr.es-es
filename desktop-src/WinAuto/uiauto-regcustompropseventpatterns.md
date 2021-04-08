---
title: Registrar propiedades, eventos y patrones de control personalizados
description: Antes de que se pueda usar una propiedad personalizada, un evento o un patrón de control, tanto el proveedor como el cliente deben registrar la propiedad, el evento o el patrón de control en tiempo de ejecución.
ms.assetid: ae36e404-8432-46ed-930e-b86dd5a88d6d
keywords:
- Automatización de la interfaz de usuario, propiedades personalizadas
- Automatización de la interfaz de usuario, información general sobre eventos
- UI Automation, información general sobre los patrones de control
- Automatización de la interfaz de usuario, registrar propiedades personalizadas
- Automatización de la interfaz de usuario, registrar eventos
- Automatización de la interfaz de usuario, registrar patrones de control
- propiedades personalizadas, registrar
- eventos, registrar
- patrones de control, registrar
- registrar, propiedades personalizadas
- registrar, eventos
- registrar, patrones de control
- patrones de control, personalizados
- patrones de control, implementar personalizados
- implementar patrones de control personalizados
- patrones de control personalizados
- contenedores de cliente
- Controladores de patrón
- implementar controladores de patrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b6b157e8f08a2c0be74af6b9f53d3578d1e4d03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078192"
---
# <a name="register-custom-properties-events-and-control-patterns"></a><span data-ttu-id="4cb07-122">Registrar propiedades, eventos y patrones de control personalizados</span><span class="sxs-lookup"><span data-stu-id="4cb07-122">Register custom properties, events, and control patterns</span></span>

<span data-ttu-id="4cb07-123">Antes de que se pueda usar una propiedad personalizada, un evento o un patrón de control, tanto el proveedor como el cliente deben registrar la propiedad, el evento o el patrón de control en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="4cb07-123">Before a custom property, event, or control pattern can be used, both the provider and the client must register the property, event, or control pattern at run time.</span></span> <span data-ttu-id="4cb07-124">El registro es efectivo globalmente dentro de un proceso de aplicación y permanece efectivo hasta que se cierra el proceso o hasta que se libera el último objeto de elemento de automatización de la interfaz de usuario de Microsoft ([**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) o [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)) dentro del proceso.</span><span class="sxs-lookup"><span data-stu-id="4cb07-124">The registration is effective globally within an application process, and remains effective until the process closes or the last Microsoft UI Automation element object ([**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) or [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)) is released within the process.</span></span>

<span data-ttu-id="4cb07-125">El registro implica pasar un GUID a la automatización de la interfaz de usuario, junto con información detallada sobre la propiedad personalizada, el evento o el patrón de control.</span><span class="sxs-lookup"><span data-stu-id="4cb07-125">Registation involves passing a GUID to UI Automation, along with detailed information about the custom property, event, or control pattern.</span></span> <span data-ttu-id="4cb07-126">Si se intenta registrar el mismo GUID una segunda vez con la misma información, se realizará correctamente, pero se producirá un error al intentar registrar el mismo GUID una segunda vez pero con información diferente (por ejemplo, una propiedad personalizada de un tipo diferente).</span><span class="sxs-lookup"><span data-stu-id="4cb07-126">Attempting to register the same GUID a second time with the same information will succeed, but attempting to register the same GUID a second time but with different information (for example, a custom property of a different type) will fail.</span></span> <span data-ttu-id="4cb07-127">En el futuro, si se acepta la especificación personalizada y se integra en el núcleo de automatización de la interfaz de usuario, la automatización de la interfaz de usuario validará la información de registro personalizada y usará el código ya registrado en lugar de la implementación del marco "oficial", con lo que se minimizan los problemas de compatibilidad de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="4cb07-127">In the future, if the custom specification is accepted and integrated into the UI Automation core, UI Automation will validate the custom registration information and use the already registered code instead of the "official" framework implementation, thereby minimizing application compatibility issues.</span></span> <span data-ttu-id="4cb07-128">No se pueden quitar las propiedades, los eventos o los patrones de control que ya están registrados.</span><span class="sxs-lookup"><span data-stu-id="4cb07-128">You cannot remove properties, events, or control patterns that are already registered.</span></span>

<span data-ttu-id="4cb07-129">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="4cb07-129">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="4cb07-130">Registrar eventos y propiedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="4cb07-130">Registering Custom Properties and Events</span></span>](#registering-custom-properties-and-events)
-   [<span data-ttu-id="4cb07-131">Implementar patrones de control personalizados</span><span class="sxs-lookup"><span data-stu-id="4cb07-131">Implementing Custom Control Patterns</span></span>](#implementing-custom-control-patterns)
    -   [<span data-ttu-id="4cb07-132">Contenedor de cliente y controlador de patrón</span><span class="sxs-lookup"><span data-stu-id="4cb07-132">The Client Wrapper and the Pattern Handler</span></span>](#the-client-wrapper-and-the-pattern-handler)
    -   [<span data-ttu-id="4cb07-133">Implementar el contenedor de cliente</span><span class="sxs-lookup"><span data-stu-id="4cb07-133">Implementing the Client Wrapper</span></span>](#implementing-the-client-wrapper)
    -   [<span data-ttu-id="4cb07-134">Implementar el controlador de patrón</span><span class="sxs-lookup"><span data-stu-id="4cb07-134">Implementing the Pattern Handler</span></span>](#implementing-the-pattern-handler)
    -   [<span data-ttu-id="4cb07-135">Registrar un patrón de control personalizado</span><span class="sxs-lookup"><span data-stu-id="4cb07-135">Registering a Custom Control Pattern</span></span>](#registering-a-custom-control-pattern)
    -   [<span data-ttu-id="4cb07-136">Ejemplo de implementación de un patrón de control personalizado</span><span class="sxs-lookup"><span data-stu-id="4cb07-136">Example Implementation of a Custom Control Pattern</span></span>](#example-implementation-of-a-custom-control-pattern)
-   [<span data-ttu-id="4cb07-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4cb07-137">Related topics</span></span>](#related-topics)

## <a name="registering-custom-properties-and-events"></a><span data-ttu-id="4cb07-138">Registrar eventos y propiedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="4cb07-138">Registering Custom Properties and Events</span></span>

<span data-ttu-id="4cb07-139">El registro de una propiedad o un evento personalizado permite al proveedor y al cliente obtener un identificador para la propiedad o evento, que se puede pasar a los distintos métodos de API que toman los identificadores como parámetros.</span><span class="sxs-lookup"><span data-stu-id="4cb07-139">Registering a custom property or event enables the provider and client to obtain an ID for the property or event, which can then be passed to various API methods that take IDs as parameters.</span></span>

<span data-ttu-id="4cb07-140">Para registrar una propiedad o un evento:</span><span class="sxs-lookup"><span data-stu-id="4cb07-140">To register a property or event:</span></span>

1.  <span data-ttu-id="4cb07-141">Defina un GUID para la propiedad o el evento personalizado.</span><span class="sxs-lookup"><span data-stu-id="4cb07-141">Define a GUID for the custom property or event.</span></span>
2.  <span data-ttu-id="4cb07-142">Rellene una estructura [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) o [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) con información sobre la propiedad o el evento, incluido el GUID y una cadena no localizable que contenga el nombre de la propiedad o el evento personalizado.</span><span class="sxs-lookup"><span data-stu-id="4cb07-142">Fill a [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) or a [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) structure with information about the property or event, including the GUID and a nonlocalizable string that contains the name of the custom property or event.</span></span> <span data-ttu-id="4cb07-143">Las propiedades personalizadas también requieren el tipo de datos de la propiedad que se va a especificar, por ejemplo, si la propiedad contiene un entero o una cadena.</span><span class="sxs-lookup"><span data-stu-id="4cb07-143">Custom properties also require the data type of the property to be specified, for example, whether the property holds an integer or a string.</span></span> <span data-ttu-id="4cb07-144">El tipo de datos debe ser uno de los siguientes tipos especificados por la enumeración [**UIAutomationType**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) .</span><span class="sxs-lookup"><span data-stu-id="4cb07-144">The data type must be one of the following types specified by the [**UIAutomationType**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) enumeration.</span></span> <span data-ttu-id="4cb07-145">No se admiten otros tipos de datos para las propiedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="4cb07-145">No other data types are supported for custom properties.</span></span>
    -   <span data-ttu-id="4cb07-146">**UIAutomationType \_ bool**</span><span class="sxs-lookup"><span data-stu-id="4cb07-146">**UIAutomationType\_Bool**</span></span>
    -   <span data-ttu-id="4cb07-147">**UIAutomationType \_ doble**</span><span class="sxs-lookup"><span data-stu-id="4cb07-147">**UIAutomationType\_Double**</span></span>
    -   <span data-ttu-id="4cb07-148">**\_Elemento UIAutomationType**</span><span class="sxs-lookup"><span data-stu-id="4cb07-148">**UIAutomationType\_Element**</span></span>
    -   <span data-ttu-id="4cb07-149">**UIAutomationType \_ int**</span><span class="sxs-lookup"><span data-stu-id="4cb07-149">**UIAutomationType\_Int**</span></span>
    -   <span data-ttu-id="4cb07-150">**\_Punto UIAutomationType**</span><span class="sxs-lookup"><span data-stu-id="4cb07-150">**UIAutomationType\_Point**</span></span>
    -   <span data-ttu-id="4cb07-151">**\_Cadena UIAutomationType**</span><span class="sxs-lookup"><span data-stu-id="4cb07-151">**UIAutomationType\_String**</span></span>
3.  <span data-ttu-id="4cb07-152">Utilice la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear una instancia del objeto [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) y recuperar un puntero a la interfaz [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) del objeto.</span><span class="sxs-lookup"><span data-stu-id="4cb07-152">Use the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) object and retrieve a pointer to the object's [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) interface.</span></span>
4.  <span data-ttu-id="4cb07-153">Llame al método [**IUIAutomationRegistrar:: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) o [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) y pase la dirección de la estructura [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) o la estructura [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) .</span><span class="sxs-lookup"><span data-stu-id="4cb07-153">Call the [**IUIAutomationRegistrar::RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) or [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) method and pass the address of the [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) structure or the [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) structure.</span></span>

<span data-ttu-id="4cb07-154">El método [**IUIAutomationRegistrar:: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) o [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) devuelve un identificador de propiedad o un identificador de evento que una aplicación puede pasar a cualquier método de automatización de la interfaz de usuario que tome dicho identificador como parámetro.</span><span class="sxs-lookup"><span data-stu-id="4cb07-154">The [**IUIAutomationRegistrar::RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) or [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) method returns a property ID or event ID that an application can pass to any UI Automation method that takes such an identifier as a parameter.</span></span> <span data-ttu-id="4cb07-155">Por ejemplo, puede pasar un identificador de propiedad registrado al método [**IUIAutomationElement:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) o al método [**IUIAutomation:: CreatePropertyCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition) .</span><span class="sxs-lookup"><span data-stu-id="4cb07-155">For example, you can pass a registered property ID to the [**IUIAutomationElement::GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) method or to the [**IUIAutomation::CreatePropertyCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition) method.</span></span>

<span data-ttu-id="4cb07-156">En el ejemplo siguiente se muestra cómo registrar una propiedad personalizada.</span><span class="sxs-lookup"><span data-stu-id="4cb07-156">The following example demonstrates how to register a custom property.</span></span>


```C++
// Declare a variable for holding the custom property ID.
PATTERNID g_MyCustomPropertyID;
// Define a GUID for the custom property.
GUID GUID_MyCustomProperty = { 0x82f383ff, 0x4b4d, 0x40d3, 
    { 0x8e, 0xd2, 0x90, 0xb5, 0x25, 0x8e, 0xaa, 0x19 } };

HRESULT RegisterProperty()
{
    // Fill the structure with the GUID, name, and data type.
    UIAutomationPropertyInfo MyCustomPropertyInfo = 
    {
        GUID_MyCustomProperty,
        L"MyCustomProp",
        UIAutomationType_String
    };

    // Create the registrar object and get the IUIAutomationRegistrar 
    // interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar = NULL;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    // Register the property and retrieve the property ID. 
    HRESULT hr = pUIARegistrar->RegisterProperty(&MyCustomPropertyInfo, &g_MyCustomPropertyID);
    pUIARegistrar->Release();

    return hr;
}
```



<span data-ttu-id="4cb07-157">Los identificadores de propiedad y evento recuperados por los métodos [**IUIAutomationRegistrar:: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) y [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) solo son válidos en el contexto de la aplicación que los recupera y solo mientras dure la duración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4cb07-157">The property and event identifiers retrieved by the [**IUIAutomationRegistrar::RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) and [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) methods are valid only in the context of the application that retrieves them, and only for the duration of the application's lifetime.</span></span> <span data-ttu-id="4cb07-158">Los métodos de registro pueden devolver valores enteros diferentes para el mismo GUID cuando se llama a través de distintas instancias en tiempo de ejecución de la misma aplicación.</span><span class="sxs-lookup"><span data-stu-id="4cb07-158">The registration methods can return different integer values for the same GUID when it is called over different runtime instances of the same application.</span></span>

<span data-ttu-id="4cb07-159">No hay ningún método que anule el registro de una propiedad o evento personalizado.</span><span class="sxs-lookup"><span data-stu-id="4cb07-159">There is no method that unregisters a custom property or event.</span></span> <span data-ttu-id="4cb07-160">En su lugar, se anula el registro de forma implícita cuando se libera el último objeto de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4cb07-160">Instead, they are implicitly unregistered when the last UI Automation object is released.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4cb07-161">Si el código es un cliente de Microsoft Active Accessibility (MSAA), debe llamar a la función [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) al cambiar el valor de una propiedad personalizada.</span><span class="sxs-lookup"><span data-stu-id="4cb07-161">If your code is a Microsoft Active Accessibility (MSAA) client, you must call the [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) function when you change the value of a custom property.</span></span>

 

## <a name="implementing-custom-control-patterns"></a><span data-ttu-id="4cb07-162">Implementar patrones de control personalizados</span><span class="sxs-lookup"><span data-stu-id="4cb07-162">Implementing Custom Control Patterns</span></span>

<span data-ttu-id="4cb07-163">Un patrón de control personalizado no se incluye en la API de automatización de la interfaz de usuario, pero lo proporciona un tercero en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="4cb07-163">A custom control pattern is not included in the UI Automation API, but is provided by a third party at run time.</span></span> <span data-ttu-id="4cb07-164">Los desarrolladores de aplicaciones de cliente y de proveedor deben funcionar juntos para definir un patrón de control personalizado, incluidos los métodos, las propiedades y los eventos que el patrón de control admitirá.</span><span class="sxs-lookup"><span data-stu-id="4cb07-164">Developers of client and provider applications must work together to define a custom control pattern, including the methods, properties, and events that the control pattern will support.</span></span> <span data-ttu-id="4cb07-165">Después de definir el patrón de control, tanto el cliente como el proveedor deben implementar objetos auxiliares del modelo de objetos componentes (COM), junto con código para registrar el patrón de control en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="4cb07-165">After defining the control pattern, both the client and the provider must implement supporting Component Object Model (COM) objects, along with code to register the control pattern at run time.</span></span> <span data-ttu-id="4cb07-166">Un patrón de control personalizado requiere la implementación de dos objetos COM: un contenedor de cliente y un controlador de patrón.</span><span class="sxs-lookup"><span data-stu-id="4cb07-166">A custom control pattern requires the implementation of two COM objects: a client wrapper and a pattern handler.</span></span>

> [!Note]  
> <span data-ttu-id="4cb07-167">En los ejemplos de los temas siguientes se muestra cómo implementar un patrón de control personalizado que duplique la funcionalidad del patrón de control [Value](uiauto-implementingvalue.md) existente.</span><span class="sxs-lookup"><span data-stu-id="4cb07-167">The examples in the following topics illustrate how to implement a custom control pattern that duplicates the functionality of the existing [Value](uiauto-implementingvalue.md) control pattern.</span></span> <span data-ttu-id="4cb07-168">Estos ejemplos son solo con fines informativos.</span><span class="sxs-lookup"><span data-stu-id="4cb07-168">These examples are for instructional purposes only.</span></span> <span data-ttu-id="4cb07-169">Un patrón de control personalizado real debe proporcionar funcionalidad que no está disponible en los patrones de control de automatización de la interfaz de usuario estándar.</span><span class="sxs-lookup"><span data-stu-id="4cb07-169">An actual custom control pattern should provide functionality that is not available from the standard UI Automation control patterns.</span></span>

 

### <a name="the-client-wrapper-and-the-pattern-handler"></a><span data-ttu-id="4cb07-170">Contenedor de cliente y controlador de patrón</span><span class="sxs-lookup"><span data-stu-id="4cb07-170">The Client Wrapper and the Pattern Handler</span></span>

<span data-ttu-id="4cb07-171">El contenedor de cliente implementa la API que usa el cliente para recuperar las propiedades y llamar a los métodos expuestos por el patrón de control personalizado.</span><span class="sxs-lookup"><span data-stu-id="4cb07-171">The client wrapper implements the API that is used by the client to retrieve properties and call methods exposed by the custom control pattern.</span></span> <span data-ttu-id="4cb07-172">La API se implementa como una interfaz COM que pasa todas las solicitudes de propiedades y llamadas a métodos al núcleo de automatización de la interfaz de usuario, que luego calcula las referencias de las solicitudes y llamadas al proveedor.</span><span class="sxs-lookup"><span data-stu-id="4cb07-172">The API is implemented as a COM interface that passes all property requests and method calls to the UI Automation core, which then marshals the requests and calls to the provider.</span></span>

<span data-ttu-id="4cb07-173">El código que registra un patrón de control personalizado debe proporcionar un generador de clases que la automatización de la interfaz de usuario puede usar para crear instancias del objeto contenedor de cliente.</span><span class="sxs-lookup"><span data-stu-id="4cb07-173">The code that registers a custom control pattern must supply a class factory that UI Automation can use to create instances of the client wrapper object.</span></span> <span data-ttu-id="4cb07-174">Cuando un patrón de control personalizado se registra correctamente, la automatización de la interfaz de usuario devuelve un puntero de la interfaz [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) que usa el cliente para reenviar solicitudes de propiedades y llamadas a métodos al núcleo de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4cb07-174">When a custom control pattern is successfully registered, UI Automation returns an [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) interface pointer that is used by the client to forward property requests and methods calls to the UI Automation core.</span></span>

<span data-ttu-id="4cb07-175">En el lado del proveedor, el núcleo de automatización de la interfaz de usuario toma las solicitudes de propiedades y las llamadas a métodos desde el cliente y las pasa al objeto de controlador de patrón.</span><span class="sxs-lookup"><span data-stu-id="4cb07-175">On the provider side, the UI Automation core takes the property requests and method calls from the client and passes them to the pattern handler object.</span></span> <span data-ttu-id="4cb07-176">A continuación, el controlador de patrón llama a los métodos adecuados en la interfaz del proveedor para el patrón de control personalizado.</span><span class="sxs-lookup"><span data-stu-id="4cb07-176">The pattern handler then calls the appropriate methods on the provider interface for the custom control pattern.</span></span>

<span data-ttu-id="4cb07-177">El código que registra un patrón de control personalizado crea el objeto de controlador de patrón y, al registrar el patrón de control, proporciona automatización de la interfaz de usuario con un puntero a la interfaz [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) del objeto.</span><span class="sxs-lookup"><span data-stu-id="4cb07-177">The code that registers a custom control pattern creates the pattern handler object and, when registering the control pattern, provides UI Automation with a pointer to the object's [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface.</span></span>

<span data-ttu-id="4cb07-178">En el diagrama siguiente se muestra cómo una solicitud de propiedad de cliente o una llamada de método fluyen desde el contenedor de cliente, a través de los componentes principales de UI Automation hasta el controlador de patrón y, a continuación, a la interfaz del proveedor.</span><span class="sxs-lookup"><span data-stu-id="4cb07-178">The following diagram shows how a client property request or method call flows from the client wrapper, through the UI Automation core components to the pattern handler, and then to the provider interface.</span></span>

![diagrama que muestra el flujo del contenedor del cliente al controlador y al proveedor del patrón](images/custompatternsupport.jpg)

<span data-ttu-id="4cb07-180">Los objetos que implementan las interfaces de contenedor de cliente y controlador de patrón deben ser de subprocesamiento libre.</span><span class="sxs-lookup"><span data-stu-id="4cb07-180">The objects that implement the client wrapper and pattern handler interfaces must be free-threaded.</span></span> <span data-ttu-id="4cb07-181">Además, el núcleo de automatización de la interfaz de usuario debe poder llamar a los objetos directamente sin ningún código de serialización intermedio.</span><span class="sxs-lookup"><span data-stu-id="4cb07-181">Also, the UI Automation core must be able to call the objects directly without any intermediate marshaling code.</span></span>

### <a name="implementing-the-client-wrapper"></a><span data-ttu-id="4cb07-182">Implementar el contenedor de cliente</span><span class="sxs-lookup"><span data-stu-id="4cb07-182">Implementing the Client Wrapper</span></span>

<span data-ttu-id="4cb07-183">El contenedor de cliente es un objeto que expone una interfaz IXxxPattern que el cliente usa para solicitar propiedades y llamar a métodos admitidos por el patrón de control personalizado.</span><span class="sxs-lookup"><span data-stu-id="4cb07-183">The client wrapper is an object that exposes an IXxxPattern interface that the client uses to request properties and call methods supported by the custom control pattern.</span></span> <span data-ttu-id="4cb07-184">La interfaz está formada por un par de métodos de "captador" para cada propiedad admitida (get \_ CurrentXxx y Get \_ CachedXxx Method) y un método "Caller" para cada método admitido.</span><span class="sxs-lookup"><span data-stu-id="4cb07-184">The interface consists of a pair of "getter" methods for each supported property (get\_CurrentXxx and get\_CachedXxx method), and a "caller" method for each supported method.</span></span> <span data-ttu-id="4cb07-185">Cuando se crea una instancia del objeto, el constructor de objeto recibe un puntero a la interfaz [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) , que se implementa mediante el núcleo de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4cb07-185">When the object is instantiated, the object constructor receives a pointer to the [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) interface, which is implemented by the UI Automation core.</span></span> <span data-ttu-id="4cb07-186">Los métodos de la interfaz IXxxPattern usan los métodos [**IUIAutomationPatternInstance:: GetProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-getproperty) y [**CallMethod**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod) para reenviar las solicitudes de propiedades y las llamadas de método al núcleo de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4cb07-186">The methods of the IXxxPattern interface use the [**IUIAutomationPatternInstance::GetProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-getproperty) and [**CallMethod**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod) methods to forward property requests and method calls to the UI Automation core.</span></span>

<span data-ttu-id="4cb07-187">En el ejemplo siguiente se muestra cómo implementar un objeto contenedor de cliente para un patrón de control personalizado simple que admite una sola propiedad.</span><span class="sxs-lookup"><span data-stu-id="4cb07-187">The following example shows how to implement a client wrapper object for a simple custom control pattern that supports a single property.</span></span> <span data-ttu-id="4cb07-188">Para obtener un ejemplo más complejo, vea [ejemplo de implementación de un patrón de control personalizado](#example-implementation-of-a-custom-control-pattern).</span><span class="sxs-lookup"><span data-stu-id="4cb07-188">For a more complex example, see [Example Implementation of a Custom Control Pattern](#example-implementation-of-a-custom-control-pattern).</span></span>


```C++
// Define the client interface.
interface __declspec(uuid("c78b266d-b2c0-4e9d-863b-e3f74a721d47"))
IMyCustomPattern : public IUnknown
{
    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;
};

// Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IMyCustomPattern
{
    IUIAutomationPatternInstance * _pInstance;
    
public:
    // Get IUIAutomationPatternInstance interface pointer from the
    // UI Automation core.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
        : _pInstance(pInstance)
    {
        _pInstance->AddRef();
    }
    
    ~CMyValuePatternClientWrapper()
    {
        _pInstance->Release();
    }

    // Note: Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, FALSE, UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, TRUE, UIAutomationType_Bool, pIsReadOnly);
    }
};
```



### <a name="implementing-the-pattern-handler"></a><span data-ttu-id="4cb07-189">Implementar el controlador de patrón</span><span class="sxs-lookup"><span data-stu-id="4cb07-189">Implementing the Pattern Handler</span></span>

<span data-ttu-id="4cb07-190">El controlador de patrón es un objeto que implementa la interfaz [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) .</span><span class="sxs-lookup"><span data-stu-id="4cb07-190">The pattern handler is an object that implements the [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface.</span></span> <span data-ttu-id="4cb07-191">Esta interfaz tiene dos métodos: [**IUIAutomationPatternHandler:: CreateClientWrapper**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-createclientwrapper) y [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch).</span><span class="sxs-lookup"><span data-stu-id="4cb07-191">This interface has two methods: [**IUIAutomationPatternHandler::CreateClientWrapper**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-createclientwrapper) and [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch).</span></span> <span data-ttu-id="4cb07-192">El núcleo de la automatización de la interfaz de usuario llama al método **CreateClientWrapper** y recibe un puntero a la interfaz [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) .</span><span class="sxs-lookup"><span data-stu-id="4cb07-192">The **CreateClientWrapper** method is called by the UI Automation core and receives a pointer to the [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) interface.</span></span> <span data-ttu-id="4cb07-193">**CreateClientWrapper** responde creando instancias del objeto contenedor de cliente y pasando el puntero de la interfaz **IUIAutomationPatternInstance** al constructor contenedor de cliente.</span><span class="sxs-lookup"><span data-stu-id="4cb07-193">**CreateClientWrapper** responds by instantiating the client wrapper object and passing the **IUIAutomationPatternInstance** interface pointer to the client wrapper constructor.</span></span>

<span data-ttu-id="4cb07-194">El núcleo de automatización de la interfaz de usuario usa el método [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch) para pasar las solicitudes de propiedad y las llamadas de método a la interfaz del proveedor para el patrón de control personalizado.</span><span class="sxs-lookup"><span data-stu-id="4cb07-194">The [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch) method is used by the UI Automation core to pass property requests and method calls to the provider interface for the custom control pattern.</span></span> <span data-ttu-id="4cb07-195">Los parámetros incluyen un puntero a la interfaz del proveedor, el índice de base cero del captador de propiedad o método al que se llama, y una matriz de estructuras [**UIAutomationParameter**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter) que contienen los parámetros que se van a pasar al proveedor.</span><span class="sxs-lookup"><span data-stu-id="4cb07-195">Parameters include a pointer to the provider interface, the zero-based index of the property getter or method being called, and an array of [**UIAutomationParameter**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter) structures that contain the parameters to pass to the provider.</span></span> <span data-ttu-id="4cb07-196">El controlador de patrón responde comprobando el parámetro de índice para determinar el método de proveedor al que llamar y, a continuación, llama a la interfaz del proveedor, pasando los parámetros contenidos en las estructuras **UIAutomationParameter** .</span><span class="sxs-lookup"><span data-stu-id="4cb07-196">The pattern handler responds by checking the index parameter to determine which provider method to call, and then calls that provider interface, passing the parameters contained in the **UIAutomationParameter** structures.</span></span>

<span data-ttu-id="4cb07-197">Se crea una instancia del objeto de controlador de patrón mediante el mismo código que registra el patrón de control personalizado antes de que se registre el patrón de control.</span><span class="sxs-lookup"><span data-stu-id="4cb07-197">The pattern handler object is instantiated by the same code that registers the custom control pattern, before the control pattern is registered.</span></span> <span data-ttu-id="4cb07-198">El código debe pasar el puntero de la interfaz [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) del objeto de controlador de patrón al núcleo de automatización de la interfaz de usuario en el momento del registro.</span><span class="sxs-lookup"><span data-stu-id="4cb07-198">The code must pass the pattern handler object's [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface pointer to the UI Automation core at registration time.</span></span>

<span data-ttu-id="4cb07-199">En el ejemplo siguiente se muestra cómo implementar un objeto de controlador de patrón para un patrón de control personalizado simple que admite una sola propiedad.</span><span class="sxs-lookup"><span data-stu-id="4cb07-199">The following example shows how to implement a pattern handler object for a simple custom control pattern that supports a single property.</span></span> <span data-ttu-id="4cb07-200">Para obtener un ejemplo más complejo, vea [ejemplo de implementación de un patrón de control personalizado](#example-implementation-of-a-custom-control-pattern).</span><span class="sxs-lookup"><span data-stu-id="4cb07-200">For a more complex example, see [Example Implementation of a Custom Control Pattern](#example-implementation-of-a-custom-control-pattern).</span></span>


```C++
// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
};            

// Index used by IUIAutomationPatternHandler::Dispatch.
const int MyValue_GetIsReadOnly = 0; 
            
// Define the pattern handler class.        
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:
    
    // Put standard IUnknown implementation here.

    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);
        }
        return E_INVALIDARG;
    }
};
```



### <a name="registering-a-custom-control-pattern"></a><span data-ttu-id="4cb07-201">Registrar un patrón de control personalizado</span><span class="sxs-lookup"><span data-stu-id="4cb07-201">Registering a Custom Control Pattern</span></span>

<span data-ttu-id="4cb07-202">Antes de que se pueda usar, el proveedor y el cliente deben registrar un patrón de control personalizado.</span><span class="sxs-lookup"><span data-stu-id="4cb07-202">Before it can be used, a custom control pattern must be registered by both the provider and the client.</span></span> <span data-ttu-id="4cb07-203">El registro proporciona el núcleo de automatización de la interfaz de usuario con información detallada sobre el patrón de control y proporciona al proveedor o al cliente el identificador de patrón de control, así como los identificadores de las propiedades y los eventos que admite el patrón de control.</span><span class="sxs-lookup"><span data-stu-id="4cb07-203">Registering provides the UI Automation core with detailed information about the control pattern, and supplies the provider or client with the control pattern ID, and IDs for the properties and events that are supported by the control pattern.</span></span> <span data-ttu-id="4cb07-204">En el lado del proveedor, se debe registrar el patrón de control personalizado antes de que el control asociado administre el mensaje de la [**\_ GETOBJECT de WM**](wm-getobject.md) o al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="4cb07-204">On the provider side, the custom control pattern must be registered before the associated control handles the [**WM\_GETOBJECT**](wm-getobject.md) message, or at the same time.</span></span>

<span data-ttu-id="4cb07-205">Al registrar un patrón de control personalizado, el proveedor o el cliente proporciona la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="4cb07-205">When registering a custom control pattern, the provider or client supplies the following information:</span></span>

-   <span data-ttu-id="4cb07-206">GUID del patrón de control personalizado.</span><span class="sxs-lookup"><span data-stu-id="4cb07-206">The GUID of the custom control pattern.</span></span>
-   <span data-ttu-id="4cb07-207">Una cadena no localizable que contiene el nombre del patrón de control personalizado.</span><span class="sxs-lookup"><span data-stu-id="4cb07-207">A nonlocalizable string containing the name of the custom control pattern.</span></span>
-   <span data-ttu-id="4cb07-208">GUID de la interfaz del proveedor que admite el patrón de control personalizado.</span><span class="sxs-lookup"><span data-stu-id="4cb07-208">The GUID of the provider interface that supports the custom control pattern.</span></span>
-   <span data-ttu-id="4cb07-209">GUID de la interfaz de cliente que admite el patrón de control personalizado.</span><span class="sxs-lookup"><span data-stu-id="4cb07-209">The GUID of the client interface that supports the custom control pattern.</span></span>
-   <span data-ttu-id="4cb07-210">Matriz de estructuras [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) que describen las propiedades admitidas por el patrón de control personalizado.</span><span class="sxs-lookup"><span data-stu-id="4cb07-210">An array of [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) structures that describe the properties supported by the custom control pattern.</span></span> <span data-ttu-id="4cb07-211">Para cada propiedad, se deben especificar el GUID, el nombre de la propiedad y el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4cb07-211">For each property, the GUID, property name, and data type must be specified.</span></span>
-   <span data-ttu-id="4cb07-212">Matriz de estructuras [**UIAutomationMethodInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo) que describen los métodos admitidos por el patrón de control personalizado.</span><span class="sxs-lookup"><span data-stu-id="4cb07-212">An array of [**UIAutomationMethodInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo) structures that describe the methods supported by the custom control pattern.</span></span> <span data-ttu-id="4cb07-213">Para cada método, la estructura incluye la información siguiente: el nombre del método, un recuento de parámetros, una lista de tipos de datos de parámetros y una lista de los nombres de parámetro.</span><span class="sxs-lookup"><span data-stu-id="4cb07-213">For each method, the structure includes the following information: the method name, a count of parameters, a list of parameter data types, and a list of the parameter names.</span></span>
-   <span data-ttu-id="4cb07-214">Matriz de estructuras [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) que describen los eventos generados por el patrón de control personalizado.</span><span class="sxs-lookup"><span data-stu-id="4cb07-214">An array of [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) structures that describe the events raised by the custom control pattern.</span></span> <span data-ttu-id="4cb07-215">Para cada evento, debe especificarse el GUID y el nombre del evento.</span><span class="sxs-lookup"><span data-stu-id="4cb07-215">For each event, the GUID and event name must be specified.</span></span>
-   <span data-ttu-id="4cb07-216">Dirección de la interfaz [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) del objeto de controlador de patrón que hace que el patrón de control personalizado esté disponible para los clientes.</span><span class="sxs-lookup"><span data-stu-id="4cb07-216">The address of the [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface of the pattern handler object that makes the custom control pattern available to clients.</span></span>

<span data-ttu-id="4cb07-217">Para registrar el patrón de control personalizado, el código de cliente o proveedor debe realizar los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="4cb07-217">To register the custom control pattern, the provider or client code must perform the following steps:</span></span>

1.  <span data-ttu-id="4cb07-218">Rellene una estructura [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) con la información anterior.</span><span class="sxs-lookup"><span data-stu-id="4cb07-218">Fill a [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) structure with the preceding information.</span></span>
2.  <span data-ttu-id="4cb07-219">Utilice la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para crear una instancia del objeto [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) y recuperar un puntero a la interfaz [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) del objeto.</span><span class="sxs-lookup"><span data-stu-id="4cb07-219">Use the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) object and retrieve a pointer to the object's [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) interface.</span></span>
3.  <span data-ttu-id="4cb07-220">Llame al método [**IUIAutomationRegistrar:: RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) , pasando la dirección de la estructura [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) .</span><span class="sxs-lookup"><span data-stu-id="4cb07-220">Call the [**IUIAutomationRegistrar::RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) method, passing the address of the [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) structure.</span></span>

<span data-ttu-id="4cb07-221">El método [**RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) devuelve un identificador de patrón de control, junto con una lista de identificadores de propiedades e identificadores de eventos.</span><span class="sxs-lookup"><span data-stu-id="4cb07-221">The [**RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) method returns a control pattern ID, along with a list of property IDs and event IDs.</span></span> <span data-ttu-id="4cb07-222">Una aplicación puede pasar estos identificadores a cualquier método de automatización de la interfaz de usuario que tome dicho identificador como parámetro.</span><span class="sxs-lookup"><span data-stu-id="4cb07-222">An application can pass these IDs to any UI Automation method that takes such an identifier as a parameter.</span></span> <span data-ttu-id="4cb07-223">Por ejemplo, puede pasar un identificador de patrón registrado al método [**IUIAutomationElement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) para recuperar un puntero a la interfaz del proveedor para el patrón de control.</span><span class="sxs-lookup"><span data-stu-id="4cb07-223">For example, you can pass a registered pattern ID to the [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method to retrieve a pointer to the provider interface for the control pattern.</span></span>

<span data-ttu-id="4cb07-224">No hay ningún método que anule el registro de un patrón de control personalizado.</span><span class="sxs-lookup"><span data-stu-id="4cb07-224">There is no method that unregisters a custom control pattern.</span></span> <span data-ttu-id="4cb07-225">En su lugar, se anula el registro de forma implícita cuando se libera el último objeto de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4cb07-225">Instead, it is implicitly unregistered when the last UI Automation object is released.</span></span>

<span data-ttu-id="4cb07-226">Para obtener un ejemplo en el que se muestra cómo registrar un patrón de control personalizado, consulte la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="4cb07-226">For an example that shows how to register a custom control pattern, see the following section.</span></span>

### <a name="example-implementation-of-a-custom-control-pattern"></a><span data-ttu-id="4cb07-227">Ejemplo de implementación de un patrón de control personalizado</span><span class="sxs-lookup"><span data-stu-id="4cb07-227">Example Implementation of a Custom Control Pattern</span></span>

<span data-ttu-id="4cb07-228">Esta sección contiene código de ejemplo que muestra cómo implementar los objetos contenedor de cliente y controlador de patrón para un patrón de control personalizado.</span><span class="sxs-lookup"><span data-stu-id="4cb07-228">This section contains example code that demonstrates how to implement the client wrapper and pattern handler objects for a custom control pattern.</span></span> <span data-ttu-id="4cb07-229">En el ejemplo se implementa un patrón de control personalizado basado en el patrón de control [Value](uiauto-implementingvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="4cb07-229">The example implements a custom control pattern that is based on the [Value](uiauto-implementingvalue.md) control pattern.</span></span>


```C++
// Step 1: Define the public provider and client interfaces using IDL. Interface 
// definitions are in C here to simplify the example.

// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_Value)(BSTR * pValue) = 0;
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Define the client interface.
interface __declspec(uuid("103b8323-b04a-4180-9140-8c1e437713a3"))
IUIAutomationMyValuePattern : public IUnknown
{
    STDMETHOD (get_CurrentValue)(BSTR * pValue) = 0;
    STDMETHOD (get_CachedValue)(BSTR * pValue) = 0;

    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;

    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Enumerate the properties and methods starting from 0, and placing the 
// properties first. 
enum
{
    MyValue_GetValue = 0,
    MyValue_GetIsReadOnly = 1,
    MyValue_SetValue = 2,
    MyValue_Reset = 3,
};

// Step 2: Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IUIAutomationMyValuePattern
{
    IUIAutomationPatternInstance * _pInstance;

public:
    // Get IUIAutomationPatternInstance interface pointer.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
    {
        _pInstance = pInstance;
        _pInstance->AddRef();
    }

    // Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, FALSE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CachedValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, TRUE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, FALSE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, TRUE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP SetValue(LPCWSTR pValue)
    {
        UIAutomationParameter SetValueParams[] = 
                { UIAutomationType_String, &pValue };
        return _pInstance->CallMethod(MyValue_SetValue,  SetValueParams, 
                ARRAYSIZE(SetValueParams));
    }

    STDMETHODIMP Reset()
    {
        return _pInstance->CallMethod(MyValue_Reset, NULL, 0);
    }
};

// Step 3: Implement the pattern handler class.
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:

    // Put standard IUnknown implementation here.
    
    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, 
            UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetValue:
            return ((IMyValueProvider*)pTarget)->get_Value((BSTR*)pParams[0].pData);

        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);

        case MyValue_SetValue:
            return ((IMyValueProvider*)pTarget)->SetValue(*(LPCWSTR*)pParams[0].pData);

        case MyValue_Reset:
            return ((IMyValueProvider*)pTarget)->Reset();
        }
        return E_INVALIDARG;
    }
};

CMyValuePatternHandler g_MyValuePatternHandler;

// Step 4: Declare information about the properties and methods supported
// by the custom control pattern.

// Define GUIDs for the custom control pattern and each of its properties 
// and events.
static const GUID MyValue_Pattern_Guid = { 0xa49aa3c0, 0xe413, 0x4ecf, 
        { 0xa1, 0xc3, 0x37, 0x42, 0xa7, 0x86, 0x67, 0x3f } };
static const GUID MyValue_Value_Property_Guid = { 0xe58f3f67, 0x22c7, 0x44f0, 
        { 0x83, 0x55, 0xd8, 0x76, 0x14, 0xa1, 0x10, 0x81 } };
static const GUID MyValue_IsReadOnly_Property_Guid = { 0x480540f2, 0x9829, 0x4acd, 
        { 0xb8, 0xea, 0x6e, 0x2a, 0xdc, 0xe5, 0x3a, 0xfb } };
static const GUID MyValue_Reset_Event_Guid = { 0x5b80edd3, 0x67f, 0x4a70, 
        { 0xb0, 0x7, 0x4, 0x12, 0x85, 0x11, 0x1, 0x7a } };

// Declare information about the properties, in the same order as the
// previously defined "MyValue_" enumerated type.
UIAutomationPropertyInfo g_MyValueProperties[] = 
{
    // GUID, name, data type.
    { MyValue_Value_Property_Guid, L"MyValuePattern.Value", 
                                                    UIAutomationType_String },
    { MyValue_IsReadOnly_Property_Guid, L"MyValuePattern.IsReadOnly", 
                                                    UIAutomationType_Bool },
};

// Declare information about the event.
UIAutomationEventInfo g_MyValueEvents [] =
{
    { MyValue_Reset_Event_Guid,  L"MyValuePattern.Reset" },
};

// Declare the data type and name of the SetValue method parameter. 
UIAutomationType g_SetValueParamTypes[] = { UIAutomationType_String };
LPCWSTR g_SetValueParamNames[] = {L"pNewValue"};

// Declare information about the methods.
UIAutomationMethodInfo g_MyValueMethods[] =
{
    // Name, focus flag, count of in parameters, count of out parameters, types, parameter names.
    { L"MyValuePattern.SetValue", TRUE, 1, 0, g_SetValueParamTypes, g_SetValueParamNames },
    { L"MyValuePattern.Reset", TRUE, 0, 0, NULL, NULL },
};

// Declare the custom control pattern using the previously defined information.
UIAutomationPatternInfo g_ValuePatternInfo =
{
    MyValue_Pattern_Guid,
    L"MyValuePattern",
    __uuidof(IMyValueProvider),
    __uuidof(IUIAutomationMyValuePattern),
    ARRAYSIZE(g_MyValueProperties), g_MyValueProperties, // properties
    ARRAYSIZE(g_MyValueMethods), g_MyValueMethods,       // methods
    ARRAYSIZE(g_MyValueEvents), g_MyValueEvents,         // events 
    &g_MyValuePatternHandler
};

// Step 5: Register the custom control pattern and retrieve the control pattern and property 
// identifiers.

// Control pattern, property, and event IDs.
PATTERNID  g_MyValue_PatternID;
PROPERTYID g_MyValue_Value_PropertyID;
PROPERTYID g_MyValue_IsReadOnly_PropertyID;
EVENTID    g_MyValueReset_EventID;

// ID used by the client to determine whether the custom control pattern is available.
PROPERTYID g_IsMyValuePatternAvailable_PropertyID;

HRESULT RegisterPattern()
{
    // Create the registrar object and get the IUIAutomationRegistrar interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    PROPERTYID propIDs[2]; // Array for property IDs.

    // Register the control pattern.
    HRESULT hr = pUIARegistrar->RegisterPattern(
        &g_ValuePatternInfo,
        &g_MyValue_PatternID,
        &g_IsMyValuePatternAvailable_PropertyID,
        ARRAYSIZE(propIDs), 
        propIDs,
        1,
        &g_MyValueReset_EventID);
            
    if (hr == S_OK)
    {
        // Copy the property IDs.
        g_MyValue_Value_PropertyID = propIDs[0];
        g_MyValue_IsReadOnly_PropertyID = propIDs[1];
    }

    pUIARegistrar->Release();
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="4cb07-230">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4cb07-230">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4cb07-231">**Vista**</span><span class="sxs-lookup"><span data-stu-id="4cb07-231">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4cb07-232">Diseñar propiedades, eventos y patrones de control personalizados</span><span class="sxs-lookup"><span data-stu-id="4cb07-232">Designing Custom Properties, Events, and Control Patterns</span></span>](uiauto-designingcustompropseventpatterns.md)
</dt> <dt>

[<span data-ttu-id="4cb07-233">Información general acerca de las propiedades de UI Automation</span><span class="sxs-lookup"><span data-stu-id="4cb07-233">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="4cb07-234">Información general sobre eventos de UI Automation</span><span class="sxs-lookup"><span data-stu-id="4cb07-234">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

[<span data-ttu-id="4cb07-235">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="4cb07-235">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 