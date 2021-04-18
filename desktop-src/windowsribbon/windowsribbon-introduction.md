---
title: Introducción al marco de cinta de Windows
description: El marco de la cinta de opciones de Windows es un sistema de presentación de comandos enriquecido que proporciona una alternativa moderna a los menús, las barras de herramientas y los paneles de tareas de las aplicaciones Windows tradicionales.
ms.assetid: bc19d5eb-e3a4-4022-8051-512cb3a3e065
keywords:
- Cinta de Windows, marco
- Cinta de opciones, marco
- Cinta de Windows, acerca de
- Cinta, acerca de
- Cinta de Windows, componentes
- Cinta de opciones, componentes
- Cinta de opciones de Windows, vistas
- Cinta de opciones, vistas
- Cinta de Windows, arquitectura
- Cinta de opciones, arquitectura
- Cinta de Windows, API
- Cinta de opciones, API
- Cinta de opciones de Windows, seguridad
- Cinta de opciones, seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ac5c3acccf1c48a54f93b1752729067e63e4c6
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104562195"
---
# <a name="introducing-the-windows-ribbon-framework"></a>Introducción al marco de cinta de Windows

El marco de la cinta de opciones de Windows es un sistema de presentación de comandos enriquecido que proporciona una alternativa moderna a los menús, las barras de herramientas y los paneles de tareas de las aplicaciones Windows tradicionales.

