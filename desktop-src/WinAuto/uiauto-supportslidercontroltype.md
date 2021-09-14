---
title: Tipo de control deslizante
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control Slider.
ms.assetid: dc7bef7a-b68c-4184-a9e7-745bb41b592e
keywords:
- Automatización de la interfaz de usuario,compatibilidad con el tipo de control Slider
- Automatización de la interfaz de usuario, tipo de control Slider
- Automatización de la interfaz de usuario estructura de árbol para el tipo de control Slider
- Automatización de la interfaz de usuario,properties para el tipo de control Slider
- Automatización de la interfaz de usuario,patrones de control para el tipo de control Slider
- Automatización de la interfaz de usuario,events para el tipo de control Slider
- estructuras de árbol, tipo de control Slider
- properties,Slider (tipo de control)
- patrones de control, Tipo de control deslizante
- events,Slider (tipo de control)
- Compatibilidad con el tipo de control Slider
- Slider (tipo de control)
- tipos de control, estructura de árbol para tipo de control Slider
- tipos de control, patrones de control para el tipo de control Slider
- tipos de control, compatibilidad con Slider
- tipos de control, Control deslizante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 354217323ba4c3c59e416f7b9c36661d8ffe8a77
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242289"
---
# <a name="slider-control-type"></a>Tipo de control deslizante

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **Slider.**

Un control deslizante es un control compuesto con botones que permiten al usuario establecer un intervalo numérico o seleccionar entre un conjunto de elementos.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo **de** control Slider. Los Automatización de la interfaz de usuario se aplican a todos los controles deslizantes en los que el marco o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control típico y una vista de contenido del árbol de Automatización de la interfaz de usuario que pertenece a los controles deslizantes y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario, vea [información general Automatización de la interfaz de usuario árbol de datos.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>Control deslizante<ul><li>Button (2 o 4)</li><li>Thumb (1)</li><li>Elemento de lista (0 o más)</li></ul></li></ul> | <ul><li>Control deslizante<ul><li>Elemento de lista (0 o más)</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para los controles deslizantes. Para obtener más información sobre Automatización de la interfaz de usuario propiedades, vea [Recuperar propiedades de Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value      | Notas                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato Automatización de la interfaz de usuario árbol.                                                                                                                   |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                                                       |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | La mayoría de los controles deslizantes deben devolver el error [**UIA \_ E \_ NOCLICKABLEPOINT**](uiauto-error-codes.md) porque todo el rectángulo delimitador del control deslizante está ocupado por controles secundarios. |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **Slider** | Este valor es el mismo para todos los marcos de trabajo.                                                                                                                                                                                     |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | true       | El control deslizante siempre se incluye en la vista de contenido del Automatización de la interfaz de usuario control deslizante.                                                                                                                                           |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | true       | El control deslizante siempre se incluye en la vista de control del Automatización de la interfaz de usuario control.                                                                                                                                           |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas. | Si el control puede recibir el foco del teclado, debe admitir esta propiedad. Los secundarios (botones y thumb) de un control deslizante nunca deben tomar el foco. El foco siempre debe permanecer en el propio control deslizante.       |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas. | Si hay una etiqueta de texto estático asociada al control , esta propiedad debe exponer una referencia a ese control. Si el control de texto es un subcomponente de otro control, no tendrá una **propiedad LabeledBy** establecida.   |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada correspondiente al tipo **de** control Slider. El valor predeterminado es "slider" para en-US o Inglés (Estados Unidos).                                                                                             |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | El nombre del control deslizante normalmente se genera a partir de una etiqueta de texto estático. Si no hay una etiqueta de texto estático, el desarrollador de la aplicación debe asignar un valor de propiedad para **Name.**                              |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con todos los controles deslizantes. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                          | Soporte técnico/valor | Notas                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | Depende       | Un control deslizante debe admitir el patrón de control [RangeValue](uiauto-implementingrangevalue.md) si el contenido se puede establecer en un valor dentro de un intervalo numérico.                                                                                                                                                 |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)   | Depende       | Un control deslizante debe admitir el [patrón de](uiauto-implementingselection.md) control Selección si el contenido representa un valor entre un conjunto discreto de opciones. Si se admite el patrón de control Selection, la selección correspondiente se debe exponer como uno o varios elementos de lista secundarios del control deslizante. |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)           | Depende       | Un control deslizante debe admitir el [patrón de](uiauto-implementingvalue.md) control Valor si el contenido representa un valor entre un conjunto discreto de opciones.                                                                                                                                                     |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran Automatización de la interfaz de usuario eventos que los controles deslizantes son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**UIA \_ Evento de cambio de propiedad RangeValueValuePropertyId.**](uiauto-control-pattern-propids.md)        | Si el control admite el patrón de control [RangeValue,](uiauto-implementingrangevalue.md) debe admitir este evento.   |
| [**UIA \_ Selection \_ InvalidtedEventId**](uiauto-event-ids.md)                                       | Si el control admite el patrón de control [Selection,](uiauto-implementingselection.md) debe admitir este evento.     |
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

 

 




