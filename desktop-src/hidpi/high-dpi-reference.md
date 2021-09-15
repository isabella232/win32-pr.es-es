---
title: Referencia de valores altos de PPP
description: Referencia de valores altos de PPP
ms.assetid: 07A2D45E-721C-4DA8-82A5-38B2FB94BC6D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9c6a9302541683dbf97c06194285f9e8cfcf3c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570649"
---
# <a name="high-dpi-reference"></a>Referencia de valores altos de PPP

## <a name="functions"></a>Functions



| Tema                                                                                         |Descripción                                                                                                                                                                   |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdjustWindowRectExForDpi**](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi)                             | Variante de [AdjustWindowRectEx que](/windows/desktop/api/winuser/nf-winuser-adjustwindowrectex) devuelve valores escalados a un PPP específico.       |
| [**AreDpiAwarenessContextsEqual**](/windows/desktop/api/Winuser/nf-winuser-aredpiawarenesscontextsequal)                     | Determina si dos valores [**DE CONTEXTO DE RECONOCIMIENTO \_ \_ DE PPP**](dpi-awareness-context.md) son equivalentes.                                                            |
| [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling)                           | Habilita el escalado automático del área no cliente de la ventana de nivel superior especificada.                                                                               |
| [**GetAwarenessFromDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-getawarenessfromdpiawarenesscontext)       | Recupera el valor DE [**RECONOCIMIENTO \_ DE PPP**](/windows/desktop/api/windef/ne-windef-dpi_awareness) de un [**CONTEXTO DE RECONOCIMIENTO DE \_ \_ PPP**](dpi-awareness-context.md)                                       |
| [**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)                                             | Consulta la información de PPP asociada a un monitor.                                                                                                            |
| [**GetDpiForSystem**](/windows/desktop/api/Winuser/nf-winuser-getdpiforsystem)                                               | Devuelve el valor de PPP del sistema.                                                                                                                                           |
| [**GetDpiForWindow**](/windows/desktop/api/Winuser/nf-winuser-getdpiforwindow)                                               | Devuelve el valor de PPP actual de la ventana especificada.                                                                                                                 |
| [**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)                                 | Recupera el modo de virtualización de PPP del proceso especificado.                                                                                                   |
| [**GetSystemMetricsForDpi**](/windows/desktop/api/Winuser/nf-winuser-getsystemmetricsfordpi)                                 | Variante de [GetSystemMetrics que](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) devuelve valores escalados a un PPP específico.         |
| [**GetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-getthreaddpiawarenesscontext)                     | Recupera el contexto de reconocimiento de PPP activo para el subproceso actual.                                                                                                |
| [**GetWindowDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-getwindowdpiawarenesscontext)                     | Recupera el contexto de reconocimiento de PPP de una ventana.                                                                                                                 |
| [**IsValidDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-isvaliddpiawarenesscontext)                         | Determina si un CONTEXTO [**\_ DE RECONOCIMIENTO \_ DE PPP**](dpi-awareness-context.md) es válido y es compatible con el sistema actual.                                            |
| [**LogicalToPhysicalPointForPerMonitorDPI**](/windows/desktop/api/winuser/nf-winuser-logicaltophysicalpointforpermonitordpi) | Convierte un punto de una ventana de coordenadas lógicas en coordenadas físicas, independientemente del reconocimiento de PPP del autor de la llamada.                                   |
| [**PhysicalToLogicalPointForPerMonitorDPI**](/windows/desktop/api/winuser/nf-winuser-physicaltologicalpointforpermonitordpi) | Convierte un punto de una ventana de coordenadas físicas en coordenadas lógicas, independientemente del reconocimiento de PPP del autor de la llamada.                                   |
| [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)                                 | Establece el modo de virtualización de PPP para el proceso actual.                                                                                                         |
| [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext)                     | Cambia el contexto de reconocimiento de PPP activo para el subproceso actual.                                                                                                  |
| [**SystemParametersInfoForDpi**](/windows/desktop/api/Winuser/nf-winuser-systemparametersinfofordpi)                         | Variante de [SystemParametersInfo que](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) devuelve valores escalados a un PPP específico.     |
| [**SetProcessDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)                   | Establece el contexto de reconocimiento de PPP para el proceso actual.                                                                                                           |
| [**SetDialogDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-setdialogdpichangebehavior)                         | Invalida el comportamiento predeterminado de escalado de PPP por monitor de un cuadro de diálogo.                                                                                               |
| [**GetDialogDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-getdialogdpichangebehavior)                         | Recupera el comportamiento de escalado de PPP por monitor de un cuadro de diálogo.                                                                                                       |
| [**SetDialogControlDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-setdialogcontroldpichangebehavior)                     | Invalida el comportamiento predeterminado de escalado de PPP por monitor de una ventana secundaria en un cuadro de diálogo.                                                                             |
| [**GetDialogControlDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-getdialogcontroldpichangebehavior)                     | Recupera las invalidaciones del comportamiento de escalado de PPP por monitor de una ventana secundaria en un cuadro de diálogo.                                                                           |
| [**OpenThemeDataForDpi**](/windows/desktop/api/uxtheme/nf-uxtheme-openthemedatafordpi)                                       | Variante de [OpenThemeData que abre](/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata) los identificadores de tema asociados a un PPP específico. |
| [**GetSystemDpiForProcess**](/windows/desktop/api/winuser/nf-winuser-getsystemdpiforprocess)                                 | Recupera el valor de PPP del sistema asociado a un proceso determinado.                                                                                                         |
| [**GetDpiFromDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)                   | Recupera el valor de PPP de un determinado [identificador DE CONTEXTO DE RECONOCIMIENTO \_ \_ DE PPP.](dpi-awareness-context.md)                                                                       |
| [**SetThreadDpiHostingBehavior**](/windows/desktop/api/winuser/nf-winuser-setthreaddpihostingbehavior)                       | Invalida el comportamiento de hospedaje de PPP predeterminado del subproceso actual.                                                                                                 |
| [**GetThreadDpiHostingBehavior**](/windows/desktop/api/winuser/nf-winuser-getthreaddpihostingbehavior)                       | Recupera el comportamiento de hospedaje de PPP del subproceso actual.                                                                                                         |
| [**GetWindowDpiHostingBehavior**](/windows/desktop/api/winuser/nf-winuser-getwindowdpihostingbehavior)                       | Recupera el comportamiento de hospedaje de PPP de la ventana especificada.                                                                                                       |



 

