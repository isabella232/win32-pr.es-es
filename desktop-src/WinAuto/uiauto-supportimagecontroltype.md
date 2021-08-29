---
title: Tipo de control de imagen
description: En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo de control Image.
ms.assetid: 439c708c-4fb4-481b-a2ff-3816d649f3ff
keywords:
- Automatización de la interfaz de usuario,compatibilidad con el tipo de control Image
- Automatización de la interfaz de usuario,Tipo de control Image
- Automatización de la interfaz de usuario,tree structure for Image control type
- Automatización de la interfaz de usuario,properties para el tipo de control Image
- Automatización de la interfaz de usuario,patrones de control para el tipo de control Image
- Automatización de la interfaz de usuario,events para el tipo de control Image
- tree structures,Image control type
- properties,Tipo de control Image
- patrones de control, tipo de control Image
- events,Tipo de control Image
- Compatibilidad con el tipo de control Imagen
- Image (tipo de control)
- tipos de control, estructura de árbol para el tipo de control Image
- tipos de control, patrones de control para el tipo de control Image
- tipos de control, compatibilidad con la imagen
- tipos de control, Imagen
ms.topic: article
ms.date: 10/08/2019
ms.openlocfilehash: 868db06a1ede025171e7a6cb9ef0d076267e095c9e17ed0ee7c65eb362f87590
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122045"
---
# <a name="image-control-type"></a>Tipo de control de imagen

En este tema se proporciona información sobre microsoft Automatización de la interfaz de usuario compatibilidad con el tipo **de** control Image.

Los controles de imagen que se usan como iconos, gráficos informativos y gráficos admitirán el tipo **de** control Imagen. Los controles usados como imágenes de fondo o marca de agua no admitirán el **tipo de** control Imagen.

En las secciones siguientes se definen los Automatización de la interfaz de usuario estructura de árbol, propiedades, patrones de control y eventos necesarios para el tipo de control **Image.** Los Automatización de la interfaz de usuario se aplican a todos los controles de imagen en los que el marco o plataforma de interfaz de usuario Automatización de la interfaz de usuario compatibilidad con los tipos de control y los patrones de control.

En este tema se incluyen las siguientes secciones.

- [Estructura de árbol típica](#typical-tree-structure)
- [Propiedades pertinentes](#relevant-properties)
- [Patrones de control necesarios](#required-control-patterns)
- [Eventos necesarios](#required-events)
- [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se muestra un control típico y una vista de contenido del árbol de Automatización de la interfaz de usuario que pertenece a los controles de imagen y se describe lo que se puede incluir en cada vista. Para obtener más información sobre el Automatización de la interfaz de usuario, vea [información general Automatización de la interfaz de usuario árbol de datos.](uiauto-treeoverview.md)

| Vista de control | Vista de contenido |
| ------------ | ------------ |
| Imagen | Image (depende de si la imagen contiene información, en función del valor de la propiedad Identificadores de propiedad [del elemento automation)](uiauto-automation-element-propids.md) |

## <a name="relevant-properties"></a>Propiedades pertinentes

En la tabla siguiente se enumeran Automatización de la interfaz de usuario propiedades cuyo valor o definición es especialmente relevante para los controles de imagen. Para obtener más información sobre Automatización de la interfaz de usuario propiedades, vea [Recuperar propiedades de Automatización de la interfaz de usuario Elements](uiauto-propertiesforclients.md).

| Propiedad de automatización de interfaz de usuario                                                                                              | Value      | Notas                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomationIdPropertyId de UIA \_**](uiauto-automation-element-propids.md)                 | Vea las notas. | El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato Automatización de la interfaz de usuario árbol.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vea las notas. | El rectángulo exterior que contiene el control completo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vea las notas. | El punto en el que se puede hacer clic del control de imagen debe ser un punto dentro del rectángulo delimitador del control de imagen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)                   | **Imagen**  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Vea las notas. | La **propiedad HelpText** expone una cadena localizada que describe la apariencia visual real del control u otra información sobre herramientas asociada a la imagen. Esta propiedad debe ser compatible cuando se necesita una descripción larga para transmitir más información sobre el control de imagen (por ejemplo, si la imagen es un gráfico o diagrama complicado). Esta propiedad se asigna a la etiqueta **LongDesc html** y a la etiqueta **Desc** scalable vector graphics (SVG). Los desarrolladores que trabajan con controles de imagen deben admitir una propiedad para permitir la descripción visual que se establecerá en el control. Esta propiedad debe asignarse al Automatización de la interfaz de usuario **propiedad VisualDescription.** |
| [**IsContentElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | Vea las notas. | El control de imagen debe incluirse en la vista de contenido del árbol de Automatización de la interfaz de usuario cuando contiene información significativa que aún no se ha expuesto al usuario final.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**IsControlElementPropertyId de UIA \_**](uiauto-automation-element-propids.md)         | TRUE       | El control de imagen siempre se incluye en la vista de control del Automatización de la interfaz de usuario control.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**\_IsKeyboardFocusablePropertyId de UIA**](uiauto-automation-element-propids.md)   | Vea las notas. | Si el control puede recibir el foco del teclado, debe admitir esta propiedad.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**ItemStatusPropertyId de UIA \_**](uiauto-automation-element-propids.md)                     | Vea las notas. | Si el control de imagen representa la información del estado sobre un elemento concreto de la pantalla, el control debe incluirse dentro del elemento. Cuando la imagen se encuentra dentro de un elemento, el elemento debe admitir la propiedad status y generar las notificaciones adecuadas cuando cambia el estado. Si una imagen es un control independiente y transmite el estado, se debe admitir esta propiedad.                                                                                                                                                                                                                                                                                    |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vea las notas. | Si hay una etiqueta de texto estático, esta propiedad debe exponer una referencia a ese control.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vea las notas. | Cadena localizada correspondiente al tipo **de** control Imagen. El valor predeterminado es "image" para en-US o English (Estados Unidos).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Nombre de \_ UIAPropertyId**](uiauto-automation-element-propids.md)                                 | Vea las notas. | La **propiedad Name** debe exponerse para todos los controles de imagen que contienen información. El acceso mediante programación a esta información requiere que se ofrezca un equivalente textual al gráfico. Si el control de imagen es meramente descriptivo, solo debe aparecer en la vista de control del árbol Automatización de la interfaz de usuario y no es necesario tener un nombre (vea [Comentarios](#remarks)). Los marcos de trabajo de interfaz de usuario deben admitir propiedad de texto alternativo o ALT en las imágenes que se pueden establecer desde dentro de su marco de trabajo. A continuación, esta propiedad se asignará a la Automatización de la interfaz de usuario nombre.                                                                                                                                                     |

## <a name="required-control-patterns"></a>Patrones de control necesarios

En la tabla siguiente se enumeran los Automatización de la interfaz de usuario de control necesarios para ser compatibles con los controles de imagen. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

| Patrón de control                                                 | Soporte técnico | Notas                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)           | Depende | El control de imagen admite el patrón de control [GridItem](uiauto-implementinggriditem.md) si el control está dentro de un contenedor de cuadrícula.                                                                                                                                                                                                                                                                                                                      |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)               | Nunca.   | Si el control de imagen es un objeto en el que se puede hacer clic, el control debe admitir un tipo de control que admita el patrón de control [Invoke,](uiauto-implementinginvoke.md) como [el tipo de](uiauto-supportbuttoncontroltype.md) control Button. En el caso de un objeto de imagen que contiene varios objetos en los que se puede hacer clic, el elemento (tipo de control Image) puede hospedar vínculos secundarios[(tipo](uiauto-supporthyperlinkcontroltype.md) de control Hyperlink) en el Automatización de la interfaz de usuario texto. |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) | Nunca.   | Los controles image no deben admitir el patrón de control [SelectionItem.](uiauto-implementingselectionitem.md) Si las imágenes forman parte de un contenedor que se puede seleccionar, como un botón que tiene un icono de imagen como contenido, ese contenedor admite el patrón, no la imagen dentro de .                                                                                                                                                                           |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)         | Depende | El control de imagen admite el patrón de control [TableItem](uiauto-implementingtableitem.md) si el control está dentro de un contenedor que tiene controles de encabezado.                                                                                                                                                                                                                                                                                                |

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran Automatización de la interfaz de usuario eventos que los controles de imagen son necesarios para admitir. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).

