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
# <a name="deprecated-node-functions"></a>Funciones de nodo en desuso

> [!Note]  
> Las funciones de patrón de control descritas en esta sección están desusadas. Las aplicaciones cliente deben usar las interfaces del modelo de objetos componentes (COM) que se describen en las siguientes secciones:
>
> -   [Interfaces de elementos de UI Automation para clientes](uiauto-entry-uiautoclientinterfaces.md)
> -   [Interfaz de condición de propiedad para clientes](uiauto-client-propconditioninterfaces.md)
> -   [Interfaces de patrón de control para clientes](uiauto-client-controlpatterninterfaces.md)
> -   [Interfaces de control de eventos para clientes](uiauto-client-eventhandlinginterfaces.md)
> -   [Interfaces de generador de proxy para clientes](uiauto-client-proxyfactoryinterfaces.md)

 

## <a name="in-this-section"></a>En esta sección



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Función</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaaddevent"><strong>UiaAddEvent</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario de Microsoft.
</blockquote>
<br/> Agrega un agente de escucha para los eventos de un nodo en el árbol de automatización de la interfaz de usuario.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventaddwindow"><strong>UiaEventAddWindow</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Agrega una ventana al agente de escucha de eventos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaeventcallback"><em>UiaEventCallback</em></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Función implementada por el cliente a la que llama la automatización de la interfaz de usuario cuando se produce un evento al que se ha suscrito el cliente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventremovewindow"><strong>UiaEventRemoveWindow</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Quita una ventana del agente de escucha de eventos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiafind"><strong>UiaFind</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Recupera uno o varios nodos de automatización de la interfaz de usuario que coinciden con los criterios de búsqueda.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiageterrordescription"><strong>UiaGetErrorDescription</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Obtiene una cadena de error para que se pueda pasar al cliente. Los clientes no utilizan este método directamente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpatternprovider"><strong>UiaGetPatternProvider</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Recupera un <em>patrón de control</em>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpropertyvalue"><strong>UiaGetPropertyValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Recupera el valor de una propiedad de automatización de la interfaz de usuario.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetrootnode"><strong>UiaGetRootNode</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Recupera el nodo de automatización de la interfaz de usuario raíz.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetruntimeid"><strong>UiaGetRuntimeId</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Recupera el identificador en tiempo de ejecución de un nodo de automatización de la interfaz de usuario.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetupdatedcache"><strong>UiaGetUpdatedCache</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Actualiza la memoria caché de los valores de propiedad y los patrones de control.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahpatternobjectfromvariant"><strong>UiaHPatternObjectFromVariant</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Obtiene un objeto de patrón de control de un tipo <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahtextrangefromvariant"><strong>UiaHTextRangeFromVariant</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Obtiene un intervalo de texto a partir de un tipo <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahuianodefromvariant"><strong>UiaHUiaNodeFromVariant</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Obtiene un HUIANODE de un tipo <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid"><strong>UiaLookupId</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Obtiene el identificador entero que se puede utilizar en métodos que requieren PROPERTYID, PATTERNID, CONTROLTYPEID, TEXTATTRIBUTEID o EVENTID.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianavigate"><strong>UiaNavigate</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Navega en el árbol de automatización de la interfaz de usuario, recuperando opcionalmente la información almacenada en caché.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromfocus"><strong>UiaNodeFromFocus</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Recupera el nodo de automatización de la interfaz de usuario para el elemento de la interfaz de usuario que actualmente tiene el foco de entrada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromhandle"><strong>UiaNodeFromHandle</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Recupera el nodo de automatización de la interfaz de usuario asociado a una ventana.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefrompoint"><strong>UiaNodeFromPoint</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Recupera el nodo de automatización de la interfaz de usuario para el elemento en el punto especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromprovider"><strong>UiaNodeFromProvider</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Recupera el nodo de automatización de la interfaz de usuario para un proveedor de elementos sin formato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianoderelease"><strong>UiaNodeRelease</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Elimina un nodo de la memoria.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiapatternrelease"><strong>UiaPatternRelease</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Elimina un objeto de patrón asignado de la memoria.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaprovidercallback"><em>UiaProviderCallback</em></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Una función definida por la aplicación a la que llama la automatización de la interfaz de usuario para obtener un proveedor del lado cliente para un elemento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectisempty"><strong>UiaRectIsEmpty</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Obtiene un valor booleano que especifica si un rectángulo tiene todas sus coordenadas establecidas en 0.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectsetempty"><strong>UiaRectSetEmpty</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Establece los elementos de una estructura <a href="/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect"><strong>UiaRect</strong></a> en 0.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaregisterprovidercallback"><strong>UiaRegisterProviderCallback</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Registra el método definido por la aplicación al que llama la automatización de la interfaz de usuario para obtener un proveedor para un elemento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaremoveevent"><strong>UiaRemoveEvent</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Quita un agente de escucha de los eventos de un nodo en el árbol de automatización de la interfaz de usuario.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiasetfocus"><strong>UiaSetFocus</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Establece el foco de entrada en el elemento especificado en la interfaz de usuario.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiatextrangerelease"><strong>UiaTextRangeRelease</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario.
</blockquote>
<br/> Elimina un objeto de intervalo de texto asignado de la memoria.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clientes de UI Automation](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

