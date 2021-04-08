---
title: Información general sobre proveedores de UI Automation
description: En este tema se proporciona información general sobre cómo los desarrolladores de controles implementan proveedores de automatización de la interfaz de usuario.
ms.assetid: 8928c889-0e0a-439f-87e8-a9d121fcf73f
keywords:
- Automatización de la interfaz de usuario, información general de proveedores
- Automatización de la interfaz de usuario, tipos de proveedor
- Automatización de la interfaz de usuario, conceptos del proveedor
- proveedores, acerca de
- proveedores, tipos
- proveedores, conceptos
- proveedores, elementos
- proveedores, navegación
- proveedores, vistas
- proveedores, marcos de trabajo
- proveedores, fragmentos
- proveedores, hosts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f70a806fe33b16eed2555c123cc50f1f2b28da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994111"
---
# <a name="ui-automation-providers-overview"></a>Información general sobre proveedores de UI Automation

Un proveedor de automatización de la interfaz de usuario de Microsoft es un objeto de software que expone un elemento de la interfaz de usuario de una aplicación para que las aplicaciones cliente de accesibilidad puedan recuperar información sobre el elemento e invocar su funcionalidad. En general, cada control u otro elemento distinto de una interfaz de usuario tiene un proveedor.

Microsoft incluye un proveedor para cada uno de los controles estándar que se proporcionan con Microsoft Win32, Windows Forms y Windows Presentation Foundation (WPF). Esto significa que los controles estándar se exponen automáticamente a los clientes de automatización de la interfaz de usuario; no es necesario implementar ninguna interfaz de accesibilidad para los controles estándar.

Si su aplicación incluye controles personalizados, debe implementar proveedores de automatización de la interfaz de usuario para esos controles para que puedan tener acceso a ellos las aplicaciones cliente de accesibilidad. También debe implementar proveedores para cualquier control de terceros que no incluya un proveedor. Para implementar un proveedor, implemente interfaces del proveedor de automatización de la interfaz de usuario e interfaces de patrón de control.

En este tema se proporciona información general sobre cómo los desarrolladores de controles implementan proveedores de automatización de la interfaz de usuario. Incluye las siguientes secciones.

