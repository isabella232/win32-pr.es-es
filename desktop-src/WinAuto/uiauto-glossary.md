---
title: Glosario (características de accesibilidad de Windows)
description: Página de glosario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: c45583f2-a6e8-4a01-9577-9b604b5bbc62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16679c63f0716058e53c7c9d164a24593c481dff
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105685822"
---
# <a name="glossary-windows-accessibility-features"></a>Glosario (características de accesibilidad de Windows)

## <a name="a"></a>A

<dl> <dt>

**clave de acceso**
</dt> <dd>

Carácter subrayado en el texto de la etiqueta de un control.

</dd> <dt>

**ayuda de accesibilidad**
</dt> <dd>

También se denomina tecnología de asistencia; programas especializados que funcionan con el sistema operativo de un equipo para acomodar discapacidades específicas, como un intervalo limitado de movimiento o ceguera. Entre los productos se incluyen teclados más grandes, teclados que funcionan con miras, utilidades de entrada de voz, teclados en pantalla y productos que pueden convertir texto en voz o en una presentación de Braille dinámica. Para obtener más información, vea [productos de tecnología de asistencia](https://www.microsoft.com/enable/at/default.aspx).

</dd> <dt>

**objeto accesible**
</dt> <dd>

Cualquier elemento de la interfaz de usuario que implementa la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y tiene propiedades que describen el nombre del objeto, las ubicaciones de la pantalla y otra información necesaria para las ayudas de accesibilidad. Para obtener más información, vea [objetos accesibles](accessible-objects.md).

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**elemento secundario**
</dt> <dd>

Vea [*elemento simple*](uiauto-glossary.md).

</dd> <dt>

**client**
</dt> <dd>

Cualquier programa que utilice la automatización de la interfaz de usuario o Microsoft Active Accessibility para tener acceso, identificar o manipular los elementos de la interfaz de usuario de una aplicación. los clientes incluyen ayudas para la accesibilidad, herramientas de pruebas automatizadas y algunas aplicaciones de aprendizaje basadas en equipos. Para obtener más información, vea [Cómo funciona Active Accessibility](how-active-accessibility-works.md).

</dd> <dt>

**proveedor del lado cliente**
</dt> <dd>

Componente de software implementado por un cliente de automatización de la interfaz de usuario para recuperar información sobre la interfaz de usuario de una aplicación que no admite o no es totalmente compatible con la automatización de la interfaz de usuario. Normalmente, los proveedores del lado cliente (servidores proxy) se comunican con la aplicación a través del límite del proceso mediante el envío y la recepción de mensajes de Windows.

</dd> <dt>

**container**
</dt> <dd>

También se denomina primario; objeto accesible que corresponde a uno o varios elementos simples; por ejemplo, un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para un cuadro de lista es el elemento primario de los elementos de lista.

</dd> <dt>

**patrón de control**
</dt> <dd>

En la automatización de la interfaz de usuario, es una implementación de diseño que describe un fragmento de funcionalidad discreto para un control. Esta funcionalidad puede incluir la apariencia visual de un control y las acciones que puede realizar.

</dd> <dt>

**objeto de patrón de control**
</dt> <dd>

Instancia en tiempo de ejecución de un objeto COM que expone una o más interfaces de patrón de control.

</dd> <dt>

**proveedor de patrón de control**
</dt> <dd>

Componente de software que implementa una o varias interfaces de patrón de control.

</dd> <dt>

**control personalizado**
</dt> <dd>

Un control creado por un usuario o un proveedor de software de terceros, o un control definido por el sistema modificado por un usuario o un proveedor de software de terceros.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**intervalo de texto degenerado (intervalo vacío)**
</dt> <dd>

Objeto que representa un intervalo de texto vacío (de cero caracteres). Un intervalo de texto degenerado tiene extremos adyacentes y especifica un punto entre dos caracteres.

</dd> <dt>

**intervalo de texto separado**
</dt> <dd>

Objeto que representa varios intervalos de texto que no son físicamente adyacentes entre sí.

</dd> <dt>

**contenedor de acoplamiento**
</dt> <dd>

Control que permite la organización de elementos secundarios, tanto horizontal como verticalmente, con respecto a los límites del contenedor de acoplamiento y otros elementos dentro del contenedor.

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**agente de escucha de eventos**
</dt> <dd>

Una aplicación cliente que se ha registrado para recibir notificaciones de la automatización de la interfaz de usuario o de Microsoft Active Accessibility siempre que se produzcan cambios específicos en la interfaz de usuario.

</dd> <dt>

**notificación de eventos**
</dt> <dd>

Llamada de un proveedor de automatización de la interfaz de usuario a un cliente, en el que el proveedor notifica al cliente de un evento que puede afectar al estado o la apariencia de un elemento de la interfaz de usuario.

</dd> </dl>

## <a name="f"></a>F

<dl> <dt>

**\[filtrar\]**
</dt> <dd>

Para definir los tipos de elementos de automatización de la interfaz de usuario que se van a incluir en una vista del árbol de automatización de la interfaz de usuario. Vea también: vista sin formato, vista de control y vista de contenido.

</dd> <dt>

**raíz de fragmento**
</dt> <dd>

El elemento de automatización de la interfaz de usuario en el nodo raíz de un subárbol del árbol de automatización de la interfaz de usuario. Una raíz de fragmento no tiene un elemento primario, pero se hospeda en otro marco de trabajo, normalmente un identificador de ventana Win32 (**hWnd**).

</dd> </dl>

## <a name="h"></a>H

<dl> <dt>

**host**
</dt> <dd>

Elemento de la interfaz de usuario, como una ventana o un control, que contiene otros elementos de la interfaz de usuario. Un host realiza servicios de automatización de la interfaz de usuario en nombre de los elementos hospedados.

</dd> </dl>

## <a name="i"></a>I

<dl> <dt>

**IAccessible**
</dt> <dd>

La interfaz COM que contiene todos los métodos y propiedades de Microsoft Active Accessibility.

</dd> <dt>

**Proxy IAccessible**
</dt> <dd>

Un tipo de compatibilidad de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que proporciona información de accesibilidad predeterminada para los elementos de la interfaz de usuario estándar: controles de usuario, menús de usuario y controles comunes de COMCTL y comctl32. Para obtener más información, consulte objetos [proxy IAccessible](iaccessible-proxies.md).

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**navegación lógica**
</dt> <dd>

Uno de los dos modos de navegación [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en los que un cliente explora la jerarquía de objetos de Microsoft Active Accessibility (siguiente, anterior, primario, primer secundario, último elemento secundario).

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

El tipo de compatibilidad que proporcionan los elementos de la interfaz de usuario que implementan la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

</dd> </dl>

## <a name="o"></a>O

<dl> <dt>

**modelo fuera de pantalla**
</dt> <dd>

Este modelo es una base de datos de objetos en la pantalla e incluye sus propiedades y sus relaciones espaciales.

</dd> <dt>

**OLEACC**
</dt> <dd>

La biblioteca de vínculos dinámicos que proporciona el tiempo de ejecución de Microsoft Active Accessibility y administra las solicitudes de los clientes de Microsoft Active Accessibility.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**parent**
</dt> <dd>

También se denomina contenedor; objeto accesible que corresponde a uno o varios elementos simples; por ejemplo, un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para un cuadro de lista es el elemento primario de los elementos de lista.

</dd> <dt>

**placeholder (elemento de Automation)**
</dt> <dd>

Elemento de automatización de la interfaz de usuario que representa un elemento virtualizado en el árbol de automatización de la interfaz de usuario. Normalmente, un marcador de posición no tiene datos cargados para todas las propiedades de automatización de la interfaz de usuario y solo es necesario para implementar el patrón de control [VirtualizedItem](uiauto-implementingvirtualizeditem.md) .

</dd> <dt>

**evento de cambio de propiedad**
</dt> <dd>

Evento que se desencadena cuando el valor de una propiedad ha cambiado. Los clientes se registran para recibir eventos de cambio de propiedad específicos y la automatización de la interfaz de usuario informa a los clientes registrados cuando se producen esos eventos.

</dd> <dt>

**interfaz del proveedor**
</dt> <dd>

Colección de métodos públicos implementada por un proveedor de automatización de la interfaz de usuario.

</dd> <dt>

**proxi**
</dt> <dd>

Vea [*proxy IAccessible*](uiauto-glossary.md).

</dd> </dl>

## <a name="r"></a>R

<dl> <dt>

**vista sin formato**
</dt> <dd>

Árbol completo de objetos [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) en el árbol de automatización de la interfaz de usuario para el que el escritorio es la raíz. La vista sin formato sigue estrechamente la estructura de programación nativa de una aplicación y, por lo tanto, es la vista más precisa de la estructura de la interfaz de usuario. También es la base sobre la que se crean las otras vistas del árbol.

</dd> <dt>

**elemento realizado**
</dt> <dd>

Elemento de interfaz de usuario para el que se ha cargado toda la información en la memoria, lo que permite a la automatización de la interfaz de usuario crear un elemento de automatización para el elemento.

</dd> <dt>

**identificador en tiempo de ejecución**
</dt> <dd>

Matriz de enteros que identifica la instancia en ejecución de un elemento de automatización de la interfaz de usuario. El identificador es único en la interfaz de usuario del escritorio en el que se generó.

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**matriz segura**
</dt> <dd>

Un tipo de datos autodescriptivo para declarar matrices utilizadas en la creación de componentes COM. Junto con los datos, una matriz segura contiene información sobre el número y los límites de sus dimensiones.

</dd> <dt>

**ámbitos**
</dt> <dd>

Definir la extensión de la vista, a partir de un elemento base.

</dd> <dt>

**servidor**
</dt> <dd>

Cualquier control, módulo o aplicación que use Microsoft Active Accessibility para exponer información sobre su interfaz de usuario.

</dd> <dt>

**proveedor de servidor**
</dt> <dd>

Componente de software que expone información sobre un elemento de la interfaz de usuario que se basa en un marco de interfaz de usuario que no admite la automatización de la interfaz de usuario de forma nativa. Los proveedores del lado servidor (proveedores nativos) se comunican con las aplicaciones cliente a través del límite del proceso mediante la exposición de interfaces COM al sistema principal de automatización de la interfaz de usuario, que ofrece servicio a las solicitudes de los clientes.

</dd> <dt>

**elemento simple**
</dt> <dd>

También se conoce como elemento secundario; cualquier elemento de la interfaz de usuario que comparte un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) con otros elementos y se basa en ese objeto **IAccessible** para exponer sus propiedades. Para obtener más información, vea [elementos simples](simple-elements.md).

</dd> <dt>

**navegación espacial**
</dt> <dd>

Uno de los dos modos de navegación [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en los que un cliente se mueve de un elemento de la interfaz de usuario a otro basándose en sus posiciones en pantalla (arriba, abajo, izquierda, derecha).

</dd> </dl>

## <a name="t"></a>T

<dl> <dt>

**Text Services Framework (TSF)**
</dt> <dd>

Marco de trabajo del sistema escalable que habilita los servicios de lenguaje natural y la entrada de texto avanzada en el escritorio y en las aplicaciones.

</dd> <dt>

**unidad de texto**
</dt> <dd>

Unidad predefinida de texto (carácter, palabra, línea o párrafo) utilizada para navegar por los segmentos lógicos de un intervalo de texto.

</dd> </dl>

## <a name="u"></a>U

<dl> <dt>

**Cliente de UI Automation**
</dt> <dd>

Aplicación de tecnología de asistencia, como un lector de pantalla, que utiliza la automatización de la interfaz de usuario para obtener acceso mediante programación a los elementos de la interfaz de usuario de una interfaz de usuario de la aplicación. El cliente presenta información sobre los elementos de la interfaz de usuario al usuario final. Los scripts de pruebas automatizadas también se consideran clientes de automatización de la interfaz de usuario.

</dd> <dt>

**Núcleo de UI Automation**
</dt> <dd>

Componente de tiempo de ejecución que implementa el marco de automatización de la interfaz de usuario.

</dd> <dt>

**UI Automation (elemento)**
</dt> <dd>

Elemento de la interfaz de usuario representado por un objeto COM que implementa una interfaz del proveedor de automatización de la interfaz de usuario y que expone la interfaz [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) a los clientes de automatización de la interfaz de usuario.

</dd> <dt>

**Marco de UI Automation**
</dt> <dd>

Componente integral de Windows que admite el acceso mediante programación a la mayoría de los elementos de la interfaz de usuario en el escritorio. Permite a los productos de tecnología de asistencia, como lectores de pantalla, proporcionar información sobre la interfaz de usuario a los usuarios finales y manipular la interfaz de usuario por medios distintos de la entrada estándar. UI Automation también permite que los scripts de pruebas automatizadas interactúen con la interfaz de usuario.

</dd> <dt>

**Nodo de UI Automation**
</dt> <dd>

En desuso. Vea elemento de automatización de la interfaz de usuario.

</dd> <dt>

**Proveedor de UI Automation**
</dt> <dd>

Implementación de interfaces de automatización de la interfaz de usuario que expone información de programación sobre un elemento de la interfaz de usuario. El proveedor proporciona esta información al marco de automatización de la interfaz de usuario en respuesta a las solicitudes de cliente de automatización de la interfaz de usuario.

</dd> <dt>

**Árbol de UI Automation**
</dt> <dd>

Representación jerárquica de todos los elementos de automatización de la interfaz de usuario del escritorio de Windows. El árbol está compuesto de un elemento raíz que representa el escritorio actual y cuyos elementos secundarios representan las ventanas de la aplicación. Cada uno de estos elementos secundarios puede contener elementos que representan partes de la interfaz de usuario, como menús, botones, barras de herramientas y cuadros de lista. Estos elementos pueden contener elementos como elementos de lista.

</dd> <dt>

**Marco de interfaz de usuario**
</dt> <dd>

Componente que administra controles secundarios, pruebas de posicionamiento y representación en un área de la pantalla.

</dd> </dl>

## <a name="v"></a>V

<dl> <dt>

**identificador de vista**
</dt> <dd>

Valor que identifica una vista que está disponible para un elemento de automatización de la interfaz de usuario que implementa un patrón de control. Este tipo de elemento proporciona y puede cambiar entre varias representaciones del mismo conjunto de información o controles secundarios.

</dd> <dt>

**elemento virtualizado**
</dt> <dd>

Un elemento de la interfaz de usuario que solo se carga en la memoria cuando es necesario, normalmente cuando el elemento está visible en la pantalla. Un elemento virtualizado se representa mediante un elemento de automatización de marcadores de posición en el árbol de automatización de la interfaz de usuario.

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**Eventos de ventana (WinEvents)**
</dt> <dd>

El tipo de evento que se usa para notificar a los clientes que un objeto accesible ha cambiado de alguna manera.

</dd> <dt>

**elemento basado en ventanas**
</dt> <dd>

Un elemento de automatización de la interfaz de usuario que representa un elemento de interfaz de usuario que tiene su propio identificador de ventana de Win32 (**hWnd**).

</dd> </dl>

 

 




