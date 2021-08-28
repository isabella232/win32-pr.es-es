---
title: Implementación de un proveedor Server-Side Automatización de la interfaz de usuario aplicación
description: En este tema se describe cómo implementar un proveedor de microsoft Automatización de la interfaz de usuario servidor para un control personalizado escrito en C++.
ms.assetid: c3a919b2-8b8c-4dde-ad71-587f3845a9f5
keywords:
- Automatización de la interfaz de usuario implementación del proveedor del lado servidor
- Automatización de la interfaz de usuario,implementación del proveedor
- Automatización de la interfaz de usuario, implementar proveedores del lado servidor
- Automatización de la interfaz de usuario, implementar proveedores
- proveedores del lado servidor, implementar
- proveedores del lado servidor, interfaces
- proveedores del lado servidor, valores de propiedad
- proveedores del lado servidor, eventos
- proveedores del lado servidor, asignación de un nuevo elemento primario
- eventos, proveedores del lado servidor
- interfaces, proveedores del lado servidor
- providers,implementing
- implementar proveedores del lado servidor
- implementar proveedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 583b9a5f91bb8be53a3e8b0e356ce558978b8ea28d5b726b56f52420cd7bff37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413445"
---
# <a name="implement-a-server-side-ui-automation-provider"></a>Implementación de un proveedor Server-Side Automatización de la interfaz de usuario aplicación

En este tema se describe cómo implementar un proveedor de microsoft Automatización de la interfaz de usuario servidor para un control personalizado escrito en C++. Contiene las secciones siguientes:

