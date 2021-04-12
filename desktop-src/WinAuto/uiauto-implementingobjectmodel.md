---
title: ObjectModel (patrón de control)
description: Describe las directrices y convenciones para implementar IObjectModelProvider, incluida información sobre los métodos. El patrón de control ObjectModel se usa para exponer un puntero al modelo de objetos subyacente de un documento.
ms.assetid: 90A6937E-0E98-41EF-8EEB-E23CB71510E4
keywords:
- Automatización de la interfaz de usuario, implementar el patrón de control ObjectModel
- UI Automation, ObjectModel (patrón de control)
- Automatización de la interfaz de usuario, IObjectModelProvider
- IObjectModelProvider
- implementar el patrón de control ObjectModel de automatización de la interfaz de usuario
- ObjectModel (patrón de control)
- patrones de control, IObjectModelProvider
- patrones de control, implementación de UI Automation ObjectModel
- patrones de control, ObjectModel
- interfaces, IObjectModelProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ff115233faf19f93963153a0b2a0a1ff52c3f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359189"
---
# <a name="objectmodel-control-pattern"></a><span data-ttu-id="d0a0a-114">ObjectModel (patrón de control)</span><span class="sxs-lookup"><span data-stu-id="d0a0a-114">ObjectModel Control Pattern</span></span>

<span data-ttu-id="d0a0a-115">Describe las directrices y convenciones para implementar [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider), incluida información sobre los métodos.</span><span class="sxs-lookup"><span data-stu-id="d0a0a-115">Describes guidelines and conventions for implementing [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider), including information about methods.</span></span> <span data-ttu-id="d0a0a-116">El patrón de control **ObjectModel** se usa para exponer un puntero al modelo de objetos subyacente de un documento.</span><span class="sxs-lookup"><span data-stu-id="d0a0a-116">The **ObjectModel** control pattern is used to expose a pointer to the underlying object model of a document.</span></span>

<span data-ttu-id="d0a0a-117">Muchas aplicaciones implementan modelos de objetos enriquecidos que agregan valor más allá de lo que proporciona automatización de la interfaz de usuario de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d0a0a-117">Many applications implement rich object models that add value beyond what Microsoft UI Automation provides.</span></span> <span data-ttu-id="d0a0a-118">Este patrón de control permite a un cliente navegar desde un elemento de automatización de la interfaz de usuario hasta el modelo de objetos subyacente.</span><span class="sxs-lookup"><span data-stu-id="d0a0a-118">This control pattern allows a client to navigate from a UI Automation element into the underlying object model.</span></span>

<span data-ttu-id="d0a0a-119">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="d0a0a-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d0a0a-120">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="d0a0a-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="d0a0a-121">Miembros requeridos para **IObjectModelProvider**</span><span class="sxs-lookup"><span data-stu-id="d0a0a-121">Required Members for **IObjectModelProvider**</span></span>](#required-members-for-iobjectmodelprovider)
-   [<span data-ttu-id="d0a0a-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d0a0a-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="d0a0a-123">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="d0a0a-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="d0a0a-124">Al implementar el patrón de control **ObjectModel** , tenga en cuenta las siguientes directrices y convenciones:</span><span class="sxs-lookup"><span data-stu-id="d0a0a-124">When implementing the **ObjectModel** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="d0a0a-125">El método [**IObjectModelProvider:: GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) debe devolver un puntero al objeto lo más cerca posible del elemento de la interfaz de usuario de origen.</span><span class="sxs-lookup"><span data-stu-id="d0a0a-125">The [**IObjectModelProvider::GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) method should return a pointer to the object that is as close as possible to the source UI element.</span></span> <span data-ttu-id="d0a0a-126">Por ejemplo, en un explorador Web, un proveedor de automatización de la interfaz de usuario para un único elemento debe devolver un puntero del modelo de objetos para el elemento.</span><span class="sxs-lookup"><span data-stu-id="d0a0a-126">For example, in a web browser, a UI Automation provider for a single element should return an object model pointer for the element.</span></span> <span data-ttu-id="d0a0a-127">Devolver un puntero del modelo de objetos para la raíz del documento sería mucho menos útil.</span><span class="sxs-lookup"><span data-stu-id="d0a0a-127">Returning an object model pointer for the document root would be far less useful.</span></span>
-   <span data-ttu-id="d0a0a-128">Se espera que el cliente del patrón de control **ObjectModel** tenga el IID de la interfaz que buscan, por lo que es suficiente para devolver un puntero [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) simple.</span><span class="sxs-lookup"><span data-stu-id="d0a0a-128">The client of the **ObjectModel** control pattern is expected to have the IID for the interface they are seeking, which is why it is enough to return a simple [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer.</span></span>
-   <span data-ttu-id="d0a0a-129">Dado que la automatización de la interfaz de usuario calcula las referencias del puntero al proceso del cliente, el proveedor debe esperar que el cliente tenga acceso al modelo de objetos mediante los procedimientos estándar del modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="d0a0a-129">Because UI Automation marshals the pointer to the client process, the provider should expect the client to access the object model using standard Component Object Model (COM) practices.</span></span>

## <a name="required-members-for-iobjectmodelprovider"></a><span data-ttu-id="d0a0a-130">Miembros requeridos para **IObjectModelProvider**</span><span class="sxs-lookup"><span data-stu-id="d0a0a-130">Required Members for **IObjectModelProvider**</span></span>

<span data-ttu-id="d0a0a-131">El método siguiente es necesario para implementar la interfaz [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider) .</span><span class="sxs-lookup"><span data-stu-id="d0a0a-131">The following method is required for implementing the [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider) interface.</span></span>



| <span data-ttu-id="d0a0a-132">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="d0a0a-132">Required members</span></span>                                                                             | <span data-ttu-id="d0a0a-133">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="d0a0a-133">Member type</span></span> | <span data-ttu-id="d0a0a-134">Notas</span><span class="sxs-lookup"><span data-stu-id="d0a0a-134">Notes</span></span>                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d0a0a-135">**GetUnderlyingObjectModel**</span><span class="sxs-lookup"><span data-stu-id="d0a0a-135">**GetUnderlyingObjectModel**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) | <span data-ttu-id="d0a0a-136">Método</span><span class="sxs-lookup"><span data-stu-id="d0a0a-136">Method</span></span>      | <span data-ttu-id="d0a0a-137">Devuelve un puntero COM al modelo de objetos subyacente.</span><span class="sxs-lookup"><span data-stu-id="d0a0a-137">Returns a COM pointer to the underlying object model.</span></span> <span data-ttu-id="d0a0a-138">Se espera que el cliente llame al método [**IUnknown:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para recuperar punteros específicos del modelo de objetos.</span><span class="sxs-lookup"><span data-stu-id="d0a0a-138">The client is expected to call the [**IUnknown::QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method to retrieve specific object model pointers.</span></span> |



 

<span data-ttu-id="d0a0a-139">Este patrón de control no tiene eventos asociados.</span><span class="sxs-lookup"><span data-stu-id="d0a0a-139">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0a0a-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d0a0a-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0a0a-141">Tipos de control y sus patrones de control admitidos</span><span class="sxs-lookup"><span data-stu-id="d0a0a-141">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="d0a0a-142">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="d0a0a-142">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="d0a0a-143">Información general sobre el árbol de la UI Automation</span><span class="sxs-lookup"><span data-stu-id="d0a0a-143">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 