---
title: Tipo de control de documento
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control Document.
ms.assetid: 62565f16-f0d6-42ff-bc36-897a2618c867
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Document
- Automatización de la interfaz de usuario, tipo de control Document
- Automatización de la interfaz de usuario,tree structure for Document control type
- Automatización de la interfaz de usuario,properties para el tipo de control Document
- Automatización de la interfaz de usuario,patrones de control para el tipo de control Document
- Automatización de la interfaz de usuario,events para el tipo de control Document
- tree structures,Document control type
- properties,Document (tipo de control)
- patrones de control, Tipo de control de documento
- events,Document (tipo de control)
- compatibilidad con el tipo de control Document
- Document (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Document
- tipos de control, patrones de control para el tipo de control Document
- tipos de control, compatibilidad con document
- tipos de control, Documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cb068e5b2d69c3b7ac180b65436888ca550b1db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172642"
---
# <a name="document-control-type"></a>Tipo de control de documento

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo **de** control Document.

Los controles de documento permiten a un usuario ver y manipular varias páginas de texto. A diferencia de los controles de edición que solo admiten una línea simple de texto sin formato, los controles de documento pueden hospedar texto con un estilo y un formato enriquecidos.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo **de** control Document. Los Automatización de la interfaz de usuario se aplican a todos los controles de documentos en los que el marco o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control típico y una vista de contenido del árbol de Automatización de la interfaz de usuario que pertenece a los controles de documento y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario, vea [información general Automatización de la interfaz de usuario árbol de datos.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>Documento<ul><li>Varía</li></ul></li></ul> | <ul><li>Documento<ul><li>Varía</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para los controles de documento. Para obtener más información sobre Automatización de la interfaz de usuario propiedades, vea [Recuperar propiedades de Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value        | Notas                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas.   | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel de la vista sin formato Automatización de la interfaz de usuario árbol.                                      |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.   | El rectángulo exterior que contiene el control completo.                                                                                          |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.   | El documento tiene un punto en el que se puede hacer clic que provocará que el foco pase al documento de uno de sus elementos del contenedor de documento.                   |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **Documento** |                                                                                                                                                   |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | true         | El control de documento siempre se incluye en la vista de contenido del Automatización de la interfaz de usuario contenido.                                                            |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | true         | El control de documento siempre se incluye en la vista de control del Automatización de la interfaz de usuario control.                                                            |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas.   | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                         |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas.   | El valor de esta propiedad debe ser la etiqueta del control de documento. Normalmente, se utiliza el título del documento.                             |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.   | Cadena localizada correspondiente al tipo **de** control Document. El valor predeterminado es "document" para en-US o Inglés (Estados Unidos).            |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.   | Normalmente, el control de documento obtiene su nombre del nombre de archivo desde el que se carga. A menudo, esto se muestra en el título de un marco o una ventana contenedora. |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con los controles de documento. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                  | Soporte técnico/valor | Notas                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) | Depende       | El control de documento puede abarcar más de lo que puede la ventanilla. El control debe admitir el [patrón de](uiauto-implementingscroll.md) control Scroll si el contenido se puede desplazar.                                                                                                                              |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | Obligatorio      | Todos los controles de documento deben admitir el [patrón de](uiauto-implementingtextandtextrange.md) control Texto.                                                                                                                                                                                                                |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | Depende       | Aunque Automatización de la interfaz de usuario clientes pueden usar [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) para obtener información de texto sobre un documento, necesitan el patrón de [control](uiauto-implementingvalue.md) Valor para establecer el valor interno. La entrada de texto simple solo es posible a través del patrón de control Valor. |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran Automatización de la interfaz de usuario eventos que los controles de documento son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                                        | Notas                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                      |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                      | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                  | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)   | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.           |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md) | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.           |
| [**UIA \_ Evento de cambio de propiedad ScrollHorizontalViewSizePropertyId.**](uiauto-control-pattern-propids.md)           | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.           |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)       | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.           |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md)     | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.           |
| [**UIA \_ Evento de cambio de propiedad ScrollVerticalViewSizePropertyId.**](uiauto-control-pattern-propids.md)               | Si el control admite el patrón de control [Scroll,](uiauto-implementingscroll.md) debe admitir este evento.           |
| [**Selección de UIA \_ \_ InvalidatedEventId**](uiauto-event-ids.md)                                                            | Si el control admite el patrón de control [Selection,](uiauto-implementingselection.md) debe admitir este evento.     |
| [**Texto UIA \_ \_ TextSelectionChangedEventId**](uiauto-event-ids.md)                                                    |                                                                                                                            |
| [**Texto de UIA \_ \_ TextChangedEventId**](uiauto-event-ids.md)                                                                      |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad ValueValuePropertyId.**](uiauto-control-pattern-propids.md)                                       | Si el control admite el [patrón de](uiauto-implementingvalue.md) control Valor, debe admitir este evento.             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




