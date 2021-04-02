---
title: SplitButton (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control SplitButton.
ms.assetid: ca4f8e45-7487-4a8b-9df5-edc2b0e56663
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control SplitButton
- Automatización de la interfaz de usuario, tipo de control SplitButton
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control SplitButton
- Automatización de la interfaz de usuario, propiedades para el tipo de control SplitButton
- Automatización de la interfaz de usuario, patrones de control para el tipo de control SplitButton
- Automatización de la interfaz de usuario, eventos para el tipo de control SplitButton
- estructuras de árbol, tipo de control SplitButton
- propiedades, tipo de control SplitButton
- patrones de control, tipo de control SplitButton
- Events, tipo de control SplitButton
- compatibilidad con el tipo de control SplitButton
- SplitButton (tipo de control)
- tipos de control, estructura de árbol para el tipo de control SplitButton
- tipos de control, patrones de control para el tipo de control SplitButton
- tipos de control, compatibilidad con SplitButton
- tipos de control, SplitButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c56cd6b22838dfa92ba25ce05e74d228f4173ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778234"
---
# <a name="splitbutton-control-type"></a>SplitButton (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **splitButton** .

El control de botón de expansión permite realizar una acción en un control y expandir el control para ver una lista de otras acciones posibles que se pueden realizar.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario necesaria, las propiedades, los patrones de control y los eventos para el tipo de control **splitButton** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de botón de expansión en los que la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Ejemplo de tipo de control SplitButton](#splitbutton-control-type-example)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de botón de expansión y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>SplitButton
<ul>
<li>Image (0 o 1)</li>
<li>Text (0 o 1)</li>
<li>Button (1 o 2)
<ul>
<li>Menu (0 o 1; aparece como elemento secundario de un subbotón que admite el patrón ExpandCollapse)
<ul>
<li>MenuItem (1 o varios)</li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>SplitButton
<ul>
<li>Button (1 o 2)
<ul>
<li>MenuItem (1 o varios)</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para el tipo de control **splitButton** . Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value           | Notas                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas.      | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.      | El rectángulo exterior que contiene el control completo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.      | Se admite si hay un rectángulo delimitador. Si no todos los puntos del rectángulo delimitador son seleccionables, y el elemento realiza pruebas de posicionamiento especializadas, invalide y proporcione un punto seleccionable. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **SplitButton** | Este valor es el mismo para todos los marcos de trabajo de la interfaz de usuario.                                                                                                                                                        |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Vea las notas.      | El texto de ayuda puede indicar el resultado de la activación del botón de división, que normalmente es el mismo tipo de información que se presenta mediante un elemento de información sobre herramientas.                                                   |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE            | El control de botón de división contiene información para el usuario final.                                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE            | El control de botón de división es visible para el usuario final.                                                                                                                                                 |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas.      | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL            | Los controles de botón de expansión no tienen una etiqueta de texto estático.                                                                                                                                               |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.      | Cadena localizada que corresponde al tipo de control **splitButton** . El valor predeterminado es "Split Button" para en-US o inglés (Estados Unidos).                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.      | Texto que se usa para etiquetar el botón de expansión. Siempre que se utiliza una imagen para etiquetar un botón de expansión, se debe proporcionar texto alternativo para la propiedad nombre de botón de expansión.                              |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se muestran los patrones de control de UI Automation que se deben admitir por todos los controles de botón de expansión. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                                   | Soporte técnico  | Notas                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Obligatorio | Dado que los botones de expansión siempre tienen la capacidad de expandir una lista de opciones, deben admitir el patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) .                                                      |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Obligatorio | Dado que los botones de expansión siempre tienen una acción predeterminada asociada con el método [**IInvokeProvider:: Invoke**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) , deben admitir el patrón de control [Invoke](uiauto-implementinginvoke.md) . |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                                                | Notas                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId.                              |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ExpandCollapseExpandCollapseStatePropertyId. |                                                                                                                            |
| [**\_InvokedEventId de invocación de UIA \_**](uiauto-event-ids.md)                                                                                  |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                                              | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.                                          | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                            |



 

## <a name="splitbutton-control-type-example"></a>Ejemplo de tipo de control SplitButton

En la imagen siguiente se muestra un control que implementa el tipo de control **splitButton** .

![captura de pantalla que muestra un ejemplo de un control splitbutton](images/splitbuttonxmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Árbol de UI Automation: vista de control</th>
<th>Árbol de UI Automation: vista de contenido</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>&quot;Nombre &quot; de splitButton (Invoke, ExpandCollapse)
<ul>
<li>Opción de botón &quot; más &quot; (invocar)
<ul>
<li>Menú
<ul>
<li>MenuItem</li>
<li>...</li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>&quot;Nombre &quot; de splitButton (Invoke, ExpandCollapse)
<ul>
<li>Opción de botón &quot; más &quot; (invocar)
<ul>
<li>Menú
<ul>
<li>MenuItem</li>
<li>...</li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




