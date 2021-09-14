---
title: Glosario (Windows de accesibilidad)
description: Página de glosario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: c45583f2-a6e8-4a01-9577-9b604b5bbc62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16679c63f0716058e53c7c9d164a24593c481dff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070522"
---
# <a name="glossary-windows-accessibility-features"></a>Glosario (Windows de accesibilidad)

## <a name="a"></a>A

<dl> <dt>

**clave de acceso**
</dt> <dd>

Carácter subrayado en el texto de la etiqueta de un control.

</dd> <dt>

**ayuda de accesibilidad**
</dt> <dd>

También se denomina tecnología de asistencia; programas especializados que funcionan con el sistema operativo de un equipo para dar cabida a discapacidades específicas, como un intervalo limitado de movimiento o cegura. Entre los productos se incluyen teclados más grandes, teclados con mirada con los ojos, utilidades de entrada de voz, teclados en pantalla y productos que pueden convertir texto en voz o en una pantalla de Grafía dinámica. Para obtener más información, vea [Assistive Technology Products](https://www.microsoft.com/enable/at/default.aspx).

</dd> <dt>

**objeto accesible**
</dt> <dd>

Cualquier elemento de interfaz de usuario que implemente la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y tenga propiedades que describen el nombre del objeto, las ubicaciones de la pantalla y otra información necesaria para las ayuda de accesibilidad. Para obtener más información, vea [Objetos accesibles.](accessible-objects.md)

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**elemento secundario**
</dt> <dd>

Vea [*el elemento simple*](uiauto-glossary.md).

</dd> <dt>

**client**
</dt> <dd>

Cualquier programa que use Automatización de la interfaz de usuario o Microsoft Active Accessibility para acceder, identificar o manipular los elementos de la interfaz de usuario de una aplicación; los clientes incluyen ayuda de accesibilidad, herramientas de prueba automatizadas y algunas aplicaciones de entrenamiento basadas en equipos. Para obtener más información, [vea How Active Accessibility Works](how-active-accessibility-works.md).

</dd> <dt>

**proveedor del lado cliente**
</dt> <dd>

Componente de software implementado por un cliente de Automatización de la interfaz de usuario para recuperar información sobre la interfaz de usuario de una aplicación que no admite o no admite completamente Automatización de la interfaz de usuario. Normalmente, los proveedores del lado cliente (servidores proxy) se comunican con la aplicación a través del límite del proceso mediante el envío y la recepción Windows mensajes.

</dd> <dt>

**container**
</dt> <dd>

También se denomina elemento primario; un objeto accesible que corresponde a uno o varios elementos simples; Por ejemplo, un [**objeto IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para un cuadro de lista es el elemento primario de los elementos de lista.

</dd> <dt>

**patrón de control**
</dt> <dd>

En Automatización de la interfaz de usuario, una implementación de diseño que describe una parte discreta de la funcionalidad de un control. Esta funcionalidad puede incluir la apariencia visual de un control y las acciones que puede realizar.

</dd> <dt>

**objeto de patrón de control**
</dt> <dd>

Instancia en tiempo de ejecución de un objeto COM que expone una o varias interfaces de patrón de control.

</dd> <dt>

**proveedor de patrones de control**
</dt> <dd>

Componente de software que implementa una o varias interfaces de patrón de control.

</dd> <dt>

**control personalizado**
</dt> <dd>

Control creado por un usuario o proveedor de software de terceros, o un control definido por el sistema que ha modificado un usuario o un proveedor de software de terceros.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**intervalo de texto degenerado (intervalo vacío)**
</dt> <dd>

Objeto que representa un intervalo de texto vacío (de carácter cero). Un intervalo de texto degenerado tiene puntos de conexión adyacentes y especifica un punto entre dos caracteres.

</dd> <dt>

**intervalo de texto desconexo**
</dt> <dd>

Objeto que representa varios intervalos de texto que no son físicamente adyacentes entre sí.

</dd> <dt>

**contenedor de acoplamiento**
</dt> <dd>

Control que permite la organización de elementos secundarios, tanto horizontal como verticalmente, en relación con los límites del contenedor de acoplamiento y otros elementos dentro del contenedor.

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**agente de escucha de eventos**
</dt> <dd>

Una aplicación cliente que se ha registrado para recibir notificaciones de Automatización de la interfaz de usuario o Microsoft Active Accessibility cada vez que se producen cambios específicos en la interfaz de usuario.

</dd> <dt>

**notificación de eventos**
</dt> <dd>

Una llamada de un Automatización de la interfaz de usuario a un cliente, en la que el proveedor notifica al cliente de un evento que podría afectar al estado o la apariencia de un elemento de la interfaz de usuario.

</dd> </dl>

## <a name="f"></a>F

<dl> <dt>

**filtrado \[\]**
</dt> <dd>

Para definir los tipos de Automatización de la interfaz de usuario que se incluirán en una vista del Automatización de la interfaz de usuario árbol. Vea también: vista sin formato, vista de control y vista de contenido.

</dd> <dt>

**raíz del fragmento**
</dt> <dd>

Elemento Automatización de la interfaz de usuario en el nodo raíz de un subárbol del Automatización de la interfaz de usuario árbol. Una raíz de fragmento no tiene un elemento primario, pero se hospeda en algún otro marco, normalmente un identificador de ventana win32 **(HWND).**

</dd> </dl>

## <a name="h"></a>H

<dl> <dt>

**host**
</dt> <dd>

Elemento de interfaz de usuario, como una ventana o un control, que contiene otros elementos de la interfaz de usuario. Un host realiza Automatización de la interfaz de usuario servicios en nombre de los elementos hospedados.

</dd> </dl>

## <a name="i"></a>I

<dl> <dt>

**IAccessible**
</dt> <dd>

Interfaz COM que contiene todos los métodos y propiedades de Microsoft Active Accessibility.

</dd> <dt>

**Proxy IAccessible**
</dt> <dd>

Tipo de compatibilidad [**con IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que proporciona información de accesibilidad predeterminada para elementos de interfaz de usuario estándar: controles USER, menús USER y controles comunes de COMCTL y COMCTL32. Para obtener más información, vea [IAccessible Proxies](iaccessible-proxies.md).

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**navegación lógica**
</dt> <dd>

Uno de los dos modos de navegación [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en los que un cliente explora la jerarquía de objetos Microsoft Active Accessibility (siguiente, anterior, primario, primer elemento secundario, último elemento secundario).

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**marshaling**
</dt> <dd>

Empaquetado y envío de parámetros de interfaz a través de los límites del proceso.

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**implementación nativa**
</dt> <dd>

Tipo de compatibilidad que proporcionan los elementos de la interfaz de usuario que implementan la [**interfaz IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

</dd> </dl>

## <a name="o"></a>O

<dl> <dt>

**modelo fuera de pantalla**
</dt> <dd>

Este modelo es una base de datos de objetos en la pantalla e incluye sus propiedades y sus relaciones espaciales.

</dd> <dt>

**OLEACC**
</dt> <dd>

Biblioteca de vínculos dinámicos que proporciona el Microsoft Active Accessibility de ejecución y administra las solicitudes de Microsoft Active Accessibility clientes.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**parent**
</dt> <dd>

También se denomina contenedor; un objeto accesible que corresponde a uno o varios elementos simples; Por ejemplo, un [**objeto IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para un cuadro de lista es el elemento primario de los elementos de lista.

</dd> <dt>

**elemento de automatización de marcador de posición**
</dt> <dd>

Elemento Automatización de la interfaz de usuario que representa un elemento virtualizado en el Automatización de la interfaz de usuario virtualizado. Normalmente, un marcador de posición no tiene datos cargados para todas las propiedades Automatización de la interfaz de usuario y solo es necesario implementar el patrón de control [VirtualizedItem.](uiauto-implementingvirtualizeditem.md)

</dd> <dt>

**evento de cambio de propiedad**
</dt> <dd>

Evento que se desencadena cuando cambia el valor de una propiedad. Los clientes se registran para recibir eventos específicos de cambio de propiedad y Automatización de la interfaz de usuario a los clientes registrados cuando se producen esos eventos.

</dd> <dt>

**interfaz de proveedor**
</dt> <dd>

Colección de métodos públicos implementados por un Automatización de la interfaz de usuario de datos.

</dd> <dt>

**Proxy**
</dt> <dd>

Consulte [*IAccessible proxy (Proxy de IAccessible).*](uiauto-glossary.md)

</dd> </dl>

## <a name="r"></a>R

<dl> <dt>

**vista sin formato**
</dt> <dd>

Árbol completo de [**objetos IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) en el Automatización de la interfaz de usuario para el que el escritorio es la raíz. La vista sin formato sigue estrechamente la estructura de programación nativa de una aplicación y, por tanto, es la vista más precisa de la estructura de la interfaz de usuario. También es la base sobre la que se crean las otras vistas del árbol.

</dd> <dt>

**elemento realizado**
</dt> <dd>

Elemento de interfaz de usuario para el que se ha cargado toda la información en la memoria, lo que Automatización de la interfaz de usuario crear un elemento de automatización para el elemento.

</dd> <dt>

**identificador en tiempo de ejecución**
</dt> <dd>

Matriz de enteros que identifica la instancia en ejecución de un Automatización de la interfaz de usuario elemento. El identificador es único dentro de la interfaz de usuario del escritorio en el que se generó.

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**Matriz segura**
</dt> <dd>

Tipo de datos autodescripto para declarar matrices usadas en la creación de componentes COM. Junto con los datos, una matriz segura contiene información sobre el número y los límites de sus dimensiones.

</dd> <dt>

**Ámbito**
</dt> <dd>

Definir la extensión de la vista, empezando por un elemento base.

</dd> <dt>

**servidor**
</dt> <dd>

Cualquier control, módulo o aplicación que use Microsoft Active Accessibility para exponer información sobre su interfaz de usuario

</dd> <dt>

**proveedor de servidor**
</dt> <dd>

Componente de software que expone información sobre un elemento de interfaz de usuario basado en un marco de interfaz de usuario que no Automatización de la interfaz de usuario de forma nativa. Los proveedores del lado servidor (proveedores nativos) se comunican con las aplicaciones cliente a través del límite del proceso mediante la exposición de interfaces COM al sistema principal de Automatización de la interfaz de usuario, que los servicios solicitan a los clientes.

</dd> <dt>

**elemento simple**
</dt> <dd>

También se conoce como elemento secundario; cualquier elemento de interfaz de usuario que comparta un [**objeto IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) con otros elementos y se base en ese **objeto IAccessible** para exponer sus propiedades. Para obtener más información, vea [Elementos simples](simple-elements.md).

</dd> <dt>

**navegación espacial**
</dt> <dd>

Uno de los dos modos de navegación [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en los que un cliente se mueve de un elemento de la interfaz de usuario a otro en función de sus posiciones en pantalla (arriba, abajo, izquierda, derecha).

</dd> </dl>

## <a name="t"></a>T

<dl> <dt>

**Text Services Framework (TSF)**
</dt> <dd>

Un marco de trabajo del sistema escalable que permite servicios de lenguaje natural y entrada de texto avanzada en el escritorio y dentro de las aplicaciones.

</dd> <dt>

**unidad de texto**
</dt> <dd>

Unidad predefinida de texto (carácter, palabra, línea o párrafo) que se usa para navegar por segmentos lógicos de un intervalo de texto.

</dd> </dl>

## <a name="u"></a>U

<dl> <dt>

**Automatización de la interfaz de usuario cliente**
</dt> <dd>

Una aplicación de tecnología de asistencia, como un lector de pantalla, que usa Automatización de la interfaz de usuario para obtener acceso mediante programación a los elementos de la interfaz de usuario en una interfaz de usuario de la aplicación. El cliente presenta información sobre los elementos de la interfaz de usuario al usuario final. Los scripts de prueba automatizados también se consideran Automatización de la interfaz de usuario clientes.

</dd> <dt>

**Automatización de la interfaz de usuario core**
</dt> <dd>

Componente en tiempo de ejecución que implementa el marco de trabajo de automatización de la interfaz de usuario.

</dd> <dt>

**Automatización de la interfaz de usuario elemento**
</dt> <dd>

Elemento de interfaz de usuario representado por un objeto COM que implementa una interfaz de proveedor de Automatización de la interfaz de usuario y que expone la interfaz [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) a Automatización de la interfaz de usuario clientes.

</dd> <dt>

**marco de trabajo de automatización de la interfaz de usuario**
</dt> <dd>

Un componente de Windows que admite el acceso mediante programación a la mayoría de los elementos de la interfaz de usuario en el escritorio. Permite que los productos de tecnología de asistencia, como los lectores de pantalla, proporcionen información sobre la interfaz de usuario a los usuarios finales y manipulen la interfaz de usuario por medios distintos de la entrada estándar. Automatización de la interfaz de usuario también permite que los scripts de prueba automatizados interactúen con la interfaz de usuario.

</dd> <dt>

**Automatización de la interfaz de usuario nodo**
</dt> <dd>

En desuso. Vea Automatización de la interfaz de usuario elemento .

</dd> <dt>

**Automatización de la interfaz de usuario proveedor**
</dt> <dd>

Implementación de interfaces Automatización de la interfaz de usuario que expone información de programación sobre un elemento de interfaz de usuario. El proveedor proporciona esta información a la marco de trabajo de automatización de la interfaz de usuario en respuesta a Automatización de la interfaz de usuario solicitudes de cliente.

</dd> <dt>

**Automatización de la interfaz de usuario árbol**
</dt> <dd>

Representación jerárquica de todos los Automatización de la interfaz de usuario en el Windows escritorio. El árbol consta de un elemento raíz que representa el escritorio actual y cuyos elementos secundarios representan los elementos de Windows. Cada uno de estos elementos secundarios puede contener elementos que representan partes de la interfaz de usuario, como menús, botones, barras de herramientas y cuadros de lista. Estos elementos pueden contener elementos como elementos de lista.

</dd> <dt>

**Marco de interfaz de usuario**
</dt> <dd>

Componente que administra los controles secundarios, las pruebas de acceso y la representación en un área de la pantalla.

</dd> </dl>

## <a name="v"></a>V

<dl> <dt>

**identificador de vista**
</dt> <dd>

Valor que identifica una vista que está disponible para un elemento Automatización de la interfaz de usuario que implementa un patrón de control. Este tipo de elemento proporciona y es capaz de cambiar entre varias representaciones del mismo conjunto de información o controles secundarios.

</dd> <dt>

**elemento virtualizado**
</dt> <dd>

Elemento de interfaz de usuario que se carga en la memoria solo cuando es necesario, normalmente cuando el elemento se vuelve visible en la pantalla. Un elemento virtualizado se representa mediante un elemento de automatización de marcadores de posición en Automatización de la interfaz de usuario árbol.

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**Eventos de ventana (WinEvents)**
</dt> <dd>

Tipo de evento usado para notificar a los clientes que un objeto accesible ha cambiado de alguna manera.

</dd> <dt>

**elemento basado en ventanas**
</dt> <dd>

Un Automatización de la interfaz de usuario que representa un elemento de interfaz de usuario que tiene su propio identificador de ventana win32 **(HWND).**

</dd> </dl>

 

 




