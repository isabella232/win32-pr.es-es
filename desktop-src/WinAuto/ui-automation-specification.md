---
title: Automatización de la interfaz de usuario especificación
description: En este tema se proporciona información general sobre la especificación de Automatización de la interfaz de usuario Microsoft, que constituye la base de la Windows implementación de Automatización de la interfaz de usuario.
ms.assetid: 45160767-09b0-4fd1-bd73-bc5ac0e6f75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fc07b70128a401d48813ded68c31dfcfca5bb5a49d2ca46683e9a902af003ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325106"
---
# <a name="ui-automation-specification"></a>Automatización de la interfaz de usuario especificación

En este tema se proporciona información general sobre la especificación de Automatización de la interfaz de usuario Microsoft, que constituye la base de la Windows implementación de Automatización de la interfaz de usuario. La especificación Automatización de la interfaz de usuario puede ser compatible con otras plataformas que no sean Microsoft Windows. Para obtener más información, vea [Automatización de la interfaz de usuario especificación.](./uiauto-specandcommunitypromise.md)

Este tema contiene las siguientes secciones:

-   [Introducton](#introducton)
-   [Automatización de la interfaz de usuario elements](#ui-automation-elements)
-   [Automatización de la interfaz de usuario árbol](#ui-automation-tree)
-   [Automatización de la interfaz de usuario propiedades](#ui-automation-properties)
-   [Patrones de control de UI Automation](#ui-automation-control-patterns)
-   [Tipos de control de UI Automation](#ui-automation-control-types)
-   [Automatización de la interfaz de usuario eventos](#ui-automation-events)
-   [Temas relacionados](#related-topics)

## <a name="introducton"></a>Introducton

La especificación de Automatización de la interfaz de usuario proporciona acceso flexible mediante programación a los elementos de la interfaz de usuario en el escritorio de Windows, lo que permite que los productos de tecnología de asistencia, como los lectores de pantalla, proporcionen información sobre la interfaz de usuario a los usuarios finales y manipulen la interfaz de usuario por medios distintos de la entrada estándar.

Automatización de la interfaz de usuario es más amplio en el ámbito que solo una definición de interfaz. Proporciona:

-   Un modelo de objetos y funciones que hacen que sea fácil para las aplicaciones cliente recibir eventos, recuperar valores de propiedad y manipular elementos de la interfaz de usuario.
-   Una infraestructura básica para buscar y capturar a través de los límites del proceso.
-   Conjunto de interfaces para que los proveedores expresen la estructura de árbol, las propiedades generales y la funcionalidad de los elementos de la interfaz de usuario.
-   Propiedad de "tipo de control" que permite a los clientes y proveedores indicar claramente las propiedades comunes, la funcionalidad y la estructura de un objeto de interfaz de usuario.

Automatización de la interfaz de usuario mejora el rendimiento Microsoft Active Accessibility:

-   Habilitación de clientes fuera de proceso eficaces, a la vez que se sigue permitiendo el acceso en proceso.
-   Exponer más información sobre la interfaz de usuario de forma que permita a los clientes estar fuera de proceso.
-   Coexistir con y aprovechar Microsoft Active Accessibility sin heredar sus limitaciones. Para obtener más información, [vea Microsoft Active Accessibility y Automatización de la interfaz de usuario Comparado.](microsoft-active-accessibility-and-ui-automation-compared.md)
-   Proporcionar una alternativa a [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que sea fácil de implementar.

La implementación de la especificación Automatización de la interfaz de usuario en Windows interfaces basadas en el Modelo de objetos componentes (COM) e interfaces administradas.

## <a name="ui-automation-elements"></a>Automatización de la interfaz de usuario elements

Automatización de la interfaz de usuario expone cada parte de la interfaz de usuario a las aplicaciones cliente como un *elemento de automatización*. Los proveedores suministran valores de propiedad para cada elemento. Los elementos se exponen como una estructura de árbol, con el escritorio como elemento raíz.

Los elementos de Automation exponen propiedades comunes de los elementos de la interfaz de usuario que representan. Una de estas propiedades es el tipo de control , que describe su apariencia y funcionalidad básicas (por ejemplo, un botón o una casilla).

## <a name="ui-automation-tree"></a>Automatización de la interfaz de usuario árbol

El Automatización de la interfaz de usuario representa toda la interfaz de usuario: el elemento raíz es el escritorio actual y los elementos secundarios son ventanas de aplicación. Cada uno de estos elementos secundarios puede contener elementos que representan menús, botones, barras de herramientas, y así sucesivamente. A su vez, estos elementos pueden contener elementos como elementos de lista, como se muestra en la ilustración siguiente.

![captura de pantalla que muestra el árbol de automatización de la interfaz de usuario](images/uiatree.gif)

Tenga en cuenta que el orden de los elementos del mismo nivel en Automatización de la interfaz de usuario árbol es bastante importante. Los objetos que están juntos visualmente también deben estar juntos entre sí en el Automatización de la interfaz de usuario árbol.

Automatización de la interfaz de usuario para un control determinado admiten la navegación entre los elementos secundarios de ese control. Sin embargo, a los proveedores no les preocupa la navegación entre estos subárquidos de control. Esto se administra mediante el núcleo Automatización de la interfaz de usuario, utilizando la información de los proveedores de ventana predeterminados.

Para ayudar a los clientes a procesar la información de la interfaz de usuario de forma más eficaz, el marco admite vistas alternativas del árbol de automatización: vista sin formato, vista de control y vista de contenido. Como se muestra en la tabla siguiente, el tipo de filtrado determina las vistas y el cliente define el ámbito de una vista.



| Árbol de Automation | Descripción                                                                                                             |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| Vista sin formato        | Árbol completo de objetos de elementos de automatización para los que el escritorio es la raíz.                                          |
| Vista de control    | Subconjunto de la vista sin procesar que se asigna estrechamente a la estructura de la interfaz de usuario a medida que el usuario la percibe.                                |
| Vista de contenido    | Subconjunto de la vista de control que contiene el contenido más relevante para el usuario, como los valores de un cuadro combinado desplegable. |



 

Para obtener más información, [vea información general Automatización de la interfaz de usuario árbol de árbol.](uiauto-treeoverview.md)

## <a name="ui-automation-properties"></a>Automatización de la interfaz de usuario propiedades

La Automatización de la interfaz de usuario especificación define dos tipos de propiedades: propiedades de elementos de automatización y propiedades de patrón de control. Las propiedades de elementos de Automation se aplican a la mayoría de los controles, lo que proporciona información fundamental sobre el elemento, como su nombre. Las propiedades del patrón de control se aplican a los patrones de control, que se describen a continuación.

A diferencia de Microsoft Active Accessibility, cada Automatización de la interfaz de usuario propiedad se identifica mediante un GUID y un nombre de programación, lo que facilita la introducción de nuevas propiedades.

Para obtener más información, consulta [UI Automation Properties Overview](uiauto-propertiesoverview.md).

## <a name="ui-automation-control-patterns"></a>Patrones de control de UI Automation

Un patrón de control describe un aspecto determinado de la funcionalidad de un elemento de automatización. Por ejemplo, un control simple "con capacidad de clic", como un botón o hipervínculo, debe admitir el patrón de control Invoke para representar la acción de "clic".

Cada patrón de control es una representación canónica de las posibles funciones y características de la interfaz de usuario. La implementación actual de Automatización de la interfaz de usuario define 22 patrones de control. La WINDOWS Automation API también puede admitir patrones de control personalizados. A Microsoft Active Accessibility propiedades de estado o rol, un elemento de automatización puede admitir varios Automatización de la interfaz de usuario de control.

Para obtener más información, consulta [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

## <a name="ui-automation-control-types"></a>Tipos de control de UI Automation

Un tipo de control es una propiedad de elemento de automatización que especifica un control conocido que el elemento representa. Actualmente, Automatización de la interfaz de usuario define treinta y ocho tipos de control, incluidos Button, CheckBox, ComboBox, DataGrid, Document, Hyperlink, Image, ToolTip, Tree y Window.

Para poder asignar un tipo de control a un elemento, el elemento debe cumplir ciertas condiciones, incluida una estructura de árbol de automatización determinada, valores de propiedad, patrones de control y eventos. Sin embargo, no se limita a estos. Puede extender un control con patrones y propiedades personalizados, así como con los predefinidos.

El número total de tipos de control predefinidos es significativamente inferior Microsoft Active Accessibility los [roles](object-roles.md)de objeto , ya que los tipos de control de Automatización de la interfaz de usuario se pueden combinar para expresar un conjunto mayor de características, Microsoft Active Accessibility los roles no.

Para obtener más información, consulta [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

## <a name="ui-automation-events"></a>Automatización de la interfaz de usuario eventos

Automatización de la interfaz de usuario eventos notifican a las aplicaciones los cambios en y las acciones realizadas con elementos de automatización. Hay cuatro tipos diferentes de eventos Automatización de la interfaz de usuario y no significan necesariamente que el estado visual de la interfaz de usuario haya cambiado. El Automatización de la interfaz de usuario de eventos de Automatización de la interfaz de usuario es independiente del marco [WinEvent](winevents-infrastructure.md) en Windows, aunque la API de automatización de Windows hace que Automatización de la interfaz de usuario eventos interoperables con el marco Microsoft Active Accessibility.

Para obtener más información, consulta [UI Automation Events Overview](uiauto-eventsoverview.md).

## <a name="related-topics"></a>Temas relacionados

[Automatización de la interfaz de usuario specification ,](./uiauto-specandcommunitypromise.md)información [general Windows API de Automation](windows-automation-api-overview.md)