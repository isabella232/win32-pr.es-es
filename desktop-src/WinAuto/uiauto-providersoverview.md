---
title: Información general sobre proveedores de UI Automation
description: En este tema se proporciona información general sobre cómo los desarrolladores de controles implementan Automatización de la interfaz de usuario proveedores.
ms.assetid: 8928c889-0e0a-439f-87e8-a9d121fcf73f
keywords:
- Automatización de la interfaz de usuario,introducción a los proveedores
- Automatización de la interfaz de usuario, tipos de proveedor
- Automatización de la interfaz de usuario,conceptos del proveedor
- providers,about
- providers,types
- providers,concepts
- providers,elements
- providers,navigation
- providers,views
- providers,frameworks
- providers,fragments
- providers,hosts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f70a806fe33b16eed2555c123cc50f1f2b28da
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569725"
---
# <a name="ui-automation-providers-overview"></a>Información general sobre proveedores de UI Automation

Un proveedor Automatización de la interfaz de usuario microsoft es un objeto de software que expone un elemento de la interfaz de usuario de una aplicación para que las aplicaciones cliente de accesibilidad puedan recuperar información sobre el elemento e invocar su funcionalidad. En general, cada control u otro elemento distinto de una interfaz de usuario tiene un proveedor.

Microsoft incluye un proveedor para cada uno de los controles estándar que se proporcionan con Microsoft Win32, Windows Forms y Windows Presentation Foundation (WPF). Esto significa que los controles estándar se exponen automáticamente a Automatización de la interfaz de usuario cliente; no es necesario implementar ninguna interfaz de accesibilidad para los controles estándar.

Si la aplicación incluye controles personalizados, debe implementar proveedores de Automatización de la interfaz de usuario para esos controles para que puedan ser accesibles para las aplicaciones cliente de accesibilidad. También debe implementar proveedores para los controles de terceros que no incluyan un proveedor. Para implementar un proveedor, implemente Automatización de la interfaz de usuario interfaces de proveedor e interfaces de patrón de control.

En este tema se proporciona información general sobre cómo los desarrolladores de controles implementan Automatización de la interfaz de usuario proveedores. Incluye las secciones siguientes.

