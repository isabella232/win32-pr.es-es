---
title: Image (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control Image.
ms.assetid: 439c708c-4fb4-481b-a2ff-3816d649f3ff
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control Image
- Automatización de la interfaz de usuario, tipo de control Image
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control Image
- UI Automation, propiedades para el tipo de control Image
- Automatización de la interfaz de usuario, patrones de control para el tipo de control Image
- Automatización de la interfaz de usuario, eventos para el tipo de control Image
- estructuras de árbol, tipo de control Image
- propiedades, tipo de control Image
- patrones de control, tipo de control Image
- Events, Image (tipo de control)
- compatibilidad con el tipo de control Image
- Image (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Image
- tipos de control, patrones de control para el tipo de control Image
- tipos de control, compatibilidad con imágenes
- tipos de control, imagen
ms.topic: article
ms.date: 10/08/2019
ms.openlocfilehash: b91d55bf8e21813e180476146625172e3eab1a6d
ms.sourcegitcommit: da8cc3fb3c9f14cb768855502a2b6815ddee13b6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/10/2019
ms.locfileid: "105676281"
---
# <a name="image-control-type"></a>Image (tipo de control)

En este tema se proporciona información sobre la compatibilidad de Microsoft UI Automation para el tipo de control **Image** .

Los controles de imagen usados como iconos, gráficos informativos y gráficos admitirán el tipo de control **Image** . Los controles usados como imágenes de marca de agua o de fondo no admitirán el tipo de control **Image** .

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario, las propiedades, los patrones de control y los eventos necesarios para el tipo de control **Image** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles de imagen donde la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y patrones de control

En este tema se incluyen las siguientes secciones.

- [Estructura de árbol típica](#typical-tree-structure)
- [Propiedades relevantes](#relevant-properties)
- [Patrones de control necesarios](#required-control-patterns)
- [Eventos necesarios](#required-events)
- [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece a los controles de imagen y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).

| Vista de control | Vista de contenido |
| ------------ | ------------ |
| Imagen | Imagen (depende de si la imagen contiene información, según el valor de la propiedad [identificadores de propiedad del elemento de automatización](uiauto-automation-element-propids.md) ) |

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles de imagen. Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).

| Propiedad de automatización de interfaz de usuario                                                                                              | Value      | Notas                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | El punto en el que se puede hacer clic del control de imagen debe ser un punto dentro del rectángulo delimitador del control de imagen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Imagen**  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Vea las notas. | La propiedad **HelpText** expone una cadena localizada que describe el aspecto visual real del control u otra información sobre herramientas asociada a la imagen. Se debe admitir esta propiedad cuando se necesite una descripción larga para transmitir más información sobre el control de imagen (por ejemplo, si la imagen es un gráfico o diagrama complicado). Esta propiedad se asigna a la etiqueta **longdesc** HTML y la etiqueta **DESC** de Scalable Vector Graphics (SVG). Los desarrolladores que trabajan con controles de imagen deben admitir una propiedad para permitir la descripción visual que se establecerá en el control. Esta propiedad se debe asignar a la propiedad **VisualDescription** de automatización de la interfaz de usuario. |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | Vea las notas. | El control de imagen debe estar incluido en la vista de contenido del árbol de automatización de la interfaz de usuario cuando contiene información significativa aún no expuesta al usuario final.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | El control de imagen siempre se incluye en la vista de control del árbol de automatización de la interfaz de usuario.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vea las notas. | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | Vea las notas. | Si el control de imagen representa la información del estado sobre un elemento concreto de la pantalla, el control debe incluirse dentro del elemento. Cuando la imagen está contenida dentro de un elemento, el elemento debe admitir la propiedad de estado y generar las notificaciones adecuadas cuando cambie el estado. Si una imagen es un control independiente y transmite el estado, se debe admitir esta propiedad.                                                                                                                                                                                                                                                                                    |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas. | Si hay una etiqueta de texto estático, esta propiedad debe exponer una referencia a ese control.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada que corresponde al tipo de control **Image** . El valor predeterminado es "Image" para en-US o inglés (Estados Unidos).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | La propiedad **Name** se debe exponer para todos los controles de imagen que contienen información. El acceso mediante programación a esta información requiere que se ofrezca un equivalente textual al gráfico. Si el control de imagen es puramente decorativo, solo debe aparecer en la vista de control del árbol de automatización de la interfaz de usuario y no es necesario que tenga un nombre (vea la [sección Comentarios](#remarks)). Los marcos de trabajo de interfaz de usuario deben admitir propiedad de texto alternativo o ALT en las imágenes que se pueden establecer desde dentro de su marco de trabajo. Esta propiedad se asignará a la propiedad de nombre de automatización de la interfaz de usuario.                                                                                                                                                     |

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los patrones de control de automatización de la interfaz de usuario que se deben admitir para los controles de imagen. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

| Patrón de control                                                 | Soporte técnico | Notas                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)           | Depende | El control de imagen admite el patrón de control [GridItem](uiauto-implementinggriditem.md) si el control está dentro de un contenedor de cuadrícula.                                                                                                                                                                                                                                                                                                                      |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)               | Nunca   | Si el control de imagen es un objeto en el que se hace clic, el control debe admitir un tipo de control que admita el patrón de control [Invoke](uiauto-implementinginvoke.md) , como el tipo de control [Button](uiauto-supportbuttoncontroltype.md) . Para un objeto Image que contiene varios objetos que se pueden hacer clic, el elemento (tipo de control Image) puede hospedar vínculos secundarios (tipo de control[HYPERLINK](uiauto-supporthyperlinkcontroltype.md) ) en el árbol de automatización de la interfaz de usuario. |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) | Nunca   | Los controles de imagen no deben admitir el patrón de control [SelectionItem](uiauto-implementingselectionitem.md) . Si las imágenes forman parte de un contenedor que es seleccionable, como un botón que tiene un icono de imagen como contenido, ese contenedor admite el patrón, no la imagen dentro de.                                                                                                                                                                           |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)         | Depende | El control de imagen admite el patrón de control [TableItem](uiauto-implementingtableitem.md) si el control está dentro de un contenedor que tiene controles de encabezado.                                                                                                                                                                                                                                                                                                |

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que los controles de imagen deben admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).

| Evento de automatización de la interfaz de usuario                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                 | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.             | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de ItemStatusPropertyId.               | Si el control admite la propiedad [**ItemStatus**](uiauto-automation-element-propids.md) , debe admitir este evento.  |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de NamePropertyId.                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |

## <a name="remarks"></a>Observaciones

El World Wide Web Consortium (W3C) define una imagen decorativa como una que no agrega información al contenido de una página. Para obtener más información, vea el tema de W3C sobre [imágenes decorativas](https://www.w3.org/WAI/tutorials/images/decorative/).

Con respecto a la automatización de la interfaz de usuario:

- Si una imagen es puramente decorativa, no es interactiva y no transmite ninguna información, la imagen:
  - Puede o no estar en el árbol de UIA
  - Puede o no estar en la vista sin formato de UIA
  - No debe estar en la vista de control de UIA
  - No debe estar en la vista de contenido
  - Puede tener o no un nombre
- Si una imagen transmite información, pero hay texto claramente asociado que proporciona la misma información (por ejemplo, un botón de reproducción que contiene un gráfico de triángulo que señala a la izquierda junto con el texto "reproducir"), la imagen se considera decorativa y la imagen:
  - Debe estar en la vista sin formato
  - Debe estar en la vista de control
  - No debe estar en la vista de contenido
  - Puede tener o no un valor en la propiedad nombre
  - El texto que también transmite el significado de la imagen debe estar en la vista de contenido
- Si una imagen es informativa y transmite detalles que no proporciona ningún texto asociado, la imagen:
  - Debe estar en la vista sin formato
  - Debe estar en la vista de control
  - Debe estar en la vista de contenido
  - Debe tener un valor de nombre que describa la imagen y su significado.

## <a name="related-topics"></a>Temas relacionados

### <a name="conceptual"></a>Conceptual

- [Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
- [Información general sobre UI Automation](uiauto-uiautomationoverview.md)
