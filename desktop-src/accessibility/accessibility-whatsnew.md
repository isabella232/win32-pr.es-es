---
description: Describe las innovaciones y actualizaciones recientes para Windows de accesibilidad, herramientas, documentación y ejemplos.
title: Novedades de la Windows para desarrolladores
ms.topic: article
ms.date: 04/18/2019
ms.openlocfilehash: 6cffebe307b06aceb506e8576e2a9c99c395c1257f575c6be3757a9426df2459
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954485"
---
# <a name="new-windows-accessibility-features-tools-documentation-and-samples-for-developers"></a>Nuevas Windows de accesibilidad, herramientas, documentación y ejemplos para desarrolladores

La Windows se actualiza constantemente con nuevas características de accesibilidad y automatización para desarrolladores.

[Instale las](https://developer.microsoft.com/windows/downloads/#_blank) herramientas y el SDK en Windows 10 y está listo para crear una nueva aplicación universal de Windows o explorar cómo puede usar el código de aplicación existente en Windows.

Para obtener más información sobre las herramientas más recientes disponibles para probar la implementación de accesibilidad de Windows aplicaciones web, consulte [Pruebas de accesibilidad.](accessibility-testwithuia.md)

## <a name="whats-new-for-windows-10-may-2019-update-version-1903"></a>Novedades de Actualización de mayo de 2019 de Windows 10 (versión 1903)

Las siguientes características, herramientas, instrucciones para desarrolladores, ejemplos y vídeos están disponibles para [el Actualización de mayo de 2019 de Windows 10](https://blogs.windows.com/windowsexperience/2019/04/08/releasing-the-may-2019-update-to-the-release-preview-ring/#oTrOrMWFFgWJuCqO.97).

| Release | Plataforma | Característica | Descripción | Vínculo |
| --- | --- | --- | --- | --- |
| 1903 | Win32 | Automatización de la interfaz de usuario admite IAccessible2 | Automatización de la interfaz de usuario clientes pueden acceder sin problemas a la información de proveedores de IAccessible2, como el explorador Chrome. | N/D |
| 1903 | UWP | Visibilidad de la barra de desplazamiento  | Las barras de desplazamiento se ocultan automáticamente cuando no se interactúa con . | [Propiedad UISettings.AutoHideScrollBars](/uwp/api/windows.ui.viewmanagement.uisettings.autohidescrollbars) |
| 1903 | Win32 | Automatización de la interfaz de usuario admite marcado estructurado | Se ha diseñado, pero no se limita a, el análisis de MathML. | N/D |

## <a name="whats-new-for-windows-10-october-2018-update-version-1809"></a>Novedades de Actualización de octubre de 2018 de Windows 10 (versión 1809)

Las siguientes características, herramientas, instrucciones para desarrolladores, ejemplos y vídeos están disponibles para [el Actualización de octubre de 2018 de Windows 10](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/#R6DJStjqlIkK34BT.97).

| Release | Plataforma | Característica | Descripción | Vínculo |
| --- | --- | --- | --- | --- |
| 1809 | Win32 | Automatización de la interfaz de usuario admite eventos de cambio de posición de texto activo | Automatización de la interfaz de usuario de texto pueden establecer explícitamente una posición inicial dentro de un intervalo de texto. Los clientes de tecnología de asistencia (AT) pueden transmitir esta posición a un usuario. Por ejemplo, si un usuario hace clic en un vínculo a un delimitador en la misma página (un vínculo de marcador), la nueva ubicación se proporciona a AT. | [Interfaz IUIAutomation6](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation6) |
| 1809 | Win32 | Automatización de la interfaz de usuario admite la conjunción de eventos | Mejora el rendimiento al intentar detectar, filtrar y omitir eventos MSAA secuenciales duplicados y textChanged de UIA producidos por algunos proveedores. | [Interfaz IUIAutomation6](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation6) |
| 1809 | Win32 | Automatización de la interfaz de usuario admite el comportamiento de recuperación de conexiones | Los mensajes de Automatización de la interfaz de usuario cliente a un proveedor se suspenden (durante dos segundos, de forma predeterminada) si el proveedor no responde. Esto reduce la frecuencia de tiempos de espera extendidos y minimiza la saturación de un proveedor que no responde con eventos y solicitudes. | [Interfaz IUIAutomation6](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation6) |
| 1809 | UWP | Servicios de lector de pantalla mejorados | Los clientes at conocen la ubicación de lectura de la pantalla (control o contenido) y el modo de lectura. | [ScreenReaderService (clase)](/uwp/api/windows.ui.accessibility.screenreaderservice) |
| 1809 | Win32, UWP | Automatización de la interfaz de usuario ventanas de diálogo | Automatización de la interfaz de usuario pueden marcar elementos UIA específicamente como ventanas de diálogo. A menudo, los AT presentan diálogos de forma diferente a los usuarios.  | [IUIAutomationElement9](https://review.docs.microsoft.com/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement9)<br/><br/>[ContentDialog (clase)](/uwp/api/windows.ui.xaml.controls.contentdialog) |
| 1809 |  UWP | Ajuste de escala de texto  | Escala el tamaño del texto en aplicaciones y páginas web. | [Evento UISettings.TextScaleFactorChanged](/uwp/api/windows.ui.viewmanagement.uisettings.textscalefactorchanged)<br/><br/>[Ajuste de escala de texto](/windows/uwp/design/input/text-scaling) |