-   [Tipos de proveedores](#types-of-providers)
-   [Conceptos del proveedor de la automatización de la interfaz de usuario](#ui-automation-provider-concepts)
    -   [Elementos](#elements)
    -   [Marcos de trabajo](#frameworks)
    -   [Fragmentos](#fragments)
    -   [Hosts](#hosts)
-   [Temas relacionados](#related-topics)

## <a name="types-of-providers"></a>Tipos de proveedores

Automatización de la interfaz de usuario se divide en dos categorías: proveedores del lado servidor y proveedores de cliente *(o proxy).*

Un proveedor del lado servidor es un objeto, como un control personalizado, que contiene su propia implementación nativa de las interfaces de proveedor de Automatización de la interfaz de usuario correspondientes. Un proveedor del lado servidor se comunica con las aplicaciones cliente a través del límite del proceso mediante la exposición de su implementación de las interfaces de proveedor al núcleo Automatización de la interfaz de usuario, que los servicios solicitan a los clientes. Para obtener más información sobre los proveedores del lado servidor, vea [Implementing a Server-Side Automatización de la interfaz de usuario Provider](uiauto-serversideprovider.md).

Un proveedor del lado cliente, o proxy, es un objeto que implementa interfaces de proveedor de Automatización de la interfaz de usuario en nombre de un control no incluye una implementación de proveedor completa propia. Sin un proxy, este control es en gran medida opaco para Automatización de la interfaz de usuario, que solo puede proporcionar información básica disponible desde el identificador de ventana **(HWND),** como la ubicación del control. Normalmente, los proveedores de proxy se comunican con la aplicación a través del límite del proceso mediante el envío y la recepción Windows mensajes. Para obtener más información, vea [Implementing a Client-Side (Proxy) Automatización de la interfaz de usuario Provider](uiauto-clientsideprovider.md).

## <a name="ui-automation-provider-concepts"></a>Conceptos del proveedor de la automatización de la interfaz de usuario

En esta sección se ofrecen breves explicaciones de algunos de los conceptos clave que debe entender para implementar proveedores de automatización de la interfaz de usuario.

### <a name="elements"></a>Elementos

Automatización de la interfaz de usuario elementos son partes de la interfaz de usuario ,normalmente ventanas o controles, que son visibles para Automatización de la interfaz de usuario clientes. Entre los ejemplos se incluyen ventanas de aplicación, paneles, botones, información sobre herramientas, cuadros de lista y elementos de lista.

Automatización de la interfaz de usuario los elementos se exponen a los clientes como un árbol. Automatización de la interfaz de usuario crea el árbol navegando de un elemento a otro. El proveedor habilita la navegación para cada elemento. Cada elemento puede apuntar a su propio elemento primario, sus elementos relacionados y sus primeros y últimos elementos secundarios.

Un cliente puede ver el Automatización de la interfaz de usuario en tres vistas principales, como se describe en la tabla siguiente:



| Ver         | Descripción                                                    |
|--------------|----------------------------------------------------------------|
| Vista sin formato     | Incluye todos los elementos.                                         |
| Vista de control | Incluye elementos que son controles.                           |
| Vista de contenido | Incluye elementos de control que transmiten información al usuario. |



 

Es responsabilidad de la implementación del proveedor definir un elemento como un elemento de contenido o un elemento de control. Los elementos de control pueden o no ser elementos de contenido, pero todos los elementos de contenido son elementos de control.

Para obtener más información sobre la vista de cliente del árbol, [vea información general Automatización de la interfaz de usuario árbol de datos](uiauto-treeoverview.md).

### <a name="frameworks"></a>Marcos de trabajo

Un marco de trabajo es un componente que administra controles secundarios, pruebas de aciertos y representación en un área de la pantalla. Por ejemplo, una ventana de Win32, a menudo denominada **HWND**, puede actuar como un marco que contiene varios elementos Automatización de la interfaz de usuario, como una barra de menús, una barra de estado y botones.

Los controles de contenedor de Win32, como los cuadros de lista y los controles de vista de árbol, se consideran marcos porque contienen su propio código para representar elementos secundarios y realizar pruebas de acceso en ellos. Por el contrario, un cuadro de lista de WPF no es un marco de trabajo, ya que la ventana de contenido controla la representación y las pruebas de acceso.

La interfaz de usuario de una aplicación se puede crear con marcos diferentes. Por ejemplo, un **HWND** en una aplicación podría contener HTML dinámico (DHTML) que, a su vez, puede contener un componente como un cuadro combinado en **un HWND**.

### <a name="fragments"></a>Fragments

Un subárbol completo de elementos de un marco determinado se denomina fragmento. El elemento del nodo raíz del subárbol se denomina raíz del fragmento. Una raíz de fragmento no tiene un elemento primario, pero se hospeda en algún otro marco, normalmente una ventana win32 **(HWND).**

### <a name="hosts"></a>Hosts

El nodo raíz de cada fragmento debe hospedarse en un elemento, normalmente una ventana win32 **(HWND).** La excepción es el escritorio, que no se hospeda en ningún otro elemento. El host de un control personalizado es el **HWND** del propio control, no la ventana de aplicación ni ninguna otra ventana que pueda contener grupos de controles de nivel superior.

El host de un fragmento desempeña un papel importante a la hora de proporcionar Automatización de la interfaz de usuario servicios. Permite la navegación a la raíz del fragmento y ofrece algunas propiedades predeterminadas para que el proveedor personalizado no tenga que implementarlas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Implementar un proveedor de Client-Side Automatización de la interfaz de usuario de datos](uiauto-clientsideprovider.md)
</dt> <dt>

[Implementar un proveedor de Server-Side Automatización de la interfaz de usuario de datos](uiauto-serversideprovider.md)
</dt> <dt>

[Información general sobre el árbol de la UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 




