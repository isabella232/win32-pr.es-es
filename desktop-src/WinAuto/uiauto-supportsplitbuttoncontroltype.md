---
title: Tipo de control SplitButton
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control SplitButton.
ms.assetid: ca4f8e45-7487-4a8b-9df5-edc2b0e56663
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control SplitButton
- Automatización de la interfaz de usuario, tipo de control SplitButton
- Automatización de la interfaz de usuario estructura de árbol para el tipo de control SplitButton
- Automatización de la interfaz de usuario,properties para el tipo de control SplitButton
- Automatización de la interfaz de usuario,patrones de control para el tipo de control SplitButton
- Automatización de la interfaz de usuario,events para el tipo de control SplitButton
- estructuras de árbol, tipo de control SplitButton
- properties,Tipo de control SplitButton
- patrones de control, tipo de control SplitButton
- events,Tipo de control SplitButton
- compatibilidad con el tipo de control SplitButton
- Tipo de control SplitButton
- tipos de control, estructura de árbol para el tipo de control SplitButton
- tipos de control, patrones de control para el tipo de control SplitButton
- tipos de control, compatibilidad con SplitButton
- tipos de control,SplitButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e420d369ee09dfd2d92b5e5d79cf94c7013566
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569712"
---
# <a name="splitbutton-control-type"></a>Tipo de control SplitButton

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **SplitButton.**

El control de botón de división permite realizar una acción en un control y expandir el control para ver una lista de otras acciones posibles que se pueden realizar.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo de control **SplitButton.** Los Automatización de la interfaz de usuario se aplican a todos los controles de botón de división en los que la plataforma o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Ejemplo de tipo de control SplitButton](#splitbutton-control-type-example)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control típico y una vista de contenido del árbol Automatización de la interfaz de usuario que pertenece a los controles de botón de división y se describe lo que se puede incluir en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario, vea [información general Automatización de la interfaz de usuario árbol de datos.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>SplitButton<ul><li>Image (0 o 1)</li><li>Text (0 o 1)</li><li>Button (1 o 2)<ul><li>Menú (0 o 1; aparece como un elemento secundario de un botón secundario que admite el patrón ExpandCollapse)<ul><li>MenuItem (1 o varios)</li></ul></li></ul></li></ul></li></ul> | <ul><li>SplitButton<ul><li>Button (1 o 2)<ul><li>MenuItem (1 o varios)</li></ul></li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para el tipo de control **SplitButton.** Para obtener más información sobre Automatización de la interfaz de usuario propiedades, vea [Recuperar propiedades de Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value           | Notas                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas.      | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel de la vista sin formato Automatización de la interfaz de usuario árbol.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.      | El rectángulo exterior que contiene el control completo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.      | Se admite si hay un rectángulo delimitador. Si no se puede hacer clic en todos los puntos del rectángulo delimitador y el elemento realiza pruebas de acceso especializadas, invalide y proporcione un punto en el que se puede hacer clic. |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **SplitButton** | Este valor es el mismo para todos los marcos de trabajo de la interfaz de usuario.                                                                                                                                                        |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Vea las notas.      | El texto de ayuda puede indicar el resultado de la activación del botón de división, que normalmente es el mismo tipo de información que se presenta mediante un elemento de información sobre herramientas.                                                   |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | true            | El control de botón de división contiene información para el usuario final.                                                                                                                                      |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | true            | El control de botón de división es visible para el usuario final.                                                                                                                                                 |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas.      | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL            | Los controles de botón de expansión no tienen una etiqueta de texto estático.                                                                                                                                               |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.      | Cadena localizada correspondiente al tipo de control **SplitButton.** El valor predeterminado es "botón de división" para en-US o inglés (Estados Unidos).                                                        |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.      | Texto que se usa para etiquetar el botón de división. Siempre que se usa una imagen para etiquetar un botón de división, se debe proporcionar texto alternativo para la propiedad Nombre del botón de división.                              |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con todos los controles de botón de división. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                                   | Soporte técnico  | Notas                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Obligatorio | Dado que los botones de división siempre tienen la capacidad de expandir una lista de opciones, deben admitir el patrón de control [ExpandCollapse.](uiauto-implementingexpandcollapse.md)                                                      |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Obligatorio | Dado que los botones de división siempre tienen una acción predeterminada asociada al método [**IInvokeProvider::Invoke,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) deben admitir el patrón de control [Invoke.](uiauto-implementinginvoke.md) |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario que se necesitan para admitir los controles de botón de división. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                                                | Notas                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                              |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad ExpandCollapseExpandCollapseStatePropertyId.**](uiauto-control-pattern-propids.md) |                                                                                                                            |
| [**Invoke \_ InvokeEventId de UIA \_**](uiauto-event-ids.md)                                                                                  |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                              | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                          | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                            |



 

## <a name="splitbutton-control-type-example"></a>Ejemplo de tipo de control SplitButton

En la imagen siguiente se muestra un control que implementa el tipo de control **SplitButton.**

![captura de pantalla que muestra un ejemplo de un control splitbutton](images/splitbuttonxmpl.jpg)




| Automatización de la interfaz de usuario árbol de control: Vista de control | Automatización de la interfaz de usuario árbol de contenido: vista de contenido | 
|-----------------------------------|-----------------------------------|
| <ul><li>SplitButton "Nombre" (Invoke, ExpandCollapse)<ul><li>Botón "Más opción" (Invocar)<ul><li>Menú<ul><li>MenuItem</li><li>...</li></ul></li></ul></li></ul></li></ul> | <ul><li>SplitButton "Nombre" (Invoke, ExpandCollapse)<ul><li>Botón "Más opción" (Invocar)<ul><li>Menú<ul><li>MenuItem</li><li>...</li></ul></li></ul></li></ul></li></ul> | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




