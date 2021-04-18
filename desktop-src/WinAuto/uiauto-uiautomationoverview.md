---
title: Información general sobre UI Automation
description: La automatización de la interfaz de usuario de Microsoft es un marco de accesibilidad para Windows.
ms.assetid: 99610542-761c-432d-a4ac-4cd3812577a8
keywords:
- Automatización de la interfaz de usuario, acerca de
- Automatización de la interfaz de usuario, accesibilidad
- Automatización de la interfaz de usuario, componentes
- Automatización de la interfaz de usuario, API de proveedor
- Automatización de la interfaz de usuario, API de cliente
- Automatización de la interfaz de usuario, archivos de encabezado
- Automatización de la interfaz de usuario, modelo
- components
- accesibilidad
- API de proveedor
- API de cliente
- archivos de encabezado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ea29b0abd4c6ed791ae3195f36a0f8184c8596
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104420208"
---
# <a name="ui-automation-overview"></a>Información general sobre UI Automation

La automatización de la interfaz de usuario de Microsoft es un marco de accesibilidad para Windows. Proporciona acceso mediante programación a la mayoría de los elementos de la interfaz de usuario en el escritorio. Permite productos de tecnología de asistencia, como lectores de pantalla, para proporcionar información sobre la interfaz de usuario a los usuarios finales y manipular la interfaz de usuario por medios distintos de la entrada estándar. UI Automation también permite que los scripts de pruebas automatizadas interactúen con la interfaz de usuario.

La automatización de la interfaz de usuario estaba disponible por primera vez en Windows XP como parte del marco de Microsoft .NET. Aunque una API de C++ no administrada también se publicó en ese momento, la utilidad de las funciones de cliente estaba limitada debido a problemas de interoperabilidad. En Windows 7, la API se ha vuelto a escribir en el modelo de objetos componentes (COM).

> [!Note]  
> Aunque las funciones de la biblioteca introducidas en la versión anterior de la automatización de la interfaz de usuario todavía están documentadas, no se deben usar en nuevas aplicaciones.

 

Las aplicaciones cliente de automatización de la interfaz de usuario se pueden escribir con la certeza de que funcionarán en varios marcos de control de Microsoft Windows. El núcleo de automatización de la interfaz de usuario enmascara cualquier diferencia en los marcos de trabajo que subyacen a varias partes de la interfaz de usuario. Por ejemplo, la propiedad de **contenido** de un botón Windows Presentation Foundation (WPF), la propiedad **título** de un botón de Microsoft Win32 y la propiedad **Alt** de una imagen HTML se asignan todos a una sola propiedad, **nombre**, en la vista de automatización de la interfaz de usuario.

La automatización de la interfaz de usuario proporciona funcionalidad completa en Windows XP, Windows Server 2003 y sistemas operativos posteriores.

Los proveedores de UI Automation son componentes que implementan la compatibilidad con la automatización de la interfaz de usuario en los controles y ofrecen compatibilidad con las aplicaciones cliente de Microsoft Active Accessibility, a través de un servicio de puente integrado.

> [!Note]  
> La automatización de la interfaz de usuario no permite la comunicación entre procesos iniciados por distintos usuarios mediante el comando **Ejecutar como** .

 

En este tema se incluyen las siguientes secciones.

