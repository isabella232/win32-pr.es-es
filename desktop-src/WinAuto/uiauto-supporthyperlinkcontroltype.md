---
title: Tipo de control Hyperlink
description: En este tema se proporciona información sobre la compatibilidad Automatización de la interfaz de usuario Microsoft para el tipo de control Hyperlink.
ms.assetid: 6dd16ae6-eff0-4913-8916-5092aec34f1f
keywords:
- Automatización de la interfaz de usuario,compatibilidad con el tipo de control Hyperlink
- Automatización de la interfaz de usuario,Tipo de control Hyperlink
- Automatización de la interfaz de usuario estructura de árbol para el tipo de control Hyperlink
- Automatización de la interfaz de usuario,properties para el tipo de control Hyperlink
- Automatización de la interfaz de usuario,patrones de control para el tipo de control Hyperlink
- Automatización de la interfaz de usuario,events para el tipo de control Hyperlink
- estructuras de árbol, tipo de control Hyperlink
- properties,Hyperlink (tipo de control)
- patrones de control, tipo de control Hyperlink
- events,Hyperlink (tipo de control)
- Compatibilidad con el tipo de control Hyperlink
- Hyperlink (tipo de control)
- tipos de control, estructura de árbol para tipo de control Hyperlink
- tipos de control, patrones de control para tipo de control Hyperlink
- tipos de control, compatibilidad con Hyperlink
- tipos de control,Hyperlink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52735983429a60061a548bf4cce71b7b128f4b6e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359236"
---
# <a name="hyperlink-control-type"></a>Tipo de control Hyperlink

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **Hyperlink.**

Los controles de hipervínculo crean vínculos que permiten a los usuarios navegar dentro de la misma página o de una página a otra.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo de control **Hyperlink.** Los Automatización de la interfaz de usuario se aplican a todos los controles de hipervínculo en los que el marco o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Comentarios:](#remarks)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol Automatización de la interfaz de usuario que pertenece a los controles de hipervínculo y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario árbol, vea [Información general Automatización de la interfaz de usuario árbol de árbol.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>Hyperlink</li></ul> | <ul><li>Hyperlink</li></ul> | 




 

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para los controles de hipervínculo. Para obtener más información sobre Automatización de la interfaz de usuario, vea [Retrieving Properties from Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Value         | Notas                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas.    | El valor de esta propiedad debe ser único en todos los controles de una aplicación.                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas.    | El rectángulo exterior que contiene el control completo.                                                                                 |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas.    | El punto en el que se puede hacer clic del control de hipervínculo debe ser un punto que inicie el hipervínculo si se hace clic con un puntero del mouse.                     |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **Hipervínculo** |                                                                                                                                          |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | true          | El control de hipervínculo siempre se incluye en la vista de contenido del Automatización de la interfaz de usuario árbol.                                                  |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | true          | El control de hipervínculo siempre se incluye en la vista de control del Automatización de la interfaz de usuario control.                                                  |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas.    | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas.    | Si hay una etiqueta de texto estático, esta propiedad debe exponer una referencia a ese control.                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas.    | Cadena localizada correspondiente al tipo de control **Hyperlink.** El valor predeterminado es "hipervínculo" para en-US o inglés (Estados Unidos). |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas.    | El nombre del control de hipervínculo es el texto que se muestra en la pantalla como subrayado.                                                  |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que los controles de hipervínculo son necesarios para admitir. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                  | Soporte técnico/valor                | Notas                                                                                                                                                                                                                                                  |
|---------------------------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) | Obligatorio                     | Todos los controles de hipervínculo deben admitir el patrón de control [Invoke.](uiauto-implementinginvoke.md)                                                                                                                                                       |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | Depende                      | Los controles de hipervínculo deben admitir [el patrón de](uiauto-implementingvalue.md) control Valor cuando el vínculo contiene información que es utilizable y significativa para el usuario.                                                                              |
| [**Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)      | Por ejemplo, "https://www..". | Una dirección URL para una dirección de Internet o intranet es un ejemplo de un hipervínculo que contiene información significativa para el usuario. Sin embargo, un vínculo mediante programación solo es significativo para una aplicación y no se recomienda para la **propiedad Value.** |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos Automatización de la interfaz de usuario que los controles de hipervínculo son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**Invoke \_ InvokeEventId de UIA \_**](uiauto-event-ids.md)                                                     |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="remarks"></a>Observaciones

El tipo de control Hyperlink solo debe aplicarse a un objeto que, al hacer clic en él, hace que se produzca la navegación; no se debe aplicar al contenedor del hipervínculo. Por ejemplo, solo las "zonas populares" en las que se puede hacer clic dentro de un mapa de imágenes deben tener el tipo de control **Hipervínculo.** Lo mismo sucede con los hipervínculos de un campo de texto o contenedor de documentos. En este caso, solo el texto o la imagen del hipervínculo debe tener el tipo de control **Hyperlink,** no el contenedor.

El [patrón de](uiauto-implementingtextandtextrange.md) control Text es ideal para admitir hipervínculos incrustados en elementos de texto o documento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




