---
title: Información general sobre UI Automation
description: Microsoft Automatización de la interfaz de usuario es un marco de accesibilidad para Windows.
ms.assetid: 99610542-761c-432d-a4ac-4cd3812577a8
keywords:
- Automatización de la interfaz de usuario,about
- Automatización de la interfaz de usuario,accesibilidad
- Automatización de la interfaz de usuario,components
- Automatización de la interfaz de usuario,PROVIDER API
- Automatización de la interfaz de usuario,API de cliente
- Automatización de la interfaz de usuario,archivos de encabezado
- Automatización de la interfaz de usuario,model
- components
- accesibilidad
- API de proveedor
- API de cliente
- archivos de encabezado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3664866280d570f9fa5f07acc6245ca2b4c1bff7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470062"
---
# <a name="ui-automation-overview"></a>Información general sobre UI Automation

Microsoft Automatización de la interfaz de usuario es un marco de accesibilidad para Windows. Proporciona acceso mediante programación a la mayoría de los elementos de la interfaz de usuario en el escritorio. Permite que los productos de tecnología de asistencia, como los lectores de pantalla, proporcionen información sobre la interfaz de usuario a los usuarios finales y manipulen la interfaz de usuario por medios distintos de la entrada estándar. Automatización de la interfaz de usuario también permite que los scripts de prueba automatizados interactúen con la interfaz de usuario.

Automatización de la interfaz de usuario primero estaba disponible en Windows XP como parte de Microsoft .NET Framework. Aunque en ese momento también se publicó una API de C++ no administrada, la utilidad de las funciones de cliente estaba limitada debido a problemas de interoperabilidad. Para Windows 7, la API se ha reescrito en Component Object Model (COM).

> [!Note]  
> Aunque las funciones de biblioteca introducidas en la versión anterior de Automatización de la interfaz de usuario todavía están documentadas, no deben usarse en nuevas aplicaciones.

 

Automatización de la interfaz de usuario aplicaciones cliente se pueden escribir con la garantía de que funcionarán en varios marcos de control Windows Microsoft. El Automatización de la interfaz de usuario enmascara las diferencias en los marcos que subyacen a varias partes de la interfaz de usuario. Por ejemplo, la propiedad **Content** de un botón Windows Presentation Foundation (WPF), la propiedad **Caption** de un botón de Microsoft Win32 y la propiedad **ALT** de una imagen HTML se asignan a una sola propiedad, **Name**, en la vista Automatización de la interfaz de usuario.

Automatización de la interfaz de usuario proporciona funcionalidad completa en Windows XP, Windows Server 2003 y sistemas operativos posteriores.

Automatización de la interfaz de usuario son componentes que implementan compatibilidad con Automatización de la interfaz de usuario en controles y ofrecen compatibilidad con aplicaciones cliente de Microsoft Active Accessibility, a través de un servicio de puente integrado.

> [!Note]  
> Automatización de la interfaz de usuario no habilita la comunicación entre los procesos iniciados por distintos usuarios mediante el **comando Ejecutar** como.

 

En este tema se incluyen las siguientes secciones.

