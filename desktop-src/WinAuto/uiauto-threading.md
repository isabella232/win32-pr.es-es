---
title: Descripción de los problemas de subprocesos
description: En este tema se describen escenarios comunes de subprocesos para implementaciones de cliente de automatización de la interfaz de usuario de Microsoft y se explica cómo evitar problemas que pueden producirse si un cliente usa el subproceso de forma incorrecta.
ms.assetid: 0772969a-da55-488e-8b21-7368434df8a9
keywords:
- clientes, problemas de subprocesos de automatización de la interfaz de usuario
- clientes, problemas de subprocesos
- clientes, modelo de subprocesos del controlador de eventos
- clientes, modelo de subprocesos del controlador de eventos de UI Automation
- clientes, afinidad de UI Automation
- clientes, afinidad
- Automatización de la interfaz de usuario, problemas de subprocesos
- Automatización de la interfaz de usuario, modelo de subprocesos del controlador de eventos
- Automatización de la interfaz de usuario, afinidad
- problemas con el subprocesamiento
- modelo de subprocesos del controlador de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a002132efe4055bb247c7d7290e271e153ac297e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077805"
---
# <a name="understanding-threading-issues"></a><span data-ttu-id="14202-114">Descripción de los problemas de subprocesos</span><span class="sxs-lookup"><span data-stu-id="14202-114">Understanding Threading Issues</span></span>

<span data-ttu-id="14202-115">En este tema se describen escenarios comunes de subprocesos para implementaciones de cliente de automatización de la interfaz de usuario de Microsoft y se explica cómo evitar problemas que pueden producirse si un cliente usa el subproceso de forma incorrecta.</span><span class="sxs-lookup"><span data-stu-id="14202-115">This topic describes common threading scenarios for Microsoft UI Automation client implementations and explains how to avoid problems that can occur if a client uses threading incorrectly.</span></span>

