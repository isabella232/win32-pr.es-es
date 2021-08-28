---
title: Funciones de nodo en desuso
description: Funciones de nodo en desuso
ms.assetid: 72833757-a356-4727-8fc8-77a60e26aa99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d700c506ee0bb0baf41cdd2facb85b0e7153d57
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476171"
---
# <a name="deprecated-node-functions"></a>Funciones de nodo en desuso

> [!Note]  
> Las funciones de patrón de control descritas en esta sección están en desuso. Las aplicaciones cliente deben usar las interfaces del Modelo de objetos componentes (COM) descritas en las secciones siguientes:
>
> -   [Automatización de la interfaz de usuario interfaces de elemento para clientes](uiauto-entry-uiautoclientinterfaces.md)
> -   [Interfaz de condición de propiedad para clientes](uiauto-client-propconditioninterfaces.md)
> -   [Interfaces de patrón de control para clientes](uiauto-client-controlpatterninterfaces.md)
> -   [Interfaces de control de eventos para clientes](uiauto-client-eventhandlinginterfaces.md)
> -   [Interfaces de generador de proxy para clientes](uiauto-client-proxyfactoryinterfaces.md)

 

## <a name="in-this-section"></a>En esta sección




| Función | Descripción | 
|----------|-------------|
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaaddevent"><strong>UiaAddEvent</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las interfaces COM Automatización de la interfaz de usuario Microsoft en su lugar.</blockquote><br /> Agrega un agente de escucha para los eventos de un nodo del Automatización de la interfaz de usuario servidor.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventaddwindow"><strong>UiaEventAddWindow</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Agrega una ventana al agente de escucha de eventos.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaeventcallback"><em>UiaEventCallback</em></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Función implementada por el cliente a la que llama Automatización de la interfaz de usuario cuando se genera un evento al que se ha suscrito el cliente.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventremovewindow"><strong>UiaEventRemoveWindow</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Quita una ventana del agente de escucha de eventos.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiafind"><strong>UiaFind</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Recupera uno o varios nodos Automatización de la interfaz de usuario que coinciden con los criterios de búsqueda.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiageterrordescription"><strong>UiaGetErrorDescription</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Obtiene una cadena de error para que se pueda pasar al cliente. Los clientes no usan directamente este método.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpatternprovider"><strong>UiaGetPatternProvider</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Recupera un patrón <em>de control</em>.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpropertyvalue"><strong>UiaGetPropertyValue</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Recupera el valor de una Automatización de la interfaz de usuario propiedad.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetrootnode"><strong>UiaGetRootNode</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Recupera el nodo Automatización de la interfaz de usuario raíz.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetruntimeid"><strong>UiaGetRuntimeId</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Recupera el identificador en tiempo de ejecución de Automatización de la interfaz de usuario nodo.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetupdatedcache"><strong>UiaGetUpdatedCache</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Actualiza la caché de valores de propiedad y patrones de control.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahpatternobjectfromvariant"><strong>UiaHPatternObjectFromVariant</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Obtiene un objeto de patrón de control de un <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>tipo VARIANT.</strong></a><br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahtextrangefromvariant"><strong>UiaHTextRangeFromVariant</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Obtiene un intervalo de texto de <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>un tipo VARIANT.</strong></a><br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahuianodefromvariant"><strong>UiaHUiaNodeFromVariant</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Obtiene un HUIANODE de un <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>tipo VARIANT.</strong></a><br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid"><strong>UiaLookupId</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Obtiene el identificador entero que se puede usar en métodos que requieren PROPERTYID, PATTERNID, CONTROLTYPEID, TEXTATTRIBUTEID o EVENTID.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianavigate"><strong>UiaNavigate</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Navega por el árbol Automatización de la interfaz de usuario, recuperando opcionalmente la información almacenada en caché.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromfocus"><strong>UiaNodeFromFocus</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Recupera el nodo Automatización de la interfaz de usuario para el elemento de interfaz de usuario que actualmente tiene el foco de entrada.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromhandle"><strong>UiaNodeFromHandle</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Recupera el Automatización de la interfaz de usuario asociado a una ventana.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefrompoint"><strong>UiaNodeFromPoint</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Recupera el Automatización de la interfaz de usuario nodo del elemento en el punto especificado.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromprovider"><strong>UiaNodeFromProvider</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Recupera el nodo Automatización de la interfaz de usuario para un proveedor de elementos sin formato.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianoderelease"><strong>UiaNodeRelease</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Elimina un nodo de la memoria.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiapatternrelease"><strong>UiaPatternRelease</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Elimina un objeto de patrón asignado de la memoria.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaprovidercallback"><em>UiaProviderCallback</em></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Función definida por la aplicación a la que llama Automatización de la interfaz de usuario para obtener un proveedor del lado cliente para un elemento .<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectisempty"><strong>UiaRectIsEmpty</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Obtiene un valor booleano que especifica si un rectángulo tiene todas sus coordenadas establecidas en 0.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectsetempty"><strong>UiaRectSetEmpty</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Establece los elementos de una <a href="/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect"><strong>estructura UiaRect</strong></a> en 0.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaregisterprovidercallback"><strong>UiaRegisterProviderCallback</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Registra el método definido por la aplicación al que llama Automatización de la interfaz de usuario obtener un proveedor para un elemento .<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaremoveevent"><strong>UiaRemoveEvent</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Quita un agente de escucha para los eventos de un nodo del Automatización de la interfaz de usuario servidor.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiasetfocus"><strong>UiaSetFocus</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Establece el foco de entrada en el elemento especificado de la interfaz de usuario.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiatextrangerelease"><strong>UiaTextRangeRelease</strong></a><br /> | <blockquote>[!Note]<br />Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.</blockquote><br /> Elimina un objeto de intervalo de texto asignado de la memoria.<br /> | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Automatización de la interfaz de usuario clientes](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

