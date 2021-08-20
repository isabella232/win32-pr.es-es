---
title: Tipo de control De encabezado
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control Header.
ms.assetid: 032fc3a1-f939-40db-abbb-532afe309ba3
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Header
- Automatización de la interfaz de usuario,Tipo de control Header
- Automatización de la interfaz de usuario,tree structure for Header control type
- Automatización de la interfaz de usuario,properties para el tipo de control Header
- Automatización de la interfaz de usuario,patrones de control para el tipo de control Header
- Automatización de la interfaz de usuario,events para el tipo de control Header
- tree structures,Header (tipo de control)
- properties,Header (tipo de control)
- patrones de control, Tipo de control de encabezado
- events,Header (tipo de control)
- Compatibilidad con el tipo de control Header
- Header (tipo de control)
- tipos de control, estructura de árbol para tipo de control Encabezado
- tipos de control, patrones de control para tipo de control Encabezado
- tipos de control, compatibilidad con el encabezado
- tipos de control, Encabezado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472a0d7185fa3c2b2dc1dc7593afd106008890bb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482520"
---
# <a name="header-control-type"></a>Tipo de control De encabezado

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **Header.**

El control de encabezado proporciona un contenedor visual para las etiquetas de filas o columnas de información.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, las propiedades, los patrones de control y los eventos necesarios para el tipo **de** control Header. Los Automatización de la interfaz de usuario se aplican a todos los controles de encabezado en los que el marco o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol Automatización de la interfaz de usuario que pertenece a los controles de encabezado y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol Automatización de la interfaz de usuario, vea [información general Automatización de la interfaz de usuario árbol de árbol.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>Encabezado<ul><li>HeaderItem (1 o más)</li></ul></li></ul> | (No aplicable) | 




 

Los controles de encabezado siempre tienen uno o varios secundarios en la vista de control del Automatización de la interfaz de usuario control.

Los controles de encabezado tienen cero secundarios en la vista de contenido del Automatización de la interfaz de usuario encabezado.

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para los controles de encabezado. Para obtener más información sobre Automatización de la interfaz de usuario, vea [Retrieving Properties from Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Valor                                                            | Notas                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas.                                                       | El valor de esta propiedad debe ser único en todos los controles de una aplicación.                                                                                                                     |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.                                                       | El rectángulo exterior que contiene el control completo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.                                                       | Se admite si hay un rectángulo delimitador. Si no se puede hacer clic en todos los puntos del rectángulo delimitador y el elemento realiza pruebas de acceso especializadas, invalide y proporcione un punto en el que se puede hacer clic. |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **Header**                                                       |                                                                                                                                                                                                      |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | FALSE                                                            | El control de encabezado no se incluye en la vista de contenido del Automatización de la interfaz de usuario encabezado.                                                                                                                    |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE                                                             | El control de encabezado siempre se incluye en la vista de control del Automatización de la interfaz de usuario control.                                                                                                                 |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas.                                                       | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL                                                             | Los controles de encabezado no tienen una etiqueta estática.                                                                                                                                                          |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.                                                       | El valor predeterminado es "header" para en-US o inglés (Estados Unidos).                                                                                                                                  |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.                                                       | El control de encabezado necesita un nombre si hay más de un encabezado de fila o más de un encabezado de columna. Esto identifica la información dentro del encabezado.                                              |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | **OrientationType \_ Horizontal** u **OrientationType \_ Vertical** | El valor de esta propiedad expone la posición del control de encabezado, ya sea un encabezado de fila **(OrientationType \_ Horizontal)** o un encabezado de columna **(OrientationType \_ Vertical).**                 |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control necesarios para ser compatibles con los controles de encabezado. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                         | Soporte técnico | Notas                                                                                                             |
|---------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------|
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Depende | Implemente el [patrón](uiauto-implementingtransform.md) de control Transformar si se puede cambiar el tamaño del control de encabezado. |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran Automatización de la interfaz de usuario eventos que los controles de encabezado son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
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

 

 




