---
title: Referencia de PPP alta
description: .
ms.assetid: 07A2D45E-721C-4DA8-82A5-38B2FB94BC6D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ec59f34aa5ed036d7f4376cb3d170b5d7849f4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420561"
---
# <a name="high-dpi-reference"></a>Referencia de PPP alta

## <a name="functions"></a>Functions



|                                                                                          |                                                                                                                                                                   |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tema.**                                                                                | **Descripción**                                                                                                                                                   |
| [**AdjustWindowRectExForDpi**](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi)                             | Una variante de [AdjustWindowRectEx](/windows/desktop/api/winuser/nf-winuser-adjustwindowrectex) que devuelve valores escalados a un valor de PPP específico.       |
| [**AreDpiAwarenessContextsEqual**](/windows/desktop/api/Winuser/nf-winuser-aredpiawarenesscontextsequal)                     | Determina si dos valores de [**\_ \_ contexto de reconocimiento de PPP**](dpi-awareness-context.md) son equivalentes.                                                            |
| [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling)                           | Habilita el escalado automático del área no cliente de la ventana de nivel superior especificada.                                                                               |
| [**GetAwarenessFromDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-getawarenessfromdpiawarenesscontext)       | Recupera el valor [**de \_ reconocimiento de PPP**](/windows/desktop/api/windef/ne-windef-dpi_awareness) de [**un \_ \_ contexto de reconocimiento de PPP**](dpi-awareness-context.md) .                                       |
| [**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)                                             | Consulta la información de PPP asociada a un monitor.                                                                                                            |
| [**GetDpiForSystem**](/windows/desktop/api/Winuser/nf-winuser-getdpiforsystem)                                               | Devuelve el PPP del sistema.                                                                                                                                           |
| [**GetDpiForWindow**](/windows/desktop/api/Winuser/nf-winuser-getdpiforwindow)                                               | Devuelve el PPP actual para la ventana especificada.                                                                                                                 |
| [**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)                                 | Recupera el modo de virtualización de PPP del proceso especificado.                                                                                                   |
| [**GetSystemMetricsForDpi**](/windows/desktop/api/Winuser/nf-winuser-getsystemmetricsfordpi)                                 | Una variante de [GetSystemMetrics](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) que devuelve valores escalados a un valor de PPP específico.         |
| [**GetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-getthreaddpiawarenesscontext)                     | Recupera el contexto de reconocimiento de PPP activo para el subproceso actual.                                                                                                |
| [**GetWindowDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-getwindowdpiawarenesscontext)                     | Recupera el contexto de reconocimiento de PPP para una ventana.                                                                                                                 |
| [**IsValidDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-isvaliddpiawarenesscontext)                         | Determina si un [**\_ \_ contexto de reconocimiento de PPP**](dpi-awareness-context.md) es válido y es compatible con el sistema actual.                                            |
| [**LogicalToPhysicalPointForPerMonitorDPI**](/windows/desktop/api/winuser/nf-winuser-logicaltophysicalpointforpermonitordpi) | Convierte un punto de una ventana de coordenadas lógicas en coordenadas físicas, independientemente del reconocimiento de PPP del llamador.                                   |
| [**PhysicalToLogicalPointForPerMonitorDPI**](/windows/desktop/api/winuser/nf-winuser-physicaltologicalpointforpermonitordpi) | Convierte un punto de una ventana de coordenadas físicas en coordenadas lógicas, independientemente del reconocimiento de PPP del llamador.                                   |
| [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)                                 | Establece el modo de virtualización de PPP para el proceso actual.                                                                                                         |
| [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext)                     | Cambia el contexto de reconocimiento de PPP activo para el subproceso actual.                                                                                                  |
| [**SystemParametersInfoForDpi**](/windows/desktop/api/Winuser/nf-winuser-systemparametersinfofordpi)                         | Variante de [SystemParametersInfo](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) que devuelve valores escalados a un valor de PPP específico.     |
| [**SetProcessDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)                   | Establece el contexto de reconocimiento de PPP para el proceso actual.                                                                                                           |
| [**SetDialogDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-setdialogdpichangebehavior)                         | Invalida el comportamiento predeterminado de escala de PPP por monitor de un cuadro de diálogo.                                                                                               |
| [**GetDialogDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-getdialogdpichangebehavior)                         | Recupera el comportamiento de escala de PPP por monitor de un cuadro de diálogo.                                                                                                       |
| [**SetDialogControlDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-setdialogcontroldpichangebehavior)                     | Invalida el comportamiento predeterminado de escala de PPP por monitor de una ventana secundaria en un cuadro de diálogo.                                                                             |
| [**GetDialogControlDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-getdialogcontroldpichangebehavior)                     | Recupera cualquier invalidación del comportamiento de ajuste de escala de PPP por monitor de una ventana secundaria en un cuadro de diálogo.                                                                           |
| [**OpenThemeDataForDpi**](/windows/desktop/api/uxtheme/nf-uxtheme-openthemedatafordpi)                                       | Una variante de [OpenThemeData](/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata) que abre los identificadores de tema asociados a un valor de PPP específico. |
| [**GetSystemDpiForProcess**](/windows/desktop/api/winuser/nf-winuser-getsystemdpiforprocess)                                 | Recupera los PPP del sistema asociados a un proceso determinado.                                                                                                         |
| [**GetDpiFromDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)                   | Recupera el PPP de un identificador de [ \_ \_ contexto de reconocimiento de PPP](dpi-awareness-context.md) determinado.                                                                       |
| [**SetThreadDpiHostingBehavior**](/windows/desktop/api/winuser/nf-winuser-setthreaddpihostingbehavior)                       | Invalida el comportamiento predeterminado de hospedaje de PPP del subproceso actual.                                                                                                 |
| [**GetThreadDpiHostingBehavior**](/windows/desktop/api/winuser/nf-winuser-getthreaddpihostingbehavior)                       | Recupera el comportamiento de hospedaje de PPP del subproceso actual.                                                                                                         |
| [**GetWindowDpiHostingBehavior**](/windows/desktop/api/winuser/nf-winuser-getwindowdpihostingbehavior)                       | Recupera el comportamiento de hospedaje de PPP de la ventana especificada.                                                                                                       |



 

