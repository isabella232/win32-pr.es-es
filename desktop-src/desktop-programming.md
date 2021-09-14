---
description: Aprenda los conceptos básicos de la creación de aplicaciones de escritorio excelentes en esta sección.
ms.assetid: 15690E05-9AF7-41A3-AF7C-8DB7C5FB9BE4
title: Introducción
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84879e6373f4bfeb5a7e4b6a6138423d7688afe2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970092"
---
# <a name="get-started-with-desktop-windows-apps-that-use-the-win32-api"></a>Introducción a las aplicaciones de Windows escritorio que usan la API win32

Win32 API (también conocida como la API de Windows) es la plataforma original para aplicaciones Windows en C y C++ nativas que requieren acceso directo a Windows y al hardware. Proporciona una experiencia de desarrollo de primera clase sin depender de un entorno de tiempo de ejecución administrado como .NET y WinRT (para aplicaciones para UWP para Windows 10). Esto hace que Win32 API sea la plataforma preferida para las aplicaciones que necesitan el mayor nivel de rendimiento y acceso directo al hardware del sistema.

> [!NOTE]
> En esta documentación se explica cómo crear aplicaciones de escritorio Windows con la API Win32. La API win32 es una de las distintas plataformas de aplicaciones que puede usar para compilar aplicaciones de Windows escritorio. Para obtener más información sobre otras plataformas de aplicaciones, [vea Elegir la plataforma.](/windows/apps/desktop/choose-your-platform)

## <a name="get-set-up"></a>Prepárate

Siga estas instrucciones y comience a crear aplicaciones de escritorio para Windows 10 que usan la API Win32.

1. Descargue o actualice Visual Studio 2019. Si todavía no tienes Visual Studio 2019, puedes instalar Microsoft Visual Studio Community 2019 de forma gratuita. Al instalar Visual Studio, asegúrese de seleccionar la opción **Desarrollo para el escritorio con C++.** Para ver los vínculos de descarga, consulte [nuestra página Descargas.](https://developer.microsoft.com/windows/downloads)

    > [!NOTE]
    > Al instalar Visual Studio, opcionalmente puede seleccionar las opciones desarrollo de escritorio de **.NET** y Desarrollo de plataforma **universal de Windows** para acceder a otros tipos de proyecto y plataformas de aplicaciones para compilar aplicaciones de escritorio Windows.

2. Si quiere compilar la aplicación de escritorio en un paquete [MSIX](/windows/msix/desktop/desktop-to-uwp-root) y probar o depurar la aplicación empaquetada en el equipo de desarrollo, deberá habilitar el modo de desarrollador en [el equipo.](/windows/uwp/get-started/enable-your-device-for-development)

> [!NOTE]
> Para los scripts que puede usar para configurar el equipo de desarrollo e instalar otras características o paquetes, consulte [este GitHub proyecto](https://github.com/Microsoft/windows-dev-box-setup-scripts).

## <a name="learn-how-to-create-desktop-apps-using-the-win32-api"></a>Aprenda a crear aplicaciones de escritorio mediante la API Win32

Si no está de acuerdo con la creación de aplicaciones de escritorio con la API Win32, los siguientes tutoriales y artículos le ayudarán a empezar a trabajar.

| Tema        | Descripción      |
|---------------|-----------------|
| [Creación de la primera aplicación Win32 de C++](LearnWin32/learn-to-program-for-windows.md)    | En este tutorial se enseña a escribir un programa Windows en C++ mediante Win32 y LAS API COM.  |
| [Creación de la primera aplicación mediante DirectX](direct3dgetstarted/building-your-first-directx-app.md) | Este tutorial básico le ayudará a empezar a trabajar con el desarrollo de aplicaciones de DirectX.            |
| [Guía de programación de Windows de 64 bits](WinProg64/programming-guide-for-64-bit-windows.md)    | Describe la programación para versiones de 64 bits del Windows operativo. |
| [Uso de los Windows encabezados](WinProg/using-the-windows-headers.md)     | Proporciona información general sobre algunas de las convenciones usadas en los archivos Windows encabezado. |

También puede examinar los ejemplos [de la aplicación de escritorio.](https://github.com/Microsoft/Windows-classic-samples)

## <a name="modernize-your-desktop-apps-for-windows-10"></a>Modernización de las aplicaciones de escritorio para Windows 10

Si tienes una aplicación Win32 de escritorio existente, hay muchas características en la Plataforma universal de Windows (UWP) que puedes usar para ofrecer la mejor experiencia posible en Windows 10. Por ejemplo, a partir Windows 10, versión 1903, puedes hospedar controles XAML de UWP en tu aplicación Win32 de escritorio mediante una característica denominada Islas XAML.

La mayoría de estas características de UWP están disponibles como componentes modulares que puede adoptar en la aplicación de escritorio a su propio ritmo sin tener que volver a escribir toda la aplicación. Puedes mejorar tu aplicación de escritorio existente si eliges qué partes de Windows 10 y UWP debes adoptar.

Para más información, consulta [Modernización de las aplicaciones de escritorio](/windows/apps/desktop/modernize).

## <a name="cwinrt"></a>C++/WinRT

Opcionalmente, puede configurar el equipo de desarrollo para que use [C++/WinRT.](/windows/uwp/cpp-and-winrt-apis/) C++/WinRT es una proyección de lenguaje C++17 moderna totalmente estándar que permite consumir fácilmente las API de tiempo de ejecución de Windows Windows Runtime (WinRT) desde la aplicación de escritorio Win32 de C++. C++/WinRT se implementa como una biblioteca basada en archivos de encabezado.

Para configurar el proyecto para C++/WinRT:

* En el caso de los proyectos nuevos, puedes instalar la [extensión de Visual Studio para C++/WinRT (VSIX)](https://marketplace.visualstudio.com/items?itemName=CppWinRTTeam.cppwinrt101804264) y usar una de las plantillas de proyecto de C++/WinRT incluidas en esa extensión.
* Para los Windows de aplicaciones de escritorio existentes, puede instalar [Microsoft.Windows. CppWinRT NuGet](https://www.nuget.org/packages/Microsoft.Windows.CppWinRT/) paquete en el proyecto.

Para obtener más información sobre estas opciones, consulta [este artículo](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt#visual-studio-support-for-cwinrt-xaml-the-vsix-extension-and-the-nuget-package).

## <a name="whats-new-for-win32-apis-in-windows-10"></a>Novedades de las API de Win32 en Windows 10

Para obtener información sobre las nuevas API de Win32 que se han introducido en Windows 10, consulte [novedades.](whats-new.md)

## <a name="get-started-with-win32-features-and-technologies"></a>Introducción a las características y tecnologías de Win32

Existen API win32 para muchas características y tecnologías de Windows 10, incluidas la interfaz de usuario principal y las API de ventana, audio y gráficos, y redes. Para obtener instrucciones y ejemplos de código sobre el uso de estas API, [consulte nuestro índice de características y tecnologías](desktop-app-technologies.md).

## <a name="related-topics"></a>Temas relacionados

* [Desarrollo de aplicaciones de escritorio](/windows/apps/desktop)
* [Windows Referencia de API](/windows/desktop/api/)
* [Índice de API de Windows](/windows/desktop/apiindex/api-index-portal)
* [Windows Referencia de C++ en tiempo de ejecución](/windows/desktop/winrt/reference)
