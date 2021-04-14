---
title: Funciones de patrón de control desusadas
description: Funciones de patrón de control desusadas
ms.assetid: 06434b07-7592-4909-8c4e-064382bdbf98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f646f9a9e3139d487785e344b9d3fc242b1a40e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418445"
---
# <a name="deprecated-control-pattern-functions"></a><span data-ttu-id="1fd39-103">Funciones de patrón de control desusadas</span><span class="sxs-lookup"><span data-stu-id="1fd39-103">Deprecated Control Pattern Functions</span></span>

> [!Note]  
> <span data-ttu-id="1fd39-104">Las funciones de patrón de control descritas en esta sección están desusadas.</span><span class="sxs-lookup"><span data-stu-id="1fd39-104">The control pattern functions described in this section are deprecated.</span></span> <span data-ttu-id="1fd39-105">Las aplicaciones cliente deben usar las interfaces del modelo de objetos componentes (COM) que se describen en las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="1fd39-105">Client applications should use the Component Object Model (COM) interfaces described in the following sections:</span></span>
>
> -   [<span data-ttu-id="1fd39-106">Interfaces de elementos de UI Automation para clientes</span><span class="sxs-lookup"><span data-stu-id="1fd39-106">UI Automation Element Interfaces for Clients</span></span>](uiauto-entry-uiautoclientinterfaces.md)
> -   [<span data-ttu-id="1fd39-107">Interfaz de condición de propiedad para clientes</span><span class="sxs-lookup"><span data-stu-id="1fd39-107">Property Condition Interface for Clients</span></span>](uiauto-client-propconditioninterfaces.md)
> -   [<span data-ttu-id="1fd39-108">Interfaces de patrón de control para clientes</span><span class="sxs-lookup"><span data-stu-id="1fd39-108">Control Pattern Interfaces for Clients</span></span>](uiauto-client-controlpatterninterfaces.md)
> -   [<span data-ttu-id="1fd39-109">Interfaces de control de eventos para clientes</span><span class="sxs-lookup"><span data-stu-id="1fd39-109">Event Handling Interfaces for Clients</span></span>](uiauto-client-eventhandlinginterfaces.md)
> -   [<span data-ttu-id="1fd39-110">Interfaces de generador de proxy para clientes</span><span class="sxs-lookup"><span data-stu-id="1fd39-110">Proxy Factory Interfaces for Clients</span></span>](uiauto-client-proxyfactoryinterfaces.md)

 

