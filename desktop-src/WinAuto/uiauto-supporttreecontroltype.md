---
title: Tipo de control Tree
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control Tree.
ms.assetid: 0fa8f308-7815-4561-a1ce-c5f5582861da
keywords:
- Automatización de la interfaz de usuario,compatibilidad con el tipo de control Tree
- Automatización de la interfaz de usuario, tipo de control Tree
- Automatización de la interfaz de usuario,tree structure for Tree control type
- Automatización de la interfaz de usuario,properties para el tipo de control Tree
- Automatización de la interfaz de usuario,patrones de control para el tipo de control Tree
- Automatización de la interfaz de usuario,events para el tipo de control Tree
- tree structures,Tree control type
- properties,Tree control type
- patrones de control, tipo de control Tree
- events,Tree control type
- compatibilidad con el tipo de control Tree
- Tree (tipo de control)
- tipos de control, estructura de árbol para tipo de control Árbol
- tipos de control, patrones de control para el tipo de control Tree
- tipos de control, compatibilidad con tree
- tipos de control, Árbol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea7ac6330428c2e79fca1e9a51d4ca0f7c63e8a7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472851"
---
# <a name="tree-control-type"></a>Tipo de control Tree

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo **de** control Tree.

El **tipo de** control Árbol se usa para contenedores cuyo contenido tiene relevancia como jerarquía de nodos, como con la forma en que se muestran los archivos y carpetas en el panel izquierdo de Windows Explorer. Cada nodo tiene el potencial de contener otros nodos, denominados nodos secundarios. Los nodos primarios o los nodos que contienen nodos secundarios se pueden mostrar expandidos o contraídos. El Windows de vista de árbol (identificado por [**WC \_ TREEVIEW)**](/windows/desktop/Controls/common-control-window-classes)es un ejemplo de un control que pertenece al tipo **de** control Tree.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo **de** control Tree. Los Automatización de la interfaz de usuario se aplican a todos los controles de elementos de árbol en los que la plataforma o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control típico y una vista de contenido del árbol Automatización de la interfaz de usuario que pertenece a los controles de árbol y se describe lo que se puede incluir en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario, [vea información general Automatización de la interfaz de usuario árbol de datos.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>Árbol<ul><li>DataItem (0 o más)</li><li>TreeItem (0 o más)<ul><li>TreeItem (0 o más)<ul><li>...</li></ul></li></ul></li><li>ScrollBar (0, 1, 2)</li></ul></li></ul> | <ul><li>Árbol<ul><li>DataItem (0 o más)</li><li>TreeItem (0 o más)<ul><li>TreeItem (0 o más)<ul><li>...</li></ul></li></ul></li></ul></li></ul> | 




 

La vista de control del Automatización de la interfaz de usuario árbol consta de:

-   Cero de muchos elementos dentro del contenedor (los elementos se pueden basar en los tipos de control [TreeItem](uiauto-supporttreeitemcontroltype.md) [o DataItem).](uiauto-supportdataitemcontroltype.md)
-   Cero, uno o dos controles de barra de desplazamiento

La vista de contenido del árbol Automatización de la interfaz de usuario está formada por cero o varios elementos dentro del contenedor (los elementos se pueden basar en los tipos de control [TreeItem](uiauto-supporttreeitemcontroltype.md) [o DataItem).](uiauto-supportdataitemcontroltype.md)

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para el **tipo de** control Tree. Para obtener más información sobre Automatización de la interfaz de usuario propiedades, vea [Recuperar propiedades de Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Valor      | Notas                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del Automatización de la interfaz de usuario árbol.                                                                                                                                                                               |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                                   |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | Los controles de árbol tienen un punto en el que se puede hacer clic que hace que el árbol o uno de los elementos del contenedor de árbol reciba el foco. Un control de árbol solo puede tener un punto en el que se puede hacer clic si es posible hacer clic en una ubicación del árbol sin hacer que se seleccione un elemento o reciba el foco. |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **Árbol**   | Este valor es el mismo para todos los marcos de trabajo de la interfaz de usuario.                                                                                                                                                                                                                                              |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE       | El control de árbol siempre se incluye en la vista de contenido del Automatización de la interfaz de usuario árbol.                                                                                                                                                                                                         |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE       | El control de árbol siempre se incluye en la vista de control del Automatización de la interfaz de usuario árbol.                                                                                                                                                                                                         |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas. | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                                                                                                  |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas. | Si el control de árbol tiene una etiqueta asociada, esta propiedad devuelve un puntero [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para esa etiqueta. De lo contrario, la propiedad devuelve una referencia nula.                                                                          |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada correspondiente al tipo **de** control Tree. El valor predeterminado es "tree" para en-US o English (Estados Unidos).                                                                                                                                                             |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | El valor de la propiedad del nombre de un control de árbol normalmente procede del texto que etiqueta el control. Si no hay ninguna etiqueta de texto, debe proporcionar un valor para esta propiedad.                                                                                                                        |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con todos los controles de árbol. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                                             | Soporte técnico/valor | Notas                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | Depende       | Implemente [el patrón de](uiauto-implementingscroll.md) control Scroll si se pueden desplazar los elementos del contenedor de árbol.                                                                                                                 |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | Depende       | Los controles de árbol que contienen un conjunto de elementos seleccionables deben implementar el [patrón de](uiauto-implementingselection.md) control Selección. No es necesario implementarlo si al seleccionar un elemento no se transmite información significativa al usuario. |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | Vea las notas.    | Implemente esta propiedad si el control del árbol admite selección múltiple (la mayoría de los controles de árbol admiten selección múltiple).                                                                                                       |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | Vea las notas.    | El valor de esta propiedad se expone si el control requiere que se seleccione un elemento.                                                                                                                                               |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran Automatización de la interfaz de usuario eventos que deben admitir todos los controles de árbol. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                                        | Notas                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                      |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                      | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                  | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)   | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.           |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md) | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.           |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontalViewSizePropertyId.**](uiauto-control-pattern-propids.md)           | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.           |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md)     | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.           |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)       | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.           |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticalViewSizePropertyId.**](uiauto-control-pattern-propids.md)               | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.           |
| [**Selección de UIA \_ \_ InvalidatedEventId**](uiauto-event-ids.md)                                                            | Si el control admite el patrón de control [Selection,](uiauto-implementingselection.md) debe admitir este evento.     |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 
