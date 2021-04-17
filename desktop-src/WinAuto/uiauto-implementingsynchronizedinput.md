---
title: Patrón de control SynchronizedInput
description: Describe las directrices y convenciones para implementar ISynchronizedInputProvider, incluida información sobre propiedades y métodos.
ms.assetid: 3e2d65ea-8093-4e65-b43e-28478ec74607
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control SynchronizedInput
- Automatización de la interfaz de usuario, patrón de control SynchronizedInput
- Automatización de la interfaz de usuario, ISynchronizedInputProvider
- ISynchronizedInputProvider
- implementación de patrones de control SynchronizedInput de UI Automation
- Patrones de control de SynchronizedInput
- patrones de control, ISynchronizedInputProvider
- patrones de control, implementar la automatización de la interfaz de usuario SynchronizedInput
- patrones de control, SynchronizedInput
- interfaces, ISynchronizedInputProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 105e75163fdac742adaad6b778c251b4b7b8ae70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704735"
---
# <a name="synchronizedinput-control-pattern"></a><span data-ttu-id="dfc3b-113">Patrón de control SynchronizedInput</span><span class="sxs-lookup"><span data-stu-id="dfc3b-113">SynchronizedInput Control Pattern</span></span>

<span data-ttu-id="dfc3b-114">Describe las directrices y convenciones para implementar [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider), incluida información sobre propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="dfc3b-114">Describes guidelines and conventions for implementing [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider), including information about properties and methods.</span></span> <span data-ttu-id="dfc3b-115">El patrón de control **SynchronizedInput** permite a las aplicaciones cliente de automatización de la interfaz de usuario de Microsoft dirigir la entrada del mouse o del teclado a un elemento específico de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="dfc3b-115">The **SynchronizedInput** control pattern enables Microsoft UI Automation client applications to direct the mouse or keyboard input to a specific UI element.</span></span>

<span data-ttu-id="dfc3b-116">Este patrón de control se usa normalmente en scripts de pruebas automatizadas para enviar la entrada del mouse o del teclado a un elemento específico de la interfaz de usuario y, a continuación, comprobar que el elemento ha recibido la entrada.</span><span class="sxs-lookup"><span data-stu-id="dfc3b-116">This control pattern is typically used in automated test scripts to send mouse or keyboard input to a specific user-interface element, and then verify that the element received the input.</span></span>

