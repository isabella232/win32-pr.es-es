---
title: SemanticZoom (tipo de control)
description: En este tema se proporciona información sobre la compatibilidad de UI Automation para el tipo de control SemanticZoom.
ms.assetid: 37C14610-431F-46BF-97B6-CB476EA1642D
keywords:
- Automatización de la interfaz de usuario, compatibilidad con el tipo de control SemanticZoom
- Automatización de la interfaz de usuario, tipo de control SemanticZoom
- Automatización de la interfaz de usuario, estructura de árbol para el tipo de control SemanticZoom
- Automatización de la interfaz de usuario, propiedades para el tipo de control SemanticZoom
- Automatización de la interfaz de usuario, patrones de control para el tipo de control SemanticZoom
- Automatización de la interfaz de usuario, eventos para el tipo de control SemanticZoom
- estructuras de árbol, tipo de control SemanticZoom
- propiedades, tipo de control SemanticZoom
- patrones de control, tipo de control SemanticZoom
- Events, tipo de control SemanticZoom
- compatibilidad con el tipo de control SemanticZoom
- SemanticZoom (tipo de control)
- tipos de control, estructura de árbol para el tipo de control SemanticZoom
- tipos de control, patrones de control para el tipo de control SemanticZoom
- tipos de control, compatibilidad con SemanticZoom
- tipos de control, SemanticZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17d4712aa4f10489081b1b5d0f69fed849080bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149294"
---
# <a name="semanticzoom-control-type"></a>SemanticZoom (tipo de control)

En este tema se proporciona información sobre la compatibilidad de UI Automation para el tipo de control **SemanticZoom** .

El zoom semántico es una técnica introducida en Windows 8 para presentar y navegar por grandes conjuntos de datos o contenido relacionados en una sola vista, como un álbum de fotos, una lista de aplicaciones o una libreta de direcciones. El zoom semántico usa dos modos distintos de clasificación, o *niveles de zoom*, para organizar y presentar el contenido. El modo de bajo nivel (o *de zoom en*) muestra los elementos en una estructura plana "todo arriba"; y el modo de alto nivel (o *alejado*) muestra los elementos en grupos, lo que permite al usuario navegar rápidamente por el contenido y desplazarse por él. Por ejemplo, la ampliación de una lista de ciudades podría cambiar a una lista de Estados que contengan esas ciudades. La ampliación de una lista de programas podría cambiar a una lista de grupos de programas lógicos.

Para obtener más información sobre el zoom semántico específicamente tal como se usa para las aplicaciones de la tienda Windows, consulte [directrices para el zoom semántico](/windows/uwp/controls-and-patterns/semantic-zoom).

El modelo de uso para el tipo de control **SemanticZoom** es inusual en que existe principalmente para el acceso mediante programación. Los clientes de automatización de la interfaz de usuario de Microsoft pueden supervisar y manipular el control de zoom semántico para controlar el estado de la lista. Los usuarios que no usan la tecnología de asistencia normalmente manipulan el control de zoom semántico directamente a través de gestos táctiles o métodos abreviados de teclado.

En las secciones siguientes se definen la estructura de árbol de automatización de la interfaz de usuario necesaria, las propiedades, los patrones de control y los eventos para el tipo de control **SemanticZoom** . Los requisitos de automatización de la interfaz de usuario se aplican a todos los controles semánticos de zoom en los que la plataforma o marco de interfaz de usuario integra la compatibilidad de UI Automation con los tipos de control y

En este tema se incluyen las siguientes secciones.

