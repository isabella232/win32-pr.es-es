---
title: Tecnologías de interfaz de usuario
description: En este tema se proporciona una breve encuesta de las tecnologías de Microsoft para desarrollar interfaces de IU para aplicaciones basadas en Windows.
ms.assetid: 5ecbaaf0-704e-4c27-b3ce-b5436e577d62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d9343672d064cf073ea8018758b90083f440bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995544"
---
# <a name="user-interface-technologies"></a>Tecnologías de interfaz de usuario

En este tema se proporciona una breve encuesta de las tecnologías de Microsoft para desarrollar interfaces de IU para aplicaciones basadas en Windows. Proporciona la información necesaria para ayudarle a determinar si va a usar una tecnología determinada e identifica dónde puede encontrar más información sobre ella.

En este tema se describen las siguientes tecnologías:

-   [Tecnologías de interfaz de usuario para aplicaciones no administradas](#user-interface-technologies-for-unmanaged-applications)
    -   [Controles de Windows](#windows-controls)
    -   [Estilos visuales](#visual-styles)
    -   [Marco de cinta de Windows](#windows-ribbon-framework)
    -   [Administrador de animaciones de Windows](#windows-animation-manager)
    -   [Administrador de ventanas de escritorio](#desktop-window-manager)
    -   [API de automatización de Windows](#windows-automation-api)
    -   [Speech API](#speech-api)
    -   [API de ampliación](#magnification-api)
    -   [Compilador de recursos](#resource-compiler)
-   [Tecnologías de interfaz de usuario para aplicaciones administradas](#user-interface-technologies-for-managed-applications)
    -   [Windows Forms](#windows-forms)
    -   [Windows Presentation Foundation](#windows-presentation-foundation)
    -   [Silverlight](#silverlight)
    -   [Expression Blend 3 + SketchFlow](/windows)
    -   [Automatización de la interfaz de usuario para aplicaciones administradas](#ui-automation-for-managed-applications)

## <a name="user-interface-technologies-for-unmanaged-applications"></a>Tecnologías de interfaz de usuario para aplicaciones no administradas

En esta sección se describen las tecnologías de Microsoft para desarrollar ius para aplicaciones Windows no administradas. Estas tecnologías están destinadas a desarrolladores de C/C++ con experiencia que están familiarizados con los conceptos de programación de WindowsAPI y que usan el kit de desarrollo de software (SDK) de Microsoft Windows. Algunas tecnologías tienen requisitos previos adicionales, como el conocimiento de los problemas de programación de gráficos o la familiaridad con los aspectos básicos de la programación del modelo de objetos componentes (COM).

### <a name="windows-controls"></a>Controles de Windows

Los controles de Windows son elementos de la interfaz de usuario que se usan junto con otra ventana (normalmente un cuadro de diálogo o ventana de cliente) para permitir que el usuario interactúe con una aplicación. Muchos de los elementos que componen la interfaz de usuario de una aplicación basada en Windows tradicional son controles de Windows, incluidos elementos como menús, barras de desplazamiento, botones, cuadros de lista, vistas de árbol, etc.

Los controles de Windows son compatibles con todas las versiones de Windows. Sin embargo, dado que los componentes en tiempo de ejecución que admiten los controles han evolucionado con el tiempo, algunos controles y características introducidos en versiones posteriores no se admiten en versiones anteriores. Las aplicaciones necesitan detectar las versiones y usar solo las características disponibles.

Debe usar los controles de Windows si desea crear una interfaz de usuario tradicional para una aplicación no administrada basada en Windows que se ejecuta en una amplia gama de versiones de Windows.

Para obtener más información, vea [controles de Windows](../controls/window-controls.md).

### <a name="visual-styles"></a>Estilos visuales

Los estilos visuales son especificaciones para la apariencia de los controles. Por ejemplo, un estilo visual puede definir la apariencia general de los controles y permitir que los desarrolladores de software configuren la interfaz visual de esos controles para que se coordinen con la apariencia de una aplicación. Además, los estilos visuales proporcionan un mecanismo para todas las aplicaciones basadas en Windows para normalizar la apariencia de una aplicación.

Los estilos visuales se admiten en Windows XP y versiones posteriores, y solo afectan a la apariencia de los controles estándar de Windows y los controles comunes de Microsoft Win32.

Debe usar estilos visuales si necesita cambiar la apariencia de los controles estándar de Windows y los controles comunes para que coincidan con la apariencia de la interfaz de usuario de la aplicación.

Para obtener más información, vea [estilos visuales](../controls/themes-overview.md).

### <a name="windows-ribbon-framework"></a>Marco de cinta de Windows

El marco de la cinta de opciones de Windows es un sistema de presentación de comandos enriquecido para aplicaciones basadas en Windows. Consta de una barra de comandos de la cinta de opciones que expone las características principales de una aplicación a través de una serie de pestañas en la parte superior de una ventana de la aplicación y un sistema de menús contextuales. El marco de cinta de Windows se admite en las siguientes versiones de Windows:

-   Windows Vista con Service Pack 2 (SP2) y la actualización de la plataforma para Windows Vista
-   Windows 7 y versiones posteriores
-   Windows Server 2008 R2
-   Windows Server 2008 con Service Pack 2 (SP2) y la actualización de la plataforma para Windows Server 2008

Debe usar el marco de la cinta de opciones de Windows si desea implementar una interfaz de usuario de comandos que es una alternativa a los menús, las barras de herramientas y los paneles de tareas de las aplicaciones Windows tradicionales.

El marco de la cinta de Windows está diseñado para desarrolladores que son expertos en la programación COM.

Para obtener más información, vea [marco de cinta de Windows](../windowsribbon/-uiplat-windowsribbon-entry.md).

### <a name="windows-animation-manager"></a>Administrador de animaciones de Windows

El administrador de animaciones de Windows admite la animación de elementos de interfaz de usuario al proporcionar un potente motor de animación y una interfaz de programación estandarizada. La plataforma simplifica el desarrollo y el mantenimiento de las secuencias de animación de la interfaz de usuario y permite a los desarrolladores implementar animaciones de IU coherentes e intuitivas. La animación de Windows se puede usar con cualquier plataforma de gráficos, como Direct2D, Microsoft Direct3D o Windows GDI+.

El marco de animación de Windows se admite en Windows Vista con actualización de plataforma para Windows VistaWindows vista con SP2 y actualización de plataforma para Windows Vista, y Windows 7 y versiones posteriores.

Debe usar el administrador de animaciones de Windows si desea agregar secuencias de animación a la interfaz de usuario de una aplicación basada en Windows no administrada.

Para obtener más información, vea [Administrador de animaciones de Windows](../uianimation/-main-portal.md).

### <a name="desktop-window-manager"></a>Administrador de ventanas de escritorio

Administrador de ventanas de escritorio (DWM) es un componente de tiempo de ejecución de Windows que admite la composición del escritorio, una característica introducida en Windows Vista. A través de la composición del escritorio, DWM permite efectos visuales en la interfaz de usuario, como los marcos de la ventana de cristal, animaciones de transición de ventanas 3D, Windows Flip y Windows Flip3D y compatibilidad con alta resolución.

DWM expone una API para controlar muchos de los efectos visuales asociados a la composición del escritorio. Por ejemplo, una aplicación puede Mostrar miniaturas, aplicar un efecto translúcido y borroso en el área cliente de las ventanas de nivel superior, controlar los efectos de transparencia y transición utilizados en la región no cliente de Windows, etc.

DWM es compatible con Windows Vista y Windows Server 2008.

Debe usar DWM si la aplicación necesita tener acceso y controlar los efectos visuales asociados a la composición del escritorio.

Para obtener más información, vea [Administrador de ventanas de escritorio](../dwm/dwm-overview.md).

### <a name="windows-automation-api"></a>API de automatización de Windows

La API de automatización de Windows ayuda a los desarrolladores a crear aplicaciones que son accesibles para la audiencia más amplia posible, incluidas las personas con visión, audición o discapacidades de movimiento. La API funciona mediante la exposición de información sobre los elementos que componen una interfaz de usuario de la aplicación. Las aplicaciones de tecnología de asistencia, como los lectores de pantalla, pueden usar la información para presentar la interfaz de usuario de forma que las personas con discapacidades puedan usarla.

La API de automatización de Windows consta de dos marcos de API independientes, Microsoft Active Accessibility y Microsoft UI Automation. Microsoft Active Accessibility es una API heredada que se presentó en Windows 95 como un complemento de plataforma. La automatización de la interfaz de usuario es el sucesor de Microsoft Active Accessibility y es una implementación de Windows de la especificación de automatización de la interfaz de usuario.

La compatibilidad total con Microsoft Active Accessibility está integrada en Windows XP y Windows Server 2003. Microsoft Active Accessibility también es compatible con Windows NT 4,0 con Service Pack 6 (SP6) y versiones posteriores, y con Windows 98. La automatización de la interfaz de usuario es compatible con los siguientes sistemas operativos: Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows Server 2008 y Windows Server 2008 R2.

Si la aplicación contiene controles personalizados u otras características de la interfaz de usuario personalizada, debe usar la API de automatización de Windows para asegurarse de que los controles y las características personalizados son totalmente accesibles. En general, los desarrolladores necesitan un nivel moderado de comprensión sobre objetos COM e interfaces, Unicode y programación de la API de Windows.

Para obtener más información, consulte [API de automatización de Windows](../winauto/windows-automation-api-portal.md).

### <a name="speech-api"></a>Speech API

Microsoft Speech API (SAPI) proporciona una interfaz de alto nivel entre una aplicación y los motores de voz. SAPI implementa todos los detalles de bajo nivel necesarios para controlar y administrar las operaciones en tiempo real de varios motores de voz.

Los dos tipos básicos de motores de SAPI son los sistemas de texto a voz (TTS) y los reconocedores de voz. Los sistemas de TTS sintetizan cadenas de texto y archivos en audio hablado mediante voces sintéticas. Los reconocedores de voz convierten el audio oral humano en archivos y cadenas de texto legibles.

Debe usar SAPI si desea implementar una interfaz de usuario que permita al usuario interactuar con la aplicación mediante el reconocimiento de voz y TTS además de los dispositivos de entrada estándar, como el teclado, el mouse y la pantalla.

Para obtener más información, vea [Microsoft Speech API (SAPI) 5,4](/previous-versions/windows/desktop/ee125663(v=vs.85)).

### <a name="magnification-api"></a>API de ampliación

La API de ampliación (MAPI) se usa para ampliar partes de la pantalla y para aplicar efectos de color y otras transformaciones. Esta API está pensada principalmente para aplicaciones de tecnología de asistencia que amplían partes de la pantalla para que sean más fáciles de ver.

MAPI es compatible con Windows Vista, Windows 7, Windows Server 2008 y Windows Server 2008 R2. Está dirigido a los desarrolladores que están familiarizados con los conceptos de programación de gráficos.

Para obtener más información, consulte ampliación de la [API](/previous-versions/windows/desktop/magapi/entry-magapi-sdk).

### <a name="resource-compiler"></a>compilador de recursos

El compilador de recursos de Microsoft Windows es una herramienta de desarrollo de aplicaciones que se usa para agregar la interfaz de usuario y otros recursos a una aplicación basada en Windows. Un recurso es cualquier dato no ejecutable utilizado por una aplicación e incluye elementos como cuadros de diálogo, menús, cadenas, cursores, iconos, mapas de bits, etc. El compilador de recursos se incluye en Microsoft Visual Studio y en el Windows SDK.

Para más información, consulte [Compilador de recursos](../menurc/resource-compiler.md).

## <a name="user-interface-technologies-for-managed-applications"></a>Tecnologías de interfaz de usuario para aplicaciones administradas

En esta sección se describen las tecnologías de Microsoft para desarrollar interfaces de IU para aplicaciones Windows administradas que se ejecutan en el contexto de la .NET Framework. Para obtener más información, vea [desarrollo de .net](/previous-versions/ff361664(v=vs.100)).

### <a name="windows-forms"></a>Windows Forms

Windows Forms es una interfaz de programación de aplicaciones gráfica para crear aplicaciones Windows administradas basadas en el .NET Framework. En Windows Forms, un formulario es una superficie visual en la que se muestra información al usuario y a través de la cual se recibe la entrada del usuario.

Cree Windows Forms aplicaciones mediante la adición de controles a formularios y el desarrollo de respuestas a las acciones del usuario, como clics del mouse o presiones de teclas. Un control es un elemento de interfaz de usuario (IU) discreto que muestra datos o acepta la entrada de datos. Windows Forms contiene diversos controles que puede agregar a los formularios: controles que muestran cuadros de texto, botones, cuadros desplegables, botones de radio e incluso páginas web. Windows Forms también admite la creación de controles personalizados.

Para obtener más información, vea [Windows Forms](/previous-versions/dotnet/netframework-4.0/cc656767(v=vs.100)).

### <a name="windows-presentation-foundation"></a>Windows Presentation Foundation

Windows Presentation Foundation (WPF) es el sucesor de [Windows Forms](/previous-versions/dotnet/netframework-4.0/cc656767(v=vs.100)). WPF es un sistema de presentación para crear y representar interfaces de usuario en aplicaciones cliente basadas en Windows y en aplicaciones hospedadas en explorador. El núcleo de WPF es un motor de representación basado en vectores e independiente de la resolución que está diseñado para sacar partido al moderno hardware gráfico. WPF amplía el núcleo con un conjunto completo de características de desarrollo de aplicaciones que incluyen Extensible Application Markup Language (XAML), controles, enlace de datos, diseño, gráficos en 2D y 3D, animación, estilos, plantillas, documentos, multimedia, texto y tipografía.

WPF se incluye en .NET Framework, lo que permite compilar aplicaciones que incorporan otros elementos de la biblioteca de clases de .NET Framework. WPF es compatible con Windows Vista, Windows 7, Windows Server 2008, Windows Server 2008 R2 y también está disponible para Windows XP con Service Pack 2 (SP2) y Windows Server 2003.

Para obtener más información, vea [Windows Presentation Foundation](/dotnet/framework/wpf/).

### <a name="silverlight"></a>Silverlight

Microsoft Silverlight es una plataforma de desarrollo eficaz para la creación de aplicaciones multimedia enriquecidas y aplicaciones empresariales para dispositivos móviles, de escritorio y Web.

En función del .NET Framework, el complemento gratuito de Silverlight funciona en varios exploradores, dispositivos y sistemas operativos para incorporar nuevas interactividad a la Web. Con amplias opciones de diseño y estilo, protocolos de comunicación potentes, acceso de datos sólido y soporte para la interacción con el usuario y los medios de alta definición, Silverlight ayuda a crear experiencias de cliente rápidas, suaves y visualmente enriquecidas. Las aplicaciones de Silverlight se pueden desarrollar rápidamente con la plataforma web de Microsoft, Visual Studio y Expression Studio.

Para obtener más información, vea [Microsoft Silverlight](/previous-versions/windows/silverlight/dotnet-windows-silverlight/cc838158(v=vs.95)).

### <a name="expression-blend-3--sketchflow"></a>Expression Blend 3 + SketchFlow

Expression Blend 3 + SketchFlow es una herramienta visual para diseñar, crear prototipos y crear interfaces de usuario sofisticadas para aplicaciones web y de escritorio de WPF y Silverlight. Para compilar una aplicación, puede dibujar formas, dibujar controles, como botones y cuadros de lista, hacer que las partes de la aplicación respondan a los clics del mouse y a otros datos proporcionados por el usuario, y aplicar estilo a todo para que tenga una apariencia única.

Para obtener más información, vea [prototipos con SketchFlow](/previous-versions/visualstudio/design-tools/expression-studio-3/ee341458(v=expression.30)).

### <a name="ui-automation-for-managed-applications"></a>Automatización de la interfaz de usuario para aplicaciones administradas

La automatización de la interfaz de usuario es un marco de accesibilidad para Windows, disponible en todos los sistemas operativos compatibles con WPF.

La automatización de la interfaz de usuario proporciona acceso mediante programación a la mayoría de los elementos de la interfaz de usuario en el escritorio, lo que permite a los productos de tecnología de asistencia como lectores de pantalla proporcionar información sobre la interfaz de usuario a los usuarios finales y manipular la interfaz de usuario por medio de la entrada estándar. UI Automation también permite que los scripts de pruebas automatizadas interactúen con la interfaz de usuario.

Para obtener más información, vea [automatización de la interfaz de usuario para aplicaciones administradas](/dotnet/framework/ui-automation/).

 

 