## <a name="in-this-section"></a><span data-ttu-id="1fd39-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="1fd39-111">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1fd39-112">Función</span><span class="sxs-lookup"><span data-stu-id="1fd39-112">Function</span></span></th>
<th><span data-ttu-id="1fd39-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="1fd39-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1fd39-114"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-dockpattern_setdockposition"><strong>DockPattern_SetDockPosition</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-114"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-dockpattern_setdockposition"><strong>DockPattern_SetDockPosition</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-115">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-115">This function is deprecated.</span></span> <span data-ttu-id="1fd39-116">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1fd39-116">Client applications should use the Microsoft UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-117">Acopla el elemento de automatización de la interfaz de usuario en el <em>dockPosition</em> solicitado dentro de un contenedor de acoplamiento.</span><span class="sxs-lookup"><span data-stu-id="1fd39-117">Docks the UI Automation element at the requested <em>dockPosition</em> within a docking container.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-118"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_collapse"><strong>ExpandCollapsePattern_Collapse</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-118"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_collapse"><strong>ExpandCollapsePattern_Collapse</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-119">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-119">This function is deprecated.</span></span> <span data-ttu-id="1fd39-120">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-120">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-121">Oculta todos los nodos descendientes, los controles o el contenido del elemento de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-121">Hides all descendant nodes, controls, or content of the UI Automation element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-122"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_expand"><strong>ExpandCollapsePattern_Expand</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-122"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_expand"><strong>ExpandCollapsePattern_Expand</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-123">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-123">This function is deprecated.</span></span> <span data-ttu-id="1fd39-124">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-124">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-125">Expande un control de la pantalla para que muestre más información.</span><span class="sxs-lookup"><span data-stu-id="1fd39-125">Expands a control on the screen so that it shows more information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-126"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-gridpattern_getitem"><strong>GridPattern_GetItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-126"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-gridpattern_getitem"><strong>GridPattern_GetItem</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-127">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-127">This function is deprecated.</span></span> <span data-ttu-id="1fd39-128">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-128">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-129">Obtiene el nodo de un elemento en una cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="1fd39-129">Gets the node for an item in a grid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-130"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-invokepattern_invoke"><strong>InvokePattern_Invoke</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-130"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-invokepattern_invoke"><strong>InvokePattern_Invoke</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-131">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-131">This function is deprecated.</span></span> <span data-ttu-id="1fd39-132">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-132">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-133">Envía una solicitud para activar un control e iniciar su acción única e inequívoca.</span><span class="sxs-lookup"><span data-stu-id="1fd39-133">Sends a request to activate a control and initiate its single, unambiguous action.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-134"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-itemcontainerpattern_finditembyproperty"><strong>ItemContainerPattern_FindItemByProperty</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-134"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-itemcontainerpattern_finditembyproperty"><strong>ItemContainerPattern_FindItemByProperty</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-135">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-135">This function is deprecated.</span></span> <span data-ttu-id="1fd39-136">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-136">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-137">Recupera un nodo dentro de un nodo contenedor, basado en un valor de propiedad especificado.</span><span class="sxs-lookup"><span data-stu-id="1fd39-137">Retrieves a node within a containing node, based on a specified property value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-138"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_dodefaultaction"><strong>LegacyIAccessiblePattern_DoDefaultAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-138"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_dodefaultaction"><strong>LegacyIAccessiblePattern_DoDefaultAction</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-139">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-139">This function is deprecated.</span></span> <span data-ttu-id="1fd39-140">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-140">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-141">Realiza la acción predeterminada de Microsoft Active Accessibility para el elemento.</span><span class="sxs-lookup"><span data-stu-id="1fd39-141">Performs the Microsoft Active Accessibility default action for the element.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-142"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_getiaccessible"><strong>LegacyIAccessiblePattern_GetIAccessible</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-142"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_getiaccessible"><strong>LegacyIAccessiblePattern_GetIAccessible</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-143">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-143">This function is deprecated.</span></span> <span data-ttu-id="1fd39-144">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-144">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-145">Recupera un objeto <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible"><strong>IAccessible</strong></a> que corresponde al elemento de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-145">Retrieves an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible"><strong>IAccessible</strong></a> object that corresponds to the UI Automation element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-146"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_select"><strong>LegacyIAccessiblePattern_Select</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-146"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_select"><strong>LegacyIAccessiblePattern_Select</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-147">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-147">This function is deprecated.</span></span> <span data-ttu-id="1fd39-148">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-148">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-149">Realiza una selección de Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="1fd39-149">Performs a Microsoft Active Accessibility selection.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-150"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_setvalue"><strong>LegacyIAccessiblePattern_SetValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-150"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_setvalue"><strong>LegacyIAccessiblePattern_SetValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-151">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-151">This function is deprecated.</span></span> <span data-ttu-id="1fd39-152">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-152">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-153">Establece la propiedad de valor de Microsoft Active Accessibility para el nodo.</span><span class="sxs-lookup"><span data-stu-id="1fd39-153">Sets the Microsoft Active Accessibility value property for the node.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-154"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_getviewname"><strong>MultipleViewPattern_GetViewName</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-154"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_getviewname"><strong>MultipleViewPattern_GetViewName</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-155">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-155">This function is deprecated.</span></span> <span data-ttu-id="1fd39-156">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-156">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-157">Recupera el nombre de una vista específica del control.</span><span class="sxs-lookup"><span data-stu-id="1fd39-157">Retrieves the name of a control-specific view.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-158"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_setcurrentview"><strong>MultipleViewPattern_SetCurrentView</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-158"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_setcurrentview"><strong>MultipleViewPattern_SetCurrentView</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-159">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-159">This function is deprecated.</span></span> <span data-ttu-id="1fd39-160">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-160">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-161">Establece un control en un diseño diferente.</span><span class="sxs-lookup"><span data-stu-id="1fd39-161">Sets a control to a different layout.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-162"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-rangevaluepattern_setvalue"><strong>RangeValuePattern_SetValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-162"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-rangevaluepattern_setvalue"><strong>RangeValuePattern_SetValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-163">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-163">This function is deprecated.</span></span> <span data-ttu-id="1fd39-164">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-164">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-165">Establece el valor de un control que tiene un intervalo numérico.</span><span class="sxs-lookup"><span data-stu-id="1fd39-165">Sets the value of a control that has a numerical range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-166"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollitempattern_scrollintoview"><strong>ScrollItemPattern_ScrollIntoView</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-166"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollitempattern_scrollintoview"><strong>ScrollItemPattern_ScrollIntoView</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-167">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-167">This function is deprecated.</span></span> <span data-ttu-id="1fd39-168">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-168">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-169">Desplaza el área de contenido de un objeto contenedor para mostrar el elemento de automatización de la interfaz de usuario dentro del área visible (ventanilla) del contenedor.</span><span class="sxs-lookup"><span data-stu-id="1fd39-169">Scrolls the content area of a container object in order to display the UI Automation element within the visible region (viewport) of the container.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-170"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_scroll"><strong>ScrollPattern_Scroll</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-170"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_scroll"><strong>ScrollPattern_Scroll</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-171">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-171">This function is deprecated.</span></span> <span data-ttu-id="1fd39-172">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-172">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-173">Desplaza la región visible actualmente del área de contenido a los <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount"><strong>ScrollAmount</strong></a>especificados, horizontalmente, verticalmente, o ambos.</span><span class="sxs-lookup"><span data-stu-id="1fd39-173">Scrolls the currently visible region of the content area the specified <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount"><strong>ScrollAmount</strong></a>, horizontally, vertically, or both.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-174"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_setscrollpercent"><strong>ScrollPattern_SetScrollPercent</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-174"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_setscrollpercent"><strong>ScrollPattern_SetScrollPercent</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-175">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-175">This function is deprecated.</span></span> <span data-ttu-id="1fd39-176">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-176">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-177">Desplaza un contenedor a una posición específica horizontalmente, verticalmente o ambos.</span><span class="sxs-lookup"><span data-stu-id="1fd39-177">Scrolls a container to a specific position horizontally, vertically, or both.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-178"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_addtoselection"><strong>SelectionItemPattern_AddToSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-178"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_addtoselection"><strong>SelectionItemPattern_AddToSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-179">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-179">This function is deprecated.</span></span> <span data-ttu-id="1fd39-180">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-180">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-181">Agrega un elemento no seleccionado a una selección de un control.</span><span class="sxs-lookup"><span data-stu-id="1fd39-181">Adds an unselected element to a selection in a control.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-182"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_removefromselection"><strong>SelectionItemPattern_RemoveFromSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-182"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_removefromselection"><strong>SelectionItemPattern_RemoveFromSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-183">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-183">This function is deprecated.</span></span> <span data-ttu-id="1fd39-184">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-184">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-185">Quita un elemento de la selección de un contenedor de selección.</span><span class="sxs-lookup"><span data-stu-id="1fd39-185">Removes an element from the selection in a selection container.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-186"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_select"><strong>SelectionItemPattern_Select</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-186"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_select"><strong>SelectionItemPattern_Select</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-187">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-187">This function is deprecated.</span></span> <span data-ttu-id="1fd39-188">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-188">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-189">Selecciona un elemento de un contenedor de selección.</span><span class="sxs-lookup"><span data-stu-id="1fd39-189">Selects an element in a selection container.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-190"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_cancel"><strong>SynchronizedInputPattern_Cancel</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-190"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_cancel"><strong>SynchronizedInputPattern_Cancel</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-191">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-191">This function is deprecated.</span></span> <span data-ttu-id="1fd39-192">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-192">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-193">Hace que el proveedor de automatización de la interfaz de usuario deje de escuchar la entrada del mouse o del teclado.</span><span class="sxs-lookup"><span data-stu-id="1fd39-193">Causes the UI Automation provider to stop listening for mouse or keyboard input.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-194"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_startlistening"><strong>SynchronizedInputPattern_StartListening</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-194"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_startlistening"><strong>SynchronizedInputPattern_StartListening</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-195">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-195">This function is deprecated.</span></span> <span data-ttu-id="1fd39-196">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-196">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-197">Hace que el proveedor de automatización de la interfaz de usuario empiece a escuchar la entrada del mouse o del teclado.</span><span class="sxs-lookup"><span data-stu-id="1fd39-197">Causes the UI Automation provider to start listening for mouse or keyboard input.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-198"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_documentrange"><strong>TextPattern_get_DocumentRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-198"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_documentrange"><strong>TextPattern_get_DocumentRange</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-199">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-199">This function is deprecated.</span></span> <span data-ttu-id="1fd39-200">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-200">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-201">Obtiene el intervalo de texto para todo el documento.</span><span class="sxs-lookup"><span data-stu-id="1fd39-201">Gets the text range for the entire document.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-202"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_supportedtextselection"><strong>TextPattern_get_SupportedTextSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-202"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_supportedtextselection"><strong>TextPattern_get_SupportedTextSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-203">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-203">This function is deprecated.</span></span> <span data-ttu-id="1fd39-204">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-204">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-205">Determina si el contenido del contenedor de texto se puede seleccionar y anular la selección.</span><span class="sxs-lookup"><span data-stu-id="1fd39-205">Ascertains whether the text container's contents can be selected and deselected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-206"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getselection"><strong>TextPattern_GetSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-206"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getselection"><strong>TextPattern_GetSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-207">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-207">This function is deprecated.</span></span> <span data-ttu-id="1fd39-208">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-208">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-209">Obtiene el intervalo actual del texto seleccionado de un contenedor de texto que admite el patrón de texto.</span><span class="sxs-lookup"><span data-stu-id="1fd39-209">Gets the current range of selected text from a text container supporting the text pattern.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-210"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getvisibleranges"><strong>TextPattern_GetVisibleRanges</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-210"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getvisibleranges"><strong>TextPattern_GetVisibleRanges</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-211">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-211">This function is deprecated.</span></span> <span data-ttu-id="1fd39-212">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-212">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-213">Recupera una matriz de intervalos de texto no contiguos de un contenedor de texto donde cada intervalo comienza con la primera línea parcialmente visible y continúa hasta el final de la última línea parcialmente visible.</span><span class="sxs-lookup"><span data-stu-id="1fd39-213">Retrieves an array of disjoint text ranges from a text container where each text range begins with the first partially visible line through to the end of the last partially visible line.</span></span> <span data-ttu-id="1fd39-214">Por ejemplo, un diseño de varias columnas en el que las columnas se desplazan parcialmente fuera del área visible de la ventanilla y el contenido fluye desde la parte inferior de una columna hasta la parte superior de la siguiente.</span><span class="sxs-lookup"><span data-stu-id="1fd39-214">For example, a multi-column layout where the columns are partially scrolled out of the visible area of the viewport and the content flows from the bottom of one column to the top of the next.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-215"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefromchild"><strong>TextPattern_RangeFromChild</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-215"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefromchild"><strong>TextPattern_RangeFromChild</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-216">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-216">This function is deprecated.</span></span> <span data-ttu-id="1fd39-217">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-217">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-218">Obtiene el intervalo de texto que abarca un nodo determinado.</span><span class="sxs-lookup"><span data-stu-id="1fd39-218">Gets the text range that a given node spans.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-219"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefrompoint"><strong>TextPattern_RangeFromPoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-219"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefrompoint"><strong>TextPattern_RangeFromPoint</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-220">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-220">This function is deprecated.</span></span> <span data-ttu-id="1fd39-221">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-221">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-222">Recupera el intervalo de texto degenerado (vacío) más cercano a las coordenadas de pantalla especificadas.</span><span class="sxs-lookup"><span data-stu-id="1fd39-222">Retrieves the degenerate (empty) text range nearest to the specified screen coordinates.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-223"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_addtoselection"><strong>TextRange_AddToSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-223"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_addtoselection"><strong>TextRange_AddToSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-224">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-224">This function is deprecated.</span></span> <span data-ttu-id="1fd39-225">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-225">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-226">Agrega a la colección existente de texto resaltado en un contenedor de texto que admite varias selecciones discontinuas resaltando el texto complementario correspondiente a los extremos <em>inicial</em> y <em>final</em> del intervalo de texto que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-226">Adds to the existing collection of highlighted text in a text container that supports multiple, disjoint selections by highlighting supplementary text corresponding to the calling text range <em>Start</em> and <em>End</em> endpoints.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-227"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_clone"><strong>TextRange_Clone</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-227"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_clone"><strong>TextRange_Clone</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-228">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-228">This function is deprecated.</span></span> <span data-ttu-id="1fd39-229">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-229">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-230">Copia un intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="1fd39-230">Copies a text range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-231"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compare"><strong>TextRange_Compare</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-231"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compare"><strong>TextRange_Compare</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-232">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-232">This function is deprecated.</span></span> <span data-ttu-id="1fd39-233">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-233">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-234">Compara dos intervalos de texto.</span><span class="sxs-lookup"><span data-stu-id="1fd39-234">Compares two text ranges.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-235"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compareendpoints"><strong>TextRange_CompareEndpoints</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-235"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compareendpoints"><strong>TextRange_CompareEndpoints</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-236">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-236">This function is deprecated.</span></span> <span data-ttu-id="1fd39-237">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-237">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-238">Devuelve un valor que indica si dos intervalos de texto tienen extremos idénticos.</span><span class="sxs-lookup"><span data-stu-id="1fd39-238">Returns a value indicating whether two text ranges have identical endpoints.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-239"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_expandtoenclosingunit"><strong>TextRange_ExpandToEnclosingUnit</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-239"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_expandtoenclosingunit"><strong>TextRange_ExpandToEnclosingUnit</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-240">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-240">This function is deprecated.</span></span> <span data-ttu-id="1fd39-241">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-241">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-242">Expande el intervalo de texto a una unidad más grande o más pequeña, como carácter, palabra, línea o página.</span><span class="sxs-lookup"><span data-stu-id="1fd39-242">Expands the text range to a larger or smaller unit such as Character, Word, Line, or Page.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-243"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findattribute"><strong>TextRange_FindAttribute</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-243"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findattribute"><strong>TextRange_FindAttribute</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-244">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-244">This function is deprecated.</span></span> <span data-ttu-id="1fd39-245">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-245">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-246">Busca en una dirección especificada para el primer fragmento de texto compatible con un atributo de texto especificado.</span><span class="sxs-lookup"><span data-stu-id="1fd39-246">Searches in a specified direction for the first piece of text supporting a specified text attribute.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-247"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findtext"><strong>TextRange_FindText</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-247"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findtext"><strong>TextRange_FindText</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-248">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-248">This function is deprecated.</span></span> <span data-ttu-id="1fd39-249">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-249">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-250">Devuelve el primer intervalo de texto en la dirección especificada que contiene el texto que el cliente está buscando.</span><span class="sxs-lookup"><span data-stu-id="1fd39-250">Returns the first text range in the specified direction that contains the text the client is searching for.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-251"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getattributevalue"><strong>TextRange_GetAttributeValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-251"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getattributevalue"><strong>TextRange_GetAttributeValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-252">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-252">This function is deprecated.</span></span> <span data-ttu-id="1fd39-253">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-253">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-254">Obtiene el valor de un atributo de texto para un intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="1fd39-254">Gets the value of an text attribute for a text range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-255"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getboundingrectangles"><strong>TextRange_GetBoundingRectangles</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-255"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getboundingrectangles"><strong>TextRange_GetBoundingRectangles</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-256">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-256">This function is deprecated.</span></span> <span data-ttu-id="1fd39-257">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-257">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-258">Recupera el número mínimo de rectángulos delimitadores que pueden incluir el intervalo, un rectángulo por línea.</span><span class="sxs-lookup"><span data-stu-id="1fd39-258">Retrieves the minimum number of bounding rectangles that can enclose the range, one rectangle per line.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-259"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getchildren"><strong>TextRange_GetChildren</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-259"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getchildren"><strong>TextRange_GetChildren</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-260">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-260">This function is deprecated.</span></span> <span data-ttu-id="1fd39-261">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-261">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-262">Devuelve todos los elementos de automatización de la interfaz de usuario contenidos en el intervalo de texto especificado.</span><span class="sxs-lookup"><span data-stu-id="1fd39-262">Returns all UI Automation elements contained within the specified text range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-263"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getenclosingelement"><strong>TextRange_GetEnclosingElement</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-263"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getenclosingelement"><strong>TextRange_GetEnclosingElement</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-264">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-264">This function is deprecated.</span></span> <span data-ttu-id="1fd39-265">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-265">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-266">Devuelve el nodo del siguiente proveedor más pequeño que cubre el intervalo.</span><span class="sxs-lookup"><span data-stu-id="1fd39-266">Returns the node for the next smallest provider that covers the range.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-267"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_gettext"><strong>TextRange_GetText</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-267"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_gettext"><strong>TextRange_GetText</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-268">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-268">This function is deprecated.</span></span> <span data-ttu-id="1fd39-269">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-269">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-270">Devuelve el texto de un intervalo de texto, hasta un número especificado de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1fd39-270">Returns the text in a text range, up to a specified number of characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-271"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_move"><strong>TextRange_Move</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-271"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_move"><strong>TextRange_Move</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-272">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-272">This function is deprecated.</span></span> <span data-ttu-id="1fd39-273">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-273">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-274">Mueve el intervalo de texto el número especificado de unidades que solicita el cliente.</span><span class="sxs-lookup"><span data-stu-id="1fd39-274">Moves the text range the specified number of units requested by the client.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-275"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyrange"><strong>TextRange_MoveEndpointByRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-275"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyrange"><strong>TextRange_MoveEndpointByRange</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-276">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-276">This function is deprecated.</span></span> <span data-ttu-id="1fd39-277">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-277">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-278">Mueve un extremo de un intervalo al extremo de otro intervalo.</span><span class="sxs-lookup"><span data-stu-id="1fd39-278">Moves an endpoint of one range to the endpoint of another range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-279"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyunit"><strong>TextRange_MoveEndpointByUnit</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-279"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyunit"><strong>TextRange_MoveEndpointByUnit</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-280">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-280">This function is deprecated.</span></span> <span data-ttu-id="1fd39-281">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-281">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-282">Mueve un extremo del intervalo el número de unidades especificado.</span><span class="sxs-lookup"><span data-stu-id="1fd39-282">Moves an endpoint of the range the specified number of units.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-283"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_removefromselection"><strong>TextRange_RemoveFromSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-283"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_removefromselection"><strong>TextRange_RemoveFromSelection</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-284">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-284">This function is deprecated.</span></span> <span data-ttu-id="1fd39-285">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-285">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-286">Quita el texto seleccionado, que se corresponde con el intervalo de texto que realiza la llamada <em>TextPatternRangeEndpoint_Start</em> y <em>TextPatternRangeEndpoint_End</em> puntos de conexión, de una colección existente de texto seleccionado en un contenedor de texto que admite varias selecciones discontinuas.</span><span class="sxs-lookup"><span data-stu-id="1fd39-286">Removes the selected text, corresponding to the calling text range <em>TextPatternRangeEndpoint_Start</em> and <em>TextPatternRangeEndpoint_End</em> endpoints, from an existing collection of selected text in a text container that supports multiple, disjoint selections.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-287"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_scrollintoview"><strong>TextRange_ScrollIntoView</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-287"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_scrollintoview"><strong>TextRange_ScrollIntoView</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-288">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-288">This function is deprecated.</span></span> <span data-ttu-id="1fd39-289">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-289">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-290">Desplaza el texto para que el intervalo especificado esté visible en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="1fd39-290">Scrolls the text so the specified range is visible in the viewport.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-291"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_select"><strong>TextRange_Select</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-291"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_select"><strong>TextRange_Select</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-292">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-292">This function is deprecated.</span></span> <span data-ttu-id="1fd39-293">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-293">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-294">Selecciona un intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="1fd39-294">Selects a text range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-295"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-togglepattern_toggle"><strong>TogglePattern_Toggle</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-295"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-togglepattern_toggle"><strong>TogglePattern_Toggle</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-296">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-296">This function is deprecated.</span></span> <span data-ttu-id="1fd39-297">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-297">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-298">Alterna un control a su siguiente estado admitido.</span><span class="sxs-lookup"><span data-stu-id="1fd39-298">Toggles a control to its next supported state.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-299"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_move"><strong>TransformPattern_Move</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-299"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_move"><strong>TransformPattern_Move</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-300">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-300">This function is deprecated.</span></span> <span data-ttu-id="1fd39-301">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-301">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-302">Mueve un elemento a una ubicación especificada de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="1fd39-302">Moves an element to a specified location on the screen.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-303"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_resize"><strong>TransformPattern_Resize</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-303"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_resize"><strong>TransformPattern_Resize</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-304">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-304">This function is deprecated.</span></span> <span data-ttu-id="1fd39-305">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-305">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-306">Cambia el tamaño de un elemento de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="1fd39-306">Resizes an element on the screen.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-307"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_rotate"><strong>TransformPattern_Rotate</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-307"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_rotate"><strong>TransformPattern_Rotate</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-308">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-308">This function is deprecated.</span></span> <span data-ttu-id="1fd39-309">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-309">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-310">Gira un elemento en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="1fd39-310">Rotates an element on the screen.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-311"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-valuepattern_setvalue"><strong>ValuePattern_SetValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-311"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-valuepattern_setvalue"><strong>ValuePattern_SetValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-312">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-312">This function is deprecated.</span></span> <span data-ttu-id="1fd39-313">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-313">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-314">Establece el valor de texto de un elemento.</span><span class="sxs-lookup"><span data-stu-id="1fd39-314">Sets the text value of an element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-315"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-virtualizeditempattern_realize"><strong>VirtualizedItemPattern_Realize</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-315"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-virtualizeditempattern_realize"><strong>VirtualizedItemPattern_Realize</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-316">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-316">This function is deprecated.</span></span> <span data-ttu-id="1fd39-317">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-317">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-318">Hace que el elemento virtual sea totalmente accesible como elemento de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-318">Makes the virtual item fully accessible as a UI Automation element.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-319"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_close"><strong>WindowPattern_Close</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-319"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_close"><strong>WindowPattern_Close</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-320">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-320">This function is deprecated.</span></span> <span data-ttu-id="1fd39-321">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-321">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-322">Cierra una ventana abierta.</span><span class="sxs-lookup"><span data-stu-id="1fd39-322">Closes an open window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd39-323"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_setwindowvisualstate"><strong>WindowPattern_SetWindowVisualState</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-323"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_setwindowvisualstate"><strong>WindowPattern_SetWindowVisualState</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-324">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-324">This function is deprecated.</span></span> <span data-ttu-id="1fd39-325">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-325">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-326">Establece el estado visual de una ventana; por ejemplo, para maximizar una ventana.</span><span class="sxs-lookup"><span data-stu-id="1fd39-326">Sets the visual state of a window; for example, to maximize a window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd39-327"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_waitforinputidle"><strong>WindowPattern_WaitForInputIdle</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd39-327"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_waitforinputidle"><strong>WindowPattern_WaitForInputIdle</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="1fd39-328">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-328">This function is deprecated.</span></span> <span data-ttu-id="1fd39-329">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1fd39-329">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="1fd39-330">Hace que el código de llamada se bloquee durante el tiempo especificado o hasta que el proceso asociado entre en un estado de inactividad, lo que ocurra primero.</span><span class="sxs-lookup"><span data-stu-id="1fd39-330">Causes the calling code to block for the specified time or until the associated process enters an idle state, whichever completes first.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="1fd39-331">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1fd39-331">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fd39-332">Clientes de UI Automation</span><span class="sxs-lookup"><span data-stu-id="1fd39-332">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