-   [Estructura de árbol típica](#typical-tree-structure)
-   [Propiedades relevantes](#relevant-properties)
-   [Patrones de control y propiedades necesarios](#required-control-patterns-and-properties)
-   [Eventos necesarios](#required-events)
-   [Comentarios:](#remarks)
-   [Temas relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estructura de árbol típica

En la tabla siguiente se describe un control y una vista de contenido típicos del árbol de automatización de la interfaz de usuario que pertenece al tipo de control **SemanticZoom** y se describe lo que puede incluirse en cada vista. Para obtener más información sobre el árbol de automatización de la interfaz de usuario, vea [UI Automation Tree Overview](uiauto-treeoverview.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Vista de control</th>
<th>Vista de contenido</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>List
<ul>
<li>SemanticZoom
<ul>
<li>Elemento de lista (0 o más)</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>List
<ul>
<li>Elemento de lista (0 o más)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

O:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Vista de control</th>
<th>Vista de contenido</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>SemanticZoom
<ul>
<li>List
<ul>
<li>Elemento de lista (0 o más)</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>List
<ul>
<li>Elemento de lista (0 o más)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propiedades relevantes

En la tabla siguiente se enumeran las propiedades de automatización de la interfaz de usuario cuyo valor o definición es especialmente relevante para los controles que implementan el tipo de control **SemanticZoom** . Para obtener más información sobre las propiedades de automatización de la interfaz de usuario, vea [recuperar propiedades de elementos de UI Automation](uiauto-propertiesforclients.md).



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Propiedad de automatización de interfaz de usuario</th>
<th>Value</th>
<th>Notas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_AutomationIdPropertyId</strong></a></td>
<td>Vea las notas.</td>
<td>El valor de esta propiedad debe ser único entre todos los elementos del mismo nivel en la vista sin formato del árbol de automatización de la interfaz de usuario.</td>
</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a></td>
<td>Vea las notas.</td>
<td>El rectángulo exterior que contiene el control completo.</td>
</tr>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a></td>
<td>Vea las notas.</td>
<td>Si el control de lista tiene un punto seleccionable (un punto en el que se puede hacer clic para que la lista tenga el foco), dicho punto se debe exponer a través de esta propiedad. Si el valor de la propiedad <a href="uiauto-automation-element-propids.md"><strong>UIA_IsOffscreenPropertyId</strong></a> es <strong>true</strong>, el intento de recuperar esta propiedad produce el error de <a href="uiauto-error-codes.md"><strong>UIA_E_NOCLICKABLEPOINT</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_ControlTypePropertyId</strong></a></td>
<td><strong>SemanticZoom</strong></td>

</tr>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_IsContentElementPropertyId</strong></a></td>
<td>TRUE</td>

</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_IsControlElementPropertyId</strong></a></td>
<td>TRUE</td>

</tr>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_IsKeyboardFocusablePropertyId</strong></a></td>
<td>false</td>

</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_LabeledByPropertyId</strong></a></td>
<td>Vea las notas.</td>
<td>Si hay una etiqueta de texto estático, esta propiedad debe exponer una referencia a ese control.</td>
</tr>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a></td>
<td>Vea las notas.</td>
<td>Cadena localizada que corresponde al tipo de control <strong>SemanticZoom</strong> . El valor predeterminado es el &quot; zoom semántico &quot; para en-US o inglés (Estados Unidos).
<blockquote>
[!Note]<br />
Algunos Marcos concatenaron esto como &quot; semanticzoom &quot; .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a></td>
<td>Vea las notas.</td>
<td>Una cadena vacía es aceptable, o se puede proporcionar un nombre más útil, siempre y cuando no contenga el término zoom semántico, lo que haría que la combinación de tipo de control y el nombre resulten confusas.</td>
</tr>
</tbody>
</table>



 

## <a name="required-control-patterns-and-properties"></a>Patrones de control y propiedades necesarios

En la tabla siguiente se enumeran los patrones de control de automatización de la interfaz de usuario que se deben admitir por todos los controles semánticos de zoom. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Patrón de control/Propiedad de patrón                  | Soporte técnico/valor | Notas                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | Depende       | Los controles de zoom semántico admiten el patrón de control [Toggle](uiauto-implementingtoggle.md) para permitir que el zoom se habilite o deshabilite. [**ToggleState \_ Desactivado**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) se corresponde con el estado plano, todo el activo y [**ToggleState \_ en**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corresponde a la vista alejada de alto nivel. |



 

## <a name="required-events"></a>Eventos necesarios

En la tabla siguiente se enumeran los eventos de automatización de la interfaz de usuario que deben admitir los controles de zoom semántico. Para más información sobre los eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento de automatización de la interfaz de usuario                                                                                                                   | Notas                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsEnabledPropertyId.                 | Si el control admite la propiedad [**IsEnabled**](uiauto-automation-element-propids.md) , debe admitir este evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de cambio de propiedad de IsOffscreenPropertyId.             | Si el control admite la propiedad [**IsOffscreen**](uiauto-automation-element-propids.md) , debe admitir este evento. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de cambio de propiedad de ToggleToggleStatePropertyId.    |                                                                                                                            |



 

## <a name="remarks"></a>Observaciones

Si una interfaz de usuario tiene un botón visible para alternar el comportamiento del control de zoom semántico, este botón no debe tener un tipo de control **SemanticZoom** . Esto es un contador intuitivo, pero el tipo de control **SemanticZoom** caracteriza el contenedor del contenido de zoom, no un botón que controla el zoom. (Este tipo de botón podría representarse simplemente como un tipo de control [Button](uiauto-supportbuttoncontroltype.md) con el patrón de control [Toggle](uiauto-implementingtoggle.md) ).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general sobre UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

