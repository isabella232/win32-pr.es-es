---
title: Tipo de control ProgressBar
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control ProgressBar.
ms.assetid: 2ea0c1f1-1a0a-4360-bdcb-8edc13cc3c31
keywords:
- Automatización de la interfaz de usuario,compatibilidad con el tipo de control ProgressBar
- Automatización de la interfaz de usuario, tipo de control ProgressBar
- Automatización de la interfaz de usuario estructura de árbol para el tipo de control ProgressBar
- Automatización de la interfaz de usuario,properties para el tipo de control ProgressBar
- Automatización de la interfaz de usuario,patrones de control para el tipo de control ProgressBar
- Automatización de la interfaz de usuario,events para el tipo de control ProgressBar
- estructuras de árbol, tipo de control ProgressBar
- properties,Tipo de control ProgressBar
- patrones de control, tipo de control ProgressBar
- events,Tipo de control ProgressBar
- Compatibilidad con el tipo de control ProgressBar
- ProgressBar (tipo de control)
- tipos de control, estructura de árbol para el tipo de control ProgressBar
- tipos de control, patrones de control para el tipo de control ProgressBar
- tipos de control, compatibilidad con ProgressBar
- tipos de control, ProgressBar
ms.topic: article
ms.date: 12/04/2019
ms.openlocfilehash: 5dc5dd22abcaca70ae9ce86717db6055642a21ce
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472319"
---
# <a name="progressbar-control-type"></a>Tipo de control ProgressBar

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **ProgressBar.**

Los controles de barra de progreso indican el progreso de una operación larga. El control está compuesto de un rectángulo que se rellena gradualmente con el color de resaltado del sistema a medida que una operación progresa.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo de control **ProgressBar.** Los Automatización de la interfaz de usuario se aplican a todos los controles de barra de progreso en los que la plataforma o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

- [Estructura de árbol típica](#typical-tree-structure)
- [Propiedades pertinentes](#relevant-properties)
- [Patrones de control necesarios](#required-control-patterns)
- [Eventos necesarios](#required-events)
- [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol Automatización de la interfaz de usuario que pertenece a los controles de barra de progreso y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol Automatización de la interfaz de usuario, vea [información general Automatización de la interfaz de usuario árbol de árbol.](uiauto-treeoverview.md)


| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>ProgressBar</li></ul> | <ul><li>ProgressBar</li></ul> | 


Los controles de barra de progreso no tienen ningún elemento secundarios en el control o la vista de contenido del Automatización de la interfaz de usuario árbol.

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran las Automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para las barras de progreso. Para obtener más información sobre Automatización de la interfaz de usuario, vea [Retrieving Properties from Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).

| Propiedad de automatización de interfaz de usuario                                                                                              | Valor           | Notas                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas.      | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del Automatización de la interfaz de usuario árbol.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.      | El rectángulo exterior que contiene el control completo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.      | Se admite si hay un rectángulo delimitador. Si no se puede hacer clic en todos los puntos del rectángulo delimitador y el elemento realiza pruebas de acceso especializadas, invalide y proporcione un punto en el que se puede hacer clic. |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **Progressbar** |                                                                                                                                                                                                      |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | **TRUE**        | El control de barra de progreso siempre se incluye en la vista de contenido del Automatización de la interfaz de usuario de progreso.                                                                                                           |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | **TRUE**        | El control de barra de progreso siempre se incluye en la vista de control del Automatización de la interfaz de usuario árbol.                                                                                                           |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas.      | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas.      | Si hay una etiqueta de texto estático, esta propiedad debe exponer una referencia a ese control.                                                                                                              |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.      | Cadena localizada correspondiente al tipo de control **ProgressBar.** El valor predeterminado es "barra de progreso" para en-US o inglés (Estados Unidos).                                                        |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.      | El control de barra de progreso suele recibir su nombre de una etiqueta de texto estático. Si no hay ninguna etiqueta de texto estático, el desarrollador de aplicaciones debe exponer un valor para la propiedad Name.                  |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control necesarios para que sean compatibles con los controles de barra de progreso. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                              | Soporte técnico/valor | Notas                                                                                                                                      |
|---------------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)     | Depende       | Los controles de barra de progreso que toman un intervalo numérico deben implementar el patrón de control [RangeValue.](uiauto-implementingrangevalue.md)        |
| [**Mínima**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Depende           | El valor de esta propiedad es el valor mínimo en el que se puede establecer el control. Este valor debe ser menor que [**Maximum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum).                                                      |
| [**Máxima**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Depende         | El valor de esta propiedad es el valor máximo en el que se puede establecer el control. Este valor debe ser mayor que [**minimum.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)                                                        |
| [**SmallChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | **NaN**       | Esta propiedad no es necesaria porque los controles de barra de progreso son de solo lectura.                                                                 |
| [**LargeChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | **NaN**       | Esta propiedad no es necesaria porque los controles de barra de progreso son de solo lectura.                                                                 |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)               | Depende       | Los controles de barra de progreso que dan una indicación textual del progreso deben implementar el [patrón de](uiauto-implementingvalue.md) control Valor. |
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly)        | **TRUE**      | El valor de esta propiedad siempre es **TRUE.**                                                                                            |
| [**Valor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)                  | Vea las notas.    | Esta propiedad expone el progreso textual de un control de barra de progreso.                                                                          |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran Automatización de la interfaz de usuario eventos de progreso que se requieren para admitir las barras de progreso. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**UIA \_ Evento de cambio de propiedad NamePropertyId.**](uiauto-automation-element-propids.md)                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad RangeValueValuePropertyId.**](uiauto-control-pattern-propids.md)        | Si el control admite el patrón de control [RangeValue,](uiauto-implementingrangevalue.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad ValueValuePropertyId.**](uiauto-control-pattern-propids.md)                  | Si el control admite el [patrón de](uiauto-implementingvalue.md) control Valor, debe admitir este evento.             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