<span data-ttu-id="dfc3b-117">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="dfc3b-117">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="dfc3b-118">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="dfc3b-118">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="dfc3b-119">Miembros requeridos para **ISynchronizedInputProvider**</span><span class="sxs-lookup"><span data-stu-id="dfc3b-119">Required Members for **ISynchronizedInputProvider**</span></span>](#required-members-for-isynchronizedinputprovider)
-   [<span data-ttu-id="dfc3b-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dfc3b-120">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="dfc3b-121">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="dfc3b-121">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="dfc3b-122">Al implementar el patrón de control **SynchronizedInput** , tenga en cuenta las siguientes directrices y convenciones:</span><span class="sxs-lookup"><span data-stu-id="dfc3b-122">When implementing the **SynchronizedInput** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="dfc3b-123">Cuando se llama al método [**ISynchronizedInputProvider:: StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) , el proveedor de automatización de la interfaz de usuario debe iniciar la comprobación de la entrada del tipo especificado y, a continuación, realizar una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="dfc3b-123">When the [**ISynchronizedInputProvider::StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) method is called, the UI Automation provider should start checking for input of the specified type, and then take one of the following actions:</span></span>
    -   <span data-ttu-id="dfc3b-124">Cuando se encuentra una entrada coincidente para el elemento, el proveedor debe generar el evento de [**\_ InputReachedTargetEventId de UIA**](uiauto-event-ids.md) .</span><span class="sxs-lookup"><span data-stu-id="dfc3b-124">When matching input is found for the element, the provider should raise the [**UIA\_InputReachedTargetEventId**](uiauto-event-ids.md) event.</span></span>
    -   <span data-ttu-id="dfc3b-125">Cuando se encuentra la entrada coincidente, pero alcanzó un elemento diferente, el proveedor debe generar el evento de [**\_ InputReachedOtherElementEventId de UIA**](uiauto-event-ids.md) .</span><span class="sxs-lookup"><span data-stu-id="dfc3b-125">When matching input is found, but it reached a different element, the provider should raise the [**UIA\_InputReachedOtherElementEventId**](uiauto-event-ids.md) event.</span></span>
    -   <span data-ttu-id="dfc3b-126">Cuando se encuentra una entrada no coincidente, el proveedor debe descartar la entrada y generar el evento [**\_ InputDiscardedEventId de UIA**](uiauto-event-ids.md) .</span><span class="sxs-lookup"><span data-stu-id="dfc3b-126">When mismatched input is found, the provider should discard the input and raise the [**UIA\_InputDiscardedEventId**](uiauto-event-ids.md) event.</span></span>
-   <span data-ttu-id="dfc3b-127">El proveedor de automatización de la interfaz de usuario debe descartar la entrada si es para un elemento distinto del elemento actual.</span><span class="sxs-lookup"><span data-stu-id="dfc3b-127">The UI Automation provider must discard the input if it is for an element other than the current element.</span></span>
-   <span data-ttu-id="dfc3b-128">Cuando el elemento recibe la entrada, o cuando se llama al método [**ISynchronizedInputProvider:: CANCEL**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel) , el proveedor detiene la comprobación de la entrada y continúa de la forma habitual.</span><span class="sxs-lookup"><span data-stu-id="dfc3b-128">When the element receives the input, or when the [**ISynchronizedInputProvider::Cancel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel) method is called, the provider stops checking input and continues as normal.</span></span>
-   <span data-ttu-id="dfc3b-129">Si se llama a [**ISynchronizedInputProvider:: StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) cuando el proveedor ya está escuchando la entrada, el proveedor debe devolver [**UIA \_ E \_ INVALIDOPERATION**](uiauto-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="dfc3b-129">If [**ISynchronizedInputProvider::StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) is called when the provider is already listening for input, the provider should return [**UIA\_E\_INVALIDOPERATION**](uiauto-error-codes.md).</span></span>

## <a name="required-members-for-isynchronizedinputprovider"></a><span data-ttu-id="dfc3b-130">Miembros requeridos para **ISynchronizedInputProvider**</span><span class="sxs-lookup"><span data-stu-id="dfc3b-130">Required Members for **ISynchronizedInputProvider**</span></span>

<span data-ttu-id="dfc3b-131">Se requieren las siguientes propiedades, métodos y eventos para implementar la interfaz [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider) .</span><span class="sxs-lookup"><span data-stu-id="dfc3b-131">The following properties, methods, and events are required for implementing the [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider) interface.</span></span>



| <span data-ttu-id="dfc3b-132">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="dfc3b-132">Required members</span></span>                                                                         | <span data-ttu-id="dfc3b-133">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="dfc3b-133">Member type</span></span> | <span data-ttu-id="dfc3b-134">Notas</span><span class="sxs-lookup"><span data-stu-id="dfc3b-134">Notes</span></span> |
|------------------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="dfc3b-135">**StartListening**</span><span class="sxs-lookup"><span data-stu-id="dfc3b-135">**StartListening**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening)               | <span data-ttu-id="dfc3b-136">Método</span><span class="sxs-lookup"><span data-stu-id="dfc3b-136">Method</span></span>      | <span data-ttu-id="dfc3b-137">None</span><span class="sxs-lookup"><span data-stu-id="dfc3b-137">None</span></span>  |
| [<span data-ttu-id="dfc3b-138">**Cancelar**</span><span class="sxs-lookup"><span data-stu-id="dfc3b-138">**Cancel**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel)                               | <span data-ttu-id="dfc3b-139">Método</span><span class="sxs-lookup"><span data-stu-id="dfc3b-139">Method</span></span>      | <span data-ttu-id="dfc3b-140">None</span><span class="sxs-lookup"><span data-stu-id="dfc3b-140">None</span></span>  |
| [<span data-ttu-id="dfc3b-141">**UIA \_ InputReachedTargetEventId**</span><span class="sxs-lookup"><span data-stu-id="dfc3b-141">**UIA\_InputReachedTargetEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="dfc3b-142">Evento</span><span class="sxs-lookup"><span data-stu-id="dfc3b-142">Event</span></span>       | <span data-ttu-id="dfc3b-143">None</span><span class="sxs-lookup"><span data-stu-id="dfc3b-143">None</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="dfc3b-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dfc3b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfc3b-145">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="dfc3b-145">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