-   [Tipos de proveedores](#types-of-providers)
-   [Conceptos del proveedor de la automatización de la interfaz de usuario](#ui-automation-provider-concepts)
    -   [Elementos](#elements)
    -   [Marcos de trabajo](#frameworks)
    -   [Fragmentos](#fragments)
    -   [Hosts](#hosts)
-   [Temas relacionados](#related-topics)

## <a name="types-of-providers"></a>Tipos de proveedores

Los proveedores de automatización de la interfaz de usuario se dividen en dos categorías: proveedores del lado servidor y proveedores del lado cliente (o *proxy*).

Un proveedor del lado servidor es un objeto, como un control personalizado, que contiene su propia implementación nativa de las interfaces relevantes del proveedor de automatización de la interfaz de usuario. Un proveedor del lado servidor se comunica con las aplicaciones cliente a través del límite del proceso al exponer su implementación de las interfaces del proveedor al núcleo de automatización de la interfaz de usuario, que ofrece servicio a las solicitudes de los clientes. Para obtener más información sobre los proveedores del lado servidor, vea [implementar un Server-Side proveedor de automatización de la interfaz de usuario](uiauto-serversideprovider.md).

Un proveedor del lado cliente, o proxy, es un objeto que implementa las interfaces del proveedor de automatización de la interfaz de usuario en nombre de un control, no incluye una implementación de proveedor completa propia. Sin un proxy, este tipo de control es principalmente opaco a la automatización de la interfaz de usuario, que puede proporcionar solo información básica disponible en el identificador de ventana (**hWnd**), como la ubicación del control. Normalmente, los proveedores de proxy se comunican con la aplicación a través del límite del proceso mediante el envío y la recepción de mensajes de Windows. Para obtener más información, vea [implementar un proveedor de automatización de la interfaz de usuario de Client-Side (proxy)](uiauto-clientsideprovider.md).

## <a name="ui-automation-provider-concepts"></a>Conceptos del proveedor de la automatización de la interfaz de usuario

En esta sección se ofrecen breves explicaciones de algunos de los conceptos clave que debe entender para implementar proveedores de automatización de la interfaz de usuario.

### <a name="elements"></a>Elementos

Los elementos de automatización de la interfaz de usuario son partes de la interfaz de usuario, normalmente ventanas o controles, que son visibles para los clientes de automatización de la interfaz de usuario. Entre los ejemplos se incluyen ventanas de aplicación, paneles, botones, información sobre herramientas, cuadros de lista y elementos de lista.

Los elementos de automatización de la interfaz de usuario se exponen a los clientes como un árbol. La automatización de la interfaz de usuario construye el árbol navegando de un elemento a otro. El proveedor habilita la navegación para cada elemento. Cada elemento puede apuntar a su propio elemento primario, sus elementos relacionados y su primer y último elemento secundario.

Un cliente puede ver el árbol de automatización de la interfaz de usuario en tres vistas principales, como se describe en la tabla siguiente:



| Ver         | Descripción                                                    |
|--------------|----------------------------------------------------------------|
| Vista sin formato     | Incluye todos los elementos.                                         |
| Vista de control | Incluye elementos que son controles.                           |
| Vista de contenido | Incluye elementos de control que transmiten información al usuario. |



 

Es responsabilidad de la implementación del proveedor definir un elemento como un elemento de contenido o un elemento de control. Los elementos de control pueden o no ser elementos de contenido, pero todos los elementos de contenido son elementos de control.

Para obtener más información sobre la vista de cliente del árbol, vea [UI Automation Tree Overview](uiauto-treeoverview.md).

### <a name="frameworks"></a>Marcos de trabajo

Un marco de trabajo es un componente que administra controles secundarios, pruebas de aciertos y representación en un área de la pantalla. Por ejemplo, una ventana de Win32, que a menudo se conoce como **hWnd**, puede actuar como un marco de trabajo que contiene varios elementos de automatización de la interfaz de usuario, como una barra de menús, una barra de estado y botones.

Los controles de contenedor de Win32, como los cuadros de lista y los controles de vista de árbol, se consideran marcos de trabajo porque contienen su propio código para representar elementos secundarios y realizar pruebas de aciertos en ellos. Por el contrario, un cuadro de lista de WPF no es un marco de trabajo, porque la representación y las pruebas de aciertos se controlan mediante la ventana contenedora.

La interfaz de usuario de una aplicación se puede componer de diferentes marcos de trabajo. Por ejemplo, un **hWnd** en una aplicación podría contener HTML dinámico (DHTML) que a su vez puede contener un componente como un cuadro combinado en un **hWnd**.

### <a name="fragments"></a>Fragments

Un subárbol completo de elementos de un marco de trabajo determinado se denomina fragmento. El elemento del nodo raíz del subárbol se denomina raíz del fragmento. Una raíz de fragmento no tiene un elemento primario, pero se hospeda en otro marco de trabajo, normalmente una ventana Win32 (**hWnd**).

### <a name="hosts"></a>Hosts

El nodo raíz de cada fragmento se debe hospedar en un elemento, normalmente una ventana Win32 (**hWnd**). La excepción es el escritorio, que no se hospeda en ningún otro elemento. El host de un control personalizado es el **hWnd** del propio control, no la ventana de la aplicación o cualquier otra ventana que pueda contener grupos de controles de nivel superior.

El host de un fragmento desempeña un papel importante en el suministro de servicios de automatización de la interfaz de usuario. Permite la navegación a la raíz del fragmento y ofrece algunas propiedades predeterminadas para que el proveedor personalizado no tenga que implementarlas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Implementar un proveedor de automatización de la interfaz de usuario de Client-Side](uiauto-clientsideprovider.md)
</dt> <dt>

[Implementar un proveedor de automatización de la interfaz de usuario de Server-Side](uiauto-serversideprovider.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 




