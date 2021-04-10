---
title: Patrón de control CustomNavigation
description: Describe las directrices y convenciones para implementar la interfaz ICustomNavigationProvider, incluida la información sobre las propiedades y los métodos.
ms.assetid: 428540BB-5CC0-4F49-8384-0FFC130FBB38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cc6524585f3ddd7ec764a791141fce9daa3c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268722"
---
# <a name="customnavigation-control-pattern"></a><span data-ttu-id="78315-103">Patrón de control CustomNavigation</span><span class="sxs-lookup"><span data-stu-id="78315-103">CustomNavigation Control Pattern</span></span>

<span data-ttu-id="78315-104">Describe las directrices y convenciones para implementar la interfaz **ICustomNavigationProvider** , incluida la información sobre las propiedades y los métodos.</span><span class="sxs-lookup"><span data-stu-id="78315-104">Describes guidelines and conventions for implementing the **ICustomNavigationProvider** interface, including information about properties and methods.</span></span> <span data-ttu-id="78315-105">El patrón de control **CustomNavigation** se usa para habilitar la navegación personalizada entre controles en estructuras similares a las jerarquías, como elementos de lista, listas con viñetas, listas numeradas y encabezados.</span><span class="sxs-lookup"><span data-stu-id="78315-105">The **CustomNavigation** control pattern is used to enable custom navigation between controls in hierarchy-like structures such as list items, bulleted lists, numbered lists and headings.</span></span> <span data-ttu-id="78315-106">Esto permite a los proveedores describir estructuras o definir las relaciones navegables mediante el elemento por sí solo y no solo el control contenedor.</span><span class="sxs-lookup"><span data-stu-id="78315-106">This enables providers to describe structures or define the navigable relationships using the element alone and not just the containing control.</span></span>