-   [Interfaces de proveedor](#provider-interfaces)
-   [Funcionalidad necesaria para Automatización de la interfaz de usuario proveedores](#required-functionality-for-ui-automation-providers)
-   [Valores de propiedad](#property-values)
-   [Eventos de proveedores](#events-from-providers)
-   [Navegación del proveedor](#provider-navigation)
-   [Asignación de un nuevo elemento primario](#assigning-a-new-parent)
-   [Cambiar la posición del proveedor](#provider-repositioning)
-   [Desconectar proveedores](#disconnecting-providers)
-   [Temas relacionados](#related-topics)

Para obtener ejemplos de código que muestran cómo implementar proveedores del lado servidor, vea [Temas de ayuda para Automatización de la interfaz de usuario proveedores.](uiauto-howto-topics-for-uiautomation-providers.md)

## <a name="provider-interfaces"></a>Interfaces de proveedor

Las siguientes interfaces del Modelo de objetos componentes (COM) proporcionan funcionalidad para los controles personalizados. Para proporcionar funcionalidad básica, todos Automatización de la interfaz de usuario proveedor deben implementar al menos la [**interfaz IRawElementProviderSimple.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) Las interfaces [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) e [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) son opcionales, pero deben implementarse para los elementos de un control complejo para proporcionar funcionalidad adicional.



| Interfaz                                                                         | Descripción                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)             | Proporciona funcionalidad básica para un control hospedado en una ventana, incluida la compatibilidad con los patrones de control y las propiedades.                                                         |
| [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment)         | Agrega funcionalidad para un elemento de un control complejo, incluida la navegación en el fragmento, la configuración del foco y la devolución del rectángulo delimitador del elemento.             |
| [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) | Agrega funcionalidad para el elemento raíz de un control complejo, incluida la ubicación de un elemento secundario en las coordenadas especificadas y el establecimiento del estado del foco global del control. |



 

> [!Note]  
> En la API Automatización de la interfaz de usuario para código administrado, estas interfaces forman una jerarquía de herencia. Este no es el caso de C++, donde las interfaces son completamente independientes.

 

Las interfaces siguientes proporcionan funcionalidad agregada, pero la implementación es opcional.



| Interfaz                                                                         | Descripción                                                                             |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents) | Habilita al proveedor para realizar un seguimiento de las solicitudes de eventos.                                      |
| [**IRawElementProviderHwndOverride**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderhwndoverride) | Permite cambiar la posición de los elementos basados en ventanas en Automatización de la interfaz de usuario árbol de un fragmento. |



 

## <a name="required-functionality-for-ui-automation-providers"></a>Funcionalidad necesaria para Automatización de la interfaz de usuario proveedores

Para comunicarse con Automatización de la interfaz de usuario, el control debe implementar las áreas principales de funcionalidad que se describen en la tabla siguiente.



| Funcionalidad                                              | Implementación                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Exponga el proveedor a Automatización de la interfaz de usuario.                      | En respuesta a un [**mensaje \_ GETOBJECT**](wm-getobject.md) de WM enviado a la ventana de control, devuelva el objeto que implementa [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple). En el caso de los fragmentos, debe ser el proveedor de las raíces correspondientes.                                           |
| Proporcione valores de propiedad.                                   | Implemente [**IRawElementProviderSimple::GetPropertyValue para**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) proporcionar o invalidar valores.                                                                                                                                                             |
| Permitir que el cliente interactúe con el control.            | Implemente interfaces que admitan cada patrón de control adecuado, como [**IInvokeProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) Devuelve estos proveedores de patrones de control en la implementación [**de IRawElementProviderSimple::GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider). |
| Generar eventos.                                              | [**UiaRaiseAutomationEvent ,**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent)métodos de [**IProxyProviderWinEventSink**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iproxyproviderwineventsink).                                                                                                                                                |
| Habilite la navegación y el foco en un fragmento.              | Implemente [**IRawElementProviderFragment para**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) cada elemento del fragmento. No es necesario para los elementos que no forman parte de un fragmento.                                                                                                                         |
| Habilite el foco y la localización de elementos secundarios en un fragmento. | Implemente [**IRawElementProviderFragmentRoot.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) No es necesario para los elementos que no son raíces de fragmentos.                                                                                                                                                          |



 

## <a name="property-values"></a>Valores de propiedad

Automatización de la interfaz de usuario proveedores de controles personalizados deben admitir determinadas propiedades que pueden usar Automatización de la interfaz de usuario aplicaciones cliente. En el caso de los elementos hospedados en ventanas, Automatización de la interfaz de usuario recuperar algunas propiedades del proveedor de ventanas predeterminado, pero debe obtener otras del proveedor personalizado.

Normalmente, los proveedores de controles basados en ventanas no necesitan proporcionar las siguientes propiedades identificadas por **PROPERTYID**:

-   [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)
-   [**ProcessIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)
-   [**ClassNamePropertyId de UIA \_**](uiauto-automation-element-propids.md)
-   [**UIA \_ HasKeyboardFocusPropertyId**](uiauto-automation-element-propids.md)
-   [**IsEnabledPropertyId de UIA \_**](uiauto-automation-element-propids.md)
-   [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)
-   [**IsPasswordPropertyId de UIA \_**](uiauto-automation-element-propids.md)
-   [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)
-   [**RuntimeIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)

La propiedad RuntimeId de un elemento simple o raíz de fragmento hospedada en una ventana se obtiene de la ventana. Sin embargo, los elementos de fragmento debajo de la raíz, como los elementos de lista de un cuadro de lista, deben proporcionar sus propios identificadores. Para obtener más información, [**vea IRawElementProviderFragment::GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid).

La propiedad IsKeyboardFocusable debe devolverse para los proveedores hospedados en un control Windows Forms. En este caso, es posible que el proveedor de ventana predeterminado no consiga recuperar el valor correcto.

El proveedor de host suele proporcionar la propiedad Name.

## <a name="events-from-providers"></a>Eventos de proveedores

Automatización de la interfaz de usuario proveedores deben generar eventos para notificar a las aplicaciones cliente los cambios en el estado de la interfaz de usuario. Las siguientes funciones se usan para generar eventos.



| Función                                                                                   | Descripción                                                                                                              |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent)                  | Genera varios eventos, incluidos los que desencadenan los patrones de control.                                                   |
| [**UiaRaiseAutomationPropertyChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationpropertychangedevent) | Genera un evento cuando una Automatización de la interfaz de usuario propiedad ha cambiado.                                                               |
| [**UiaRaiseStructureChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisestructurechangedevent)      | Genera un evento cuando la estructura del Automatización de la interfaz de usuario ha cambiado, por ejemplo, quitando o agregando un elemento . |



 

El propósito de un evento es notificar al cliente de algo que tiene lugar en la interfaz de usuario. Los proveedores deben generar un evento independientemente de si el cambio se desencadenó por la entrada del usuario o por una aplicación cliente mediante Automatización de la interfaz de usuario. Por ejemplo, el evento identificado por [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md) debe generarse siempre que se invoque el control, ya sea a través de la entrada directa del usuario o de la aplicación cliente que llama a [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke).

Para optimizar el rendimiento, un proveedor puede generar eventos de forma selectiva o no generarlos en absoluto si no se registra ninguna aplicación cliente para recibirlos. Los siguientes elementos de API se usan para la optimización.



| Elemento API                                                                       | Descripción                                                                                                                                                       |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UiaClientsAreListening**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaclientsarelistening)           | Esta función determina si alguna aplicación cliente se ha suscrito a Automatización de la interfaz de usuario eventos.                                                                 |
| [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents) | La implementación de esta interfaz en una raíz de fragmento permite recomendar al proveedor cuando los clientes registran y anulan el registro de controladores de eventos para eventos en el fragmento. |



 

> [!Note]  
> De forma similar a la implementación del recuento de referencias en la programación COM, es importante que los proveedores de Automatización de la interfaz de usuario traten los [**métodos IRawElementProviderAdviseEvents::AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) y [**AdviseEventRemoved,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventremoved) como los métodos [**IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) y [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) Siempre que se haya llamado a **AdviseEventAdded** más veces que **AdviseEventRemoved** para un evento o propiedad específicos, el proveedor debe seguir generando los eventos correspondientes, ya que algunos clientes siguen escuchando. Como alternativa, Automatización de la interfaz de usuario pueden usar la función [**UiaClientsAreListening**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaclientsarelistening) para determinar si al menos un cliente está escuchando y, si es así, generar todos los eventos adecuados.

 

## <a name="provider-navigation"></a>Navegación del proveedor

Los proveedores de controles simples, como un botón personalizado hospedado en una ventana, no necesitan admitir la navegación en el Automatización de la interfaz de usuario personalizado. El proveedor predeterminado de la ventana host controla la navegación hacia y desde el elemento , que se especifica en la implementación de [**IRawElementProviderSimple::HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider). Sin embargo, cuando se implementa un proveedor para un control personalizado complejo, sí se debe admitir la navegación entre el nodo raíz del fragmento y sus descendientes, y entre los nodos del mismo nivel.

> [!Note]  
> Los elementos de un fragmento distinto de la raíz deben devolver **NULL** de [**HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider), porque no se hospedan directamente en una ventana y ningún proveedor predeterminado puede admitir la navegación hacia y desde ellos.

 

La estructura del fragmento viene determinada por la implementación de [**IRawElementProviderFragment::Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate). Este método devuelve el objeto de proveedor para el elemento en cada dirección posible, desde cada fragmento. Si no hay ningún elemento en esa dirección, el método devuelve **NULL.**

La raíz de fragmento solo permite navegar hacia los elementos secundarios. Por ejemplo, un cuadro de lista devuelve el primer elemento de la lista cuando la dirección es **NavigateDirection \_ FirstChild** y devuelve el último elemento cuando la dirección es **NavigateDirection \_ LastChild.** La raíz del fragmento no admite la navegación a un elemento primario o a elementos del mismo nivel; esto lo controla el proveedor de ventanas host.

Los elementos de un fragmento que no son la raíz deben admitir la navegación hacia el elemento primario, sus elementos secundarios y los elementos del mismo nivel que estos contengan.

## <a name="assigning-a-new-parent"></a>Asignación de un nuevo elemento primario

Las ventanas emergentes son en realidad ventanas de nivel superior y, de forma predeterminada, aparecen en el Automatización de la interfaz de usuario como elementos secundarios del escritorio. No obstante, en muchos casos, las ventanas emergentes son, lógicamente, elementos secundarios de otros controles. Por ejemplo, la lista desplegable de un cuadro combinado es, lógicamente, un elemento secundario de dicho cuadro. De forma similar, una ventana emergente de menú es, lógicamente, un elemento secundario de un menú. Automatización de la interfaz de usuario proporciona compatibilidad para asignar un nuevo elemento primario a una ventana emergente para que parezca ser un elemento secundario del control asociado.

Para asignar un nuevo elemento primario a una ventana emergente:

1.  Cree un proveedor para la ventana emergente. Esto requiere que la clase de la ventana emergente se conozca de antemano.
2.  Implemente todas las propiedades y los patrones de control como de costumbre para ese elemento emergente, como si fuera un control por sí mismo.
3.  Implemente la propiedad [**IRawElementProviderSimple::HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider) para que devuelva el valor obtenido de [**UiaHostProviderFromHwnd**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahostproviderfromhwnd), donde el parámetro es el identificador de ventana de la ventana emergente.
4.  Implemente [**IRawElementProviderFragment::Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) para la ventana emergente y su elemento primario para que la navegación se controle correctamente desde el elemento primario lógico a los elementos secundarios lógicos y entre los elementos secundarios relacionados.

Cuando Automatización de la interfaz de usuario encuentra la ventana emergente, reconoce que la navegación se reemplaza desde el valor predeterminado y omite la ventana emergente cuando se encuentra como un elemento secundario del escritorio. En su lugar, solo se puede acceder al nodo a través del fragmento.

La asignación de un nuevo elemento primario no es adecuada para los casos en los que un control puede hospedar una ventana de cualquier clase. Por ejemplo, un control rebar puede hospedar cualquier tipo de ventana en sus bandas. Para controlar estos casos, Automatización de la interfaz de usuario admite una forma alternativa de reubicación de ventanas, como se describe en la sección siguiente.

## <a name="provider-repositioning"></a>Cambiar la posición del proveedor

Automatización de la interfaz de usuario fragmentos pueden contener dos o más elementos que están incluidos en una ventana. Dado que cada ventana tiene su propio proveedor predeterminado que considera que la ventana es un elemento secundario de una ventana contenedora, el árbol Automatización de la interfaz de usuario mostrará de forma predeterminada las ventanas del fragmento como elementos secundarios de la ventana primaria. En la mayoría de los casos, este es un comportamiento deseable, pero a veces puede provocar confusión porque no coincide con la estructura lógica de la interfaz de usuario.

Un buen ejemplo de esto lo constituye un control rebar. Un control rebar contiene bandas, cada una de las cuales a su vez puede contener un control basado en ventana, como una barra de herramientas, un cuadro de edición o un cuadro combinado. El proveedor de ventanas predeterminado para la ventana de rebar ve las ventanas de control de banda como secundarios y el proveedor de rebar ve las bandas como secundarios. Dado que el proveedor de ventanas y el proveedor de rebar funcionan conjuntamente y combinan sus elementos secundarios, las bandas y los controles basados en ventanas aparecen como elementos secundarios del control rebar. Sin embargo, lógicamente, solo las bandas deben aparecer como elementos secundarios del control rebar y cada proveedor de banda debe estar acoplado al proveedor de ventanas predeterminado para el control que contiene.

Para ello, el proveedor raíz de fragmentos para el control rebar expone un conjunto de secundarios que representan las bandas. Cada banda tiene un único proveedor que puede exponer propiedades y patrones de control. En su implementación de [**IRawElementProviderSimple::HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider), el proveedor de banda devuelve el proveedor de ventana predeterminado para la ventana de control, que obtiene llamando a [**UiaHostProviderFromHwnd**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahostproviderfromhwnd), pasando el identificador de ventana del control **(HWND).** Por último, el proveedor raíz de fragmentos para la barra de rebar implementa la interfaz [**IRawElementProviderHwndOverride**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderhwndoverride) y, en su implementación de [**IRawElementProviderHwndOverride::GetOverrideProviderForHwnd**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderhwndoverride-getoverrideproviderforhwnd), devuelve el proveedor de banda adecuado para el control contenido en la ventana especificada.

## <a name="disconnecting-providers"></a>Desconectar proveedores

Normalmente, las aplicaciones crean controles a medida que son necesarios y los destruyen después. Después de destruir un control, los Automatización de la interfaz de usuario de proveedor asociados al control deben liberarse llamando a [**UiaDisconnectProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectprovider).

De forma similar, una aplicación debe usar la función [**UiaDisconnectAllProviders**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectallproviders) para liberar todos los recursos de Automatización de la interfaz de usuario mantenidos por todos los proveedores de la aplicación antes de cerrarse.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Automatización de la interfaz de usuario del programador del proveedor de servicios](uiauto-providerportal.md)
</dt> </dl>

 

 