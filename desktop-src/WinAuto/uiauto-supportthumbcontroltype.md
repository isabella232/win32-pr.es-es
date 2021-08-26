---
title: Tipo de control Thumb
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control Thumb.
ms.assetid: 3b1d6802-cfd4-4b07-80a0-2950ca7f4e96
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Thumb
- Automatización de la interfaz de usuario, tipo de control Thumb
- Automatización de la interfaz de usuario,estructura de árbol para el tipo de control Thumb
- Automatización de la interfaz de usuario,properties para el tipo de control Thumb
- Automatización de la interfaz de usuario,patrones de control para el tipo de control Thumb
- Automatización de la interfaz de usuario,events para el tipo de control Thumb
- estructuras de árbol, tipo de control Thumb
- properties,Thumb (tipo de control)
- patrones de control, tipo de control Thumb
- events,Thumb control type
- compatibilidad con el tipo de control Thumb
- Thumb (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Thumb
- tipos de control, patrones de control para el tipo de control Thumb
- tipos de control, compatibilidad con Thumb
- tipos de control, Thumb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea75b39ae0b17be23886823d446667299e5f0df
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478791"
---
# <a name="thumb-control-type"></a>Tipo de control Thumb

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control **Thumb.**

Los controles de posición ofrecen la funcionalidad que permite que un control se mueva (o se arrastre), como un botón de barra de desplazamiento, o que cambie su tamaño, como un widget para cambiar el tamaño de una ventana. Tenga en cuenta que un control de posición no proporciona la funcionalidad de arrastrar y colocar. Los controles thumb pueden recibir el foco del mouse, pero no el foco del teclado. El desarrollador del control debe implementar el control para que actúe correctamente (se pueda arrastrar o cambiar de tamaño).

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo de control **Thumb.** Los Automatización de la interfaz de usuario se aplican a todos los controles thumb en los que el marco o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades pertinentes](#relevant-properties)
-   [Patrones de control necesarios](#required-control-patterns)
-   [Eventos necesarios](#required-events)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control típico y una vista de contenido del árbol Automatización de la interfaz de usuario que pertenece a los controles thumb y se describe lo que se puede incluir en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario, [vea información general Automatización de la interfaz de usuario árbol de datos.](uiauto-treeoverview.md)




| Vista de control | Vista de contenido | 
|--------------|--------------|
| <ul><li>Thumb</li></ul> | (No aplicable) | 




 

Los controles thumb nunca aparecen en la vista de contenido porque solo existen para manipularse con un mouse. Se exponen a través de otro patrón de control, como el patrón de control [Scroll,](uiauto-implementingscroll.md) el patrón de control [Transform](uiauto-implementingtransform.md) o el patrón de control [RangeValue,](uiauto-implementingrangevalue.md) que se admite en el contenedor del control thumb.

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para los controles thumb. Para obtener más información sobre Automatización de la interfaz de usuario propiedades, vea [Recuperar propiedades de Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).



| Propiedad de automatización de interfaz de usuario                                                                                              | Valor      | Notas                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato Automatización de la interfaz de usuario árbol.                                                                                                                                                 |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                     |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | Punto dentro del área de cliente visible del control de posición.                                                                                                                                                                                                 |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **Pulgar**  |                                                                                                                                                                                                                                                              |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | FALSE      | El control thumb nunca se incluye en la vista de contenido del Automatización de la interfaz de usuario control.                                                                                                                                                                           |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE       | El control thumb siempre se incluye en la vista de control del Automatización de la interfaz de usuario control.                                                                                                                                                                          |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas. | Si el control puede recibir el foco del teclado, debe admitir esta propiedad. Un control de posición puede recibir el foco si se usa como un objeto "control" para cambiar el tamaño de una ventana o un panel. Un control de posición en un control deslizante o barra de desplazamiento nunca debe recibir el foco. |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL       | Los controles Thumb nunca tienen una etiqueta.                                                                                                                                                                                                                           |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada correspondiente al tipo de control **Thumb.** El valor predeterminado es "thumb" para en-US o inglés (Estados Unidos).                                                                                                                             |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | NULL       | Dado que el control de posición no está disponible en la vista de contenido Automatización de la interfaz de usuario árbol, no requiere un nombre.                                                                                                                                        |



 

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control que deben ser compatibles con los controles thumb. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control                                         | Soporte técnico  | Notas                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Requerido | Permite que el control de posición se mueva por la pantalla. Dado que el control de posición normalmente no se puede cambiar o cambiar de tamaño, el patrón de control [Transformar](uiauto-implementingtransform.md) admite principalmente la [**función Move.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move) |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran Automatización de la interfaz de usuario eventos que los controles thumb son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automatización de la interfaz de usuario evento                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




