---
description: Las cuentas de usuario de Windows XP permiten que varios usuarios inicien sesión simultáneamente, cada uno con su propia configuración y que ejecute sus propias aplicaciones.
ms.assetid: bc404afc-f73e-404d-854d-faab5cf205a5
title: Cuentas de usuario con cambio rápido de usuario y Escritorio remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc26471bcf56efce79fb5ccc91a78c24e43ae312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997752"
---
# <a name="user-accounts-with-fast-user-switching-and-remote-desktop"></a>Cuentas de usuario con cambio rápido de usuario y Escritorio remoto

Las cuentas de usuario de Windows XP permiten que varios usuarios inicien sesión simultáneamente, cada uno con su propia configuración y que ejecute sus propias aplicaciones. Dado que un usuario no tiene que cerrar sesión para permitir el acceso a otro usuario, se puede acceder fácilmente al escritorio de cada usuario mediante la característica de cambio rápido de usuario. Las cuentas de usuario también incluyen la característica de Terminal Server personal o Escritorio remoto, que permite a los usuarios tener acceso a su cuenta de escritorio desde sistemas remotos.

Se tratan los temas siguientes.

-   [Requisitos de uso de la infraestructura](#infrastructure-usage-requirements)
-   [Compatibilidad con las aplicaciones existentes](#compatibility-with-existing-applications)
-   [Registrando notificación de cambio de sesión](#registering-for-session-switching-notification)
-   [Asegurarse de que solo se está ejecutando una instancia de la aplicación](#ensuring-only-one-instance-of-your-application-is-running)
-   [Cierre de la aplicación en todas las sesiones](#shutting-down-your-application-across-all-sessions)
-   [Interacción con servicios del sistema](#interaction-with-system-services)
-   [Escritorio remoto y ancho de banda](#remote-desktop-and-bandwidth)

## <a name="infrastructure-usage-requirements"></a>Requisitos de uso de la infraestructura

La infraestructura subyacente heredada de Windows 2000 admite la separación del estado de los datos de usuario, la configuración de usuario y la configuración del equipo. Al aprovechar esta infraestructura, se necesita lo siguiente para ejecutar correctamente la aplicación en Windows XP.

-   El valor predeterminado es la carpeta **Mis documentos** para el almacenamiento de datos creados por el usuario.
-   Clasifique y almacene los datos de la aplicación correctamente.
-   Se degradan correctamente en los mensajes de "acceso denegado".

Los archivos temporales, los archivos asignados a la memoria y los documentos deben almacenarse en el subdirectorio correspondiente del directorio del perfil del usuario. Use [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) o [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) para determinar la ubicación de almacenamiento adecuada para estos archivos. Al pasar la marca [**CSIDL \_ AppData**](csidl.md) a estas funciones, se devuelve la ruta de acceso de un directorio del sistema de archivos que sirve de repositorio común para los datos específicos de la aplicación. Use la marca [**CSIDL \_ local \_ AppData**](csidl.md) en lugar de **CSIDL \_ AppData** para los datos que deben cambiar cuando el usuario cambia, como archivos temporales.

Los requisitos mencionados anteriormente son un subconjunto de los del programa de certificación de Microsoft. Para obtener más información, consulte la página del **programa certificado para Windows** en https://www.microsoft.com/windowsserver2003/partners/isvs/cfw.mspx .

## <a name="compatibility-with-existing-applications"></a>Compatibilidad con las aplicaciones existentes

Tanto el cambio rápido de usuario como el personal Terminal Server utilizan la tecnología de Terminal Services y, por tanto, son compatibles con la mayoría de las aplicaciones de Microsoft Win32 anteriores. Si una aplicación es compatible con el logotipo de Windows 2000, implementando características básicas de separación de perfiles y administración de energía, esa aplicación debe ejecutarse correctamente en cuentas de usuario individuales de Windows XP.

## <a name="registering-for-session-switching-notification"></a>Registrando notificación de cambio de sesión

Normalmente, no es necesario notificar a una aplicación cuando se produce un cambio de escritorio. Sin embargo, las aplicaciones que se deben notificar cuando la cuenta en la que se ejecutan es el escritorio actual, como las aplicaciones que tienen acceso al puerto serie u otros recursos compartidos, pueden registrarse para recibir notificaciones de cambio de escritorio. Para registrarse para una notificación, utilice la función [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) .

Una vez que se ha llamado a esa función, la ventana con el identificador *hWnd* se registra para recibir un mensaje de [**cambio de WM \_ \_ WTSSESSION**](../termserv/wm-wtssession-change.md) a través de su función **WndProc** . El identificador de sesión se envía en el parámetro **lParam** y un código que indica que el evento que generó el mensaje se envía en **wParam** como una de las marcas siguientes.

-   conexión de la consola de WTS \_ \_
-   desconexión de la consola de WTS \_ \_
-   \_conexión remota de WTS \_
-   desconexión remota de WTS \_ \_
-   cierre de sesión de sesión de WTS \_ \_
-   Inicio de sesión de sesión de WTS \_ \_

Las aplicaciones pueden usar este mensaje para realizar el seguimiento de su estado, así como para liberar y adquirir recursos específicos de la consola. Los escritorios de usuario se pueden cambiar dinámicamente entre el control remoto y el control de consola. Las aplicaciones deben usar el mensaje de [**\_ \_ cambio de WTSSESSION de WM**](../termserv/wm-wtssession-change.md) para sincronizar con el estado de conexión local o remota.

Cuando el proceso ya no requiera estas notificaciones o finalice, debe llamar a [**WTSUnRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsunregistersessionnotification) para anular el registro de su notificación.

> [!IMPORTANT]
> Se cuentan las referencias de los valores **hWnd** pasados a [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) , por lo que debe realizar un número igual de llamadas a [**WTSUnRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsunregistersessionnotification) para asegurarse de que se liberan todos los recursos asignados.

 

## <a name="ensuring-only-one-instance-of-your-application-is-running"></a>Asegurarse de que solo se está ejecutando una instancia de la aplicación

Muchas aplicaciones deben asegurarse de que solo tienen una instancia en ejecución. Hay varias maneras de hacerlo en Windows XP. Entre ellas se encuentran las siguientes:

-   Use [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) o [**FindWindowEx**](/windows/win32/api/winuser/nf-winuser-findwindowexa) para buscar una ventana conocida que abra la aplicación. Si esa ventana ya está abierta, puede usarla como una indicación de que la aplicación ya se está ejecutando.
-   Cree un objeto mutex o Semaphore cuando se abra la aplicación y cierre el objeto cuando la aplicación finalice. El espacio de nombres de objeto global se separa para cada escritorio, lo que permite una lista única de objetos de exclusión mutua y semáforo para cada uno.

## <a name="shutting-down-your-application-across-all-sessions"></a>Cierre de la aplicación en todas las sesiones

Es posible que una aplicación deba cerrarse en todas las sesiones. Por ejemplo, una aplicación que se ejecuta en dos o más sesiones simultáneamente podría descargar un nuevo archivo de la Web. Después, es posible que deba cerrarse y reiniciarse con los bits actualizados. Esto, por supuesto, debe realizarse en todas las sesiones en ejecución. Se debe escribir la aplicación para que se cierre correctamente cuando se reciba una notificación.

## <a name="interaction-with-system-services"></a>Interacción con servicios del sistema

Desde el punto de vista de programación, es necesario solucionar los siguientes casos.

-   El proceso de servidor recibe una solicitud directa de un proceso de cliente.

    En este caso, es probable que el mensaje se transmita mediante una llamada a procedimiento local (LPC) o una llamada a procedimiento remoto (RPC). Hay API para LPC o RPC que permiten la recuperación del token de cliente. Una vez que se obtiene el token de cliente, el servidor puede usarlo en una llamada a [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera). Esto abre el proceso en la estación de ventana correcta, suponiendo que el token de usuario del cliente tiene una etiqueta de sesión, que debería.

    > [!Note]  
    > [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) no admite la herencia de control entre sesiones en este momento.

     

-   El proceso de servidor recibe una notificación y debe mostrar la interfaz de usuario, pero la pantalla no tiene que estar en el contexto del usuario actual.

    En este caso, el proceso de servidor puede duplicar su token de proceso principal y cambiar el identificador de sesión en cuestión para que coincida con el identificador de sesión actual. El identificador de la sesión actual se puede obtener mediante la función [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid) .

    > [!Note]  
    > Para establecer el identificador de sesión de token, se necesita el **\_ \_ privilegio de TCB se**. Solo tendrá esto como un servicio que se ejecuta en NT AUTHORITY \\ System.

     

## <a name="remote-desktop-and-bandwidth"></a>Escritorio remoto y ancho de banda

Con la adición de la característica Escritorio remoto a Windows XP, las aplicaciones deben hacer un esfuerzo para no usar más ancho de banda de lo necesario, evitando los complejos dibujos de pantalla y los efectos de animación si el escritorio está conectado de forma remota. Para determinar si la sesión actual es remota, puede llamar a [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) con **SM \_ REMOTESESSION**. No obstante, tenga en cuenta que esta llamada no distingue entre el remoto y el desconectado.

 

 
