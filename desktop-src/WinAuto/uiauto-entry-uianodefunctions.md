---
title: Funciones de nodo en desuso
description: Funciones de nodo en desuso
ms.assetid: 72833757-a356-4727-8fc8-77a60e26aa99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7273ffd6c704c9db6408165d1eba3a293f3d1cf
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103995700"
---
# <a name="deprecated-node-functions"></a><span data-ttu-id="17624-103">Funciones de nodo en desuso</span><span class="sxs-lookup"><span data-stu-id="17624-103">Deprecated Node Functions</span></span>

> [!Note]  
> <span data-ttu-id="17624-104">Las funciones de patrón de control descritas en esta sección están desusadas.</span><span class="sxs-lookup"><span data-stu-id="17624-104">The control pattern functions described in this section are deprecated.</span></span> <span data-ttu-id="17624-105">Las aplicaciones cliente deben usar las interfaces del modelo de objetos componentes (COM) que se describen en las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="17624-105">Client applications should use the Component Object Model (COM) interfaces described in the following sections:</span></span>
>
> -   [<span data-ttu-id="17624-106">Interfaces de elementos de UI Automation para clientes</span><span class="sxs-lookup"><span data-stu-id="17624-106">UI Automation Element Interfaces for Clients</span></span>](uiauto-entry-uiautoclientinterfaces.md)
> -   [<span data-ttu-id="17624-107">Interfaz de condición de propiedad para clientes</span><span class="sxs-lookup"><span data-stu-id="17624-107">Property Condition Interface for Clients</span></span>](uiauto-client-propconditioninterfaces.md)
> -   [<span data-ttu-id="17624-108">Interfaces de patrón de control para clientes</span><span class="sxs-lookup"><span data-stu-id="17624-108">Control Pattern Interfaces for Clients</span></span>](uiauto-client-controlpatterninterfaces.md)
> -   [<span data-ttu-id="17624-109">Interfaces de control de eventos para clientes</span><span class="sxs-lookup"><span data-stu-id="17624-109">Event Handling Interfaces for Clients</span></span>](uiauto-client-eventhandlinginterfaces.md)
> -   [<span data-ttu-id="17624-110">Interfaces de generador de proxy para clientes</span><span class="sxs-lookup"><span data-stu-id="17624-110">Proxy Factory Interfaces for Clients</span></span>](uiauto-client-proxyfactoryinterfaces.md)

 

