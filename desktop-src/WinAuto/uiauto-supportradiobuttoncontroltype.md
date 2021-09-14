---
title: Tipo de control RadioButton
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control RadioButton.
ms.assetid: 6fc4a6a3-f5c0-402b-b9e7-870dfaa3370d
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control RadioButton
- Automatización de la interfaz de usuario, tipo de control RadioButton
- Automatización de la interfaz de usuario,estructura de árbol para el tipo de control RadioButton
- Automatización de la interfaz de usuario,properties para el tipo de control RadioButton
- Automatización de la interfaz de usuario,patrones de control para el tipo de control RadioButton
- Automatización de la interfaz de usuario,events para el tipo de control RadioButton
- estructuras de árbol, tipo de control RadioButton
- properties,Tipo de control RadioButton
- patrones de control, tipo de control RadioButton
- events,Tipo de control RadioButton
- Compatibilidad con el tipo de control RadioButton
- RadioButton (tipo de control)
- tipos de control, estructura de árbol para el tipo de control RadioButton
- tipos de control, patrones de control para el tipo de control RadioButton
- tipos de control, compatibilidad con RadioButton
- tipos de control, RadioButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a854eec792943a6fc094796de1e3ea6849c6a5e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242300"
---
# <a name="radiobutton-control-type"></a>Tipo de control RadioButton

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **RadioButton.**

Un botón de opción consta de un botón redondo y de texto definido por la aplicación (una etiqueta), un icono o un mapa de bits que indica una opción que el usuario puede realizar seleccionando el botón. Normalmente, una aplicación usa botones de radio en un cuadro de grupo para permitir al usuario elegir entre un conjunto de opciones relacionadas, aunque mutuamente excluyentes. Por ejemplo, la aplicación puede presentar un grupo de botones de radio desde el que el usuario puede seleccionar una preferencia de formato para el texto seleccionado en el área del cliente. El usuario podría seleccionar un formato alineado a la izquierda, alineado a la derecha o centrado seleccionando el botón de radio correspondiente. Normalmente, el usuario solo puede seleccionar una opción cada vez a partir de un conjunto de botones de radio.

> [!Note]  
> Otra generalización de controles para los botones donde solo se puede seleccionar uno de un grupo es el contenido de un botón de alternancia. Algunos marcos de interfaz de usuario consideran que un botón de radio es un botón de alternancia especializado.

 

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo de control **RadioButton.** Los Automatización de la interfaz de usuario se aplican a todos los controles de botón en los que el marco o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Comentarios:](#remarks)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control típico y una vista de contenido del árbol Automatización de la interfaz de usuario que pertenece a los controles de botón de radio y se describe lo que se puede incluir en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario, vea [información general Automatización de la interfaz de usuario árbol de datos.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>RadioButton</li></ul> | <ul><li>RadioButton</li></ul> | 




 

No hay ningún elemento secundario en la vista de control o la vista de contenido.

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para los controles que implementan el tipo de control **RadioButton** (como los controles de botón). Para obtener más información sobre Automatización de la interfaz de usuario propiedades, vea [Recuperar propiedades de Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value           | Notas                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas.      | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato Automatización de la interfaz de usuario árbol.                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.      | El rectángulo exterior que contiene el control completo.                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.      | El punto en el que se puede hacer clic debe ser un punto que, al hacer clic, seleccione el botón de radio.                                                             |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **RadioButton** |                                                                                                                                               |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | true            | El control de botón de radio siempre se incluye en la vista de contenido del Automatización de la interfaz de usuario texto.                                                    |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | true            | El control de botón de radio siempre se incluye en la vista de control del Automatización de la interfaz de usuario control.                                                    |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas.      | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                     |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL            | Los controles de botón de radio se etiquetan por su contenido.                                                                                     |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.      | Cadena localizada correspondiente al tipo de control **RadioButton.** El valor predeterminado es "botón de radio" para en-US o inglés (Estados Unidos). |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.      | El nombre del control de botón de radio es el texto que se muestra junto al botón que mantiene el estado de selección.                      |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con todos los controles de botón de radio. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                                               | Soporte técnico/valor | Notas                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                | Obligatorio      | Todos los controles de botón de radio deben admitir el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) para poder seleccionarse.                                                                                                                                                                                                                                                             |
| [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) | Vea las notas.    | La [**propiedad SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) siempre debe completarse para que un cliente Automatización de la interfaz de usuario pueda determinar qué otros botones de radio dentro de un contexto específico se relacionan entre sí. Para la versión De Microsoft Win32 del botón de radio, esta propiedad no se admite porque no es posible obtener esta información de ese marco heredado. |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                              | Nunca         | El botón de radio no puede recorrer cíclicamente su estado una vez que se ha establecido. El [patrón de](uiauto-implementingtoggle.md) control Alternar nunca debe ser compatible con un botón de radio.                                                                                                                                                                                                                                      |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario eventos que los controles de botón son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                     | Notas                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                        |                                                                                                                                |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)   |                                                                                                                                |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                   | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.       |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)               | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento.     |
| [**Elemento \_ SelectionItem de \_ UIARemovedFromSelectionEventId**](uiauto-event-ids.md) | Si el control admite el patrón de control [SelectionItem,](uiauto-implementingselectionitem.md) debe admitir este evento. |
| [**Elementos \_ SelectionItem \_ de UIASelectedEventId**](uiauto-event-ids.md)                         | Si el control admite el patrón de control [SelectionItem,](uiauto-implementingselectionitem.md) debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                    |                                                                                                                                |



 

## <a name="remarks"></a>Observaciones

Un botón de radio representa una única opción seleccionable entre un grupo de botones de radio del mismo nivel. Idealmente, los botones de radio deben tener un elemento de agrupación que aclare los límites de los botones de radio del mismo nivel. Sin embargo, a menudo, el límite está implícito en la estructura de elementos de la interfaz de usuario. Por ejemplo, un menú puede contener un conjunto de botones de radio consecutivos en lugar de elementos de menú, o un conjunto de botones de radio que se producen después de una etiqueta de grupo, pero antes de un elemento que se puede usar como botón.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




