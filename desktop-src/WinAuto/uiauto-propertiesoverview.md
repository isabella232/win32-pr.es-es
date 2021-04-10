---
title: Información general acerca de las propiedades de UI Automation
description: Los proveedores de automatización de la interfaz de usuario de Microsoft exponen propiedades en elementos de UI Automation Las propiedades permiten a las aplicaciones cliente recuperar información acerca de los controles.
ms.assetid: 35f017cb-f50a-4680-9f01-5079aa59da73
keywords:
- Automatización de la interfaz de usuario, información general sobre propiedades
- Automatización de la interfaz de usuario, propiedades frente a eventos
- Automatización de la interfaz de usuario, eventos frente a propiedades
- propiedades, acerca de
- propiedades, identificadores
- propiedades, valores
- propiedades, eventos
- eventos, propiedades
- propiedades, dinámicas
- propiedades dinámicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f4e5e1b29ae516059a531b17d50d0631282f82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268208"
---
# <a name="ui-automation-properties-overview"></a>Información general acerca de las propiedades de UI Automation

Los proveedores de automatización de la interfaz de usuario de Microsoft exponen propiedades en elementos de UI Automation Las propiedades permiten a las aplicaciones cliente recuperar información acerca de los controles.

La automatización de la interfaz de usuario expone dos tipos diferentes de propiedades: *las propiedades de los elementos de automatización y las propiedades* de los patrones de *control*. Las propiedades del elemento de automatización se componen de un conjunto común de propiedades, como name, AcceleratorKey y ClassName, que exponen todos los elementos de automatización de la interfaz de usuario, independientemente del tipo de control. La mayoría de las propiedades de elemento de automatización son valores estáticos.

Las propiedades de patrón de control son las que expone un control que admite un patrón de control determinado. Cada patrón de control tiene un conjunto correspondiente de propiedades de patrón de control que debe exponer el control. Por ejemplo, un control que admite el patrón de control [Grid](uiauto-implementinggrid.md) expone las propiedades ColumnCount y RowCount. La mayoría de las propiedades de patrón de control son valores dinámicos.

En este tema se incluyen las siguientes secciones.

-   [Identificadores de propiedad](#property-identifiers)
-   [Valores de propiedad](#property-values)
-   [Propiedades y eventos](#properties-and-events)
-   [Temas relacionados](#related-topics)

## <a name="property-identifiers"></a>Identificadores de propiedad

Cada propiedad se identifica mediante un valor numérico de **PROPERTYID** denominado *identificador de propiedad* (ID). Los proveedores y los clientes usan los identificadores numéricos en llamadas a métodos como [**IRawElementProviderAdviseEvents:: AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) y [**IUIAutomationElement:: GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue) para identificar las solicitudes de propiedad. Para obtener una descripción detallada de cada identificador de propiedad de automatización de la interfaz de usuario, incluido el tipo de datos y el valor predeterminado de cada propiedad, vea [identificadores de propiedad](uiauto-entry-propids.md).

## <a name="property-values"></a>Valores de propiedad

Todas las propiedades son de solo lectura, aunque algunas se pueden cambiar mediante métodos que actúan sobre el control, como [**IDockProvider:: SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) (Provider) o [**IUIAutomationDockPattern:: SetDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition) (Client).

Para obtener información sobre cómo recuperar los valores de propiedad, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).

## <a name="properties-and-events"></a>Propiedades y eventos

Estrechamente asociados a las propiedades de la automatización de la interfaz de usuario es el concepto de *eventos de cambio de propiedad*. En el caso de las propiedades dinámicas, una aplicación cliente necesita una manera de saber que un valor de propiedad ha cambiado, de modo que puede actualizar su caché de información o reaccionar a la nueva información de alguna otra manera. Los clientes se pueden registrar para escuchar eventos de cambio de propiedad en cualquier propiedad.

Los proveedores generan eventos cuando cambia algo en la interfaz de usuario. Por ejemplo, si una casilla está activada o desactivada, la implementación del proveedor del patrón de control [Toggle](uiauto-implementingtoggle.md) genera un evento de cambio de propiedad. Los proveedores pueden generar eventos de forma selectiva, dependiendo de si hay clientes en escucha de eventos o en escucha de eventos específicos.

No todos los cambios de propiedades generan eventos; esto depende totalmente de la implementación del proveedor de Automatización de la interfaz de usuario del elemento. Por ejemplo, los proveedores de proxy estándar para los cuadros de lista no generan un evento de cambio de propiedad cuando cambia la propiedad de selección. En este caso, la aplicación debe escuchar el evento que se genera cuando cambia la selección ([**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)).

Los clientes escuchan eventos mediante su suscripción, como se describe en [suscribirse a eventos de automatización de la interfaz de usuario](uiauto-eventsforclients.md). En el caso de los eventos de cambio de propiedad en concreto, los clientes deben implementar [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) y pasar la interfaz a [**IUIAutomation:: AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) o [**IUIAutomation:: AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
</dt> <dt>

[**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
</dt> <dt>

[**GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
</dt> <dt>

[**GetCachedPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)
</dt> <dt>

**Vista**
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre eventos de UI Automation](uiauto-eventsoverview.md)
</dt> </dl>

 

 




