---
title: Presentación del marco de Windows ribbon
description: Vea la página de aterrizaje del marco Windows Ribbon, que es una alternativa a los menús en capas, las barras de herramientas y los paneles de tareas de las aplicaciones Windows tradicionales.
ms.assetid: bc19d5eb-e3a4-4022-8051-512cb3a3e065
keywords:
- Windows Ribbon,framework
- Ribbon,framework
- Windows Cinta de opciones, acerca de
- Cinta de opciones, acerca de
- Windows Cinta de opciones, componentes
- Cinta de opciones, componentes
- Windows Cinta de opciones, vistas
- Cinta de opciones, vistas
- Windows Cinta de opciones, arquitectura
- Cinta de opciones, arquitectura
- Windows Cinta de opciones, API
- Cinta de opciones, API
- Windows Cinta de opciones, seguridad
- Cinta de opciones, seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db15165b91708a85e5ae6237b66a15bf733e80a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572237"
---
# <a name="introducing-the-windows-ribbon-framework"></a>Presentación del marco de Windows ribbon

El marco Windows ribbon es un sistema de presentación de comandos enriquecido que proporciona una alternativa moderna a los menús en capas, las barras de herramientas y los paneles de tareas de las aplicaciones Windows tradicionales.

-   [Un nuevo paradigma de comandos](#a-new-command-paradigm)
-   [Vistas](#views)
    -   [Vista de la cinta de opciones](#the-ribbon-view)
    -   [La vista ContextPopup](#the-contextpopup-view)
-   [Arquitectura de la cinta de opciones](#ribbon-architecture)
    -   [LAS API de la cinta de opciones](#the-ribbon-apis)
    -   [Seguridad y privacidad](#security-and-privacy)
    -   [Accesibilidad y localización](#accessibility-and-localization)
-   [Conclusión](#conclusion)
-   [Temas relacionados](#related-topics)

## <a name="a-new-command-paradigm"></a>Un nuevo paradigma de comandos

El marco de la cinta de opciones es una colección de API de Microsoft Win32 que admiten una gran cantidad de nuevas funcionalidades de interfaz de usuario para Windows desarrolladores.

Este marco de comandos de interfaz de usuario moderno y enriquecido ofrece:

-   Implementación sencilla para nuevas aplicaciones de marco de cinta y migración sencilla de aplicaciones Win32 existentes.
-   Apariencia y comportamiento coherentes en las aplicaciones de cinta de opciones.
-   Adherencia a las directrices de la interfaz de usuario de Windows para una experiencia de Windows de primera clase a través de estándares de accesibilidad, compatibilidad con el estilo visual (tema), ajustes automáticos de contraste alto y reconocimiento de puntos altos por pulgada (ppp).

El marco de la cinta de opciones consta de dos componentes de interfaz de usuario principales:

-   La barra de comandos de la cinta de opciones, que se compone de la barra de herramientas de acceso rápido (QAT) que expone y resalta varios comandos de la cinta de opciones según lo especificado por el usuario o la aplicación, y una fila de tabulación que contiene el menú de la aplicación, las pestañas estándar o contextual y un botón de ayuda.
-   Un sistema de menú contextual enriquecido.

Se usa una combinación de interfaces XML declarativas y COM nativas para desacoplar la presentación y la funcionalidad de estos componentes.

## <a name="views"></a>Vistas

Los componentes principales de la interfaz de usuario del marco de la cinta de opciones, la barra de comandos de la cinta de opciones y el sistema de menús contextuales, se diferencian estructuralmente a través de *Vistas*. El marco admite dos vistas: la vista [**de cinta**](windowsribbon-element-ribbon.md) de opciones y la [**vista ContextPopup.**](windowsribbon-element-contextpopup.md)

### <a name="the-ribbon-view"></a>Vista de la cinta de opciones

La interfaz de usuario de [**la vista de**](windowsribbon-element-ribbon.md) cinta de opciones es la característica principal del marco de la cinta de opciones y proporciona la experiencia del usuario de próxima generación para presentar comandos en Windows aplicaciones.

La cinta de opciones es una barra de comandos que expone las características principales de una aplicación a través de una serie de pestañas en la parte superior de una ventana de la aplicación. Es similar en funcionalidad y apariencia a la interfaz de usuario de Microsoft Office 2007 Fluent 2007. La cinta de opciones proporciona un contrapunto intuitivo al proceso de prueba y error de detección de comandos que es típico de los sistemas de menús Windows estándar. Optimizada para la eficacia y la detectabilidad, la cinta facilita la búsqueda, comprensión y uso de comandos con clics y pulsaciones de teclas mínimos del mouse a través de un sistema de controles estándar, galerías y vista previa en vivo.

En la imagen siguiente se muestra la implementación del marco de la cinta Paint para Windows 7.

![captura de pantalla que muestra la implementación de la cinta de opciones en pintura para Windows 7.](images/overviews/screenshot-paint-win7transparency-mirror.png)

### <a name="the-contextpopup-view"></a>La vista ContextPopup

La [**vista ContextPopup,**](windowsribbon-element-contextpopup.md) a través del control [Context Popup,](windowsribbon-controls-contextpopup.md) proporciona un sistema de menús contextuales más completo que el que está disponible con las Windows anteriores. Un elemento Popup de contexto solo se puede implementar en compatibilidad con una cinta de opciones; el marco de la cinta de opciones no admite un elemento Popup de contexto independiente.

## <a name="ribbon-architecture"></a>Arquitectura de la cinta de opciones

A diferencia del modelo de desarrollo de IU Windows basado en control tradicional, Windows desarrollo de la interfaz de usuario del marco de la cinta de opciones se basa en el concepto más abstracto de comandos. Al centrarse en los comandos asociados a los controles, en lugar de en los propios controles, el marco de trabajo puede ajustar automáticamente la interfaz de usuario según sea necesario en respuesta al estado de ejecución del comando recuperado de la aplicación host de la cinta de opciones.

Una aplicación que usa el marco de la cinta de opciones expone comandos sin que se le acomenten los detalles de cómo se representa ese comando en la interfaz de usuario. Esto se conoce a veces como un modelo de interfaz de usuario basado en intenciones. El [**tipo de comando**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype), sus propiedades y sus recursos definen la intención del comando para la aplicación. Por ejemplo, la entrada del mouse, la entrada del teclado o incluso el movimiento de un dispositivo giroscopio pueden dar lugar a la ejecución del mismo comando, la aplicación solo se preocupa de ejecutar el comando, no de cómo se invocó.

El marco de la cinta de opciones proporciona esta flexibilidad separando la funcionalidad de la presentación con dos estructuras de desarrollo distintas: un lenguaje de marcado basado en lenguaje XAML (XAML) para declarar controles y el diseño visual de una implementación de la cinta de opciones e interfaces basadas en COM de C++ para inicializar el marco y controlar los eventos en tiempo de ejecución. Esta distinción permite a los desarrolladores y diseñadores de la interfaz de usuario ser los únicos responsables de la apariencia de una aplicación de cinta de opciones, mientras que la funcionalidad principal sigue siendo el dominio de los ingenieros de software.

Para obtener más información, vea [Understanding Commands and Controls](windowsribbon-commandscontrols.md).

### <a name="the-ribbon-apis"></a>LAS API de la cinta de opciones

Las API de la cinta de opciones proporcionan las conexiones necesarias entre una vista y la aplicación host de la cinta. Estas API constan de las siguientes interfaces y claves de propiedad:

-   Conjunto de interfaces COM implementadas por el marco de la cinta de opciones para realizar servicios de interfaz de usuario.

    

    | Interfaz                                                                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
    |----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)           | Define los métodos para la funcionalidad principal de [**la vista ContextPopup.**](windowsribbon-element-contextpopup.md)                                                                                                                                                                                                                                                                                                                                                                                                                  |
    | [IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)                 | Define los métodos que admiten la funcionalidad principal de las vistas [**Ribbon**](windowsribbon-element-ribbon.md) y [**ContextPopup.**](windowsribbon-element-contextpopup.md)                                                                                                                                                                                                                                                                                                                                                     |
    | [IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon)                       | Define los métodos para especificar la configuración y las propiedades de una vista de [**cinta**](windowsribbon-element-ribbon.md) de opciones.                                                                                                                                                                                                                                                                                                                                                                                                                   |
    | [IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) | Define un método para recuperar el valor identificado por una clave de propiedad. Esta interfaz se implementa mediante el marco de la cinta de opciones y también se implementa mediante la aplicación host para cada elemento del objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) de una galería de elementos.<br/> Cuando se implementa mediante la aplicación host, el método definido por esta interfaz se usa para recuperar un valor de clave de propiedad para el elemento seleccionado en [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).<br/> |
    | [IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)               | Define los métodos para manipular dinámicamente los controles basados en [colecciones,](ribbon-controls-galleries.md)como el QAT de la cinta de opciones y las galerías basadas en colecciones, en tiempo de ejecución.                                                                                                                                                                                                                                                                                                                                                        |
    | [IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                         | Define el método para recuperar una imagen para mostrarla en la interfaz de usuario de la cinta de opciones.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
    | [IUIImageFromBitmap**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap)     | Define el método de generador para crear un [**objeto IUIImage.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                                                                                                                                                                                                                                                                                                                                                                                                                                 |

    

     

-   Conjunto de interfaces COM implementadas por la aplicación host de la cinta de opciones a la que el marco llama en respuesta a los cambios de la interfaz de usuario.

    

    | Interfaz                                                                                  | Descripción                                                                                                  |
    |--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
    | [IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication)                       | Define los métodos de punto de entrada de devolución de llamada de aplicación para el marco de la cinta de opciones.                               |
    | [IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)                 | Define los métodos para recopilar información de comandos y controlar eventos command desde el marco de la cinta de opciones. |
    | [IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) | Define el método necesario para controlar los cambios en una colección en tiempo de ejecución.                                   |

    

     

-   Conjunto de claves de propiedad que definen las propiedades de interfaz de usuario sobre las que la aplicación tiene control mediante programación.

    

    | Tipo de clave de propiedad                                                  | Descripción                                              |
    |--------------------------------------------------------------------|----------------------------------------------------------|
    | [Colección](windowsribbon-reference-properties-collection.md)    | Define las propiedades de los controles basados en colecciones de la cinta de opciones. |
    | [Selector de colores](windowsribbon-reference-properties-colorpicker.md) | Define las propiedades de los controles selectores de colores de la cinta de opciones.     |
    | [Font](windowsribbon-reference-properties-fontcontrol.md)         | Define las propiedades de FontControl de la cinta de opciones.           |
    | [Global](windowsribbon-reference-properties-framework.md)         | Define las propiedades globales para el marco de la cinta de opciones.      |
    | [Recurso](windowsribbon-reference-properties-resource.md)        | Define las propiedades de recursos de la cinta de opciones.                      |
    | [Cinta de opciones](windowsribbon-reference-properties-ribbon.md)            | Define las propiedades de la vista de la cinta de opciones.                          |
    | [State](windowsribbon-reference-properties-state.md)              | Define las propiedades para el contexto o el estado de control de la cinta de opciones.  |

    

     

### <a name="security-and-privacy"></a>Seguridad y privacidad

El archivo DLL del marco de opciones (uiribbon.dll) se ejecuta en proceso y tiene los mismos privilegios que la aplicación host. La cinta de opciones solo acepta lo que la aplicación host proporciona como entrada o entrada del usuario desde controles estrechamente restringidos, como el control de número y el cuadro combinado editable.

Además, el marco de trabajo no almacena permanentemente ninguna información excepto la proporcionada por la aplicación host o recopilada (según lo autorizado por el usuario final) a través del Programa de experiencia del usuario Windows participar.

### <a name="accessibility-and-localization"></a>Accesibilidad y localización

Para proporcionar una interfaz de usuario de alta accesibilidad, el marco de la cinta de opciones implementa Microsoft Active Accessibility. Al rellenar automáticamente las propiedades de Microsoft Active Accessibility relevantes con información válida y útil, el marco reduce significativamente la carga para que los desarrolladores proporcionen una experiencia inclusiva para todos los usuarios.

Para obtener más información sobre la accesibilidad en el marco de la cinta de opciones, vea [Working with Active Accessibility in the 2007 Office Fluent Interfaz de usuario](/previous-versions/office/developer/office-2007/bb404170(v=office.12)).

Además, el marco de la cinta de opciones es Windows característica y, como tal, se localiza para todos los idiomas que Windows admite. Sin embargo, los desarrolladores son responsables de la localización de sus propios recursos de aplicación específicos.

## <a name="conclusion"></a>Conclusión

La cinta de opciones es una forma nueva y atractiva de presentación de comandos que los desarrolladores, arquitectos y diseñadores de aplicaciones deben tener en cuenta al diseñar y compilar nuevas aplicaciones o actualizar las existentes.

El [foro Windows desarrollo de la](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) cinta de opciones está disponible para analizar temas y hacer preguntas relacionadas con el desarrollo de aplicaciones que implementan el marco Windows Ribbon.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Declarar comandos y controles con marcado de cinta de opciones](windowsribbon-schema.md)
</dt> <dt>

[Directrices de la experiencia del usuario de la cinta de opciones](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Proceso de diseño de la cinta de opciones](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