## <a name="in-this-section"></a><span data-ttu-id="17624-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="17624-111">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="17624-112">Función</span><span class="sxs-lookup"><span data-stu-id="17624-112">Function</span></span></th>
<th><span data-ttu-id="17624-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="17624-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="17624-114"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaaddevent"><strong>UiaAddEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-114"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaaddevent"><strong>UiaAddEvent</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-115">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-115">This function is deprecated.</span></span> <span data-ttu-id="17624-116">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="17624-116">Client applications should use the Microsoft UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-117">Agrega un agente de escucha para los eventos de un nodo en el árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-117">Adds a listener for events on a node in the UI Automation tree.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17624-118"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventaddwindow"><strong>UiaEventAddWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-118"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventaddwindow"><strong>UiaEventAddWindow</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-119">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-119">This function is deprecated.</span></span> <span data-ttu-id="17624-120">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-120">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-121">Agrega una ventana al agente de escucha de eventos.</span><span class="sxs-lookup"><span data-stu-id="17624-121">Adds a window to the event listener.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17624-122"><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaeventcallback"><em>UiaEventCallback</em></a></span><span class="sxs-lookup"><span data-stu-id="17624-122"><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaeventcallback"><em>UiaEventCallback</em></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-123">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-123">This function is deprecated.</span></span> <span data-ttu-id="17624-124">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-124">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-125">Función implementada por el cliente a la que llama la automatización de la interfaz de usuario cuando se produce un evento al que se ha suscrito el cliente.</span><span class="sxs-lookup"><span data-stu-id="17624-125">A client-implemented function that is called by UI Automation when an event is raised that the client has subscribed to.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17624-126"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventremovewindow"><strong>UiaEventRemoveWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-126"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventremovewindow"><strong>UiaEventRemoveWindow</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-127">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-127">This function is deprecated.</span></span> <span data-ttu-id="17624-128">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-128">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-129">Quita una ventana del agente de escucha de eventos.</span><span class="sxs-lookup"><span data-stu-id="17624-129">Removes a window from the event listener.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17624-130"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiafind"><strong>UiaFind</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-130"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiafind"><strong>UiaFind</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-131">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-131">This function is deprecated.</span></span> <span data-ttu-id="17624-132">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-132">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-133">Recupera uno o varios nodos de automatización de la interfaz de usuario que coinciden con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="17624-133">Retrieves one or more UI Automation nodes that match the search criteria.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17624-134"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiageterrordescription"><strong>UiaGetErrorDescription</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-134"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiageterrordescription"><strong>UiaGetErrorDescription</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-135">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-135">This function is deprecated.</span></span> <span data-ttu-id="17624-136">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-136">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-137">Obtiene una cadena de error para que se pueda pasar al cliente.</span><span class="sxs-lookup"><span data-stu-id="17624-137">Gets an error string so that it can be passed to the client.</span></span> <span data-ttu-id="17624-138">Los clientes no utilizan este método directamente.</span><span class="sxs-lookup"><span data-stu-id="17624-138">This method is not used directly by clients.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17624-139"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpatternprovider"><strong>UiaGetPatternProvider</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-139"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpatternprovider"><strong>UiaGetPatternProvider</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-140">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-140">This function is deprecated.</span></span> <span data-ttu-id="17624-141">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-141">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-142">Recupera un <em>patrón de control</em>.</span><span class="sxs-lookup"><span data-stu-id="17624-142">Retrieves a <em>control pattern</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17624-143"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpropertyvalue"><strong>UiaGetPropertyValue</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-143"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpropertyvalue"><strong>UiaGetPropertyValue</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-144">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-144">This function is deprecated.</span></span> <span data-ttu-id="17624-145">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-145">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-146">Recupera el valor de una propiedad de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-146">Retrieves the value of a UI Automation property.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17624-147"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetrootnode"><strong>UiaGetRootNode</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-147"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetrootnode"><strong>UiaGetRootNode</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-148">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-148">This function is deprecated.</span></span> <span data-ttu-id="17624-149">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-149">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-150">Recupera el nodo de automatización de la interfaz de usuario raíz.</span><span class="sxs-lookup"><span data-stu-id="17624-150">Retrieves the root UI Automation node.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17624-151"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetruntimeid"><strong>UiaGetRuntimeId</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-151"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetruntimeid"><strong>UiaGetRuntimeId</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-152">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-152">This function is deprecated.</span></span> <span data-ttu-id="17624-153">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-153">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-154">Recupera el identificador en tiempo de ejecución de un nodo de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-154">Retrieves the runtime identifier of a UI Automation node.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17624-155"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetupdatedcache"><strong>UiaGetUpdatedCache</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-155"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetupdatedcache"><strong>UiaGetUpdatedCache</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-156">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-156">This function is deprecated.</span></span> <span data-ttu-id="17624-157">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-157">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-158">Actualiza la memoria caché de los valores de propiedad y los patrones de control.</span><span class="sxs-lookup"><span data-stu-id="17624-158">Updates the cache of property values and control patterns.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17624-159"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahpatternobjectfromvariant"><strong>UiaHPatternObjectFromVariant</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-159"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahpatternobjectfromvariant"><strong>UiaHPatternObjectFromVariant</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-160">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-160">This function is deprecated.</span></span> <span data-ttu-id="17624-161">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-161">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-162">Obtiene un objeto de patrón de control de un tipo <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="17624-162">Gets a control pattern object from a <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT</strong></a> type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17624-163"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahtextrangefromvariant"><strong>UiaHTextRangeFromVariant</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-163"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahtextrangefromvariant"><strong>UiaHTextRangeFromVariant</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-164">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-164">This function is deprecated.</span></span> <span data-ttu-id="17624-165">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-165">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-166">Obtiene un intervalo de texto a partir de un tipo <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="17624-166">Gets a text range from a <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT</strong></a> type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17624-167"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahuianodefromvariant"><strong>UiaHUiaNodeFromVariant</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-167"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahuianodefromvariant"><strong>UiaHUiaNodeFromVariant</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-168">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-168">This function is deprecated.</span></span> <span data-ttu-id="17624-169">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-169">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-170">Obtiene un HUIANODE de un tipo <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="17624-170">Gets an HUIANODE from a <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT</strong></a> type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17624-171"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid"><strong>UiaLookupId</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-171"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid"><strong>UiaLookupId</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-172">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-172">This function is deprecated.</span></span> <span data-ttu-id="17624-173">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-173">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-174">Obtiene el identificador entero que se puede utilizar en métodos que requieren PROPERTYID, PATTERNID, CONTROLTYPEID, TEXTATTRIBUTEID o EVENTID.</span><span class="sxs-lookup"><span data-stu-id="17624-174">Gets the integer identifier that can be used in methods that require a PROPERTYID, PATTERNID, CONTROLTYPEID, TEXTATTRIBUTEID, or EVENTID.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17624-175"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianavigate"><strong>UiaNavigate</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-175"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianavigate"><strong>UiaNavigate</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-176">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-176">This function is deprecated.</span></span> <span data-ttu-id="17624-177">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-177">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-178">Navega en el árbol de automatización de la interfaz de usuario, recuperando opcionalmente la información almacenada en caché.</span><span class="sxs-lookup"><span data-stu-id="17624-178">Navigates in the UI Automation tree, optionally retrieving cached information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17624-179"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromfocus"><strong>UiaNodeFromFocus</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-179"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromfocus"><strong>UiaNodeFromFocus</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-180">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-180">This function is deprecated.</span></span> <span data-ttu-id="17624-181">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-181">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-182">Recupera el nodo de automatización de la interfaz de usuario para el elemento de la interfaz de usuario que actualmente tiene el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="17624-182">Retrieves the UI Automation node for the UI element that currently has input focus.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17624-183"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromhandle"><strong>UiaNodeFromHandle</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-183"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromhandle"><strong>UiaNodeFromHandle</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-184">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-184">This function is deprecated.</span></span> <span data-ttu-id="17624-185">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-185">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-186">Recupera el nodo de automatización de la interfaz de usuario asociado a una ventana.</span><span class="sxs-lookup"><span data-stu-id="17624-186">Retrieves the UI Automation node associated with a window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17624-187"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefrompoint"><strong>UiaNodeFromPoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-187"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefrompoint"><strong>UiaNodeFromPoint</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-188">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-188">This function is deprecated.</span></span> <span data-ttu-id="17624-189">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-189">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-190">Recupera el nodo de automatización de la interfaz de usuario para el elemento en el punto especificado.</span><span class="sxs-lookup"><span data-stu-id="17624-190">Retrieves the UI Automation node for the element at the specified point.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17624-191"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromprovider"><strong>UiaNodeFromProvider</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-191"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromprovider"><strong>UiaNodeFromProvider</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-192">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-192">This function is deprecated.</span></span> <span data-ttu-id="17624-193">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-193">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-194">Recupera el nodo de automatización de la interfaz de usuario para un proveedor de elementos sin formato.</span><span class="sxs-lookup"><span data-stu-id="17624-194">Retrieves the UI Automation node for a raw element provider.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17624-195"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianoderelease"><strong>UiaNodeRelease</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-195"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianoderelease"><strong>UiaNodeRelease</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-196">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-196">This function is deprecated.</span></span> <span data-ttu-id="17624-197">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-197">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-198">Elimina un nodo de la memoria.</span><span class="sxs-lookup"><span data-stu-id="17624-198">Deletes a node from memory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17624-199"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiapatternrelease"><strong>UiaPatternRelease</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-199"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiapatternrelease"><strong>UiaPatternRelease</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-200">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-200">This function is deprecated.</span></span> <span data-ttu-id="17624-201">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-201">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-202">Elimina un objeto de patrón asignado de la memoria.</span><span class="sxs-lookup"><span data-stu-id="17624-202">Deletes an allocated pattern object from memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17624-203"><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaprovidercallback"><em>UiaProviderCallback</em></a></span><span class="sxs-lookup"><span data-stu-id="17624-203"><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaprovidercallback"><em>UiaProviderCallback</em></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-204">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-204">This function is deprecated.</span></span> <span data-ttu-id="17624-205">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-205">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-206">Una función definida por la aplicación a la que llama la automatización de la interfaz de usuario para obtener un proveedor del lado cliente para un elemento.</span><span class="sxs-lookup"><span data-stu-id="17624-206">An application-defined function that is called by UI Automation to obtain a client-side provider for an element.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17624-207"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectisempty"><strong>UiaRectIsEmpty</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-207"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectisempty"><strong>UiaRectIsEmpty</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-208">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-208">This function is deprecated.</span></span> <span data-ttu-id="17624-209">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-209">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-210">Obtiene un valor booleano que especifica si un rectángulo tiene todas sus coordenadas establecidas en 0.</span><span class="sxs-lookup"><span data-stu-id="17624-210">Gets a Boolean value that specifies whether a rectangle has all its coordinates set to 0.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17624-211"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectsetempty"><strong>UiaRectSetEmpty</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-211"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectsetempty"><strong>UiaRectSetEmpty</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-212">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-212">This function is deprecated.</span></span> <span data-ttu-id="17624-213">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-213">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-214">Establece los elementos de una estructura <a href="/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect"><strong>UiaRect</strong></a> en 0.</span><span class="sxs-lookup"><span data-stu-id="17624-214">Sets the elements of a <a href="/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect"><strong>UiaRect</strong></a> structure to 0.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17624-215"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaregisterprovidercallback"><strong>UiaRegisterProviderCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-215"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaregisterprovidercallback"><strong>UiaRegisterProviderCallback</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-216">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-216">This function is deprecated.</span></span> <span data-ttu-id="17624-217">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-217">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-218">Registra el método definido por la aplicación al que llama la automatización de la interfaz de usuario para obtener un proveedor para un elemento.</span><span class="sxs-lookup"><span data-stu-id="17624-218">Registers the application-defined method that is called by UI Automation to obtain a provider for an element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17624-219"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaremoveevent"><strong>UiaRemoveEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-219"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaremoveevent"><strong>UiaRemoveEvent</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-220">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-220">This function is deprecated.</span></span> <span data-ttu-id="17624-221">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-221">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-222">Quita un agente de escucha de los eventos de un nodo en el árbol de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-222">Removes a listener for events on a node in the UI Automation tree.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17624-223"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiasetfocus"><strong>UiaSetFocus</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-223"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiasetfocus"><strong>UiaSetFocus</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-224">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-224">This function is deprecated.</span></span> <span data-ttu-id="17624-225">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-225">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-226">Establece el foco de entrada en el elemento especificado en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-226">Sets the input focus to the specified element in the UI.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17624-227"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiatextrangerelease"><strong>UiaTextRangeRelease</strong></a></span><span class="sxs-lookup"><span data-stu-id="17624-227"><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiatextrangerelease"><strong>UiaTextRangeRelease</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="17624-228">Esta función es desusada.</span><span class="sxs-lookup"><span data-stu-id="17624-228">This function is deprecated.</span></span> <span data-ttu-id="17624-229">En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="17624-229">Client applications should use the UI Automation COM interfaces instead.</span></span>
</blockquote>
<br/> <span data-ttu-id="17624-230">Elimina un objeto de intervalo de texto asignado de la memoria.</span><span class="sxs-lookup"><span data-stu-id="17624-230">Deletes an allocated text range object from memory.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="17624-231">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="17624-231">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17624-232">Clientes de UI Automation</span><span class="sxs-lookup"><span data-stu-id="17624-232">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

