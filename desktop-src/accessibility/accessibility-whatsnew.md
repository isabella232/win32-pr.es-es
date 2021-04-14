---
description: Describe las innovaciones y las actualizaciones recientes de las características, herramientas, documentación y ejemplos de accesibilidad de Windows.
title: Novedades de accesibilidad de Windows para desarrolladores
ms.topic: article
ms.date: 04/18/2019
ms.openlocfilehash: 44d8c453b09bc73e71006e132199c18b275860af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496666"
---
# <a name="new-windows-accessibility-features-tools-documentation-and-samples-for-developers"></a>Nuevas características de accesibilidad de Windows, herramientas, documentación y ejemplos para desarrolladores

La plataforma Windows se está actualizando constantemente con nuevas características de accesibilidad y automatización para los desarrolladores.

[Instale las herramientas y el SDK](https://developer.microsoft.com/windows/downloads/#_blank) en Windows 10 y esté listo para crear una nueva aplicación universal de Windows o para explorar cómo puede usar el código de aplicación existente en Windows.

Para obtener más información sobre las herramientas más recientes disponibles para probar la implementación de accesibilidad de las aplicaciones web y de Windows, consulte [probar la accesibilidad](accessibility-testwithuia.md).

## <a name="whats-new-for-windows-10-may-2019-update-version-1903"></a>Novedades de la actualización 2019 de Windows 10 (versión 1903)

Las siguientes características, herramientas, instrucciones para desarrolladores, ejemplos y vídeos están disponibles para la [actualización 2019 de Windows 10](https://blogs.windows.com/windowsexperience/2019/04/08/releasing-the-may-2019-update-to-the-release-preview-ring/#oTrOrMWFFgWJuCqO.97).

| Release | Plataforma | Característica | Descripción | Vínculo |
| --- | --- | --- | --- | --- |
| 1903 | Win32 | Automatización de la interfaz de usuario admite IAccessible2 | Los clientes de automatización de la interfaz de usuario ahora pueden acceder sin problemas a la información de proveedores de IAccessible2 como el explorador Chrome. | N/D |
| 1903 | UWP | Visibilidad de la barra de desplazamiento  | Las barras de desplazamiento se ocultan automáticamente cuando no se interactúa con ella. | [Propiedad UISettings. AutoHideScrollBars](/uwp/api/windows.ui.viewmanagement.uisettings.autohidescrollbars) |
| 1903 | Win32 | La automatización de la interfaz de usuario admite marcado estructurado | Diseñado, pero no limitado a, el análisis de MathML. | N/D |

## <a name="whats-new-for-windows-10-october-2018-update-version-1809"></a>Novedades de la actualización 2018 de octubre de Windows 10 (versión 1809)

Las siguientes características, herramientas, instrucciones para desarrolladores, ejemplos y vídeos están disponibles para la [actualización 2018 de octubre de Windows 10](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/#R6DJStjqlIkK34BT.97).

| Release | Plataforma | Característica | Descripción | Vínculo |
| --- | --- | --- | --- | --- |
| 1809 | Win32 | Automatización de la interfaz de usuario admite eventos de cambio de posición de texto activo | Los proveedores de automatización de la interfaz de usuario pueden establecer explícitamente una posición inicial dentro de un intervalo de texto. Los clientes de la tecnología de asistencia (AT) pueden transmitir esta posición a un usuario. Por ejemplo, si un usuario hace clic en un vínculo a un delimitador en la misma página (un vínculo de marcador), la nueva ubicación se proporciona a en. | [Interfaz IUIAutomation6](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation6) |
| 1809 | Win32 | Automatización de la interfaz de usuario admite la fusión de eventos | Mejora el rendimiento al intentar detectar, filtrar y pasar por alto los eventos de MSAA de MSAA y UIA secuenciales duplicados generados por algunos proveedores. | [Interfaz IUIAutomation6](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation6) |
| 1809 | Win32 | Automatización de la interfaz de usuario admite el comportamiento de recuperación de conexión | Los mensajes de un cliente de UI Automation a un proveedor se suspenden (durante dos segundos, de forma predeterminada) si el proveedor no responde. Esto reduce la frecuencia de los tiempos de espera extendidos y minimiza el desbordamiento de un proveedor que no responde con eventos y solicitudes. | [Interfaz IUIAutomation6](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation6) |
| 1809 | UWP | Servicios de lectura de pantalla mejorados | EN los clientes, conozca la ubicación de lectura de pantalla audible (control o contenido) y el modo de lectura. | [Clase ScreenReaderService](/uwp/api/windows.ui.accessibility.screenreaderservice) |
| 1809 | Win32, UWP | Automatización de la interfaz de usuario admite ventanas de cuadro de diálogo | Los proveedores de automatización de la interfaz de usuario pueden marcar elementos UIA específicamente como ventanas de cuadro de diálogo. ATs a menudo presentan los diálogos de forma diferente a los usuarios.  | [IUIAutomationElement9](https://review.docs.microsoft.com/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement9)<br/><br/>[Clase ContentDialog](/uwp/api/windows.ui.xaml.controls.contentdialog) |
| 1809 |  UWP | Ajuste de escala de texto  | Escala el tamaño del texto en aplicaciones y páginas Web. | [Evento UISettings. TextScaleFactorChanged](/uwp/api/windows.ui.viewmanagement.uisettings.textscalefactorchanged)<br/><br/>[Ajuste de escala de texto](/windows/uwp/design/input/text-scaling) |
