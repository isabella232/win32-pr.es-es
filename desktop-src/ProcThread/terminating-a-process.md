---
description: 'La terminación de un proceso tiene los siguientes resultados: los subprocesos restantes del proceso se marcan para su finalización. Se liberan todos los recursos asignados por el proceso. Todos los objetos de kernel están cerrados. El código de proceso se quita de la memoria. Se establece el código de salida del proceso. Se señala el objeto de proceso.'
ms.assetid: af24d157-2719-4052-8029-1eb8010047cc
title: Finalizar un proceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2010f1d4332a575c8ee94cf1b0f196e00ba7fb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677827"
---
# <a name="terminating-a-process"></a>Finalizar un proceso

La terminación de un proceso tiene los siguientes resultados:

-   El resto de subprocesos del proceso se marcan para su finalización.
-   Se liberan todos los recursos asignados por el proceso.
-   Todos los objetos de kernel están cerrados.
-   El código de proceso se quita de la memoria.
-   Se establece el código de salida del proceso.
-   Se señala el objeto de proceso.

Aunque los identificadores abiertos para los objetos de kernel se cierran automáticamente cuando finaliza un proceso, los propios objetos existen hasta que se cierran todos los identificadores abiertos. Por lo tanto, un objeto seguirá siendo válido después de que un proceso que lo esté usando termine si otro proceso tiene un identificador abierto.

La función [**API GetExitCodeProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess) devuelve el estado de finalización de un proceso. Mientras se ejecuta un proceso, el estado de finalización sigue siendo \_ activo. Cuando finaliza un proceso, su estado de finalización cambia de todavía \_ activo al código de salida del proceso.

Cuando finaliza un proceso, se señala el estado del objeto de proceso y se liberan los subprocesos que estaban esperando a que finalizara el proceso. Para obtener más información sobre la sincronización, vea [sincronizar la ejecución de varios subprocesos](synchronizing-execution-of-multiple-threads.md).

Cuando el sistema termina un proceso, no finaliza los procesos secundarios que haya creado el proceso. La terminación de un proceso no genera notificaciones para \_ los procedimientos de enlace de CBT.

Utilice la función [**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters) para especificar determinados aspectos de la terminación del proceso en el cierre del sistema, por ejemplo, cuando un proceso debe finalizar en relación con los demás procesos del sistema.

## <a name="how-processes-are-terminated"></a>Cómo se terminan los procesos

Un proceso se ejecuta hasta que se produce uno de los siguientes eventos:

-   Cualquier subproceso del proceso llama a la función [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) . Tenga en cuenta que algunas implementaciones de la biblioteca en tiempo de ejecución de C (CRT) llaman a **ExitProcess** si el subproceso principal del proceso devuelve.
-   Finaliza el último subproceso del proceso.
-   Cualquier subproceso llama a la función [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) con un identificador para el proceso.
-   En los procesos de la consola, el [controlador de control de consola](/windows/console/console-control-handlers) predeterminado llama a [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) cuando la consola recibe una señal CTRL + C o Ctrl + Inter.
-   El usuario apaga el sistema o cierra la sesión.

No finalice un proceso a menos que sus subprocesos se encuentren en Estados conocidos. Si un subproceso está esperando en un objeto de kernel, no se terminará hasta que se haya completado la espera. Esto puede hacer que la aplicación deje de responder.

El subproceso principal puede evitar la terminación de otros subprocesos dirigiendo para llamar a [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) antes de hacer que finalice el proceso (para obtener más información, vea [finalizar un subproceso](terminating-a-thread.md)). El subproceso principal todavía puede llamar a [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) posteriormente para asegurarse de que todos los subprocesos se terminan.

El código de salida de un proceso es el valor especificado en la llamada a [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) o [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess), o el valor devuelto por la función Main o [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) del proceso. Si un proceso finaliza debido a una excepción grave, el código de salida es el valor de la excepción que provocó la terminación. Además, este valor se usa como código de salida para todos los subprocesos que se estaban ejecutando cuando se produjo la excepción.

Si [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)finaliza un proceso, el sistema llama a la función de punto de entrada de cada dll asociada con un valor que indica que el proceso se está desasociando de la dll. No se notifica a los archivos dll cuando [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)finaliza un proceso. Para obtener más información acerca de los archivos dll, consulte [bibliotecas de vínculos dinámicos](../dlls/dynamic-link-libraries.md).

Si [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)finaliza un proceso, todos los subprocesos del proceso se terminan inmediatamente sin que sea posible ejecutar código adicional. Esto significa que el subproceso no ejecuta código en los bloques de controladores de terminación. Además, no se notifica a ningún dll adjunto que el proceso se está desasociando. Si necesita que un proceso termine otro proceso, los pasos siguientes proporcionan una solución mejor:

-   Haga que ambos procesos llamen a la función [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) para crear un mensaje privado.
-   Un proceso puede terminar el otro proceso difundiendo un mensaje privado mediante la función [**BroadcastSystemMessage**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessage) de la siguiente manera:

    ``` syntax
     DWORD dwRecipients = BSM_APPLICATIONS;
        UINT uMessage = PM_MYMSG;
        WPARAM wParam = 0;
        LPARAM lParam = 0;

        BroadcastSystemMessage( 
            BSF_IGNORECURRENTTASK, // do not send message to this process
            &dwRecipients,         // broadcast only to applications
            uMessage,              // registered private message
            wParam,                // message-specific value
            lParam );              // message-specific value
    ```

-   El proceso que recibe el mensaje privado llama a [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) para finalizar su ejecución.

La ejecución de las funciones [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread), [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)y [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) se serializa en un espacio de direcciones. Se aplican las restricciones que se indican a continuación:

-   Durante el inicio del proceso y las rutinas de inicialización de DLL, se pueden crear nuevos subprocesos, pero no inician la ejecución hasta que finalice la inicialización del archivo DLL para el proceso.
-   Solo un subproceso a la vez puede estar en una rutina de inicialización o desasociación de DLL.
-   La función [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) no devuelve hasta que no haya subprocesos en sus rutinas de inicialización o desasociación de dll.

 

 
