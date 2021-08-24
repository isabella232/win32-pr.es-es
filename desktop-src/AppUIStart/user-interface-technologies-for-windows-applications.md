---
title: Interfaz de usuario Technologies
description: En este tema se proporciona una breve encuesta de las tecnologías de Microsoft para desarrollar uri de Windows basadas en aplicaciones.
ms.assetid: 5ecbaaf0-704e-4c27-b3ce-b5436e577d62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a36bbf73d5b319e04ba2b02570c6fce4124a9ec6d54fcec201e77c4c9487dfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702325"
---
# <a name="user-interface-technologies"></a>Interfaz de usuario Technologies

En este tema se proporciona una breve encuesta de las tecnologías de Microsoft para desarrollar uri de Windows basadas en aplicaciones. Proporciona la información necesaria para ayudarle a determinar si usar una tecnología determinada e identifica dónde puede encontrar más información sobre ella.

En este tema se describen las tecnologías siguientes:

-   [Interfaz de usuario para aplicaciones no administradas](#user-interface-technologies-for-unmanaged-applications)
    -   [Windows Controles](#windows-controls)
    -   [Estilos visuales](#visual-styles)
    -   [Windows Marco de la cinta de opciones](#windows-ribbon-framework)
    -   [Windows Administrador de animaciones](#windows-animation-manager)
    -   [Administrador de ventanas de escritorio](#desktop-window-manager)
    -   [API de automatización de Windows](#windows-automation-api)
    -   [Speech API](#speech-api)
    -   [API de ampliación](#magnification-api)
    -   [Compilador de recursos](#resource-compiler)
-   [Interfaz de usuario Technologies for Managed Applications](#user-interface-technologies-for-managed-applications)
    -   [Windows Forms](#windows-forms)
    -   [Windows Presentation Foundation](#windows-presentation-foundation)
    -   [Silverlight](#silverlight)
    -   [Expression Blend 3 + SketchFlow](/windows)
    -   [Automatización de la interfaz de usuario para aplicaciones administradas](#ui-automation-for-managed-applications)

## <a name="user-interface-technologies-for-unmanaged-applications"></a>Interfaz de usuario para aplicaciones no administradas

En esta sección se describen las tecnologías de Microsoft para desarrollar interfaces de usuario para aplicaciones Windows no administradas. Estas tecnologías están destinadas a desarrolladores experimentados de C/C++ que están familiarizados con los conceptos de programación de WindowsAPI y que usan el Kit de desarrollo de software (SDK) de Microsoft Windows. Algunas tecnologías tienen requisitos previos adicionales, como el conocimiento de problemas de programación de gráficos o la familiaridad con los conceptos básicos de la programación del modelo de objetos componentes (COM).

### <a name="windows-controls"></a>Windows Controles

Windows controles son elementos de la interfaz de usuario que se usan junto con otra ventana (normalmente una ventana de cliente o un cuadro de diálogo) para permitir que el usuario interactúe con una aplicación. Muchos de los elementos que son la interfaz de usuario de una aplicación tradicional basada en Windows son controles Windows, incluidos elementos como menús, barras de desplazamiento, botones, cuadros de lista, vistas de árbol, entre otros.

Windows admiten todos los controles de Windows. Sin embargo, dado que los componentes en tiempo de ejecución que admiten los controles han evolucionado con el tiempo, algunos controles y características introducidos en versiones posteriores no se admiten en versiones anteriores. Las aplicaciones deben detectar las versiones y usar solo las características disponibles.

Debe usar Windows si desea crear una interfaz de usuario tradicional para una aplicación no administrada basada en Windows que se ejecuta en una amplia variedad de Windows versiones.

Para obtener más información, [vea Windows Controles](../controls/window-controls.md).

### <a name="visual-styles"></a>Estilos visuales

Los estilos visuales son especificaciones para la apariencia de los controles. Por ejemplo, un estilo visual puede definir la apariencia general de los controles y permitir que los desarrolladores de software configuren la interfaz visual de esos controles para coordinarse con la apariencia de una aplicación. Además, los estilos visuales proporcionan un mecanismo para que todas las Windows basadas en aplicaciones normalizar la apariencia de una aplicación.

Los estilos visuales se admiten en Windows XP y versiones posteriores, y solo afectan a la apariencia de los controles Windows estándar y los controles comunes de Microsoft Win32.

Debe usar estilos visuales si necesita cambiar la apariencia de los controles Windows estándar y los controles comunes para que coincidan con el aspecto de la interfaz de usuario de la aplicación.

Para obtener más información, vea [Estilos visuales](../controls/themes-overview.md).

### <a name="windows-ribbon-framework"></a>Windows Marco de la cinta de opciones

El marco Windows Ribbon es un completo sistema de presentación de comandos para Windows basadas en aplicaciones. Consta de una barra de comandos de la cinta de opciones que expone las características principales de una aplicación a través de una serie de pestañas en la parte superior de una ventana de la aplicación y un sistema de menús contextuales. El marco Windows ribbon de Windows se admite en las siguientes versiones de Windows:

-   Windows Vista con Service Pack 2 (SP2) y Platform Update para Windows Vista
-   Windows 7 y versiones posteriores
-   Windows Server 2008 R2
-   Windows Server 2008 con Service Pack 2 (SP2) y actualización de plataforma para Windows Server 2008

Debe usar el marco Windows ribbon si desea implementar una interfaz de usuario de comandos que sea una alternativa a los menús en capas, las barras de herramientas y los paneles de tareas de las aplicaciones Windows tradicionales.

El Windows ribbon está pensado para desarrolladores que son expertos en programación COM.

Para obtener más información, [vea Windows Ribbon Framework](../windowsribbon/-uiplat-windowsribbon-entry.md).

### <a name="windows-animation-manager"></a>Windows Administrador de animaciones

El Windows Animation Manager admite la animación de elementos de la interfaz de usuario proporcionando un motor de animación eficaz y una interfaz de programación estandarizada. La plataforma simplifica el desarrollo y el mantenimiento de secuencias de animación de interfaz de usuario y permite a los desarrolladores implementar animaciones de interfaz de usuario coherentes e intuitivas. Windows La animación se puede usar con cualquier plataforma gráfica, como Direct2D, Microsoft Direct3D o Windows GDI+.

El marco de animación Windows se admite en Windows Vista con la actualización de plataforma para Windows VistaWindows Vista con SP2 y Platform Update para Windows Vista y Windows 7 y versiones posteriores.

Debe usar Windows Animation Manager si desea agregar secuencias de animación a la interfaz de usuario de una aplicación Windows no administrada.

Para obtener más información, [vea Windows Animation Manager](../uianimation/-main-portal.md).

### <a name="desktop-window-manager"></a>Administrador de ventanas de escritorio

Administrador de ventanas de escritorio (DWM) es un Windows en tiempo de ejecución que admite la composición de escritorio, una característica introducida en Windows Vista. A través de la composición de escritorio, DWM permite efectos visuales en la interfaz de usuario, como marcos de ventanas de cristal, animaciones de transición de ventanas 3D, Windows Flip y Windows Flip3D y compatibilidad con alta resolución.

DWM expone una API para controlar muchos de los efectos visuales asociados a la composición del escritorio. Por ejemplo, una aplicación puede mostrar miniaturas, aplicar un efecto translúcido y desenfocado al área cliente de las ventanas de nivel superior, controlar los efectos de transparencia y transición usados en la región no cliente de windows, y así sucesivamente.

DWM se admite en Windows Vista y Windows Server 2008.

Debe usar DWM si la aplicación necesita acceder y controlar los efectos visuales asociados a la composición del escritorio.

Para obtener más información, [vea Administrador de ventanas de escritorio](../dwm/dwm-overview.md).

### <a name="windows-automation-api"></a>API de automatización de Windows

La API Windows Automation ayuda a los desarrolladores a crear aplicaciones que son accesibles para el público más amplio posible, incluidas las personas con discapacidades de visión, escucha o movimiento. La API funciona exponiendo información sobre los elementos que integran una interfaz de usuario de la aplicación. Las aplicaciones de tecnología de asistencia, como los lectores de pantalla, pueden usar la información para presentar la interfaz de usuario de una manera que puedan usar las personas con discapacidades.

La WINDOWS Automation API consta de dos marcos de API independientes, Microsoft Active Accessibility y Microsoft Automatización de la interfaz de usuario. Microsoft Active Accessibility es una API heredada que se introdujo en Windows 95 como complemento de plataforma. Automatización de la interfaz de usuario es el sucesor de Microsoft Active Accessibility y es una Windows implementación de la especificación Automatización de la interfaz de usuario datos.

La compatibilidad total con Microsoft Active Accessibility está integrada en Windows XP y Windows Server 2003. Microsoft Active Accessibility también se admite en Windows NT 4.0 con Service Pack 6 (SP6) y versiones posteriores, y Windows 98. Automatización de la interfaz de usuario es compatible con los siguientes sistemas operativos: Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows Server 2008 y Windows Server 2008 R2.

Si la aplicación contiene controles personalizados u otras características de interfaz de usuario personalizadas, debe usar la API de automatización de Windows para asegurarse de que los controles y características personalizados son totalmente accesibles. En general, los desarrolladores necesitan un nivel moderado de comprensión sobre objetos COM e interfaces, Unicode y Windows API.

Para obtener más información, [consulte Windows Automation API](../winauto/windows-automation-api-portal.md).

### <a name="speech-api"></a>Speech API

Microsoft Speech API (SAPI) proporciona una interfaz de alto nivel entre una aplicación y los motores de voz. SAPI implementa todos los detalles de bajo nivel necesarios para controlar y administrar las operaciones en tiempo real de varios motores de voz.

Los dos tipos básicos de motores SAPI son sistemas de texto a voz (TTS) y reconocedores de voz. Los sistemas TTS sintetizan cadenas de texto y archivos en audio hablado mediante voces sintéticas. Los reconocedores de voz convierten el audio hablado por el usuario en archivos y cadenas de texto legibles.

Debe usar SAPI si desea implementar una interfaz de usuario que permita al usuario interactuar con la aplicación a través de TTS y el reconocimiento de voz, además de los dispositivos de entrada estándar, como el teclado, el mouse y la pantalla.

Para obtener más información, vea [Microsoft Speech API (SAPI) 5.4](/previous-versions/windows/desktop/ee125663(v=vs.85)).

### <a name="magnification-api"></a>API de ampliación

La API de ampliación (MAPI) se usa para ampliar partes de la pantalla y para aplicar efectos de color y otras transformaciones. Esta API está pensada principalmente para aplicaciones de tecnología de asistencia que amplían partes de la pantalla para que sean más fáciles de ver.

SMTP se admite en Windows Vista, Windows 7, Windows Server 2008 y Windows Server 2008 R2. Está pensado para desarrolladores que están familiarizados con los conceptos de programación de gráficos.

Para obtener más información, consulte [La API de ampliación](/previous-versions/windows/desktop/magapi/entry-magapi-sdk).

### <a name="resource-compiler"></a>compilador de recursos

Microsoft Windows Resource Compiler es una herramienta de desarrollo de aplicaciones que se usa para agregar la interfaz de usuario y otros recursos a una Windows basada en aplicaciones. Un recurso es cualquier dato no ejecutable que usa una aplicación e incluye elementos como cuadros de diálogo, menús, cadenas, cursores, iconos, mapas de bits, entre otros. El compilador de recursos se incluye en Microsoft Visual Studio y el SDK Windows.

Para más información, consulte [Compilador de recursos](../menurc/resource-compiler.md).

## <a name="user-interface-technologies-for-managed-applications"></a>Interfaz de usuario Technologies for Managed Applications

En esta sección se describen las tecnologías de Microsoft para desarrollar uri para aplicaciones Windows administradas que se ejecutan en el contexto del .NET Framework. Para obtener más información, vea [Desarrollo de .NET.](/previous-versions/ff361664(v=vs.100))

### <a name="windows-forms"></a>Windows Forms

Windows Forms es una interfaz gráfica de programación de aplicaciones para crear aplicaciones Windows administradas basadas en el .NET Framework. En Windows Forms, un formulario es una superficie visual en la que se muestra información al usuario y a través de la cual se recibe la entrada del usuario.

Para compilar aplicaciones Windows Forms, agregue controles a formularios y desarrolle respuestas a las acciones del usuario, como clics del mouse o pulsaciones de tecla. Un control es un elemento de interfaz de usuario (IU) discreto que muestra datos o acepta la entrada de datos. Windows Forms contiene diversos controles que puede agregar a los formularios: controles que muestran cuadros de texto, botones, cuadros desplegables, botones de radio e incluso páginas web. Windows Los formularios también admiten la creación de controles personalizados.

Para obtener más información, [vea Windows Forms](/previous-versions/dotnet/netframework-4.0/cc656767(v=vs.100)).

### <a name="windows-presentation-foundation"></a>Windows Presentation Foundation

Windows Presentation Foundation (WPF) es el sucesor de [Windows Forms.](/previous-versions/dotnet/netframework-4.0/cc656767(v=vs.100)) WPF es un sistema de presentación para compilar y representar interfaces de usuario en Windows aplicaciones cliente basadas en el explorador y aplicaciones hospedadas en explorador. El núcleo de WPF es un motor de representación basado en vectores e independiente de la resolución que está diseñado para sacar partido al moderno hardware gráfico. WPF amplía el núcleo con un conjunto completo de características de desarrollo de aplicaciones que incluyen Extensible Application Markup Language (XAML), controles, enlace de datos, diseño, gráficos en 2D y 3D, animación, estilos, plantillas, documentos, multimedia, texto y tipografía.

WPF se incluye en .NET Framework, lo que permite compilar aplicaciones que incorporan otros elementos de la biblioteca de clases de .NET Framework. WPF se admite en Windows Vista, Windows 7, Windows Server 2008, Windows Server 2008 R2 y también está disponible para Windows XP con Service Pack 2 (SP2) y Windows Server 2003.

Para obtener más información, [vea Windows Presentation Foundation](/dotnet/framework/wpf/).

### <a name="silverlight"></a>Silverlight

Microsoft Silverlight es una plataforma de desarrollo eficaz para crear aplicaciones multimedia enriquecciones y aplicaciones empresariales para dispositivos web, de escritorio y móviles.

Según la .NET Framework, el complemento silverlight gratuito funciona en varios exploradores, dispositivos y sistemas operativos para aportar nueva interactividad a la Web. Con amplias opciones de diseño y estilo, eficaces protocolos de comunicación, un acceso a datos sólido y compatibilidad con la interacción del usuario y medios de alta definición, Silverlight ayuda a crear experiencias de cliente rápidas, fluidas y visualmente enriquecciones. Las aplicaciones de Silverlight se pueden desarrollar rápidamente con Plataforma web de Microsoft, Visual Studio y Expression Studio.

Para obtener más información, vea [Microsoft Silverlight](/previous-versions/windows/silverlight/dotnet-windows-silverlight/cc838158(v=vs.95)).

### <a name="expression-blend-3--sketchflow"></a>Expression Blend 3 + SketchFlow

Expression Blend 3 + SketchFlow es una herramienta visual para diseñar, crear prototipos y crear interfaces de usuario sofisticadas para aplicaciones web y de escritorio de WPF y Silverlight. Puede compilar una aplicación dibujando formas, dibujando controles como botones y cuadros de lista, haciendo que las partes de la aplicación respondan a los clics del mouse y a otras entradas del usuario, y aplicar estilos a todo para que se parezcan de forma única a los suyos propios.

Para obtener más información, [vea Creación de prototipos con SketchFlow.](/previous-versions/visualstudio/design-tools/expression-studio-3/ee341458(v=expression.30))

### <a name="ui-automation-for-managed-applications"></a>Automatización de la interfaz de usuario para aplicaciones administradas

Automatización de la interfaz de usuario es un marco de accesibilidad para Windows, disponible en todos los sistemas operativos que admiten WPF.

Automatización de la interfaz de usuario proporciona acceso mediante programación a la mayoría de los elementos de la interfaz de usuario en el escritorio, lo que permite que los productos de tecnología de asistencia, como los lectores de pantalla, proporcionen información sobre la interfaz de usuario a los usuarios finales y manipulen la interfaz de usuario por medios distintos de la entrada estándar. Automatización de la interfaz de usuario también permite que los scripts de prueba automatizados interactúen con la interfaz de usuario.

Para obtener más información, [vea Automatización de la interfaz de usuario para aplicaciones administradas.](/dotnet/framework/ui-automation/)

 

 