<span data-ttu-id="14202-116">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="14202-116">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="14202-117">Automatización de la interfaz de usuario y subproceso de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="14202-117">UI Automation and the UI Thread</span></span>](#ui-automation-and-the-ui-thread)
-   [<span data-ttu-id="14202-118">Modelo de subprocesos para controladores de eventos</span><span class="sxs-lookup"><span data-stu-id="14202-118">Threading Model for Event Handlers</span></span>](#threading-model-for-event-handlers)
-   [<span data-ttu-id="14202-119">Afinidad de Apartamento COM en Windows de 64 bits</span><span class="sxs-lookup"><span data-stu-id="14202-119">COM Apartment Affinity on 64-bit Windows</span></span>](#com-apartment-affinity-on-64-bit-windows)
-   [<span data-ttu-id="14202-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="14202-120">Related topics</span></span>](#related-topics)

## <a name="ui-automation-and-the-ui-thread"></a><span data-ttu-id="14202-121">Automatización de la interfaz de usuario y subproceso de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="14202-121">UI Automation and the UI Thread</span></span>

<span data-ttu-id="14202-122">Debido al modo en que la automatización de la interfaz de usuario utiliza mensajes de Windows, pueden producirse conflictos cuando una aplicación cliente intenta interactuar con su propia interfaz de usuario en el subproceso de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="14202-122">Because of the way UI Automation uses Windows messages, conflicts can occur when a client application attempts to interact with its own UI on the UI thread.</span></span> <span data-ttu-id="14202-123">Estos conflictos pueden dar lugar a un rendimiento muy lento o incluso provocar que la aplicación deje de responder.</span><span class="sxs-lookup"><span data-stu-id="14202-123">These conflicts can lead to very slow performance, or even cause the application to stop responding.</span></span>

<span data-ttu-id="14202-124">Si la aplicación cliente está diseñada para interactuar con todos los elementos del escritorio, incluida su propia interfaz de usuario, debe realizar todas las llamadas de automatización de la interfaz de usuario desde un subproceso independiente.</span><span class="sxs-lookup"><span data-stu-id="14202-124">If your client application is intended to interact with all elements on the desktop, including its own UI, you should make all UI Automation calls from a separate thread.</span></span> <span data-ttu-id="14202-125">Esto incluye la ubicación de elementos, por ejemplo, mediante [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) o el método [**IUIAutomationElement:: FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) y el uso de patrones de control.</span><span class="sxs-lookup"><span data-stu-id="14202-125">This includes locating elements, for example, by using [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) or the [**IUIAutomationElement::FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) method and using control patterns.</span></span> <span data-ttu-id="14202-126">Este subproceso no debe poseer ninguna ventana de y debe ser un subproceso del modelo de Apartamento multiproceso (MTA) de modelo de objetos componentes (COM) (uno que inicializa COM mediante una llamada a [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) con la marca de **coinit \_ multiproceso** ).</span><span class="sxs-lookup"><span data-stu-id="14202-126">This thread should not own any windows, and should be a Component Object Model (COM) Multithreaded Apartment (MTA) model thread (one that initializes COM by calling [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) with the **COINIT\_MULTITHREADED** flag.)</span></span>

<span data-ttu-id="14202-127">Es seguro realizar llamadas de automatización de la interfaz de usuario en un controlador de eventos de automatización de la interfaz de usuario, porque siempre se llama al controlador de eventos en un subproceso que no es de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="14202-127">It is safe to make UI Automation calls in a UI Automation event handler, because the event handler is always called on a non-UI thread.</span></span> <span data-ttu-id="14202-128">Sin embargo, al suscribirse a eventos que pueden originarse en la interfaz de usuario de la aplicación cliente, debe realizar la llamada a [**IUIAutomation:: AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler), o un método relacionado, en un subproceso que no sea de interfaz de usuario (que también debe ser un subproceso MTA).</span><span class="sxs-lookup"><span data-stu-id="14202-128">However, when subscribing to events that may originate from your client application UI, you must make the call to [**IUIAutomation::AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler), or a related method, on a non-UI thread (which should also be an MTA thread).</span></span> <span data-ttu-id="14202-129">Quite los controladores de eventos que estén en el mismo subproceso.</span><span class="sxs-lookup"><span data-stu-id="14202-129">Remove event handlers on the same thread.</span></span>

<span data-ttu-id="14202-130">Un cliente de UI Automation no debe utilizar varios subprocesos para agregar o quitar controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="14202-130">A UI Automation client should not use multiple threads to add or remove event handlers.</span></span> <span data-ttu-id="14202-131">Un comportamiento inesperado puede producirse si se agrega o se quita un controlador de eventos mientras se agrega o quita otro en el mismo proceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="14202-131">Unexpected behavior can result if one event handler is being added or removed while another is being added or removed in the same client process.</span></span>

## <a name="threading-model-for-event-handlers"></a><span data-ttu-id="14202-132">Modelo de subprocesos para controladores de eventos</span><span class="sxs-lookup"><span data-stu-id="14202-132">Threading Model for Event Handlers</span></span>

<span data-ttu-id="14202-133">Un cliente de automatización de la interfaz de usuario debe utilizar el modelo de subprocesos del MTA de COM para los subprocesos que implementan controladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="14202-133">A UI Automation client should use the COM MTA threading model for threads that implement event handlers.</span></span> <span data-ttu-id="14202-134">El uso del modelo de contenedor uniproceso (STA) puede causar problemas, como evitar que los clientes quiten controladores de eventos del subproceso.</span><span class="sxs-lookup"><span data-stu-id="14202-134">Using the Single-threaded Apartment (STA) model can cause problems such as preventing clients from removing event handlers from the thread.</span></span>

## <a name="com-apartment-affinity-on-64-bit-windows"></a><span data-ttu-id="14202-135">Afinidad de Apartamento COM en Windows de 64 bits</span><span class="sxs-lookup"><span data-stu-id="14202-135">COM Apartment Affinity on 64-bit Windows</span></span>

<span data-ttu-id="14202-136">Según la especificación COM, la duración de un objeto remoto se rige por la duración del apartamento donde se llama a la función [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el objeto.</span><span class="sxs-lookup"><span data-stu-id="14202-136">According to the COM specification, the lifetime of a remote object is governed by the lifetime of the apartment where the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function is called to create the object.</span></span> <span data-ttu-id="14202-137">Cuando se cierra el apartamento original, el objeto remoto también se libera.</span><span class="sxs-lookup"><span data-stu-id="14202-137">When the original apartment shuts down, the remote object is also released.</span></span>

<span data-ttu-id="14202-138">En el caso de los clientes de automatización de la interfaz de usuario, este comportamiento COM puede significar que la duración de la aplicación auxiliar Remote 32/64 (creada por UIAutomationCore.dll) utilizada por un elemento de 32 bits se rige por la duración del apartamento del subproceso que creó el elemento.</span><span class="sxs-lookup"><span data-stu-id="14202-138">For UI Automation clients, this COM behavior can mean that the lifetime of the remote 32/64 helper (created by UIAutomationCore.dll) used by a 32-bit element is governed by the apartment lifetime of the thread that created the element.</span></span> <span data-ttu-id="14202-139">Si el cliente de automatización de la interfaz de usuario calcula las referencias del elemento en otro subproceso, el elemento se puede invalidar Cuando el apartamento de origen se apaga.</span><span class="sxs-lookup"><span data-stu-id="14202-139">If the UI Automation client marshals the element to another thread, the element can become invalidated when the originating apartment shuts down.</span></span> <span data-ttu-id="14202-140">El cliente de automatización de la interfaz de usuario debe controlar estos problemas correctamente mediante la detección de errores al usar elementos de automatización de serialización.</span><span class="sxs-lookup"><span data-stu-id="14202-140">The UI Automation client should handle these issues gracefully by catching errors while using marshaled automation elements.</span></span>

<span data-ttu-id="14202-141">El mismo problema puede producirse con un cliente de automatización de la interfaz de usuario de 32 bits que tiene elementos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="14202-141">The same issue can occur with a 32-bit UI Automation client that has 64-bit elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14202-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="14202-142">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="14202-143">**Vista**</span><span class="sxs-lookup"><span data-stu-id="14202-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="14202-144">Obtener elementos de UI Automation</span><span class="sxs-lookup"><span data-stu-id="14202-144">Obtaining UI Automation Elements</span></span>](uiauto-obtainingelements.md)
</dt> <dt>

[<span data-ttu-id="14202-145">Suscribirse a eventos de UI Automation</span><span class="sxs-lookup"><span data-stu-id="14202-145">Subscribing to UI Automation Events</span></span>](uiauto-eventsforclients.md)
</dt> <dt>

[<span data-ttu-id="14202-146">Información general sobre eventos de UI Automation</span><span class="sxs-lookup"><span data-stu-id="14202-146">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

<span data-ttu-id="14202-147">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="14202-147">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="14202-148">INFORMACIÓN: descripciones y funcionamiento de modelos de subprocesos OLE</span><span class="sxs-lookup"><span data-stu-id="14202-148">INFO: Descriptions and Workings of OLE Threading Models</span></span>](https://support.microsoft.com/kb/150777)
</dt> </dl>

 

 