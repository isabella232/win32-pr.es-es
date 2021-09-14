---
description: 'La terminación de un proceso tiene los siguientes resultados: los subprocesos restantes del proceso se marcan para su finalización. Se liberan todos los recursos asignados por el proceso. Se cierran todos los objetos de kernel. El código de proceso se quita de la memoria. Se establece el código de salida del proceso. Se señala el objeto de proceso.'
ms.assetid: af24d157-2719-4052-8029-1eb8010047cc
title: Terminación de un proceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2010f1d4332a575c8ee94cf1b0f196e00ba7fb9f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062795"
---
# <a name="terminating-a-process"></a>Terminación de un proceso

La terminación de un proceso tiene los siguientes resultados:

-   Los subprocesos restantes del proceso se marcan para su finalización.
-   Se liberan todos los recursos asignados por el proceso.
-   Se cierran todos los objetos de kernel.
-   El código de proceso se quita de la memoria.
-   Se establece el código de salida del proceso.
-   Se señala el objeto de proceso.

Aunque los identificadores abiertos para los objetos de kernel se cierran automáticamente cuando finaliza un proceso, los propios objetos existen hasta que se cierran todos los identificadores abiertos. Por lo tanto, un objeto seguirá siendo válido después de que un proceso que lo usa finalice si otro proceso tiene un identificador abierto.

La [**función GetExitCodeProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess) devuelve el estado de finalización de un proceso. Mientras se ejecuta un proceso, su estado de finalización es STILL \_ ACTIVE. Cuando finaliza un proceso, su estado de finalización cambia de STILL \_ ACTIVE al código de salida del proceso.

Cuando finaliza un proceso, se señala el estado del objeto de proceso, liberando los subprocesos que estaban esperando a que finalizara el proceso. Para obtener más información sobre la sincronización, [vea Sincronizar la ejecución de varios subprocesos.](synchronizing-execution-of-multiple-threads.md)

Cuando el sistema está finalizando un proceso, no finaliza ningún proceso secundario que haya creado el proceso. La terminación de un proceso no genera notificaciones para los procedimientos de enlace \_ CBT de WH.

Use la [**función SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters) para especificar determinados aspectos de la terminación del proceso durante el cierre del sistema, como cuando un proceso debe finalizar en relación con los demás procesos del sistema.

## <a name="how-processes-are-terminated"></a>Cómo se finalizan los procesos

Un proceso se ejecuta hasta que se produce uno de los siguientes eventos:

-   Cualquier subproceso del proceso llama a la [**función ExitProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) Tenga en cuenta que alguna implementación de la biblioteca en tiempo de ejecución de C (CRT) llama **a ExitProcess** si se devuelve el subproceso principal del proceso.
-   Finaliza el último subproceso del proceso.
-   Cualquier subproceso llama a [**la función TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) con un identificador para el proceso.
-   Para los procesos de consola, el controlador [de control de](/windows/console/console-control-handlers) consola predeterminado llama a [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) cuando la consola recibe una señal CTRL+C o CTRL+BREAK.
-   El usuario apaga el sistema o cierra la sesión.

No finalice un proceso a menos que sus subprocesos estén en estados conocidos. Si un subproceso está esperando en un objeto kernel, no se finalizará hasta que se haya completado la espera. Esto puede hacer que la aplicación deje de responder.

El subproceso principal puede evitar terminar otros subprocesos si se les dirige a llamar a [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) antes de hacer que el proceso finalice (para obtener más información, vea [Terminating a Thread](terminating-a-thread.md)). El subproceso principal todavía puede llamar a [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) posteriormente para asegurarse de que todos los subprocesos finalizan.

El código de salida de un proceso es el valor especificado en la llamada a [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) o [**TerminateProcess,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)o el valor devuelto por la función main o [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) del proceso. Si un proceso finaliza debido a una excepción grave, el código de salida es el valor de la excepción que produjo la terminación. Además, este valor se usa como código de salida para todos los subprocesos que se estaban ejecutando cuando se produjo la excepción.

Si [**exitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)finaliza un proceso, el sistema llama a la función de punto de entrada de cada archivo DLL adjunto con un valor que indica que el proceso se está desasociando del archivo DLL. Los archivos DLL no se notifican cuando terminateProcess finaliza un [**proceso.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) Para obtener más información sobre los archivos DLL, vea [Bibliotecas de vínculos dinámicos.](../dlls/dynamic-link-libraries.md)

Si [**terminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)finaliza un proceso, todos los subprocesos del proceso se finalizan inmediatamente sin posibilidad de ejecutar código adicional. Esto significa que el subproceso no ejecuta código en bloques de controlador de terminación. Además, no se notifica a ningún archivo DLL adjunto que el proceso se esté desasoyando. Si necesita que un proceso finalice otro, los pasos siguientes proporcionan una solución mejor:

-   Hacer que ambos procesos llamen [**a la función RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) para crear un mensaje privado.
-   Un proceso puede finalizar el otro proceso mediante la difusión de un mensaje privado mediante la [**función BroadcastSystemMessage**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessage) como se indica a continuación:

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

-   El proceso que recibe el mensaje privado llama [**a ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) para finalizar su ejecución.

La ejecución de las [**funciones ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), [**CreateThread,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)y [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) se serializa dentro de un espacio de direcciones. Se aplican las restricciones que se indican a continuación:

-   Durante el inicio del proceso y las rutinas de inicialización de DLL, se pueden crear nuevos subprocesos, pero no comienzan la ejecución hasta que finaliza la inicialización del archivo DLL para el proceso.
-   Solo un subproceso a la vez puede estar en una rutina de inicialización o desaso según el archivo DLL.
-   La [**función ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) no se devuelve hasta que no hay subprocesos en sus rutinas de inicialización o desaso según el archivo DLL.

 

 
