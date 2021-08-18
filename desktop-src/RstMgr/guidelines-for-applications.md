---
title: Directrices para aplicaciones
description: Las aplicaciones que se ejecutan en Windows Vista y Windows Server 2008 deben cumplir estas directrices para asegurarse de que el Administrador de reinicio puede apagar y reiniciar las aplicaciones si es necesario para instalar actualizaciones.
ms.assetid: 97b1df63-65a9-47b4-891b-e4a754882b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9624f578a04267b94bde41bbdf8e3312e7b8ae0f4fb84280212ea51c2db7e2f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010133"
---
# <a name="guidelines-for-applications"></a>Directrices para aplicaciones

Las aplicaciones que se ejecutan en Windows Vista y Windows Server 2008 deben cumplir estas directrices para asegurarse de que el Administrador de reinicio puede apagar y reiniciar las aplicaciones si es necesario para instalar actualizaciones. Los servicios pueden usar las directrices que se describen en [Directrices para servicios](guidelines-for-services.md).

-   El Administrador de reinicio consulta las aplicaciones de la GUI para su apagado mediante el envío de una notificación [**\_ WM QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) que tiene el parámetro *lParam* establecido en **ENDSESSION \_ CLOSEAPP** (0x1). Las aplicaciones no deben apagarse cuando reciben un **mensaje WM \_ QUERYENDSESSION** porque es posible que otra aplicación no esté lista para apagarse. Las aplicaciones GUI deben escuchar el mensaje **WM \_ QUERYENDSESSION** y devolver un valor de **TRUE** si la aplicación está preparada para apagarse y reiniciarse. Si ninguna aplicación devuelve un valor **false**, el Administrador de reinicio envía un mensaje [**WM \_ ENDSESSION**](/windows/desktop/Shutdown/wm-endsession) con el parámetro *lParam* establecido en **ENDSESSION \_ CLOSEAPP** (0x1) y el parámetro *wparam* establecido en **TRUE.** Las aplicaciones deben apagarse solo cuando reciben el **mensaje \_ WM ENDSESSION.** El Administrador de reinicio también envía un [**mensaje WM \_ CLOSE**](../winmsg/wm-close.md) para las aplicaciones gui que no se apagan al recibir **WM \_ ENDSESSION**. Si alguna aplicación de interfaz gráfica de usuario responde a un **mensaje WM \_ QUERYENDSESSION** devolviendo un valor **de FALSE**, se cancela el apagado. Sin embargo, si se fuerza el apagado, la aplicación se termina independientemente.
-   Cuando una aplicación guia recibe un [**mensaje \_ WM ENDSESSION,**](/windows/desktop/Shutdown/wm-endsession) la aplicación debe prepararse para apagarse dentro del período de tiempo de espera especificado. Como mínimo, las aplicaciones deben prepararse guardando los datos de usuario y la información de estado que se necesitan después de un reinicio. Se recomienda que las aplicaciones guarden periódicamente los datos y el estado del usuario.
-   El Administrador de reinicio envía una **notificación CTRL \_ C \_ EVENT** a las aplicaciones de consola que se deben apagar y reiniciar. Cuando una aplicación de consola recibe una notificación **CTRL \_ C \_ EVENT,** la aplicación debe tomar las medidas necesarias para prepararse para un apagado dentro del período de tiempo de espera especificado. Como mínimo, las aplicaciones de consola deben definir una función [*HandlerRoutine*](/windows/console/handlerroutine) para controlar la notificación **CTRL C \_ \_ EVENT** y guardar los datos de usuario y la información de estado que se van a necesitar después de un reinicio. Se recomienda que las aplicaciones guarden periódicamente los datos y el estado del usuario.
-   Si alguna aplicación no se apaga en respuesta a los mensajes de apagado, los instaladores pueden usar la opción **RmForceShutdown** de la función [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) para forzar el apagado de las aplicaciones. Cuando el instalador especifica un apagado forzado, el Administrador de reinicio intenta apagar las aplicaciones limpiamente mediante el envío de los mensajes de apagado, pero los forzará a cerrarse si se produce un error. Las aplicaciones guia y las aplicaciones de consola se pueden forzar a apagar para habilitar la instalación de una actualización de seguridad crítica. Dado que esto puede provocar la pérdida de datos, las aplicaciones deben controlar los mensajes de apagado y apagarse correctamente cuando sea necesario.
-   Las aplicaciones deben registrarse para reiniciarse mediante la [**función RegisterApplicationRestart.**](/windows/desktop/api/winbase/nf-winbase-registerapplicationrestart) El Administrador de reinicio solo puede reiniciar las aplicaciones que se han registrado para el reinicio. Esta es la única manera en que el Administrador de reinicio puede determinar el comando de línea de comandos que se usará al reiniciar la aplicación. Si la aplicación debe volver a abrirse con algún estado o datos guardados, esa información debe incluirse en el comando de línea de comandos que está registrado para la aplicación.
    > [!Note]  
    > Si la aplicación reiniciada debe ejecutarse en el mismo directorio en el que se ejecutó antes de apagarse, la aplicación debe guardar la información del directorio y, a continuación, cambiar al directorio después de reiniciarse.

     

    > [!Note]  
    > La [**función RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) no reinicia las aplicaciones que no se ejecutan como el usuario que ha iniciado sesión actualmente. Por ejemplo, la **función RmRestart** no reinicia las aplicaciones iniciadas con el comando **Ejecutar como** que no se ejecutan como el usuario que ha iniciado sesión actualmente. Estas aplicaciones deben reiniciarse manualmente.

     

-   Cuando el Administrador de reinicio determina que se requiere un reinicio del sistema para instalar una actualización, no cierra ninguna aplicación y servicio. En su lugar, deja esto en el instalador para decidir cuándo programar un reinicio del sistema e instalar la actualización. Los instaladores pueden reducir la interrupción a los usuarios causada por actualizaciones que requieren un reinicio del sistema mediante la función [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) con la marca **\_ RESTARTAPPS de HUTX** o la función [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) con la marca **SHUTDOWN \_ RESTARTAPPS.** El uso de estas marcas garantiza que las aplicaciones registradas para el reinicio se reinicien después de un reinicio del sistema, lo que minimiza el impacto en el usuario.

 

 