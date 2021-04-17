---
title: ToolBar (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control ToolBar. Los controles de barra de herramientas permiten a los usuarios finales activar comandos y herramientas incluidos en una aplicación.
ms.assetid: e2a72ce3-5263-43f8-be4d-715a78224b68
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control ToolBar
- UI Automation, ToolBar (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control ToolBar
- Automatización de la interfaz de usuario, propiedades para el tipo de control ToolBar
- Automatización de la interfaz de usuario, patrones de control para el tipo de control ToolBar
- Automatización de la interfaz de usuario, eventos para el tipo de control ToolBar
- estructuras de árbol, ToolBar (tipo de control)
- Properties, ToolBar (tipo de control)
- patrones de control, ToolBar (tipo de control)
- Events, ToolBar (tipo de control)
- compatibilidad con el tipo de control ToolBar
- ToolBar (tipo de control)
- tipos de control, estructura de árbol para el tipo de control ToolBar
- tipos de control, patrones de control para el tipo de control ToolBar
- tipos de control, compatibilidad con la barra de herramientas
- tipos de controles, barra de herramientas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4327c187a86ace6f02b93082675c345eae4d4edf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419081"
---
# <a name="toolbar-control-type"></a>ToolBar (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Toolbar** . Los controles de barra de herramientas permiten a los usuarios finales activar comandos y herramientas incluidos en una aplicación.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **Toolbar** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de barra de herramientas donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y patrones

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de barra de herramientas y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>ToolBar
<ul>
<li>Varios controles (0 o más)</li>
</ul></li>
</ul></td>
<td><ul>
<li>ToolBar
<ul>
<li>Varios controles (0 o más)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Un control de barra de herramientas puede contener cualquier tipo de control dentro de su subárbol. Más a menudo contienen botones, cuadros combinados y botones de expansión.

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para el tipo de control **Toolbar** . Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value       | Notas                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas.  | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                                                                               |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.  | El rectángulo exterior que contiene el control completo.                                                                                                                                                   |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.  | Se admite si hay un rectángulo delimitador. Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable.       |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Barra** | Este valor es el mismo para todos los marcos de trabajo de la interfaz de usuario.                                                                                                                                                              |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | El control de barra de herramientas siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | El control de barra de herramientas siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.                                                                                                                      |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas.  | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                  |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL        | Un control de barra de herramientas nunca tiene una etiqueta.                                                                                                                                                                       |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.  | Cadena localizada que corresponde al tipo de control **Toolbar** . El valor predeterminado es "barra de herramientas" para en-US o inglés (Estados Unidos).                                                                      |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Depende     | El control de barra de herramientas no necesita un nombre a menos que se use más de uno dentro de una aplicación. Si hay más de uno, cada uno debe tener un nombre distintivo (por ejemplo, "formato" o "esquematización"). |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los patrones de control de automatización de la interfaz de usuario que deben admitir los controles de barra de herramientas. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                                   | Soporte técnico | Notas                                                                                                                                                         |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | Depende | Si la barra de herramientas se puede acoplar a diferentes partes de la pantalla, debe admitir el patrón de control [Dock](uiauto-implementingdock.md) .                       |
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depende | Si la barra de herramientas se puede expandir y contraer para mostrar más elementos, debe admitir el patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) . |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | Depende | Si la barra de herramientas puede cambiar de tamaño, girarse o moverse, debe admitir el patrón de control [Transform](uiauto-implementingtransform.md) .                          |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de barra de herramientas deben admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                                                | Notas                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.                              |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ExpandCollapseExpandCollapseStatePropertyId. | Si el control admite el patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) , debe admitir este evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                                              | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.         |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.                                          | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento.       |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




