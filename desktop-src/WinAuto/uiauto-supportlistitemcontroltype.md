---
title: Tipo de control ListItem
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control ListItem.
ms.assetid: 8cb579ab-92c9-4311-aad7-5363f4cf2eaf
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control ListItem
- Automatización de la interfaz de usuario, tipo de control ListItem
- Automatización de la interfaz de usuario estructura de árbol para el tipo de control ListItem
- Automatización de la interfaz de usuario,properties para el tipo de control ListItem
- Automatización de la interfaz de usuario,patrones de control para el tipo de control ListItem
- Automatización de la interfaz de usuario,events para el tipo de control ListItem
- estructuras de árbol, tipo de control ListItem
- properties,Tipo de control ListItem
- patrones de control, tipo de control ListItem
- events,Tipo de control ListItem
- compatibilidad con el tipo de control ListItem
- Tipo de control ListItem
- tipos de control, estructura de árbol para el tipo de control ListItem
- tipos de control, patrones de control para el tipo de control ListItem
- tipos de control, compatibilidad con ListItem
- tipos de control, ListItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cf7275212d44b795f354cb895c2d64727e375ea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483201"
---
# <a name="listitem-control-type"></a>Tipo de control ListItem

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **ListItem.**

Los controles de elemento de lista son un ejemplo de controles que implementan el tipo de control **ListItem.**

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **ListItem.** Los Automatización de la interfaz de usuario se aplican a todos los controles de elementos de lista en los que la plataforma o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Comentarios:](#remarks)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol Automatización de la interfaz de usuario que pertenece a los controles de elemento de lista y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol Automatización de la interfaz de usuario, vea [información general Automatización de la interfaz de usuario árbol de árbol.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>ListItem<ul><li>Imagen (0 o más)</li><li>Text (0 o más)</li><li>Edición (0 o más)</li></ul></li></ul> | <ul><li>ListItem</li></ul> | 




 

Los elementos secundarios de un control de elemento de lista dentro de la vista de contenido del Automatización de la interfaz de usuario deben mostrar siempre cero elementos secundarios. Si la estructura del control es tal que otros elementos se encuentran debajo del elemento de lista, debe seguir los requisitos de la compatibilidad de Automatización de la interfaz de usuario para el tipo de control [TreeItem.](uiauto-supporttreeitemcontroltype.md)

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para el tipo de control **ListItem.** Para obtener más información sobre Automatización de la interfaz de usuario, vea [Retrieving Properties from Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Valor        | Notas                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas.   | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del Automatización de la interfaz de usuario árbol. Asigne la **propiedad AutomationId** para un elemento de lista si se sabe que el elemento es coherente en diferentes instancias de la interfaz de usuario. Si el elemento de lista se rellena dinámicamente y no es predecible, deje la **propiedad AutomationId** en blanco.                                                          |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.   | El valor de esta propiedad debe incluir el área del contenido de imagen y texto del elemento de lista.                                                                                                                                                                                                                                                                                                                              |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Depende      | Si el control de lista tiene un punto en el que se puede hacer clic (un punto en el que se puede hacer clic para hacer que la lista tome el foco), ese punto debe exponerse a través de esta propiedad. Si el control de lista está completamente cubierto por elementos de lista descendientes, devolverá el error [**UIA \_ E \_ NOCLICKABLEPOINT**](uiauto-error-codes.md) para indicar que el cliente debe pedir a un elemento dentro del control de lista un punto en el que se pueda hacer clic. |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **ListItem** | Este valor es el mismo para todos los marcos de trabajo de la interfaz de usuario.                                                                                                                                                                                                                                                                                                                                                                                     |
| [**HelpTextPropertyId de UIA \_**](uiauto-automation-element-propids.md)                         | Vea las notas.   | El texto de ayuda para los controles de lista debe explicar por qué se le solicita al usuario que elija una opción en una lista de opciones, que es normalmente el mismo tipo de información presentada a través de una información sobre herramientas. Por ejemplo, "Seleccione un elemento para establecer la resolución de pantalla del monitor".                                                                                                                                                    |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | **TRUE**     | El control de lista siempre se incluye en la vista de contenido del Automatización de la interfaz de usuario lista.                                                                                                                                                                                                                                                                                                                                                |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | **TRUE**     | El control de lista siempre se incluye en la vista de control del Automatización de la interfaz de usuario control.                                                                                                                                                                                                                                                                                                                                                |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas.   | Si el contenedor puede aceptar la entrada de teclado, este valor de propiedad debe ser **TRUE.**                                                                                                                                                                                                                                                                                                                                           |
| [**IsOffscreenPropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | Depende      | Esta propiedad debe devolver un valor para saber si el elemento de lista se desplaza actualmente a la vista dentro del contenedor primario que implementa el patrón de control [Scroll.](uiauto-implementingscroll.md)                                                                                                                                                                                                                                  |
| [**ItemStatusPropertyId de UIA \_**](uiauto-automation-element-propids.md)                     | Depende      | Si el control contiene el estado que se está actualizando dinámicamente, esta propiedad debe ser compatible para que una tecnología de asistencia pueda recibir actualizaciones cuando cambie el estado del elemento.                                                                                                                                                                                                                                     |
| [**ItemTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                         | Depende      | Esta propiedad se debe exponer para los controles de elemento de lista que representan un objeto subyacente. Estos controles de elemento de lista suelen tener un icono asociado al control que los usuarios se asocian con el objeto subyacente.                                                                                                                                                                                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas.   | Si hay una etiqueta de texto estático, esta propiedad debe exponer una referencia a ese control.                                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.   | Cadena localizada correspondiente al tipo de control **ListItem.** El valor predeterminado es "elemento de lista" para en-US o inglés (Estados Unidos).                                                                                                                                                                                                                                                                                           |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.   | El valor de la propiedad name de un control de elemento de lista procede de la etiqueta de texto del elemento.                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control de lista que deben ser compatibles con todos los controles de elemento de lista. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                                   | Soporte técnico | Notas                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depende | Si el elemento se puede manipular para mostrar u ocultar información, se debe implementar el patrón de control [ExpandCollapse.](uiauto-implementingexpandcollapse.md)                                                                                                                                                                                                                        |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | Depende | Si se admite la navegación espacial de elemento a elemento dentro del contenedor de lista y el contenedor se organiza en filas y columnas, se debe implementar el patrón de control [GridItem.](uiauto-implementinggriditem.md)                                                                                                                                                                  |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Depende | Si el elemento tiene un comando que se puede realizar en él, independientemente de la selección, [se](uiauto-implementinginvoke.md) debe implementar el patrón de control Invoke. Se trata normalmente de una acción asociada a hacer doble clic en el control de elemento de lista. Algunos ejemplos serían iniciar un documento desde Windows Explorer o reproducir un archivo de música en Microsoft Reproductor de Windows Media.        |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | Depende | Si el elemento de lista está dentro de un contenedor que se puede desplazar, se debe implementar el patrón de control [ScrollItem.](uiauto-implementingscrollitem.md)                                                                                                                                                                                                                       |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Depende | Un control de elemento de lista que admita la selección debe implementar el patrón de control [SelectionItem.](uiauto-implementingselectionitem.md) Esto permite que los controles de elementos de lista transmitan cuando se seleccionan.                                                                                                                                                                             |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Depende | Si el elemento de lista se puede comprobar y la acción no realiza un cambio de estado de selección, se debe implementar el patrón de control [Alternar.](uiauto-implementingtoggle.md)                                                                                                                                                                                                            |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Depende | Si se puede editar el elemento, [se](uiauto-implementingvalue.md) debe implementar el patrón de control Valor. Los cambios en el control de elemento de lista provocarán cambios en los valores de las propiedades [**\_ NamePropertyId**](uiauto-automation-element-propids.md) y [**\_ ValueValuePropertyId de UIA.**](uiauto-control-pattern-propids.md) |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos Automatización de la interfaz de usuario que los controles de elemento de lista son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                                                | Notas                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                              |                                                                                                                                  |
| [**UIA \_ Evento de cambio de propiedad ExpandCollapseExpandCollapseStatePropertyId.**](uiauto-control-pattern-propids.md) | Si el control admite el patrón de control [ExpandCollapse,](uiauto-implementingexpandcollapse.md) debe admitir este evento. |
| [**Invoke \_ InvokeEventId de UIA \_**](uiauto-event-ids.md)                                                                                  | Si el control admite el patrón de control [Invoke,](uiauto-implementinginvoke.md) debe admitir este evento.                 |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                              | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.         |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                          | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento.       |
| [**UIA \_ Evento de cambio de propiedad ItemStatusPropertyId.**](uiauto-automation-element-propids.md)                                            | Si el control admite la [**propiedad ItemStatus,**](uiauto-automation-element-propids.md) es debe admitir este evento.        |
| [**UIA \_ Evento de cambio de propiedad NamePropertyId.**](uiauto-automation-element-propids.md)                                                        |                                                                                                                                  |
| [**Elemento \_ SelectionItem \_ de UIAAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Si el control admite el patrón de control [SelectionItem,](uiauto-implementingselectionitem.md) debe admitir este evento.   |
| [**Elemento \_ SelectionItem \_ de UIARemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Si el control admite el patrón de control [SelectionItem,](uiauto-implementingselectionitem.md) debe admitir este evento.   |
| [**Elementos \_ SelectionItem \_ de UIASelectedEventId**](uiauto-event-ids.md)                                                    | Si el control admite el patrón de control [SelectionItem,](uiauto-implementingselectionitem.md) debe admitir este evento.   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**UIA \_ Evento de cambio de propiedad ToggleToggleStatePropertyId.**](uiauto-control-pattern-propids.md)                                 | Si el control admite el patrón de control [Toggle,](uiauto-implementingtoggle.md) debe admitir este evento.                 |
| [**UIA \_ Evento de cambio de propiedad ValueValuePropertyId.**](uiauto-control-pattern-propids.md)                                               | Si el control admite el patrón de control [Valor,](uiauto-implementingvalue.md) debe admitir este evento.                   |



 

## <a name="remarks"></a>Comentarios

Si un contenedor hospeda elementos de lista, el medio principal de navegación debe ir a los elementos de lista. Centrarse en los subelementos a través de la navegación de lista puede resultar confuso para los usuarios y las herramientas de accesibilidad. Si el contenedor hospeda una lista vertical de elementos, al presionar las teclas FLECHA ARRIBA y FLECHA ABAJO se deben navegar por los elementos, pero al presionar las teclas FLECHA DERECHA y FLECHA IZQUIERDA se pueden navegar a los subelementos del elemento centrado, como las columnas de lista o los subelementos de la interfaz de usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




