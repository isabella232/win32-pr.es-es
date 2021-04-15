---
description: 'Hay tres maneras de que una aplicación cierre los equipos locales o remotos: Apague el sistema y reinicie itshut la aplicación, apague y reinicie el sistema y reinicie las aplicaciones que se han registrado para reiniciarse.'
ms.assetid: acadf58f-3f68-4fa1-bdcf-8f85c8479263
title: Apagar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e436dd9e3b115112e63b0440b4d51de4c7f9f619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668453"
---
# <a name="shutting-down"></a>Apagar

Hay tres maneras de que una aplicación cierre los equipos locales o remotos:

-   Apagar el sistema
-   Apagar el sistema y reiniciarlo
-   cierre la aplicación, apague y reinicie el sistema y reinicie las aplicaciones que se han registrado para reiniciarse.

Para apagar el sistema, use la función [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) con la marca de \_ cierre EWX. Para obtener un ejemplo, vea [Cómo apagar el sistema](how-to-shut-down-the-system.md). Para apagar y reiniciar el sistema, use la marca de \_ REinicio de EWX. Para reiniciar las aplicaciones que se han registrado para el reinicio mediante la función [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) , use la \_ marca RESTARTAPPS de EXW.

Las funciones [**InitiateShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna), [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)y [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) inician un temporizador y muestran un cuadro de diálogo que pide al usuario que cierre la sesión. Mientras se muestra este cuadro de diálogo, la función [**AbortSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna) puede detener el temporizador y evitar que el equipo se apague. Sin embargo, si el temporizador expira, el equipo se apaga. Estas funciones también pueden reiniciar el equipo después de una operación de cierre. Para obtener más información, vea [Mostrar el cuadro de diálogo de apagado](displaying-the-shutdown-dialog-box.md).

## <a name="shutdown-notifications"></a>Notificaciones de apagado

Las aplicaciones con una ventana y una cola de mensajes reciben notificaciones de cierre a través de los mensajes [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) y [**WM \_ ENDSESSION**](wm-endsession.md) . Estas aplicaciones deben devolver **true** para indicar que se pueden terminar. Las aplicaciones no deben bloquear el cierre del sistema a menos que sea absolutamente necesario. Las aplicaciones deben realizar cualquier limpieza necesaria mientras se procesa **WM \_ ENDSESSION**. Las aplicaciones que tienen datos no guardados pueden guardar los datos en una ubicación temporal y restaurarlos la próxima vez que se inicie la aplicación. Se recomienda que las aplicaciones guarden los datos y el estado con frecuencia. por ejemplo, guarde automáticamente los datos entre las operaciones de guardado iniciadas por el usuario para reducir la cantidad de datos que se van a guardar en el cierre.

Las aplicaciones de consola reciben notificaciones de cierre en sus rutinas de controlador. Para registrar un controlador de consola, use la función [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) .

Las aplicaciones de servicio reciben notificaciones de cierre en sus rutinas de controlador. Para registrar un controlador de control de servicio, utilice la función [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) .

## <a name="blocking-shutdown"></a>Bloqueo de cierre

Si una aplicación debe bloquear un posible cierre del sistema, puede llamar a la función [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) . El autor de la llamada proporciona una cadena de motivo que se mostrará al usuario. La cadena de motivo debe ser breve y clara, lo que proporciona al usuario la información necesaria para decidir si continuar apagando el sistema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo apagar el sistema](how-to-shut-down-the-system.md)
</dt> </dl>

 

 