## <a name="types"></a>Tipos



|                                                                            |                                                                                        |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| **Tema.**                                                                  | **Descripción**                                                                        |
| [**reconocimiento de PPP \_**](/windows/desktop/api/windef/ne-windef-dpi_awareness)                                    | Representa los modos de virtualización de coordenadas de PPP.                                        |
| [**\_contexto de reconocimiento de PPP \_**](dpi-awareness-context.md)                   | Un token que representa el modo de virtualización de PPP y los comportamientos asociados.           |
| [**\_comportamiento de \_ cambio de PPP de control de cuadro \_ de diálogo \_**](/windows/desktop/api/winuser/ne-winuser-dialog_control_dpi_change_behaviors) | Describe las invalidaciones de comportamiento de ajuste de escala de PPP por monitor para las ventanas secundarias en los cuadros de diálogo. |
| [**\_comportamientos de \_ cambio de PPP de diálogo \_**](/windows/desktop/api/winuser/ne-winuser-dialog_dpi_change_behaviors)      | Describe las invalidaciones de comportamiento de ajuste de escala de PPP por monitor para los diálogos.                      |
| [**\_tipo de PPP de monitor \_**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-monitor_dpi_type)                 | Representa el tipo de PPP asociado con un monitor.                                  |
| [**\_reconocimiento de PPP de proceso \_**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)                   | Representa el modo de virtualización de coordenadas de PPP de un proceso.                        |
| [**\_comportamiento de hospedaje de PPP \_**](/windows/win32/api/windef/ne-windef-dpi_hosting_behavior)                    | Representa el comportamiento de hospedaje de PPP para una ventana.                                      |



 

## <a name="messages"></a>error de Hadoop



|                                                                    |                                                                                                                                         |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **Tema.**                                                          | **Descripción**                                                                                                                         |
| [**DPICHANGED de WM \_**](wm-dpichanged.md)                            | Notifica a una ventana de nivel superior que su PPP ha cambiado.                                                                                   |
| [**\_BEFOREPARENT DPICHANGED \_ WM**](wm-dpichanged-beforeparent.md) | Notifica a una ventana secundaria que ha cambiado el valor de PPP asociado a su ventana contenedora. Se entrega antes de que se notifique a la ventana primaria. |
| [**\_AFTERPARENT DPICHANGED \_ WM**](wm-dpichanged-afterparent.md)   | Notifica a una ventana secundaria que ha cambiado el valor de PPP asociado a su ventana contenedora. Entregado después de notificar a la ventana primaria.  |
| [**GETDPISCALEDSIZE de WM \_**](wm-getdpiscaledsize.md)                | Permite que las ventanas de nivel superior cambien de tamaño de forma *no lineal* en respuesta a los cambios de PPP.                                                           |



 

 

 