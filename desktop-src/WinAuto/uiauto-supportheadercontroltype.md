---
title: Header (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control header.
ms.assetid: 032fc3a1-f939-40db-abbb-532afe309ba3
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control header
- Automatización de la interfaz de usuario, tipo de control header
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control header
- Automatización de la interfaz de usuario, propiedades para el tipo de control header
- Automatización de la interfaz de usuario, patrones de control para el tipo de control header
- Automatización de la interfaz de usuario, eventos para el tipo de control header
- estructuras de árbol, tipo de control header
- Properties, header (tipo de control)
- patrones de control, tipo de control header
- Events, header (tipo de control)
- compatibilidad con el tipo de control header
- Header (tipo de control)
- tipos de control, estructura de árbol para el tipo de control header
- tipos de control, patrones de control para el tipo de control header
- tipos de control, compatibilidad con el encabezado
- tipos de control, encabezado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38ee0a00749888c624b627db247f2d01d24ff1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418637"
---
# <a name="header-control-type"></a>Header (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Header** .

El control de encabezado proporciona un contenedor visual para las etiquetas de filas o columnas de información.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **Header** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de encabezado donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y patrones de control

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de encabezado y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Vista de control</th>
<th>Vista de contenido</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Encabezado
<ul>
<li>HeaderItem (1 o más)</li>
</ul></li>
</ul></td>
<td>(No aplicable)</td>
</tr>
</tbody>
</table>



 

Los controles de encabezado siempre tienen uno o más elementos secundarios en la vista de control del árbol de automatización de la interfaz de usuario.

Los controles de encabezado tienen cero elementos secundarios en la vista de contenido del árbol de automatización de la interfaz de usuario.

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles de encabezado. Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value                                                            | Notas                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas.                                                       | El valor de esta propiedad debe ser único en todos los controles de una aplicación.                                                                                                                     |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.                                                       | El rectángulo exterior que contiene el control completo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.                                                       | Se admite si hay un rectángulo delimitador. Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Header**                                                       |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | false                                                            | El control de encabezado no se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.                                                                                                                    |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE                                                             | El control de encabezado siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.                                                                                                                 |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas.                                                       | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL                                                             | Los controles de encabezado no tienen una etiqueta estática.                                                                                                                                                          |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.                                                       | El valor predeterminado es "header" para en-US o inglés (Estados Unidos).                                                                                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.                                                       | El control de encabezado necesita un nombre si hay más de un encabezado de fila o más de un encabezado de columna. Esto identifica la información dentro del encabezado.                                              |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | **OrientationType \_ Horizontal** o **OrientationType \_ vertical** | El valor de esta propiedad expone la posición del control de encabezado, ya sea un encabezado de fila (**OrientationType \_ horizontal**) o un encabezado de columna (**OrientationType \_ vertical**).                 |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los patrones de control de automatización de la interfaz de usuario que se deben admitir para los controles de encabezado. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                         | Soporte técnico | Notas                                                                                                             |
|---------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------|
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Depende | Implemente el patrón de control [Transform](uiauto-implementingtransform.md) si se puede cambiar el tamaño del control de encabezado. |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que deben admitir los controles de encabezado. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                 | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.             | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




