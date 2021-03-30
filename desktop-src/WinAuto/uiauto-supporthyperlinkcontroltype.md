---
title: HYPERLINK (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control HyperLink.
ms.assetid: 6dd16ae6-eff0-4913-8916-5092aec34f1f
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control HyperLink
- Automatización de la interfaz de usuario, tipo de control HyperLink
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control HyperLink
- Automatización de la interfaz de usuario, propiedades para el tipo de control HyperLink
- Automatización de la interfaz de usuario, patrones de control para el tipo de control HyperLink
- Automatización de la interfaz de usuario, eventos para el tipo de control HyperLink
- estructuras de árbol, tipo de control HyperLink
- propiedades, tipo de control HyperLink
- patrones de control, HYPERLINK (tipo de control)
- Events, HYPERLINK (tipo de control)
- compatibilidad con el tipo de control HyperLink
- Hyperlink (tipo de control)
- tipos de control, estructura de árbol para el tipo de control HyperLink
- tipos de control, patrones de control para el tipo de control HyperLink
- tipos de control, compatibilidad con hipervínculo
- tipos de control, hipervínculo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71547f37380aeb029e4f73f8d9b2286b285187ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775847"
---
# <a name="hyperlink-control-type"></a>HYPERLINK (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **HYPERLINK** .

Los controles de hipervínculo crean vínculos que permiten a los usuarios navegar dentro de la misma página o de una página a otra.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **HYPERLINK** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de hipervínculo en los que la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Comentarios:](#remarks)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de hipervínculo y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Hyperlink</li>
</ul></td>
<td><ul>
<li>Hyperlink</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles de hipervínculo. Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value         | Notas                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas.    | El valor de esta propiedad debe ser único en todos los controles de una aplicación.                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.    | El rectángulo exterior que contiene el control completo.                                                                                 |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.    | El punto en el que se puede hacer clic del control de hipervínculo debe ser un punto que inicie el hipervínculo si se hace clic con el puntero del mouse.                     |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Hipervínculo** |                                                                                                                                          |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE          | El control de hipervínculo siempre se incluye en la vista de contenido del árbol de automatización de la interfaz de usuario.                                                  |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE          | El control de hipervínculo siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.                                                  |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas.    | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas.    | Si hay una etiqueta de texto estático, esta propiedad debe exponer una referencia a ese control.                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.    | Cadena localizada que corresponde al tipo de control **HYPERLINK** . El valor predeterminado es "HYPERLINK" para en-US o inglés (Estados Unidos). |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.    | El nombre del control de hipervínculo es el texto que se muestra en la pantalla como subrayado.                                                  |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los patrones de control de UI Automation que los controles de hipervínculo deben admitir. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                  | Soporte técnico/valor                | Notas                                                                                                                                                                                                                                                  |
|---------------------------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) | Obligatorio                     | Todos los controles de hipervínculo deben admitir el patrón de control [Invoke](uiauto-implementinginvoke.md) .                                                                                                                                                       |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | Depende                      | Los controles de hipervínculo deben admitir el patrón de control [Value](uiauto-implementingvalue.md) si el vínculo contiene información que es utilizable y significativa para el usuario.                                                                              |
| [**Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)      | Por ejemplo, "https://www..". | Una dirección URL para una dirección de Internet o Intranet es un ejemplo de un hipervínculo que contiene información significativa para el usuario. Sin embargo, un vínculo de programación solo es significativo para una aplicación y no se recomienda para la propiedad **Value** . |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de hipervínculo deben admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId. |                                                                                                                            |
| [**\_InvokedEventId de invocación de UIA \_**](uiauto-event-ids.md)                                                     |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                 | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.             | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="remarks"></a>Observaciones

El tipo de control HyperLink solo debe aplicarse a un objeto que, cuando se hace clic en él, hace que se produzca la navegación; no se debe aplicar al contenedor del hipervínculo. Por ejemplo, solo las "zonas activas" en las que se hace clic dentro de un mapa de imágenes deben tener el tipo de control **HYPERLINK** . Lo mismo se aplica a los hipervínculos de un campo de texto o contenedor de documentos. En este caso, solo el texto o la imagen del hipervínculo deben tener el tipo de control **HYPERLINK** , no el contenedor.

El patrón de control [Text](uiauto-implementingtextandtextrange.md) es idóneo para admitir hipervínculos incrustados en elementos de texto o de documento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