-   [Un nuevo paradigma de comando](#a-new-command-paradigm)
-   [Vistas](#views)
    -   [Vista de la cinta de opciones](#the-ribbon-view)
    -   [La vista ContextPopup](#the-contextpopup-view)
-   [Arquitectura de la cinta](#ribbon-architecture)
    -   [Las API de la cinta de opciones](#the-ribbon-apis)
    -   [Seguridad y privacidad](#security-and-privacy)
    -   [Accesibilidad y localización](#accessibility-and-localization)
-   [Conclusión](#conclusion)
-   [Temas relacionados](#related-topics)

## <a name="a-new-command-paradigm"></a>Un nuevo paradigma de comando

El marco de cinta es una colección de API de Microsoft Win32 que admiten un host de nuevas capacidades de interfaz de usuario para los desarrolladores de Windows.

Este marco de trabajo de interfaz de usuario moderno y completo ofrece:

-   Implementación sencilla de nuevas aplicaciones del marco de cinta y migración directa de las aplicaciones Win32 existentes.
-   Apariencia y comportamiento coherentes en las aplicaciones de la cinta.
-   Cumplimiento de las directrices de la interfaz de usuario de Windows para una experiencia de primera clase en Windows a través de estándares de accesibilidad, compatibilidad con estilo visual (la función de los objetos), ajustes automáticos de contraste alto y reconocimiento de puntos por pulgada (PPP).

El marco de cinta está formado por dos componentes principales de la interfaz de usuario:

-   La barra de comandos de la cinta de opciones, que se compone de la barra de herramientas de acceso rápido (QAT), que expone y resalta varios comandos de la cinta de opciones según lo especificado por el usuario o la aplicación, y una fila de ficha que contiene el menú de la aplicación, las fichas estándar o contextual y un botón ayuda.
-   Un sistema de menús contextuales enriquecido.

Se utiliza una combinación de interfaces COM declarativas XML y nativas para desacoplar la presentación y la funcionalidad de estos componentes.

## <a name="views"></a>Vistas

Los componentes principales de la interfaz de usuario del marco de cinta, la barra de comandos de la cinta y el sistema de menús contextuales, se diferencian estructuralmente a través de las *vistas*. El marco de trabajo admite dos vistas: la vista de la [**cinta**](windowsribbon-element-ribbon.md) de opciones y la vista [**ContextPopup**](windowsribbon-element-contextpopup.md) .

### <a name="the-ribbon-view"></a>Vista de la cinta de opciones

La interfaz de usuario de la vista de la [**cinta**](windowsribbon-element-ribbon.md) de opciones es la característica principal del marco de cinta y proporciona la experiencia del usuario de próxima generación para presentar comandos en aplicaciones Windows.

La cinta de opciones es una barra de comandos que expone las características principales de una aplicación a través de una serie de pestañas en la parte superior de una ventana de la aplicación. Es similar en cuanto a funcionalidad y apariencia a la interfaz de usuario fluida de Microsoft Office 2007. La cinta de opciones proporciona un counterpoint intuitivo para el proceso de prueba y error de la detección de comandos, que es típico de los sistemas de menús estándar de Windows. Optimizado para mejorar la eficacia y la detectabilidad, la cinta facilita la búsqueda, la comprensión y el uso de comandos con clics del mouse y pulsaciones de teclas mínimos a través de un sistema de controles estándar, galerías y vista previa dinámica.

En la imagen siguiente se muestra la implementación del marco de cinta en Paint para Windows 7.

![captura de pantalla que muestra la implementación de la cinta de opciones en Paint para Windows 7.](images/overviews/screenshot-paint-win7transparency-mirror.png)

### <a name="the-contextpopup-view"></a>La vista ContextPopup

La vista [**ContextPopup**](windowsribbon-element-contextpopup.md) , a través del control [emergente de contexto](windowsribbon-controls-contextpopup.md) , proporciona un sistema de menús contextuales más completo que el que está disponible con las aplicaciones Windows anteriores. Un elemento emergente de contexto solo se puede implementar en la compatibilidad de una cinta; el marco de la cinta de opciones no admite un elemento emergente de contexto independiente.

## <a name="ribbon-architecture"></a>Arquitectura de la cinta

A diferencia del modelo de desarrollo de la interfaz de usuario de Windows tradicional basado en controles, el desarrollo de la interfaz de usuario de Windows Ribbon Framework se basa en el concepto de comandos más abstracto. Al centrarse en los comandos asociados a los controles, en lugar de los propios controles, el marco de trabajo puede ajustar automáticamente la interfaz de usuario según sea necesario en respuesta al estado de ejecución del comando recuperado de la aplicación host de la cinta de opciones.

Una aplicación que usa el marco de la cinta de opciones expone comandos sin una reserva de datos con los detalles de cómo se representa ese comando en la interfaz de usuario. Esto se conoce a veces como un modelo de interfaz de usuario basado en intenciones. El [**tipo de comando**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype), sus propiedades y sus recursos definen la intención del comando para la aplicación. Por ejemplo, la entrada del mouse, la entrada del teclado o incluso la sacudida de un dispositivo gyroscopic puede provocar la ejecución del mismo comando. la aplicación solo se ocupa de ejecutar el comando, no de la forma en que se invocó.

El marco de la cinta de opciones proporciona esta flexibilidad mediante la separación de la funcionalidad de la presentación con dos estructuras de desarrollo distintas: un lenguaje de marcado basado en lenguaje XAML (XAML) para declarar controles y el diseño visual de una implementación de la cinta, y las interfaces basadas en COM de C++ para inicializar el marco y controlar los eventos en tiempo de ejecución. Esta distinción permite a los desarrolladores y diseñadores de la interfaz de usuario ser el único responsable de la apariencia de una aplicación de cinta, mientras que la funcionalidad básica sigue siendo el dominio de los ingenieros de software.

Para obtener más información, vea [Descripción de los comandos y los controles](windowsribbon-commandscontrols.md).

### <a name="the-ribbon-apis"></a>Las API de la cinta de opciones

Las API de la cinta de opciones proporcionan las conexiones necesarias entre una vista y la aplicación host de la cinta de opciones. Estas API se componen de las siguientes interfaces y claves de propiedad:

-   Un conjunto de interfaces COM implementadas por el marco de la cinta de opciones para realizar servicios de interfaz de usuario.

    

    | Interfaz                                                                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
    |----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [IUIContextualUI****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)           | Define los métodos para la funcionalidad básica de la vista [**ContextPopup**](windowsribbon-element-contextpopup.md) .                                                                                                                                                                                                                                                                                                                                                                                                                  |
    | [IUIFramework****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)                 | Define los métodos que admiten la funcionalidad básica de las vistas de [**cinta**](windowsribbon-element-ribbon.md) de opciones y [**ContextPopup**](windowsribbon-element-contextpopup.md) .                                                                                                                                                                                                                                                                                                                                                     |
    | [IUIRibbon****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon)                       | Define los métodos para especificar la configuración y las propiedades de una vista de [**la cinta**](windowsribbon-element-ribbon.md) .                                                                                                                                                                                                                                                                                                                                                                                                                   |
    | [IUISimplePropertySet****](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) | Define un método para recuperar el valor identificado por una clave de propiedad. Esta interfaz se implementa mediante el marco de la cinta de opciones y también se implementa mediante la aplicación host para cada elemento en el objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) de una galería de elementos.<br/> Cuando se implementa mediante la aplicación host, el método definido por esta interfaz se utiliza para recuperar un valor de clave de propiedad para el elemento seleccionado en [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).<br/> |
    | [IUICollection****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)               | Define los métodos para manipular dinámicamente controles basados en colección, como QAT de la cinta de opciones y [galerías](ribbon-controls-galleries.md)basadas en colección, en tiempo de ejecución.                                                                                                                                                                                                                                                                                                                                                        |
    | [IUIImage****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                         | Define el método para recuperar una imagen para mostrarla en la interfaz de usuario de la cinta de opciones.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
    | [IUIImageFromBitmap****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap)     | Define el Factory Method para crear un objeto [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage) .                                                                                                                                                                                                                                                                                                                                                                                                                                 |

    

     

-   Un conjunto de interfaces COM implementado por la aplicación host de la cinta de opciones a la que llama el marco de trabajo en respuesta a los cambios de la interfaz de usuario.

    

    | Interfaz                                                                                  | Descripción                                                                                                  |
    |--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
    | [IUIApplication****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication)                       | Define los métodos de punto de entrada de devolución de llamada de la aplicación para el marco de cinta.                               |
    | [IUICommandHandler****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)                 | Define los métodos para recopilar información de comandos y controlar eventos de comandos desde el marco de la cinta de opciones. |
    | [IUICollectionChangedEvent****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) | Define el método necesario para controlar los cambios de una colección en tiempo de ejecución.                                   |

    

     

-   Conjunto de claves de propiedad que definen las propiedades de interfaz de usuario de las que la aplicación tiene control mediante programación.

    

    | Tipo de clave de propiedad                                                  | Descripción                                              |
    |--------------------------------------------------------------------|----------------------------------------------------------|
    | [Colección](windowsribbon-reference-properties-collection.md)    | Define las propiedades de los controles basados en la colección Ribbon. |
    | [Selector de colores](windowsribbon-reference-properties-colorpicker.md) | Define las propiedades de los controles de selector de color de la cinta.     |
    | [Fuente](windowsribbon-reference-properties-fontcontrol.md)         | Define las propiedades del FontControl de la cinta de opciones.           |
    | [Global](windowsribbon-reference-properties-framework.md)         | Define propiedades globales para el marco de la cinta de opciones.      |
    | [Recurso](windowsribbon-reference-properties-resource.md)        | Define las propiedades de los recursos de la cinta.                      |
    | [Cinta de opciones](windowsribbon-reference-properties-ribbon.md)            | Define las propiedades de la vista de la cinta.                          |
    | [State](windowsribbon-reference-properties-state.md)              | Define las propiedades para el contexto o el estado del control de la cinta.  |

    

     

### <a name="security-and-privacy"></a>Seguridad y privacidad

El archivo DLL del marco de cinta (uiribbon.dll) se ejecuta en proceso y tiene los mismos privilegios que la aplicación host. La cinta de opciones solo acepta lo que la aplicación host proporciona como entrada o como entrada del usuario de controles restringidos estrechamente como el cuadro combinado de control de número y de edición modificable.

Además, el marco no almacena de forma permanente ninguna información, excepto lo que proporciona la aplicación host o recopilada (como autorizada por el usuario final) a través del programa de experiencia del usuario de Windows de participación.

### <a name="accessibility-and-localization"></a>Accesibilidad y localización

Para proporcionar una interfaz de usuario de alta accesibilidad, el marco de cinta implementa Microsoft Active Accessibility. Al rellenar automáticamente las propiedades relevantes de Microsoft Active Accessibility con información válida y útil, el marco de trabajo reduce significativamente la carga de que los desarrolladores proporcionen una experiencia inclusiva a todos los usuarios.

Para obtener más información sobre la accesibilidad en el marco de cinta, vea [trabajar con Active Accessibility en la interfaz de usuario de Office Fluent de 2007](/previous-versions/office/developer/office-2007/bb404170(v=office.12)).

Además, el marco de cinta es una característica de Windows y, como tal, se localiza para todos los idiomas admitidos por Windows. Sin embargo, los desarrolladores son responsables de localizar sus propios recursos de aplicación concretos.

## <a name="conclusion"></a>Conclusión

La cinta de opciones es una forma nueva y atractiva de presentación de comandos que los desarrolladores, arquitectos y diseñadores de aplicaciones deben tener en cuenta al diseñar y compilar nuevas aplicaciones o actualizar las existentes.

El [Foro de desarrollo](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) de la cinta de opciones de Windows está disponible para discutir temas y formular preguntas relacionadas con el desarrollo de aplicaciones que implementan el marco de la cinta de Windows.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Declarar comandos y controles con el marcado de la cinta de opciones](windowsribbon-schema.md)
</dt> <dt>

[Instrucciones para la experiencia del usuario en cinta](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Proceso de diseño de la cinta](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