| Automatización de la interfaz de usuario evento                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**AutomationFocusChangedEventId de UIA \_**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ Evento de cambio de propiedad IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Si el control admite la [**propiedad IsEnabled,**](uiauto-automation-element-propids.md) debe admitir este evento.   |
| [**UIA \_ Evento de cambio de propiedad IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Si el control admite la [**propiedad IsOffscreen,**](uiauto-automation-element-propids.md) debe admitir este evento. |
| [**UIA \_ Evento de cambio de propiedad ItemStatusPropertyId.**](uiauto-automation-element-propids.md)               | Si el control admite la [**propiedad ItemStatus,**](uiauto-automation-element-propids.md) debe admitir este evento.  |
| [**UIA \_ Evento de cambio de propiedad NamePropertyId.**](uiauto-automation-element-propids.md)                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |

## <a name="remarks"></a>Comentarios

El World Wide Web Consortium (W3C) define una imagen interior como una que no agrega información al contenido de una página. Para obtener más información, vea el tema W3C sobre [imágenes escotes.](https://www.w3.org/WAI/tutorials/images/decorative/)

Con respecto a Automatización de la interfaz de usuario:

- Si una imagen es puramente interactiva, no es interactiva y no transmite ninguna información, la imagen:
  - Podría estar o no en el árbol de UIA
  - Podría estar o no en la vista sin procesar de UIA
  - No debe estar en la vista de control de UIA
  - No debe estar en la vista de contenido
  - Podría o no tener un nombre
- Si una imagen transmite información, pero hay un texto claramente asociado que proporciona la misma información (por ejemplo, un botón de reproducción que contiene un gráfico de triángulo que apunta a la izquierda junto con el texto "play"), la imagen se considera simétrico y la imagen:
  - Debe estar en la vista sin formato
  - Debe estar en la vista de control
  - No debe estar en la vista de contenido
  - Podría o no tener un valor en la propiedad Name
  - El texto que también transmite el significado de la imagen debe estar en la vista de contenido.
- Si una imagen es informativa y transmite detalles que no proporciona ningún texto asociado, la imagen:
  - Debe estar en la vista sin formato
  - Debe estar en la vista de control
  - Debe estar en la vista de contenido
  - Debe tener un valor de nombre que describa la imagen y su significado

## <a name="related-topics"></a>Temas relacionados

### <a name="conceptual"></a>Conceptual

- [Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
- [Información general sobre UI Automation](uiauto-uiautomationoverview.md)
