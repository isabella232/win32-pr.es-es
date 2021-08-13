---
title: Recuperación de propiedades de Automatización de la interfaz de usuario Elements
description: Las propiedades de los objetos IUIAutomationElement contienen información sobre los elementos de la interfaz de usuario, normalmente controles.
ms.assetid: e358fd67-22d0-4e43-a138-8afcc45f130e
keywords:
- clientes, obtener Automatización de la interfaz de usuario elementos
- clients,Automatización de la interfaz de usuario elements
- clients,properties
- clients,retrieving properties
- clients,Automatización de la interfaz de usuario propiedades
- Automatización de la interfaz de usuario, obtener elementos
- Automatización de la interfaz de usuario,elements
- Automatización de la interfaz de usuario,properties
- Automatización de la interfaz de usuario, recuperar propiedades
- recuperar propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbbe524e6f82f8c7dba018b24895ade54ced3e6a4632e1caefed410753b56fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118564376"
---
# <a name="retrieving-properties-from-ui-automation-elements"></a>Recuperación de propiedades de Automatización de la interfaz de usuario Elements

Las propiedades de [**los objetos IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) contienen información sobre los elementos de la interfaz de usuario, normalmente controles. Las propiedades de un elemento son genéricas; es decir, no es específico de un tipo de control. Las propiedades específicas del control de un elemento se exponen mediante sus interfaces de patrón de control.

Las Automatización de la interfaz de usuario de Microsoft son de solo lectura. Para establecer las propiedades de un control, debe utilizar los métodos del patrón de control adecuado. Por ejemplo, use [**IUIAutomationScrollPattern::Scroll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollpattern-scroll) para cambiar los valores de posición de una ventana de desplazamiento.

Para mejorar el rendimiento, los valores de propiedad de los controles y los patrones de control se pueden almacenar en caché cuando se recuperan los elementos. Para obtener más información, vea [Caching Automatización de la interfaz de usuario Properties and Control Patterns](uiauto-cachingforclients.md).

En este tema se incluyen las siguientes secciones.

-   [Identificadores de propiedad](#property-ids)
-   [Condiciones de propiedad](#property-conditions)
-   [Recuperación de propiedades](#retrieving-properties)
-   [Valores de propiedad predeterminados](#default-property-values)
-   [Temas relacionados](#related-topics)

## <a name="property-ids"></a>Identificadores de propiedad

Los identificadores de propiedad se definen en Uiautomationclient.h. Se usan para especificar propiedades al suscribirse a eventos modificados por propiedades, recuperar valores de propiedad y construir condiciones de propiedad. Los identificadores de propiedad también identifican la propiedad que ha cambiado cuando se llama a [**IUIAutomationPropertyChangedEventHandler::HandlePropertyChangedEvent.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationpropertychangedeventhandler-handlepropertychangedevent)

Para obtener una lista de Automatización de la interfaz de usuario identificadores de propiedad, vea [Identificadores de propiedad](uiauto-entry-propids.md).

## <a name="property-conditions"></a>Condiciones de propiedad

Los ID de propiedad se usan para construir objetos [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition) que se usan para buscar Automatización de la interfaz de usuario elementos. Por ejemplo, es posible que desee buscar un elemento que tenga un nombre determinado o todos los controles habilitados. Cada condición de propiedad especifica un identificador de propiedad y el valor que debe coincidir con la propiedad.

Para más información, consulte los temas de referencia siguientes:

-   [**IUIAutomation::CreatePropertyCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition)
-   [**IUIAutomation::CreatePropertyConditionEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertyconditionex)
-   [**IUIAutomationElement::FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst)
-   [**IUIAutomationElement::FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)

## <a name="retrieving-properties"></a>Recuperación de propiedades

Algunas propiedades genéricas, y todas las propiedades del patrón de control, están disponibles como propiedades en [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) o la interfaz de patrón de control y se pueden recuperar mediante un accessor, como [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) o [**CachedDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-get_cacheddockposition).

Además, cualquier propiedad actual o almacenada en caché (que no sea las propiedades del patrón de control) se puede recuperar mediante uno de los métodos siguientes:

-   [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
-   [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
-   [**GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
-   [**GetCachedPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)

Estos métodos ofrecen un rendimiento ligeramente mejor y acceso a toda la gama de propiedades. Sin embargo, los valores se devuelven [**en estructuras VARIANT,**](/windows/win32/api/oaidl/ns-oaidl-variant) mientras que los accessors de propiedad individuales convierten el valor al tipo adecuado.

## <a name="default-property-values"></a>Valores de propiedad predeterminados

Si un Automatización de la interfaz de usuario no implementa una propiedad, Automatización de la interfaz de usuario puede proporcionar un valor predeterminado. Por ejemplo, si el proveedor de un control no admite la propiedad identificada por [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md), Automatización de la interfaz de usuario devuelve una cadena vacía. De forma similar, si el proveedor no admite la propiedad identificada por [**UIA \_ IsDockPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md), Automatización de la interfaz de usuario **devuelve FALSE**.

La diferencia entre [**IUIAutomationElement::GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) y [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex) (y entre pares similares de métodos) es que el método "Ex" puede especificar que no se va a devolver ningún valor predeterminado. En este caso, el valor devuelto es una constante única especial, que indica que no se admite la propiedad . Al recibir este valor, la aplicación puede proporcionar su propio valor o simplemente omitir la propiedad .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general acerca de las propiedades de UI Automation](uiauto-propertiesoverview.md)
</dt> <dt>

[Identificadores de propiedad](uiauto-entry-propids.md)
</dt> </dl>

 

 