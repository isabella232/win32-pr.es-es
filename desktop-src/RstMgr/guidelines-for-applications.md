---
title: Directrices para aplicaciones
description: Las aplicaciones que se ejecutan en Windows Vista y Windows Server 2008 deben cumplir estas directrices para asegurarse de que el administrador de reinicio puede apagar y reiniciar las aplicaciones si es necesario para instalar las actualizaciones.
ms.assetid: 97b1df63-65a9-47b4-891b-e4a754882b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebace21e09956c68d34c90775c5ea646a8b2dd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793371"
---
# <a name="guidelines-for-applications"></a>Directrices para aplicaciones

Las aplicaciones que se ejecutan en Windows Vista y Windows Server 2008 deben cumplir estas directrices para asegurarse de que el administrador de reinicio puede apagar y reiniciar las aplicaciones si es necesario para instalar las actualizaciones. Los servicios pueden usar las directrices que se describen en [directrices para servicios](guidelines-for-services.md).

-   El administrador de reinicio consulta las aplicaciones GUI para el cierre mediante el envío de una notificación de [**\_ QUERYENDSESSION de WM**](/windows/desktop/Shutdown/wm-queryendsession) que tenga el parámetro *lParam* establecido en **ENDSESSION \_ CLOSEAPP** (0x1). Las aplicaciones no deben cerrarse cuando reciban un mensaje de **\_ QUERYENDSESSION de WM** porque es posible que otra aplicación no esté lista para cerrarse. Las aplicaciones GUI deben escuchar el mensaje de **\_ QUERYENDSESSION de WM** y devolver el valor **true** si la aplicación está preparada para cerrarse y reiniciarse. Si ninguna aplicación devuelve el valor **false**, el administrador de reinicio envía un mensaje de [**WM \_ ENDSESSION**](/windows/desktop/Shutdown/wm-endsession) con el parámetro *lParam* establecido en **ENDSESSION \_ CLOSEAPP** (0x1) y el parámetro *wParam* establecido en **true**. Las aplicaciones deben cerrarse solo cuando reciben el mensaje de **WM \_ ENDSESSION** . El administrador de reinicio también envía un mensaje de [**\_ cierre de WM**](../winmsg/wm-close.md) para aplicaciones GUI que no se cierran al recibir la **\_ ENDSESSION de WM**. Si alguna aplicación de GUI responde a un mensaje de **\_ QUERYENDSESSION de WM** devolviendo un valor de **false**, se cancela el cierre. Sin embargo, si se fuerza el cierre, la aplicación se termina independientemente de.
-   Cuando una aplicación GUI recibe un mensaje de [**WM \_ ENDSESSION**](/windows/desktop/Shutdown/wm-endsession) , la aplicación debe prepararse para cerrarse dentro del período de tiempo de espera especificado. Como mínimo, las aplicaciones se deben preparar guardando los datos de usuario y la información de estado que se necesita después de un reinicio. Se recomienda que las aplicaciones guarden periódicamente los datos de usuario y el estado.
-   El administrador de reinicio envía una notificación de **\_ \_ evento Ctrl C** a las aplicaciones de consola que deben cerrarse y reiniciarse. Cuando una aplicación de consola recibe una notificación de **\_ \_ eventos Ctrl C** , la aplicación debe tomar las medidas necesarias para preparar un cierre dentro del período de tiempo de espera especificado. Como mínimo, las aplicaciones de consola deben definir una función [*HandlerRoutine*](/windows/console/handlerroutine) para controlar la notificación de **\_ \_ eventos Ctrl C** y guardar los datos de usuario y la información de estado que se va a necesitar después de un reinicio. Se recomienda que las aplicaciones guarden periódicamente los datos de usuario y el estado.
-   Si alguna aplicación no se cierra en respuesta a los mensajes de cierre, los instaladores pueden usar la opción **RmForceShutdown** de la función [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) para forzar el cierre de las aplicaciones. Cuando el instalador especifica un cierre forzado, el administrador de reinicio intenta cerrar las aplicaciones de forma limpia mediante el envío de los mensajes de cierre, pero obliga a que se cierren si se produce un error. Las aplicaciones de la interfaz gráfica de usuario y las aplicaciones de consola pueden verse obligadas a cerrarse para habilitar la instalación de una actualización de seguridad crítica. Como esto puede dar lugar a la pérdida de datos, las aplicaciones deben controlar los mensajes de cierre y cerrarse correctamente cuando sea necesario.
-   Las aplicaciones deben registrarse para un reinicio mediante la función [**RegisterApplicationRestart**](/windows/desktop/api/winbase/nf-winbase-registerapplicationrestart) . El administrador de reinicio solo puede reiniciar las aplicaciones que se han registrado para reiniciarse. Esta es la única manera en que el administrador de reinicio puede determinar el comando de línea de comandos que se utilizará al reiniciar la aplicación. Si la aplicación debe volver a abrirse con algún Estado o dato guardado, esa información debe incluirse en el comando de línea de comandos registrado para la aplicación.
    > [!Note]  
    > Si la aplicación reiniciada debe ejecutarse en el mismo directorio en el que se ejecutó antes de apagarse, la aplicación debe guardar la información del directorio y, a continuación, cambiar al directorio después de reiniciar.

     

    > [!Note]  
    > La función [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) no reinicia las aplicaciones que no se ejecutan como el usuario que ha iniciado sesión actualmente. Por ejemplo, la función **RmRestart** no reinicia las aplicaciones iniciadas con el comando **Ejecutar como** que no se ejecutan como el usuario que ha iniciado sesión actualmente. Estas aplicaciones se deben reiniciar manualmente.

     

-   Cuando el administrador de reinicio determina que es necesario reiniciar el sistema para instalar una actualización, no apaga las aplicaciones y los servicios. En su lugar, lo deja al instalador para decidir cuándo programar un reinicio del sistema e instalar la actualización. Los instaladores pueden reducir la interrupción de los usuarios causados por actualizaciones que requieren un reinicio del sistema mediante la función [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) con la marca **EWX \_ RESTARTAPPS** o la función [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) con la marca **Shutdown \_ RESTARTAPPS** . El uso de estas marcas garantiza que las aplicaciones registradas para el reinicio se reinician después de un reinicio del sistema, lo que minimiza el impacto en el usuario.

 

 