-   [Componentes de UI Automation](#ui-automation-components)
-   [Archivos de encabezado de UI Automation](#ui-automation-header-files)
-   [Modelo de la automatización de la interfaz de usuario](#ui-automation-model)
-   [Temas relacionados](#related-topics)

## <a name="ui-automation-components"></a>Componentes de UI Automation

La automatización de la interfaz de usuario tiene cuatro componentes principales, como se muestra en la tabla siguiente.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Componente</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>API de proveedor</td>
<td>Un conjunto de interfaces COM que implementan los proveedores de automatización de la interfaz de usuario. Los proveedores de UI Automation son objetos que proporcionan información sobre los elementos de la interfaz de usuario y responden a la entrada mediante programación.</td>
</tr>
<tr class="even">
<td>API de cliente</td>
<td>Un conjunto de interfaces COM que permiten a las aplicaciones cliente obtener información sobre la interfaz de usuario y enviar la entrada a controles.
<blockquote>
[!Note]<br />
Las funciones descritas en <a href="uiauto-entry-cpfunctions.md">funciones de patrón de control desusadas</a> y <a href="uiauto-entry-uianodefunctions.md">funciones de nodo en desuso</a> están desusadas. En su lugar, las aplicaciones cliente deben usar las interfaces COM de automatización de la interfaz de usuario descritas en <a href="uiauto-entry-uiautoclientinterfaces.md">interfaces de elementos de automatización de la interfaz de usuario para clientes</a>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>UIAutomationCore.dll</td>
<td>La biblioteca en tiempo de ejecución, a veces denominada núcleo de automatización de la interfaz de usuario, que controla la comunicación entre proveedores y clientes.</td>
</tr>
<tr class="even">
<td>Oleacc.dll</td>
<td>Biblioteca en tiempo de ejecución de Microsoft Active Accessibility y los objetos proxy. La biblioteca también proporciona objetos de proxy utilizados por Microsoft Microsoft Active Accessibility a proxy de automatización de la interfaz de usuario para admitir controles Win32.</td>
</tr>
</tbody>
</table>



 

Hay dos maneras de usar la automatización de la interfaz de usuario: para crear compatibilidad con controles personalizados mediante la API de proveedor y para crear aplicaciones cliente que usan el núcleo de automatización de la interfaz de usuario para comunicarse con y recuperar información sobre los elementos de la interfaz de usuario. En función de su enfoque, debe hacer referencia a diferentes partes de la documentación. Si necesita crear compatibilidad para controles personalizados, vea [la guía del programador del proveedor de automatización](uiauto-providerportal.md)de la interfaz de usuario. Si necesita comunicarse con o recuperar información sobre los elementos de la interfaz de usuario, vea [la guía del programador del cliente de UI Automation](uiauto-clientportal.md).

## <a name="ui-automation-header-files"></a>Archivos de encabezado de UI Automation

La API de automatización de la interfaz de usuario se define en varios archivos de encabezado de C/C++ diferentes que se incluyen con el kit de desarrollo de software (SDK) de Windows. Los archivos de encabezado de automatización de la interfaz de usuario se describen en la tabla siguiente:



| Archivo de encabezado           | Descripción                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UIAutomationClient. h  | Define las interfaces y los elementos de programación relacionados usados por los clientes de automatización de la interfaz de usuario.                                                                                                                                                                                           |
| UIAutomationCore. h    | Define las interfaces y los elementos de programación relacionados usados por los proveedores de automatización de la interfaz de usuario.                                                                                                                                                                                         |
| UIAutomationCoreApi. h | Define constantes, GUID, tipos de datos y estructuras generales que usan los clientes y proveedores de automatización de la interfaz de usuario. También contiene definiciones para las funciones de patrón de control y nodo en desuso.                                                                                    |
| UIAutomation. h        | Incluye todos los demás archivos de encabezado de automatización de la interfaz de usuario. Dado que la mayoría de las aplicaciones de automatización de la interfaz de usuario requieren elementos de todos los archivos de encabezado de automatización de la interfaz de usuario, es mejor incluir UIAutomation. h en los proyectos de aplicación de automatización de la interfaz de usuario en lugar de incluir cada archivo individualmente. |



 

Si está desarrollando una aplicación que usa la API de automatización de la interfaz de usuario, debe incluir UIAutomation. h en el proyecto. Si la aplicación es compatible con Microsoft Active Accessibility, incluya el archivo de encabezado oleacc. h. Las aplicaciones de automatización de la interfaz de usuario que usan GUID también requieren el archivo de encabezado Initguid. h. Si es necesario, se debe incluir Initguid. h antes de UIAutomation. h.

## <a name="ui-automation-model"></a>Modelo de la automatización de la interfaz de usuario

La automatización de la interfaz de usuario expone todos los elementos de la interfaz de usuario a las aplicaciones cliente como un objeto representado por la interfaz [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) . Los elementos se encuentran en una estructura de árbol, con el escritorio como el elemento raíz. Los clientes pueden filtrar la vista sin formato del árbol como una vista de control o una vista de contenido. Estas vistas estándar de la estructura se pueden ver fácilmente mediante el uso de la aplicación de [inspección](inspect-objects.md) que se incluye con el Windows SDK. Las aplicaciones también pueden crear vistas personalizadas.

Un elemento de automatización de la interfaz de usuario expone propiedades del control o elemento de la interfaz de usuario que representa. Una de estas propiedades es el tipo de control, que define la apariencia y la funcionalidad básicas del control o el elemento de la interfaz de usuario como una única entidad reconocible, por ejemplo, un botón o una casilla. Para obtener más información sobre los tipos de control, vea [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

Además, un elemento de automatización de la interfaz de usuario expone uno o más patrones de control. Un patrón de control proporciona un conjunto de propiedades que son específicas de un tipo de control determinado. Un patrón de control también expone métodos que permiten a las aplicaciones cliente obtener más información sobre el elemento y proporcionar la entrada al elemento. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

> [!Note]  
> No hay una correspondencia uno a uno entre los tipos de control y los patrones de control. Un patrón de control puede ser compatible con varios tipos de control y un control puede admitir varios patrones de control, cada uno de los cuales expone diferentes aspectos de su comportamiento. Por ejemplo, un cuadro combinado tiene al menos dos patrones de control: uno que representa su capacidad para expandir y contraer, y otro que representa el mecanismo de selección. Sin embargo, un control solo puede presentar un tipo de control único.

 

La automatización de la interfaz de usuario proporciona información a las aplicaciones cliente a través de eventos. A diferencia de WinEvents, los eventos de automatización de la interfaz de usuario no se basan en un mecanismo de difusión. Los clientes de automatización de la interfaz de usuario se registran para notificaciones de eventos específicas y pueden solicitar que se pasen propiedades específicas e información de patrón de control a sus controladores de eventos. Además, un evento de automatización de la interfaz de usuario contiene una referencia al elemento que lo generó. Los proveedores pueden mejorar el rendimiento generando eventos de forma selectiva, dependiendo de si los clientes están escuchando. Para más información sobre eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre eventos de UI Automation](uiauto-eventsoverview.md)
</dt> </dl>

 

 





