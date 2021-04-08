---
title: Tab (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control Tab.
ms.assetid: 49e3f025-f49b-44b1-90ca-09f40dce8f2a
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Tab
- UI Automation, Tab (tipo de control)
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control Tab
- UI Automation, propiedades para el tipo de control Tab
- Automatización de la interfaz de usuario, patrones de control para el tipo de control Tab
- Automatización de la interfaz de usuario, eventos para el tipo de control Tab
- estructuras de árbol, tipo de control Tab
- Properties, Tab (tipo de control)
- patrones de control, Tab (tipo de control)
- Events, Tab (tipo de control)
- compatibilidad con el tipo de control Tab
- Tab (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Tab
- tipos de control, patrones de control para el tipo de control Tab
- tipos de control, compatibilidad con Tab
- tipos de control, pestaña
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 769a03617830c33fce4a8f64c594010b2120785b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994356"
---
# <a name="tab-control-type"></a>Tab (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Tab** .

Un control de ficha es análogo a los divisores de un bloc de notas o las etiquetas de un archivador. Mediante el uso de un control de ficha, una aplicación puede definir varias páginas para la misma área de un cuadro de diálogo o de una ventana.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **Tab** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de ficha en los que la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con tipos de control y patrones

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de ficha y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Pestaña
<ul>
<li>TabItem (1 o más)</li>
<li>ScrollBar (0 o 1)
<ul>
<li>Button (0 o 2)</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>Pestaña
<ul>
<li>TabItem (1 o más)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Los controles de ficha tienen elementos de automatización de la interfaz de usuario secundarios basados en el tipo de control [TabItem](uiauto-supporttabitemcontroltype.md) . Cuando se agrupan los elementos de ficha (por ejemplo, como en Microsoft Office aplicaciones) el tipo de control **Tab** también puede hospedar los tipos de control **Groups** para los elementos de ficha agrupados, como muestra la siguiente estructura de árbol.



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
<li>Pestaña
<ul>
<li>TabItem (1 o más)</li>
<li>Group (0 o más)
<ul>
<li>TabItem (0 o más)</li>
</ul></li>
<li>ScrollBar (0 o 1)
<ul>
<li>Button (0 o 2)</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>Pestaña
<ul>
<li>TabItem (1 o más)</li>
<li>Group (0 o más)
<ul>
<li>TabItem (0 o más)</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles de ficha. Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value      | Notas                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                                                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | No         | El control de ficha no tiene puntos seleccionables.                                                                                                                                                                                                                                                                                                                               |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Tabulación**    |                                                                                                                                                                                                                                                                                                                                                                               |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | El control de pestaña siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                                                                                                             |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | El control de pestaña siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                                                                                                             |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | TRUE       | El tipo de control Tab debe poder recibir el foco de teclado. Normalmente, un cliente de automatización de la interfaz de usuario llama a [**IUIAutomationElement:: SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) en un control de ficha y uno de sus elementos reenvía el foco del teclado al control de pestaña. Es posible que algunos contenedores de ficha obtengan el foco sin haber establecido el foco en uno de sus elementos. |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas. | Los controles de ficha suelen tener una etiqueta de texto estático que se expone a través de esta propiedad.                                                                                                                                                                                                                                                                                        |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada que corresponde al tipo de control **Tab** . El valor predeterminado es "Tab" para en-US o inglés (Estados Unidos).                                                                                                                                                                                                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | El control de ficha rara vez requiere una propiedad **Name** .                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | Vea las notas. | El control de ficha siempre debe indicar si está colocado horizontal o verticalmente.                                                                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se muestran los patrones de control de UI Automation que se deben admitir por todos los controles de ficha. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                                             | Soporte técnico/valor | Notas                                                                                                                                                                  |
|------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | Obligatorio      | Todos los controles de ficha deben admitir el patrón de control [Selection](uiauto-implementingselection.md) .                                                                       |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | TRUE          | Los controles de ficha siempre requieren que se realice una selección.                                                                                                                  |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | false         | Los controles de ficha siempre son contenedores de selección única.                                                                                                                   |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | Depende       | Se debe admitir el patrón de control [Scroll](uiauto-implementingscroll.md) si el control de pestaña tiene widgets que permiten desplazarse por un conjunto de elementos de ficha. |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que deben admitir los controles de ficha. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                                        | Notas                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                                      | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.                                  | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontallyScrollablePropertyId.   | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontalScrollPercentPropertyId. | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontalViewSizePropertyId.           | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticallyScrollablePropertyId.       | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticalScrollPercentPropertyId.     | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticalViewSizePropertyId.               | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.           |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




