---
description: Comience a aprender los aspectos básicos de la creación de excelentes aplicaciones de escritorio en esta sección.
ms.assetid: 15690E05-9AF7-41A3-AF7C-8DB7C5FB9BE4
title: Primeros pasos
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84879e6373f4bfeb5a7e4b6a6138423d7688afe2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705355"
---
# <a name="get-started-with-desktop-windows-apps-that-use-the-win32-api"></a>Introducción a las aplicaciones de escritorio de Windows que usan la API Win32

Win32 API (también conocida como la API de Windows) es la plataforma original para aplicaciones Windows en C y C++ nativas que requieren acceso directo a Windows y al hardware. Proporciona una experiencia de desarrollo de primera clase sin depender de un entorno de tiempo de ejecución administrado como .NET y WinRT (para aplicaciones UWP para Windows 10). Esto hace que Win32 API sea la plataforma preferida para las aplicaciones que necesitan el mayor nivel de rendimiento y acceso directo al hardware del sistema.

> [!NOTE]
> En esta documentación se explica cómo crear aplicaciones de escritorio de Windows con la API de Win32. La API de Win32 es una de las diversas plataformas de aplicaciones que puede usar para compilar aplicaciones de escritorio de Windows. Para obtener más información sobre otras plataformas de aplicaciones, consulte [elección de la plataforma](/windows/apps/desktop/choose-your-platform).

## <a name="get-set-up"></a>Prepárate

Siga estas instrucciones e inicie la creación de aplicaciones de escritorio para Windows 10 que usan la API de Win32.

1. Descargue o actualice Visual Studio 2019. Si todavía no tienes Visual Studio 2019, puedes instalar Microsoft Visual Studio Community 2019 de forma gratuita. Al instalar Visual Studio, asegúrese de seleccionar la opción **desarrollo de escritorio con C++** . Para obtener vínculos de descarga, consulte nuestra página de [descargas](https://developer.microsoft.com/windows/downloads) .

    > [!NOTE]
    > Al instalar Visual Studio, puede seleccionar opcionalmente el desarrollo de **escritorio de .net** y las opciones de **desarrollo de plataforma universal de Windows** para el acceso a otros tipos de proyectos y plataformas de aplicaciones para crear aplicaciones de escritorio de Windows.

2. Si desea compilar la aplicación de escritorio en un [paquete de MSIX](/windows/msix/desktop/desktop-to-uwp-root) y probar o depurar la aplicación empaquetada en el equipo de desarrollo, deberá habilitar el [modo de Desarrollador en el equipo](/windows/uwp/get-started/enable-your-device-for-development).

> [!NOTE]
> En el caso de los scripts que puede usar para configurar el equipo de desarrollo e instalar otras características o paquetes, consulte [este proyecto de github](https://github.com/Microsoft/windows-dev-box-setup-scripts).

## <a name="learn-how-to-create-desktop-apps-using-the-win32-api"></a>Aprenda a crear aplicaciones de escritorio mediante la API de Win32

Si no está familiarizado con la creación de aplicaciones de escritorio mediante la API de Win32, los siguientes tutoriales y artículos le ayudarán a empezar.

| Tema        | Descripción      |
|---------------|-----------------|
| [Cree su primera aplicación Win32 de C++](LearnWin32/learn-to-program-for-windows.md)    | En este tutorial aprenderá a escribir un programa de Windows en C++ con las API de Win32 y COM.  |
| [Creación de la primera aplicación con DirectX](direct3dgetstarted/building-your-first-directx-app.md) | Este tutorial básico le ayudará a empezar a trabajar con el desarrollo de aplicaciones de DirectX.            |
| [Guía de programación de Windows de 64 bits](WinProg64/programming-guide-for-64-bit-windows.md)    | Describe la programación para las versiones de 64 bits del sistema operativo Windows. |
| [Usar los encabezados de Windows](WinProg/using-the-windows-headers.md)     | Proporciona información general sobre algunas de las convenciones usadas en los archivos de encabezado de Windows. |

También puede examinar los [ejemplos de aplicaciones de escritorio](https://github.com/Microsoft/Windows-classic-samples).

## <a name="modernize-your-desktop-apps-for-windows-10"></a>Modernización de las aplicaciones de escritorio para Windows 10

Si tiene una aplicación de escritorio de Win32 existente, hay muchas características en el Plataforma universal de Windows (UWP) que puede usar para ofrecer la mejor experiencia posible en Windows 10. Por ejemplo, a partir de Windows 10, versión 1903, puede hospedar controles XAML de UWP en la aplicación Win32 de escritorio mediante una característica denominada islas XAML.

La mayoría de estas características de UWP están disponibles como componentes modulares que puede adoptar en su aplicación de escritorio a su propio ritmo sin tener que volver a escribir toda la aplicación. Puede mejorar la aplicación de escritorio existente eligiendo qué partes de Windows 10 y UWP adoptar.

Para más información, consulta [Modernización de las aplicaciones de escritorio](/windows/apps/desktop/modernize).

## <a name="cwinrt"></a>C++/WinRT

Opcionalmente, puede configurar el equipo de desarrollo para usar [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/). C++/WinRT es una proyección del lenguaje C++ 17 totalmente estándar que le permite usar fácilmente Windows Runtime API Windows Runtime (WinRT) de la aplicación de escritorio Win32 de C++. C++/WinRT se implementa como una biblioteca basada en archivos de encabezado.

Para configurar el proyecto para C++/WinRT:

* En el caso de los proyectos nuevos, puedes instalar la [extensión de Visual Studio para C++/WinRT (VSIX)](https://marketplace.visualstudio.com/items?itemName=CppWinRTTeam.cppwinrt101804264) y usar una de las plantillas de proyecto de C++/WinRT incluidas en esa extensión.
* En el caso de los proyectos de aplicación de escritorio de Windows existentes, puede instalar el paquete NuGet [Microsoft. Windows. CppWinRT](https://www.nuget.org/packages/Microsoft.Windows.CppWinRT/) en el proyecto.

Para obtener más información sobre estas opciones, consulta [este artículo](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt#visual-studio-support-for-cwinrt-xaml-the-vsix-extension-and-the-nuget-package).

## <a name="whats-new-for-win32-apis-in-windows-10"></a>Novedades de las API de Win32 en Windows 10

Para obtener información sobre las nuevas API de Win32 que se han introducido en Windows 10, consulte [novedades](whats-new.md).

## <a name="get-started-with-win32-features-and-technologies"></a>Introducción a las características y tecnologías de Win32

Las API de Win32 existen para muchas características y tecnologías de Windows 10, incluida la interfaz de usuario principal y las API de ventanas, audio y gráficos y redes. Para obtener instrucciones y ejemplos de código sobre el uso de estas API, [Consulte nuestro índice de características y tecnologías](desktop-app-technologies.md).

## <a name="related-topics"></a>Temas relacionados

* [Desarrollo de aplicaciones de escritorio](/windows/apps/desktop)
* [Referencia de la API de Windows](/windows/desktop/api/)
* [Índice de API de Windows](/windows/desktop/apiindex/api-index-portal)
* [Referencia de Windows Runtime C++](/windows/desktop/winrt/reference)
