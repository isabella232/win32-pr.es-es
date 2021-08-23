---
description: 'La terminación de un subproceso tiene los siguientes resultados: se liberan todos los recursos que pertenecen al subproceso, como ventanas y enlaces. Se establece el código de salida del subproceso. Se señala el objeto de subproceso. Si el subproceso es el único subproceso activo del proceso, el proceso finaliza. Para obtener más información, vea Terminating a Process.'
ms.assetid: 633e5d0c-e9d8-4f9a-9411-17cbe9e2e6e4
title: Terminación de un subproceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef64729db5490ebdab3ba759b34a105c31d2cbc421a404d07b041aa9b611ba08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799045"
---
# <a name="terminating-a-thread"></a>Terminación de un subproceso

La terminación de un subproceso tiene los siguientes resultados:

-   Se liberan todos los recursos que pertenecen al subproceso, como ventanas y enlaces.
-   Se establece el código de salida del subproceso.
-   Se señala el objeto de subproceso.
-   Si el subproceso es el único subproceso activo del proceso, el proceso finaliza. Para obtener más información, [vea Terminating a Process](terminating-a-process.md).

La [**función GetExitCodeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodethread) devuelve el estado de finalización de un subproceso. Mientras se ejecuta un subproceso, su estado de terminación es STILL \_ ACTIVE. Cuando un subproceso finaliza, su estado de finalización cambia de STILL \_ ACTIVE al código de salida del subproceso.

Cuando un subproceso finaliza, el estado del objeto de subproceso cambia a señalado, liberando cualquier otro subproceso que hubiera estado esperando a que finalizara el subproceso. Para obtener más información sobre la sincronización, [vea Sincronizar la ejecución de varios subprocesos.](synchronizing-execution-of-multiple-threads.md)

Cuando un subproceso finaliza, su objeto de subproceso no se libera hasta que se cierran todos los identificadores abiertos del subproceso.

## <a name="how-threads-are-terminated"></a>Cómo se terminan los subprocesos

Un subproceso se ejecuta hasta que se produce uno de los siguientes eventos:

-   El subproceso llama a la [**función ExitThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)
-   Cualquier subproceso del proceso llama a la [**función ExitProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)
-   La función de subproceso devuelve .
-   Cualquier subproceso llama a [**la función TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) con un identificador para el subproceso.
-   Cualquier subproceso llama a [**la función TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) con un identificador para el proceso.

El código de salida de un subproceso es el valor especificado en la llamada a [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)o [**TerminateProcess,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)o el valor devuelto por la función de subproceso.

Si [**exitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)finaliza un subproceso , el sistema llama a la función de punto de entrada de cada archivo DLL adjunto con un valor que indica que el subproceso se está desasociando del archivo DLL (a menos que llame a la [**función DisableThreadLibraryCalls).**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) Si [**exitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)finaliza un subproceso , las funciones de punto de entrada de DLL se invocan una vez para indicar que el proceso se está desasociando. Los archivos DLL no se notifican cuando [**terminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) o TerminateProcess finalizan [**un subproceso.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) Para obtener más información sobre los archivos DLL, vea [Bibliotecas de vínculos dinámicos.](../dlls/dynamic-link-libraries.md)

Las [**funciones TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) y [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) solo se deben usar en circunstancias extremas, ya que no permiten que los subprocesos se limpien, no notifican a los archivos DLL adjuntos y no liberan la pila inicial. Además, los identificadores de los objetos que pertenecen al subproceso no se cierran hasta que finaliza el proceso. Los pasos siguientes proporcionan una solución mejor:

-   Cree un objeto de evento mediante la [**función CreateEvent.**](/windows/win32/api/synchapi/nf-synchapi-createeventa)
-   Cree los subprocesos.
-   Cada subproceso supervisa el estado del evento llamando a [**la función WaitForSingleObject.**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) Use un intervalo de tiempo de espera de cero.
-   Cada subproceso finaliza su propia ejecución cuando el evento se establece en el estado señalado ([**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) devuelve WAIT \_ OBJECT \_ 0).

 

 
