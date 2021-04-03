---
title: Document (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control Document.
ms.assetid: 62565f16-f0d6-42ff-bc36-897a2618c867
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Document
- Automatización de la interfaz de usuario, tipo de control Document
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control Document
- Automatización de la interfaz de usuario, propiedades para el tipo de control Document
- Automatización de la interfaz de usuario, patrones de control para el tipo de control Document
- Automatización de la interfaz de usuario, eventos para el tipo de control Document
- estructuras de árbol, tipo de control Document
- propiedades, tipo de control Document
- patrones de control, tipo de control Document
- Events, Document (tipo de control)
- compatibilidad con el tipo de control Document
- Document (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Document
- tipos de control, patrones de control para el tipo de control Document
- tipos de control, compatibilidad con documentos
- tipos de control, documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ca481df812e3321da7bb4bbb39bdcb5628fb98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075616"
---
# <a name="document-control-type"></a>Document (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Document** .

Los controles de documento permiten a un usuario ver y manipular varias páginas de texto. A diferencia de los controles de edición que solo admiten una línea simple de texto sin formato, los controles de documento pueden hospedar texto con estilo y formato enriquecidos.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **Document** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de documento donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y patrones de control

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de documento y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Documento
<ul>
<li>Varía</li>
</ul></li>
</ul></td>
<td><ul>
<li>Documento
<ul>
<li>Varía</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles de documento. Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value        | Notas                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas.   | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                      |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.   | El rectángulo exterior que contiene el control completo.                                                                                          |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.   | El documento tiene un punto en el que se puede hacer clic que provocará que el foco pase al documento de uno de sus elementos del contenedor de documento.                   |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Documento** |                                                                                                                                                   |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | El control de documento siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.                                                            |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | El control de documento siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.                                                            |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas.   | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                         |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas.   | El valor de esta propiedad debe ser la etiqueta del control de documento. Normalmente, se utiliza el título del documento.                             |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.   | Cadena localizada que corresponde al tipo de control **Document** . El valor predeterminado es "Document" para en-US o inglés (Estados Unidos).            |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.   | Normalmente, el control de documento recibe su nombre del nombre del archivo desde el que se carga. A menudo, esto se muestra en el título de un marco o una ventana contenedora. |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los patrones de control de automatización de la interfaz de usuario que deben admitir los controles de documento. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                  | Soporte técnico/valor | Notas                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) | Depende       | El control de documento puede abarcar más de lo que puede la ventanilla. El control debe admitir el patrón de control [Scroll](uiauto-implementingscroll.md) si el contenido es desplazable.                                                                                                                              |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | Obligatorio      | Todos los controles de documento deben admitir el patrón de control [Text](uiauto-implementingtextandtextrange.md) .                                                                                                                                                                                                                |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | Depende       | Aunque los clientes de automatización de la interfaz de usuario pueden usar [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) para obtener información de texto sobre un documento, necesitan el patrón de control [Value](uiauto-implementingvalue.md) para establecer el valor interno. La entrada de texto simple solo es posible a través del patrón de control Value. |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de documento deben admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                                        | Notas                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                                      | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.                                  | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontallyScrollablePropertyId.   | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontalScrollPercentPropertyId. | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollHorizontalViewSizePropertyId.           | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticallyScrollablePropertyId.       | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticalScrollPercentPropertyId.     | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ScrollVerticalViewSizePropertyId.               | Si el control admite el patrón de control [Scroll](uiauto-implementingscroll.md) , debe admitir este evento.           |
| [**\_InvalidatedEventId de selección de UIA \_**](uiauto-event-ids.md)                                                            | Si el control admite el patrón de control [Selection](uiauto-implementingselection.md) , debe admitir este evento.     |
| [**\_TextSelectionChangedEventId de texto de UIA \_**](uiauto-event-ids.md)                                                    |                                                                                                                            |
| [**\_TextChangedEventId de texto de UIA \_**](uiauto-event-ids.md)                                                                      |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ValueValuePropertyId.                                       | Si el control admite el patrón de control [Value](uiauto-implementingvalue.md) , debe admitir este evento.             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




