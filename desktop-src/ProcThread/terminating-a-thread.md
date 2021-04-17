---
description: 'La terminación de un subproceso tiene los siguientes resultados: se liberan todos los recursos que pertenecen al subproceso, como ventanas y enlaces. Se establece el código de salida del subproceso. Se señala el objeto de subproceso. Si el subproceso es el único subproceso activo en el proceso, el proceso se termina. Para obtener más información, vea finalizar un proceso.'
ms.assetid: 633e5d0c-e9d8-4f9a-9411-17cbe9e2e6e4
title: Finalización de un subproceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada421356666316072aabff8281787cc140ad114
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677826"
---
# <a name="terminating-a-thread"></a>Finalización de un subproceso

La terminación de un subproceso tiene los siguientes resultados:

-   Se liberan todos los recursos que pertenecen al subproceso, como ventanas y enlaces.
-   Se establece el código de salida del subproceso.
-   Se señala el objeto de subproceso.
-   Si el subproceso es el único subproceso activo en el proceso, el proceso se termina. Para obtener más información, vea [finalizar un proceso](terminating-a-process.md).

La función [**GetExitCodeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodethread) devuelve el estado de finalización de un subproceso. Mientras se ejecuta un subproceso, su estado de finalización sigue siendo \_ activo. Cuando un subproceso finaliza, su estado de finalización cambia de todavía \_ activo al código de salida del subproceso.

Cuando finaliza un subproceso, el estado del objeto de subproceso cambia a señalado y libera cualquier otro subproceso que haya estado esperando a que el subproceso finalice. Para obtener más información sobre la sincronización, vea [sincronizar la ejecución de varios subprocesos](synchronizing-execution-of-multiple-threads.md).

Cuando un subproceso finaliza, su objeto de subproceso no se libera hasta que se cierran todos los identificadores abiertos al subproceso.

## <a name="how-threads-are-terminated"></a>Cómo se finalizan los subprocesos

Un subproceso se ejecuta hasta que se produce uno de los siguientes eventos:

-   El subproceso llama a la función [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) .
-   Cualquier subproceso del proceso llama a la función [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) .
-   La función Thread devuelve.
-   Cualquier subproceso llama a la función [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) con un identificador al subproceso.
-   Cualquier subproceso llama a la función [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) con un identificador para el proceso.

El código de salida de un subproceso es el valor especificado en la llamada a [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)o [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess), o el valor devuelto por la función de subproceso.

Si se termina un subproceso por [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), el sistema llama a la función de punto de entrada de cada dll asociada con un valor que indica que el subproceso se está desasociando del archivo DLL (a menos que se llame a la función [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) ). Si [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)termina un subproceso, las funciones de punto de entrada de dll se invocan una vez para indicar que el proceso se está desasociando. No se notifica a los archivos dll cuando se termina un subproceso mediante [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) o [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Para obtener más información acerca de los archivos dll, consulte [bibliotecas de vínculos dinámicos](../dlls/dynamic-link-libraries.md).

Las funciones [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) y [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) deben usarse solo en circunstancias extremas, ya que no permiten que los subprocesos se limpien, no notifican a las DLL adjuntas y no liberan la pila inicial. Además, los identificadores de los objetos que son propiedad del subproceso no se cierran hasta que finaliza el proceso. Los pasos siguientes proporcionan una solución mejor:

-   Cree un objeto de evento mediante la función [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) .
-   Cree los subprocesos.
-   Cada subproceso supervisa el estado del evento mediante una llamada a la función [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) . Use un intervalo de tiempo de espera de espera de cero.
-   Cada subproceso finaliza su propia ejecución cuando el evento se establece en el estado señalado ([**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) devuelve el \_ objeto 0 de espera \_ ).

 

 