<span data-ttu-id="78315-107">Para obtener ejemplos de controles que implementan este patrón de control, vea [tipos de control y sus patrones de control admitidos](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="78315-107">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="78315-108">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="78315-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="78315-109">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="78315-109">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="78315-110">Miembros requeridos para **ICustomNavigationProvider**</span><span class="sxs-lookup"><span data-stu-id="78315-110">Required Members for **ICustomNavigationProvider**</span></span>](#required-members-for-icustomnavigationprovider)
-   [<span data-ttu-id="78315-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="78315-111">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="78315-112">Directrices y convenciones de implementación</span><span class="sxs-lookup"><span data-stu-id="78315-112">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="78315-113">Al implementar el proveedor **CustomNavigation** , tenga en cuenta las siguientes directrices y convenciones:</span><span class="sxs-lookup"><span data-stu-id="78315-113">When implementing the **CustomNavigation** provider, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="78315-114">Los valores de propiedad de **PositionInSet**, **SizeOfSet** y **LEVEL** son valores enteros basados en uno.</span><span class="sxs-lookup"><span data-stu-id="78315-114">Property values for **PositionInSet**, **SizeOfSet**, and **Level** are one-based integer values.</span></span>
-   <span data-ttu-id="78315-115">**ICustomNavigationProvider** no proporciona una manipulación activa del control, como mover posiciones, agregar y quitar elementos, o promover y degradar niveles.</span><span class="sxs-lookup"><span data-stu-id="78315-115">**ICustomNavigationProvider** does not provide for active manipulation of the control such as moving positions, adding and removing items, or promoting and demoting levels.</span></span>
-   <span data-ttu-id="78315-116">Los controles que implementan **ICustomNavigationProvider** normalmente tienen una estructura jerárquica, pero pueden omitir los niveles mediante el método **Navigate** .</span><span class="sxs-lookup"><span data-stu-id="78315-116">Controls that implement **ICustomNavigationProvider** typically have a hierarchical structure, but can skip levels by using the **Navigate** method.</span></span> <span data-ttu-id="78315-117">Las propiedades **PositionInSet**, **SizeOfSet** y **LEVEL** son necesarias en el patrón.</span><span class="sxs-lookup"><span data-stu-id="78315-117">The properties **PositionInSet**, **SizeOfSet**, and **Level** are required on the pattern.</span></span>

## <a name="required-members-for-icustomnavigationprovider"></a><span data-ttu-id="78315-118">Miembros requeridos para **ICustomNavigationProvider**</span><span class="sxs-lookup"><span data-stu-id="78315-118">Required Members for **ICustomNavigationProvider**</span></span>

<span data-ttu-id="78315-119">Las siguientes propiedades son necesarias para implementar la interfaz **ICustomNavigationProvider** .</span><span class="sxs-lookup"><span data-stu-id="78315-119">The following properties are required for implementing the **ICustomNavigationProvider** interface.</span></span>



| <span data-ttu-id="78315-120">Miembros requeridos</span><span class="sxs-lookup"><span data-stu-id="78315-120">Required members</span></span>                                                                  | <span data-ttu-id="78315-121">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="78315-121">Member type</span></span> | <span data-ttu-id="78315-122">Notas</span><span class="sxs-lookup"><span data-stu-id="78315-122">Notes</span></span>                                                                               |
|-----------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="78315-123">**CachedLevel**</span><span class="sxs-lookup"><span data-stu-id="78315-123">**CachedLevel**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedlevel)                   | <span data-ttu-id="78315-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="78315-124">Property</span></span>    | <span data-ttu-id="78315-125">Ubicado en la interfaz [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="78315-125">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="78315-126">**CachedPositionInSet**</span><span class="sxs-lookup"><span data-stu-id="78315-126">**CachedPositionInSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedpositioninset)   | <span data-ttu-id="78315-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="78315-127">Property</span></span>    | <span data-ttu-id="78315-128">Ubicado en la interfaz [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="78315-128">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="78315-129">**CachedSizeOfSet**</span><span class="sxs-lookup"><span data-stu-id="78315-129">**CachedSizeOfSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedsizeofset)           | <span data-ttu-id="78315-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="78315-130">Property</span></span>    | <span data-ttu-id="78315-131">Ubicado en la interfaz [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="78315-131">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="78315-132">**CurrentLevel**</span><span class="sxs-lookup"><span data-stu-id="78315-132">**CurrentLevel**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentlevel)                 | <span data-ttu-id="78315-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="78315-133">Property</span></span>    | <span data-ttu-id="78315-134">Ubicado en la interfaz [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="78315-134">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="78315-135">**CurrentPositionInSet**</span><span class="sxs-lookup"><span data-stu-id="78315-135">**CurrentPositionInSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentpositioninset) | <span data-ttu-id="78315-136">Propiedad</span><span class="sxs-lookup"><span data-stu-id="78315-136">Property</span></span>    | <span data-ttu-id="78315-137">Ubicado en la interfaz [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="78315-137">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="78315-138">**CurrentSizeOfSet**</span><span class="sxs-lookup"><span data-stu-id="78315-138">**CurrentSizeOfSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentsizeofset)         | <span data-ttu-id="78315-139">Propiedad</span><span class="sxs-lookup"><span data-stu-id="78315-139">Property</span></span>    | <span data-ttu-id="78315-140">Ubicado en la interfaz [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="78315-140">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="78315-141">**Navegar**</span><span class="sxs-lookup"><span data-stu-id="78315-141">**Navigate**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate)                   | <span data-ttu-id="78315-142">Método</span><span class="sxs-lookup"><span data-stu-id="78315-142">Method</span></span>      | <span data-ttu-id="78315-143">None</span><span class="sxs-lookup"><span data-stu-id="78315-143">None</span></span>                                                                                |



 

<span data-ttu-id="78315-144">Este patrón de control no tiene métodos o propiedades asociados.</span><span class="sxs-lookup"><span data-stu-id="78315-144">This control pattern has no associated methods or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78315-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="78315-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78315-146">Tipos de control y sus patrones de control admitidos</span><span class="sxs-lookup"><span data-stu-id="78315-146">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="78315-147">ListItem (control)</span><span class="sxs-lookup"><span data-stu-id="78315-147">ListItem Control</span></span>](uiauto-supportlistitemcontroltype.md)
</dt> <dt>

[<span data-ttu-id="78315-148">HeaderItem (control)</span><span class="sxs-lookup"><span data-stu-id="78315-148">HeaderItem Control</span></span>](uiauto-supportheaderitemcontroltype.md)
</dt> <dt>

[<span data-ttu-id="78315-149">DataItem (control)</span><span class="sxs-lookup"><span data-stu-id="78315-149">DataItem Control</span></span>](uiauto-supportdataitemcontroltype.md)
</dt> <dt>

[<span data-ttu-id="78315-150">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="78315-150">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