## <a name="types"></a>Tipos



| Tema                                                                           |Descripción                                                                                        |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**RECONOCIMIENTO DE \_ PPP**](/windows/desktop/api/windef/ne-windef-dpi_awareness)                                    | Representa los modos de virtualización de coordenadas de PPP.                                        |
| [**CONTEXTO DE \_ RECONOCIMIENTO DE \_ PPP**](dpi-awareness-context.md)                   | Token que representa un modo de virtualización de PPP y comportamientos asociados.           |
| [**COMPORTAMIENTOS \_ DE CAMBIO DE PPP DEL CONTROL DE \_ \_ \_ DIÁLOGO**](/windows/desktop/api/winuser/ne-winuser-dialog_control_dpi_change_behaviors) | Describe las invalidaciones del comportamiento de escalado de PPP por monitor para ventanas secundarias dentro de los diálogos. |
| [**COMPORTAMIENTOS \_ DE CAMBIO DE PPP DEL CUADRO DE \_ \_ DIÁLOGO**](/windows/desktop/api/winuser/ne-winuser-dialog_dpi_change_behaviors)      | Describe las invalidaciones del comportamiento de escalado de PPP por monitor para los diálogos.                      |
| [**SUPERVISAR \_ TIPO DE \_ PPP**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-monitor_dpi_type)                 | Representa el tipo de PPP asociado a un monitor.                                  |
| [**RECONOCIMIENTO DE \_ PPP \_ DE PROCESO**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)                   | Representa el modo de virtualización de coordenadas de PPP de un proceso.                        |
| [**COMPORTAMIENTO \_ DE HOSPEDAJE DE \_ PPP**](/windows/win32/api/windef/ne-windef-dpi_hosting_behavior)                    | Representa el comportamiento de hospedaje de PPP para una ventana.                                      |



 

## <a name="messages"></a>error de Hadoop



| Tema                                                                   | Descripción                                                                                                                                        |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ PPPCHANGED**](wm-dpichanged.md)                            | Notifica a una ventana de nivel superior que su PPP ha cambiado.                                                                                   |
| [**WM \_ PPPCHANGED \_ BEFOREPARENT**](wm-dpichanged-beforeparent.md) | Notifica a una ventana secundaria que el valor de PPP asociado a su ventana que lo contiene ha cambiado. Se entrega antes de que se notifique a la ventana primaria. |
| [**WM \_ PPPCHANGED \_ AFTERPARENT**](wm-dpichanged-afterparent.md)   | Notifica a una ventana secundaria que el valor de PPP asociado a su ventana que lo contiene ha cambiado. Se entrega una vez notificada la ventana primaria.  |
| [**WM \_ GETDPISCALEDSIZE**](wm-getdpiscaledsize.md)                | Permite que las ventanas de nivel superior cambien de tamaño *de forma no lineal en* respuesta a los cambios de PPP.                                                           |



 

 

 