-   [Automatización de la interfaz de usuario componentes](#ui-automation-components)
-   [Automatización de la interfaz de usuario de encabezado](#ui-automation-header-files)
-   [Modelo de la automatización de la interfaz de usuario](#ui-automation-model)
-   [Temas relacionados](#related-topics)

## <a name="ui-automation-components"></a>Automatización de la interfaz de usuario componentes

Automatización de la interfaz de usuario tiene cuatro componentes principales, como se muestra en la tabla siguiente.




| Componente | Descripción | 
|-----------|-------------|
| API de proveedor | Un conjunto de interfaces COM que implementan los Automatización de la interfaz de usuario de trabajo. Automatización de la interfaz de usuario son objetos que proporcionan información sobre los elementos de la interfaz de usuario y responden a la entrada mediante programación. | 
| API de cliente | Conjunto de interfaces COM que permiten a las aplicaciones cliente obtener información sobre la interfaz de usuario y enviar entradas a los controles.<blockquote>[!Note]<br />Las funciones descritas en <a href="uiauto-entry-cpfunctions.md">Funciones de patrón de control en desuso</a> y Funciones de <a href="uiauto-entry-uianodefunctions.md">nodo</a> en desuso están en desuso. En su lugar, las aplicaciones cliente deben usar las Automatización de la interfaz de usuario COM descritas <a href="uiauto-entry-uiautoclientinterfaces.md">en Automatización de la interfaz de usuario Interfaces de elementos para clientes</a>.</blockquote><br /> | 
| UIAutomationCore.dll | La biblioteca en tiempo de ejecución, a veces denominada Automatización de la interfaz de usuario principal, que controla la comunicación entre proveedores y clientes. | 
| Oleacc.dll | La biblioteca en tiempo de ejecución para Microsoft Active Accessibility y los objetos proxy. La biblioteca también proporciona objetos proxy usados por Microsoft Microsoft Active Accessibility para Automatización de la interfaz de usuario proxy para admitir controles Win32. | 




 

Hay dos maneras de usar Automatización de la interfaz de usuario: crear compatibilidad con controles personalizados mediante la API del proveedor y crear aplicaciones cliente que usan el núcleo de Automatización de la interfaz de usuario para comunicarse con elementos de interfaz de usuario y recuperar información sobre ellos. En función de su enfoque, debe hacer referencia a diferentes partes de la documentación. Si necesita crear compatibilidad con controles personalizados, vea Automatización de la interfaz de usuario Guía del [programador del proveedor de aplicaciones.](uiauto-providerportal.md) Si necesita comunicarse con o recuperar información sobre los elementos de la interfaz de usuario, vea Automatización de la interfaz de usuario Guía del programador [de cliente.](uiauto-clientportal.md)

## <a name="ui-automation-header-files"></a>Automatización de la interfaz de usuario de encabezado

La API Automatización de la interfaz de usuario se define en varios archivos de encabezado de C/C++ diferentes que se incluyen con el Kit de desarrollo de software (SDK) de Windows. Los Automatización de la interfaz de usuario de encabezado se describen en la tabla siguiente:



| Archivo de encabezado           | Descripción                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UIAutomationClient.h  | Define las interfaces y los elementos de programación relacionados utilizados por Automatización de la interfaz de usuario clientes.                                                                                                                                                                                           |
| UIAutomationCore.h    | Define las interfaces y los elementos de programación relacionados utilizados por Automatización de la interfaz de usuario proveedores.                                                                                                                                                                                         |
| UIAutomationCoreApi.h | Define constantes generales, GUID, tipos de datos y estructuras que usan Automatización de la interfaz de usuario clientes y proveedores. También contiene definiciones para las funciones de nodo y patrón de control en desuso.                                                                                    |
| UIAutomation.h        | Incluye todos los demás archivos Automatización de la interfaz de usuario encabezado. Dado que la mayoría Automatización de la interfaz de usuario aplicaciones requieren elementos de todos los archivos de encabezado de Automatización de la interfaz de usuario, es mejor incluir UIAutomation.h en los proyectos de aplicación de Automatización de la interfaz de usuario en lugar de incluir cada archivo individualmente. |



 

Si está desarrollando una aplicación que usa la API Automatización de la interfaz de usuario, debe incluir UIAutomation.h en el proyecto. Si la aplicación admite Microsoft Active Accessibility, incluya el archivo de encabezado Oleacc.h. Automatización de la interfaz de usuario aplicaciones que usan GUID también requieren el archivo de encabezado Initguid.h. Si es necesario, se debe incluir Initguid.h antes de UIAutomation.h.

## <a name="ui-automation-model"></a>Modelo de la automatización de la interfaz de usuario

Automatización de la interfaz de usuario expone todos los elementos de la interfaz de usuario a las aplicaciones cliente como un objeto representado por la [**interfaz IUIAutomationElement.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) Los elementos se encuentran en una estructura de árbol, con el escritorio como el elemento raíz. Los clientes pueden filtrar la vista sin formato del árbol como una vista de control o una vista de contenido. Estas vistas estándar de la estructura se pueden ver fácilmente mediante la [aplicación Inspect](inspect-objects.md) que se incluye con Windows SDK. Las aplicaciones también pueden crear vistas personalizadas.

Un Automatización de la interfaz de usuario expone las propiedades del control o elemento de interfaz de usuario que representa. Una de estas propiedades es el tipo de control , que define la apariencia básica y la funcionalidad del control o elemento de interfaz de usuario como una única entidad reconocible, por ejemplo, un botón o una casilla. Para obtener más información sobre los tipos de control, [vea Automatización de la interfaz de usuario información general sobre los tipos de control](uiauto-controltypesoverview.md).

Además, un elemento Automatización de la interfaz de usuario expone uno o varios patrones de control. Un patrón de control proporciona un conjunto de propiedades que son específicas de un tipo de control determinado. Un patrón de control también expone métodos que permiten a las aplicaciones cliente obtener más información sobre el elemento y proporcionar entradas al elemento. Para más información sobre los patrones de control, vea [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

> [!Note]  
> No hay ninguna correspondencia uno a uno entre los tipos de control y los patrones de control. Un patrón de control puede ser compatible con varios tipos de control y un control puede admitir varios patrones de control, cada uno de los cuales expone diferentes aspectos de su comportamiento. Por ejemplo, un cuadro combinado tiene al menos dos patrones de control: uno que representa su capacidad para expandir y contraer, y otro que representa el mecanismo de selección. Sin embargo, un control solo puede mostrar un tipo de control único.

 

Automatización de la interfaz de usuario proporciona información a las aplicaciones cliente a través de eventos. A diferencia de WinEvents, Automatización de la interfaz de usuario eventos no se basan en un mecanismo de difusión. Automatización de la interfaz de usuario se registran para notificaciones de eventos específicas y pueden solicitar que se pasen propiedades específicas e información del patrón de control a sus controladores de eventos. Además, un Automatización de la interfaz de usuario evento contiene una referencia al elemento que lo ha producido. Los proveedores pueden mejorar el rendimiento generando eventos de forma selectiva, dependiendo de si los clientes están escuchando. Para más información sobre eventos, vea [UI Automation Events Overview](uiauto-eventsoverview.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Información general sobre eventos de UI Automation](uiauto-eventsoverview.md)
</dt> </dl>

 

 





