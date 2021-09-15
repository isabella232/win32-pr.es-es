---
title: Tipo de control HeaderItem
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control HeaderItem.
ms.assetid: c70420d6-d9f3-47c8-a09f-35ed170f815f
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control HeaderItem
- Automatización de la interfaz de usuario, tipo de control HeaderItem
- Automatización de la interfaz de usuario,estructura de árbol para el tipo de control HeaderItem
- Automatización de la interfaz de usuario,properties para el tipo de control HeaderItem
- Automatización de la interfaz de usuario,patrones de control para el tipo de control HeaderItem
- Automatización de la interfaz de usuario,events para el tipo de control HeaderItem
- estructuras de árbol, tipo de control HeaderItem
- properties,HeaderItem (tipo de control)
- patrones de control, tipo de control HeaderItem
- events,HeaderItem (tipo de control)
- compatibilidad con el tipo de control HeaderItem
- Tipo de control HeaderItem
- tipos de control, estructura de árbol para el tipo de control HeaderItem
- tipos de control, patrones de control para el tipo de control HeaderItem
- tipos de control, compatibilidad con HeaderItem
- tipos de control, HeaderItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b26dcbc293beee3afec8ba0aa9da1359cbbe4c6b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359237"
---
# <a name="headeritem-control-type"></a>Tipo de control HeaderItem

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **HeaderItem.**

El tipo de control **HeaderItem** proporciona una etiqueta visual para una fila o columna de información.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo de control **HeaderItem.** Los Automatización de la interfaz de usuario se aplican a todos los controles de elementos de encabezado en los que el marco o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control típico y una vista de contenido del árbol Automatización de la interfaz de usuario que pertenece a los controles de elemento de encabezado y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario, vea [información general Automatización de la interfaz de usuario árbol de datos.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>HeaderItem</li></ul> | (No aplicable) | 




 

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para el tipo de control **HeaderItem.** Para obtener más información sobre Automatización de la interfaz de usuario propiedades, vea [Recuperar propiedades de Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value          | Notas                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas.     | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel de la vista sin formato Automatización de la interfaz de usuario árbol.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.     | El rectángulo exterior que contiene el control completo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.     | Se admite si hay un rectángulo delimitador. Si no se puede hacer clic en todos los puntos del rectángulo delimitador y el elemento realiza pruebas de acceso especializadas, invalide y proporcione un punto en el que se puede hacer clic. |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **HeaderItem** | Este valor es el mismo para todos los marcos de trabajo de la interfaz de usuario.                                                                                                                                                        |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | false          | El control de elemento de encabezado no se incluye en la vista de contenido del Automatización de la interfaz de usuario encabezado.                                                                                                               |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | true           | El control de elemento de encabezado siempre se incluye en la vista de control del Automatización de la interfaz de usuario encabezado.                                                                                                            |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas.     | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                            |
| [**ItemStatusPropertyId de UIA \_**](uiauto-automation-element-propids.md)                     | Vea las notas      | Esta propiedad ofrece información para los criterios de ordenación mediante el elemento de encabezado.                                                                                                                               |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL           | Los controles de elemento de encabezado no tienen una etiqueta de texto estático.                                                                                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.     | Cadena localizada correspondiente al tipo de control **HeaderItem.** El valor predeterminado es "elemento de encabezado" para en-US o inglés (Estados Unidos).                                                          |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.     | El control de elemento de encabezado siempre se etiqueta automáticamente.                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con todos los controles de elemento de encabezado. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                         | Soporte técnico | Notas                                                                                                                             |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)       | Depende | Implemente [el patrón de](uiauto-implementinginvoke.md) control Invoke si se puede hacer clic en el control de elemento de encabezado para ordenar los datos. |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Depende | Implemente el [patrón de](uiauto-implementingtransform.md) control Transformar si se puede cambiar el tamaño del control de elemento de encabezado.            |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario eventos que los controles de elemento de encabezado son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**Invoke \_ InvokedEventId de UIA \_**](uiauto-event-ids.md)                                                     | Si el control admite el patrón de control [Invoke,](uiauto-implementinginvoke.md) debe admitir este evento.           |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




