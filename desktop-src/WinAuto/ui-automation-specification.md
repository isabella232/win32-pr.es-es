---
title: Especificación de UI Automation
description: En este tema se proporciona información general sobre la especificación de la automatización de la interfaz de usuario de Microsoft, que constituye la base de la implementación de Windows de la automatización de la interfaz de usuario.
ms.assetid: 45160767-09b0-4fd1-bd73-bc5ac0e6f75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d3cbb7ed2caa49e855b25f749820de8cf24f1e9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077995"
---
# <a name="ui-automation-specification"></a>Especificación de UI Automation

En este tema se proporciona información general sobre la especificación de la automatización de la interfaz de usuario de Microsoft, que constituye la base de la implementación de Windows de la automatización de la interfaz de usuario. La especificación de automatización de la interfaz de usuario se puede admitir en plataformas distintas de Microsoft Windows. Para obtener más información, consulte [UI Automation Specification](./uiauto-specandcommunitypromise.md) .

Este tema contiene las siguientes secciones:

-   [Introducton](#introducton)
-   [Elementos de UI Automation](#ui-automation-elements)
-   [Árbol de UI Automation](#ui-automation-tree)
-   [Propiedades de UI Automation](#ui-automation-properties)
-   [Patrones de control de UI Automation](#ui-automation-control-patterns)
-   [Tipos de control de UI Automation](#ui-automation-control-types)
-   [Eventos de UI Automation](#ui-automation-events)
-   [Temas relacionados](#related-topics)

## <a name="introducton"></a>Introducton

La especificación de automatización de la interfaz de usuario proporciona acceso mediante programación flexible a los elementos de la interfaz de usuario del escritorio de Windows, lo que permite que los productos de tecnología de asistencia, como lectores de pantalla, proporcionen información sobre la interfaz de usuario a los usuarios finales y manipulen la interfaz de usuario por medio de la entrada estándar.

La automatización de la interfaz de usuario es más amplia en el ámbito que solo una definición de interfaz. Proporciona:

-   Modelo de objetos y funciones que facilitan que las aplicaciones cliente reciban eventos, recuperen valores de propiedad y manipulen elementos de la interfaz de usuario.
-   Una infraestructura básica para buscar y obtener los límites de los procesos.
-   Un conjunto de interfaces para que los proveedores expresen la estructura de árbol, las propiedades generales y la funcionalidad de los elementos de la interfaz de usuario.
-   Propiedad "tipo de control" que permite a los clientes y proveedores indicar claramente las propiedades comunes, la funcionalidad y la estructura de un objeto de interfaz de usuario.

La automatización de la interfaz de usuario mejora en Microsoft Active Accessibility por:

-   Habilitación eficaz de clientes fuera de proceso, a la vez que continúa permitiendo el acceso en proceso.
-   Exponer más información sobre la interfaz de usuario de forma que permita que los clientes estén fuera de proceso.
-   Coexistencia con y aprovechando Microsoft Active Accessibility sin heredar sus limitaciones. Para obtener más información, vea [comparación de Microsoft Active Accessibility y UI Automation](microsoft-active-accessibility-and-ui-automation-compared.md).
-   Proporcionar una alternativa a [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que sea fácil de implementar.

La implementación de la especificación de automatización de la interfaz de usuario en las características de Windows interfaces basadas en el modelo de objetos componentes (COM) y las interfaces administradas.

## <a name="ui-automation-elements"></a>Elementos de UI Automation

La automatización de la interfaz de usuario expone cada parte de la interfaz de usuario a las aplicaciones cliente como un *elemento de automatización*. Los proveedores proporcionan valores de propiedad para cada elemento. Los elementos se exponen como una estructura de árbol, con el escritorio como el elemento raíz.

Los elementos de automatización exponen propiedades comunes de los elementos de la interfaz de usuario que representan. Una de estas propiedades es el tipo de control, que describe su apariencia básica y su funcionalidad (por ejemplo, un botón o una casilla).

## <a name="ui-automation-tree"></a>Árbol de UI Automation

El árbol de automatización de la interfaz de usuario representa la interfaz de usuario completa: el elemento raíz es el escritorio actual y los elementos secundarios son ventanas de la aplicación. Cada uno de estos elementos secundarios puede contener elementos que representan menús, botones, barras de herramientas, etc. Estos elementos a su vez pueden contener elementos como elementos de lista, como se muestra en la ilustración siguiente.

![captura de pantalla que muestra el árbol de UI Automation](images/uiatree.gif)

Tenga en cuenta que el orden de los elementos del mismo nivel en el árbol de automatización de la interfaz de usuario es muy importante. Los objetos que se encuentran junto a otros visualmente deberían estar también próximos entre sí en el árbol de automatización de la interfaz de usuario.

Los proveedores de automatización de la interfaz de usuario para un control determinado admiten la navegación entre los elementos secundarios de ese control. Sin embargo, los proveedores no están preocupados por la navegación entre estos subárboles de control. Se administra mediante el núcleo de automatización de la interfaz de usuario, usando la información de los proveedores de ventanas predeterminados.

Para ayudar a los clientes a procesar la información de la interfaz de usuario de forma más eficaz, el marco de trabajo admite vistas alternativas del árbol de automatización: vista sin formato, vista de control y vista de contenido. Como se muestra en la tabla siguiente, el tipo de filtrado determina las vistas y el cliente define el ámbito de una vista.



| Árbol de automatización | Descripción                                                                                                             |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| Vista sin formato        | Árbol completo de objetos de elemento de automatización para los que el escritorio es la raíz.                                          |
| Vista de control    | Subconjunto de la vista sin formato que se asigna estrechamente a la estructura de la interfaz de usuario cuando el usuario la percibe.                                |
| Vista de contenido    | Subconjunto de la vista de control que contiene el contenido más relevante para el usuario, como los valores de un cuadro combinado desplegable. |



 

Para obtener más información, vea [UI Automation Tree Overview](uiauto-treeoverview.md).

## <a name="ui-automation-properties"></a>Propiedades de UI Automation

La especificación de automatización de la interfaz de usuario define dos tipos de propiedades: propiedades de elemento de automatización y propiedades de patrón de control. Las propiedades del elemento de automatización se aplican a la mayoría de los controles, lo que proporciona información fundamental sobre el elemento, como su nombre. Las propiedades del patrón de control se aplican a los patrones de control, que se describen a continuación.

A diferencia de Microsoft Active Accessibility, todas las propiedades de automatización de la interfaz de usuario se identifican mediante un GUID y un nombre de programación, lo que facilita la introducción de nuevas propiedades.

Para obtener más información, consulta [UI Automation Properties Overview](uiauto-propertiesoverview.md).

## <a name="ui-automation-control-patterns"></a>Patrones de control de UI Automation

Un patrón de control describe un aspecto concreto de la funcionalidad de un elemento de automatización. Por ejemplo, un sencillo control "click-puede" como un botón o hipervínculo debe admitir el patrón de control Invoke para representar la acción "click".

Cada patrón de control es una representación canónica de posibles características y funciones de la interfaz de usuario. La implementación actual de la automatización de la interfaz de usuario define 22 patrones de control. La API de automatización de Windows también puede admitir patrones de control personalizados. A diferencia de las propiedades de rol o estado de Microsoft Active Accessibility, un elemento de automatización puede admitir varios patrones de control de automatización de la interfaz de usuario.

Para obtener más información, consulta [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

## <a name="ui-automation-control-types"></a>Tipos de control de UI Automation

Un tipo de control es una propiedad de elemento de automatización que especifica un control conocido que el elemento representa. Actualmente, la automatización de la interfaz de usuario define los tipos de control de 38, incluidos los botones, casillas, ComboBox, DataGrid, documento, hipervínculo, imagen, información sobre herramientas, árbol y ventana.

Antes de poder asignar un tipo de control a un elemento, el elemento debe cumplir ciertas condiciones, como una estructura de árbol de automatización determinada, valores de propiedad, patrones de control y eventos. Sin embargo, no se limita a ello. Puede extender un control con patrones y propiedades personalizados, así como con los predefinidos.

El número total de tipos de control predefinidos es significativamente menor que los [roles de objeto](object-roles.md)de Microsoft Active Accessibility, porque los tipos de control de automatización de la interfaz de usuario se pueden combinar para expresar un conjunto mayor de características, mientras que los roles de Microsoft Active Accessibility no.

Para obtener más información, consulta [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

## <a name="ui-automation-events"></a>Eventos de UI Automation

Los eventos de automatización de la interfaz de usuario notifican a las aplicaciones los cambios y las acciones realizadas con los elementos de automatización. Hay cuatro tipos diferentes de eventos de automatización de la interfaz de usuario y no necesariamente significa que el estado visual de la interfaz de usuario ha cambiado. El modelo de eventos de automatización de la interfaz de usuario es independiente del marco [WinEvent](winevents-infrastructure.md) en Windows, aunque la API de automatización de Windows hace que los eventos de automatización de la interfaz de usuario interoperan con Microsoft Active Accessibility Framework.

Para obtener más información, consulta [UI Automation Events Overview](uiauto-eventsoverview.md).

## <a name="related-topics"></a>Temas relacionados

[Especificación de UI Automation](./uiauto-specandcommunitypromise.md), [información general sobre la API de automatización de Windows](windows-automation-api-overview.md)