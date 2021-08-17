---
title: Información general acerca de las propiedades de UI Automation
description: Los proveedores Automatización de la interfaz de usuario Microsoft exponen propiedades en Automatización de la interfaz de usuario elementos. Las propiedades permiten a las aplicaciones cliente recuperar información sobre los controles.
ms.assetid: 35f017cb-f50a-4680-9f01-5079aa59da73
keywords:
- Automatización de la interfaz de usuario,información general sobre propiedades
- Automatización de la interfaz de usuario, propiedades frente a eventos
- Automatización de la interfaz de usuario, eventos frente a propiedades
- properties,about
- properties,identifiers
- properties,values
- properties,events
- events,properties
- properties,dynamic
- propiedades dinámicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58267fae50fe71c320b334c35b8da7831657e00bdd1b222db596addd40f3afef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745035"
---
# <a name="ui-automation-properties-overview"></a>Información general acerca de las propiedades de UI Automation

Los proveedores Automatización de la interfaz de usuario Microsoft exponen propiedades en Automatización de la interfaz de usuario elementos. Las propiedades permiten a las aplicaciones cliente recuperar información sobre los controles.

Automatización de la interfaz de usuario expone dos tipos diferentes de propiedades: propiedades de *elemento de automatización* y el patrón de control se *apropiado.* Las propiedades del elemento de automatización constan de un conjunto común de propiedades, como Name, AcceleratorKey y ClassName, que se exponen por todos los elementos Automatización de la interfaz de usuario, independientemente del tipo de control. La mayoría de las propiedades de elementos de automatización son valores estáticos.

Las propiedades del patrón de control son las que expone un control que admite un patrón de control determinado. Cada patrón de control tiene un conjunto correspondiente de propiedades de patrón de control que el control debe exponer. Por ejemplo, un control que admite el patrón de control [Grid](uiauto-implementinggrid.md) expone las propiedades ColumnCount y RowCount. La mayoría de las propiedades del patrón de control son valores dinámicos.

En este tema se incluyen las siguientes secciones.

-   [Identificadores de propiedad](#property-identifiers)
-   [Valores de propiedad](#property-values)
-   [Propiedades y eventos](#properties-and-events)
-   [Temas relacionados](#related-topics)

## <a name="property-identifiers"></a>Identificadores de propiedad

Cada propiedad se identifica mediante un **valor numérico PROPERTYID** denominado identificador *de propiedad* (ID). Los proveedores y clientes usan los identificadores numéricos en llamadas de método como [**IRawElementProviderAdviseEvents::AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) e [**IUIAutomationElement::GetCachedPropertyValue para**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue) identificar las solicitudes de propiedad. Para obtener una descripción detallada de cada identificador Automatización de la interfaz de usuario propiedad, incluidos el tipo de datos y el valor predeterminado de cada propiedad, vea [Identificadores de propiedad](uiauto-entry-propids.md).

## <a name="property-values"></a>Valores de propiedad

Todas las propiedades son de solo lectura, aunque algunas se pueden cambiar mediante métodos que actúan en el control, como [**IDockProvider::SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) (proveedor) o [**IUIAutomationDockPattern::SetDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition) (cliente).

Para obtener información sobre cómo recuperar valores de propiedad, vea [Recuperar propiedades de Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).

## <a name="properties-and-events"></a>Propiedades y eventos

Estrechamente asociado a las propiedades de Automatización de la interfaz de usuario es el concepto de eventos *de cambio de propiedad.* En el caso de las propiedades dinámicas, una aplicación cliente necesita una manera de saber que un valor de propiedad ha cambiado, para que pueda actualizar su memoria caché de información o reaccionar a la nueva información de alguna otra manera. Los clientes pueden registrarse para escuchar eventos de cambio de propiedad en cualquier propiedad.

Los proveedores genera eventos cuando cambia algo en la interfaz de usuario. Por ejemplo, si se activa o desactiva una casilla, la implementación del proveedor del patrón de control [Alternar](uiauto-implementingtoggle.md) genera un evento de cambio de propiedad. Los proveedores pueden generar eventos de forma selectiva, dependiendo de si hay clientes en escucha de eventos o en escucha de eventos específicos.

No todos los cambios de propiedades generan eventos; esto depende totalmente de la implementación del proveedor de Automatización de la interfaz de usuario del elemento. Por ejemplo, los proveedores de proxy estándar para los cuadros de lista no genera un evento de cambio de propiedad cuando cambia la propiedad Selection. En este caso, la aplicación debe escuchar el evento que se genera cuando cambia la selección ([**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)).

Los clientes escuchan eventos suscribiéndose a ellos, como se describe en Suscripción a [Automatización de la interfaz de usuario Eventos](uiauto-eventsforclients.md). En concreto, para los eventos modificados por propiedades, los clientes deben implementar [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) y pasar la interfaz a [**IUIAutomation::AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) o [**IUIAutomation::AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray).

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

**Conceptual**
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre eventos de UI Automation](uiauto-eventsoverview.md)
</dt> </dl>

 

 




