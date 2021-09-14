---
title: Editar tipo de control
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control Edit.
ms.assetid: ec45ec5e-4faa-4635-8726-5bbe1f20b843
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Edit
- Automatización de la interfaz de usuario,Editar tipo de control
- Automatización de la interfaz de usuario,tree structure for Edit control type
- Automatización de la interfaz de usuario,properties para Editar tipo de control
- Automatización de la interfaz de usuario,patrones de control para Editar tipo de control
- Automatización de la interfaz de usuario,events para el tipo de control Edit
- estructuras de árbol, Editar tipo de control
- properties,Editar tipo de control
- patrones de control, Editar tipo de control
- events,Editar tipo de control
- Compatibilidad con el tipo de control Edit
- Edit (tipo de control)
- tipos de control, estructura de árbol para Editar tipo de control
- tipos de control, patrones de control para Editar tipo de control
- tipos de control, compatibilidad con editar
- tipos de control, Editar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5eea05d463f191483cb53f7cbfceef83058093f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172637"
---
# <a name="edit-control-type"></a>Editar tipo de control

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el **tipo de** control Editar.

Los controles de edición habilitan a un usuario para que vea y edite una línea de texto simple sin compatibilidad con formato enriquecido.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo de control de edición. Los Automatización de la interfaz de usuario se aplican a todos los controles de edición en los que el marco o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Comentarios:](#remarks)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control típico y una vista de contenido del árbol de Automatización de la interfaz de usuario que pertenece a los controles de edición y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario, vea [información general Automatización de la interfaz de usuario árbol de datos.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>Editar</li></ul> | <ul><li>Editar</li></ul> | 




 

Los controles que implementan el tipo de control **Edit** siempre tendrán ninguna barra de desplazamiento en la vista de control del árbol Automatización de la interfaz de usuario porque es un control de una sola línea. La única línea de texto puede encapsularse en algunos escenarios de diseño. El **tipo de** control Editar solo está pensado para pequeñas cantidades de texto.

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para los controles de edición. Para obtener más información sobre Automatización de la interfaz de usuario propiedades, vea [Recuperar propiedades de Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value      | Notas                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel de la vista sin formato Automatización de la interfaz de usuario árbol.                                                                                                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | El control de edición debe tener un punto en el que se pueda hacer clic que dé enfoque de entrada a la parte de edición del control cuando un usuario hace clic en el mouse allí.                                                                                                                                           |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **Editar**   |                                                                                                                                                                                                                                                                                      |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | **TRUE**   | El control de edición siempre se incluye en la vista de contenido del Automatización de la interfaz de usuario de edición.                                                                                                                                                                                                   |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | **TRUE**   | El control de edición siempre se incluye en la vista de control del Automatización de la interfaz de usuario control.                                                                                                                                                                                                   |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas. | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                                                                                            |
| [**IsPasswordPropertyId de UIA \_**](uiauto-automation-element-propids.md)                     | Vea las notas. | Debe establecerse en **TRUE en** los controles de edición que contienen contraseñas. Si un control de edición contiene el contenido de la contraseña, esta propiedad se puede usar por un lector de pantalla para determinar si las pulsaciones de teclas se deben leer cuando el usuario las introduce.                                      |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas. | Si hay una etiqueta de texto estático asociada al control , esta propiedad debe exponer una referencia a ese control. Si el control de texto es un subcomponente de otro control, no tendrá una **propiedad LabeledBy** establecida.                                                         |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada correspondiente al tipo **de** control Edit. El valor predeterminado es "editar" para en-US o inglés (Estados Unidos).                                                                                                                                                       |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | El nombre del control de edición se genera normalmente desde una etiqueta de texto estático. Si no hay una etiqueta de texto estático, el desarrollador de la aplicación debe asignar un valor de propiedad para **Name.** La **propiedad Name** nunca debe contener el contenido textual del control de edición. |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con los controles de edición. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                              | Soporte técnico/valor | Notas                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)     | Depende       | Todos los controles de edición que toman un intervalo numérico deben exponer el patrón de control [RangeValue.](uiauto-implementingrangevalue.md)                                                                                                                                                                                                                                                                                       |
| [**Mínima**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Vea las notas.    | Esta propiedad debe ser el valor más pequeño en el que se puede establecer el contenido del control de edición.                                                                                                                                                                                                                                                                                                                     |
| [**Máxima**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Vea las notas.    | Esta propiedad debe ser el valor más grande en el que se puede establecer el contenido del control de edición.                                                                                                                                                                                                                                                                                                                      |
| [**SmallChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | Vea las notas.    | Esta propiedad debe indicar el número de posiciones decimales en el que se puede establecer el valor. Si el control de edición solo toma enteros, el valor de la propiedad **SmallChange** debe ser 1. Si el control de edición toma un intervalo de 1.0 a 2.0, el valor de la propiedad **SmallChange** debe ser 0.1. Si el control de edición toma un intervalo de 1,00 a 2,00, el valor de la propiedad **SmallChange** debe ser 0,001.                   |
| [**LargeChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | **NULL**      | Esta propiedad no necesita exponerse en un control de edición.                                                                                                                                                                                                                                                                                                                                                      |
| [**Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | Vea las notas.    | Esta propiedad indica el contenido numérico del control de edición. Cuando un cliente de Automatización de la interfaz de usuario establece un valor más preciso dentro [](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum) de los intervalos especificados en las propiedades Minimum y [**Maximum,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum) la propiedad [**Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value) se redondea automáticamente al valor aceptado más cercano. |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)                 | Obligatorio      | Todos los controles de edición deben admitir el [patrón](uiauto-implementingtextandtextrange.md) de control Texto, ya que la información detallada siempre debe estar disponible para los clientes de tecnología de asistencia.                                                                                                                                                                                                                     |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)               | Depende       | Todos los controles de edición que toman una cadena deben exponer el [patrón de](uiauto-implementingvalue.md) control Valor.                                                                                                                                                                                                                                                                                                        |
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly)        | Vea las notas.    | Esta propiedad debe establecerse para indicar si el control puede tener un valor establecido mediante programación o que el usuario puede editar.                                                                                                                                                                                                                                                                                |
| [**Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)                  | Vea las notas.    | Esta propiedad contiene el contenido textual del control de edición. Si la [**propiedad \_ IsPasswordPropertyId**](uiauto-automation-element-propids.md) de UIA está establecida en **TRUE,** la consulta a [**la propiedad Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value) debe devolver un error.                                                                                                                      |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario que se necesitan para admitir los controles de edición. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                                        | Notas                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                      |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                      | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                  | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**UIA \_ Evento de cambio de propiedad NamePropertyId.**](uiauto-automation-element-propids.md)                                                |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad RangeValueValuePropertyId.**](uiauto-control-pattern-propids.md)                             | Si el control admite el patrón de control [RangeValue,](uiauto-implementingrangevalue.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)   | Un control de edición nunca admite el [patrón de](uiauto-implementingscroll.md) control Scroll.                                |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md) | Un control de edición nunca admite el [patrón de](uiauto-implementingscroll.md) control Scroll.                                |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontalViewSizePropertyId.**](uiauto-control-pattern-propids.md)           | Un control de edición nunca admite el [patrón de](uiauto-implementingscroll.md) control Scroll.                                |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)       | Un control de edición nunca admite el [patrón de](uiauto-implementingscroll.md) control Scroll.                                |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md)     | Un control de edición nunca admite el [patrón de](uiauto-implementingscroll.md) control Scroll.                                |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticalViewSizePropertyId.**](uiauto-control-pattern-propids.md)               | Un control de edición nunca admite el [patrón de](uiauto-implementingscroll.md) control Scroll.                                |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| [**Texto de UIA \_ \_ TextChangedEventId**](uiauto-event-ids.md)                                                                      | Si el control admite el patrón de control [Text,](uiauto-implementingtextandtextrange.md) debe admitir este evento.   |
| [**Texto UIA \_ \_ TextSelectionChangedEventId**](uiauto-event-ids.md)                                                    | Si el control admite el patrón de control [Text,](uiauto-implementingtextandtextrange.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad ValueValuePropertyId**](uiauto-control-pattern-propids.md) .                                      | Si el control admite el [patrón de](uiauto-implementingvalue.md) control Valor, debe admitir este evento.             |



 

## <a name="remarks"></a>Observaciones

Un control de edición se puede usar como un campo de texto de solo lectura que no admite la selección o edición de texto. Este control de edición se comporta como un objeto de campo que tiene un nombre y un valor específicos.

Si un control de edición contiene texto de marcador de posición (por ejemplo, un banner de indicación), el texto debe usarse como la propiedad **HelpText** a menos que el usuario pueda editar el texto y volver a usarlo como texto de marcador de posición. Por ejemplo, la Windows Internet Explorer de direcciones contiene el texto "about:Tabs" cuando se abre una nueva pestaña. No es **HelpText porque** es una dirección mediante programación que el usuario puede usar o editar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




