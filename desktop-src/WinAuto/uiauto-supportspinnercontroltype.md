---
title: Tipo de control spinner
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control Spinner.
ms.assetid: 28673ad5-645d-4314-96c4-81a951226256
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Spinner
- Automatización de la interfaz de usuario, tipo de control Spinner
- Automatización de la interfaz de usuario,estructura de árbol para el tipo de control Spinner
- Automatización de la interfaz de usuario,properties para el tipo de control Spinner
- Automatización de la interfaz de usuario, patrones de control para el tipo de control Spinner
- Automatización de la interfaz de usuario,events para el tipo de control Spinner
- estructuras de árbol, tipo de control Spinner
- properties,Spinner (tipo de control)
- patrones de control, tipo de control Spinner
- events,Spinner (tipo de control)
- Compatibilidad con el tipo de control Spinner
- Spinner (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Spinner
- tipos de control, patrones de control para el tipo de control Spinner
- tipos de control, compatibilidad con Spinner
- tipos de control, Spinner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1472fe400c189b6e5a1e894e1097395e8521e757
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569713"
---
# <a name="spinner-control-type"></a>Tipo de control spinner

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **Spinner.**

Los controles Spinner se usan para seleccionar desde un dominio de elementos o un intervalo de números.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo de control **Spinner.** Los Automatización de la interfaz de usuario se aplican a todos los controles de número en los que el marco o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control típico y una vista de contenido del árbol Automatización de la interfaz de usuario que pertenecen a los controles de número cuando admiten los patrones de control **RangeValue** y **Selection,** y se describe lo que se puede incluir en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario, vea [información general Automatización de la interfaz de usuario árbol de datos.](uiauto-treeoverview.md)

**Patrón de control RangeValue**




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>Spinner<ul><li>Edición (0 o 1)</li><li>Botón (2)</li></ul></li></ul> | <ul><li>Spinner</li></ul> | 




 

**Selection (patrón de control)**




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>Spinner<ul><li>Edición (0 o 1)</li><li>Botón (2)</li><li>Elemento de lista (0 o más)</li></ul></li></ul> | <ul><li>Spinner<ul><li>Elemento de lista (0 o más)</li></ul></li></ul> | 




 

Para asegurarse de que los dos botones del subárbol de la vista de control se pueden distinguir mediante herramientas de prueba automatizadas, asigne el valor **ScrollAmount \_ SmallIncrement** o [**ScrollAmount \_ SmallDecrement**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount) a la **propiedad AutomationId** según corresponda. Para algunas implementaciones, el control de edición asociado puede ser un par del control de número.

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para los controles de número. Para obtener más información sobre Automatización de la interfaz de usuario propiedades, vea [Recuperar propiedades de Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value       | Notas                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas.  | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel de la vista sin formato Automatización de la interfaz de usuario árbol.                                                                                                                                                                                                               |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.  | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                                                                   |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.  | El punto en el que se puede hacer clic del control de número enfoca la parte de edición del control.                                                                                                                                                                                                                                      |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **Spinner** | Este valor es el mismo para todos los marcos de trabajo.                                                                                                                                                                                                                                                                                 |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | true        | El control de número siempre debe ser contenido.                                                                                                                                                                                                                                                                                |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | true        | El control de número siempre debe ser un control .                                                                                                                                                                                                                                                                              |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas.  | Si el control puede recibir el foco del teclado, debe admitir esta propiedad. Un control de número rara vez toma el foco, pero cuando lo hace, el foco debe permanecer en el propio control de número, no en los botones secundarios. El usuario debe poder realizar todas las acciones de desplazamiento mediante las teclas FLECHA ARRIBA y FLECHA ABAJO. |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas.  | Los controles de número tienen una etiqueta de texto estático.                                                                                                                                                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.  | Cadena localizada correspondiente al tipo de control **Spinner.** El valor predeterminado es "spinner" para en-US o inglés (Estados Unidos).                                                                                                                                                                                       |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.  | El control de número suele recibir su nombre de una etiqueta de texto estático.                                                                                                                                                                                                                                                      |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control necesarios para que todos los controles de número sean compatibles. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                                         | Soporte técnico/valor | Notas                                                                                                                                     |
|--------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)                | Depende       | Los controles de número que abarcan un intervalo numérico pueden admitir el patrón de control [RangeValue.](uiauto-implementingrangevalue.md)               |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                  | Depende       | Los controles de número que tienen una lista de elementos que se deben seleccionar deben admitir el [patrón de](uiauto-implementingselection.md) control Selección. |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) | false         | Los controles de número siempre son contenedores de selección única.                                                                                  |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                          | Depende       | Los controles de número que abarcan un conjunto decrete de opciones o números pueden admitir el [patrón de](uiauto-implementingvalue.md) control Valor.    |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran Automatización de la interfaz de usuario eventos que los controles de número son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**UIA \_ Evento de cambio de propiedad RangeValueValuePropertyId.**](uiauto-control-pattern-propids.md)        | Si el control admite el patrón de control [RangeValue,](uiauto-implementingrangevalue.md) debe admitir este evento.   |
| [**UIA \_ Evento \_ de cambio de propiedad InvalidatedEventId**](uiauto-event-ids.md) de selección.               | Si el control admite el patrón de control [Selection,](uiauto-implementingselection.md) debe admitir este evento.     |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad ValueValuePropertyId.**](uiauto-control-pattern-propids.md)                  | Si el control admite el patrón de control [Valor,](uiauto-implementingvalue.md) debe admitir este evento.             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




