---
title: Tipo de control ComboBox
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control ComboBox.
ms.assetid: e7c64dc1-e1e3-4f99-adde-d0d63eb6c4c9
keywords:
- Automatización de la interfaz de usuario,compatibilidad con el tipo de control ComboBox
- Automatización de la interfaz de usuario,tipo de control ComboBox
- Automatización de la interfaz de usuario estructura de árbol para el tipo de control ComboBox
- Automatización de la interfaz de usuario,properties para el tipo de control ComboBox
- Automatización de la interfaz de usuario,patrones de control para el tipo de control ComboBox
- Automatización de la interfaz de usuario,events para el tipo de control ComboBox
- estructuras de árbol, tipo de control ComboBox
- properties,Tipo de control ComboBox
- patrones de control, tipo de control ComboBox
- events,Tipo de control ComboBox
- Compatibilidad con el tipo de control ComboBox
- Tipo de control ComboBox
- tipos de control, estructura de árbol para el tipo de control ComboBox
- tipos de control, patrones de control para el tipo de control ComboBox
- tipos de control, compatibilidad con ComboBox
- tipos de control, ComboBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9d9f38dab9877aee38773e5c900ee125d2ba6a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480111"
---
# <a name="combobox-control-type"></a>Tipo de control ComboBox

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **ComboBox.**

Un cuadro combinado es un cuadro de lista combinado con un control estático o un control de edición que muestra el elemento seleccionado actualmente en la parte del cuadro de lista del cuadro combinado. La parte de cuadro de lista del control se muestra en todo momento o solo aparece cuando el usuario selecciona la flecha de lista desplegable (que es un botón de comando) junto al control. Si el campo de selección es un control de edición, el usuario puede escribir información que no esté en la lista; de lo contrario, el usuario solo puede seleccionar elementos de la lista.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo de control **ComboBox.** Los Automatización de la interfaz de usuario se aplican a todos los controles de cuadro combinado en los que la plataforma o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol Automatización de la interfaz de usuario que pertenece a los controles de cuadro combinado y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol Automatización de la interfaz de usuario, [vea información general Automatización de la interfaz de usuario árbol de árbol.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>ComboBox<ul><li>Edición (0 o 1)</li><li>Lista (0 o 1)</li><li>List Item (elemento secundario de List; de 0 a varios)</li><li>Button (1)</li></ul></li></ul> | <ul><li>ComboBox<ul><li>List Item (de 0 a varios)</li></ul></li></ul> | 




 

El control de edición de la vista de control del cuadro combinado solo es necesario si el cuadro  combinado se puede editar para tomar cualquier entrada, como es el caso del cuadro combinado en el cuadro de diálogo Ejecutar .

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para el tipo de control **ComboBox.** Para obtener más información sobre Automatización de la interfaz de usuario, vea [Retrieving Properties from Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Valor      | Notas                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del Automatización de la interfaz de usuario árbol.                                                                                                                                                                                                     |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                                                         |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | Se admite si hay un rectángulo delimitador. Si no se puede hacer clic en todos los puntos del rectángulo delimitador y el elemento realiza pruebas de acceso especializadas, invalide y proporcione un punto en el que se puede hacer clic.                                                                                                             |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | ComboBox   |                                                                                                                                                                                                                                                                                                                  |
| [**HelpTextPropertyId de UIA \_**](uiauto-automation-element-propids.md)                         | Vea las notas. | El texto de ayuda de los controles de cuadro combinado debe explicar por qué se pide al usuario que elija una opción del cuadro combinado. El texto es similar a la información que se presenta mediante un elemento de información sobre herramientas. Por ejemplo, "Seleccione un elemento para establecer la resolución de pantalla del monitor".                                                |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE       | Los controles de cuadro combinado siempre se incluyen en la vista de contenido del Automatización de la interfaz de usuario combinado.                                                                                                                                                                                                                            |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE       | Los controles de cuadro combinado siempre se incluyen en la vista de control del Automatización de la interfaz de usuario control.                                                                                                                                                                                                                            |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | TRUE       | Los controles de cuadro combinado pueden recibir el foco del teclado; sin embargo, cuando un Automatización de la interfaz de usuario establece el foco en un cuadro combinado, cualquier elemento del subárbol del cuadro combinado puede recibir el foco.                                                                                                                                          |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas. | Los controles de cuadro combinado suelen tener una etiqueta de texto estático a la que hace referencia esta propiedad.                                                                                                                                                                                                                             |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada correspondiente al tipo de control **ComboBox.** El valor predeterminado es "cuadro combinado" para en-US o inglés (Estados Unidos).                                                                                                                                                                          |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | El nombre del control de cuadro combinado se genera normalmente a partir de una etiqueta de texto estático. Si no hay una etiqueta de texto estático, debe asignar un valor para la **propiedad Name.** La **propiedad Name** nunca debe contener el contenido actual del cuadro combinado ni cambiar cuando cambia el contenido del cuadro combinado. |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con todos los controles de cuadro combinado. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                                   | Soporte técnico  | Notas                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Requerido | El patrón de control [ExpandCollapse](uiauto-implementingexpandcollapse.md) debe ser compatible porque un control de cuadro combinado siempre debe contener un botón desplegable.                                                                                                                                                                                |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)           | Depende  | Muestra la selección actual en el cuadro combinado. La compatibilidad con [el patrón](uiauto-implementingselection.md) de control Selección se delega en el cuadro de lista debajo del cuadro combinado, pero puede que no siempre sea factible.                                                                                                                               |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Depende  | Si el cuadro combinado puede tomar valores de texto arbitrarios, debe ser compatible con [el patrón](uiauto-implementingvalue.md) de control Valor. Este patrón permite establecer mediante programación el contenido de cadena del cuadro combinado. Si no se admite el patrón de control Valor, el usuario debe seleccionar en los elementos de lista del subárbol del cuadro combinado. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                 | Nunca    | El [patrón de](uiauto-implementingscroll.md) control Scroll nunca se admite directamente en un cuadro combinado. Se admite si un cuadro de lista incluido dentro de un cuadro combinado se puede desplazar y solo cuando el cuadro de lista está visible en la pantalla.                                                                                                              |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran Automatización de la interfaz de usuario eventos que los controles de cuadro combinado son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                                                | Notas                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                              |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                              | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                          | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                            |
| [**UIA \_ Evento expandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) cambiado por la propiedad . |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad ValueValuePropertyId.**](uiauto-control-pattern-propids.md)                                               | Si el control admite el [patrón de](uiauto-implementingvalue.md) control Valor, debe admitir este evento.             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




