---
description: E/S de canalización sincrónica y E/S de canalización asincrónica. Las funciones ReadFile, WriteFile, TransactNamedPipe y ConnectNamedPipe pueden realizar operaciones de entrada y salida en una canalización de forma sincrónica o asincrónica.
ms.assetid: 5ab9bb7f-1f99-4041-bba8-2863f34dbcaf
title: E/S de canalización sincrónica y superpuesta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3becfb19dfe5fa49d4121246a576fb3200226b1a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242180"
---
# <a name="synchronous-and-overlapped-pipe-io"></a>E/S de canalización sincrónica y superpuesta

Las [**funciones ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile,**](/windows/desktop/api/fileapi/nf-fileapi-writefile) [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)y [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) pueden realizar operaciones de entrada y salida en una canalización de forma sincrónica o asincrónica. Cuando una función se ejecuta sincrónicamente, no se devuelve hasta que se completa la operación que está realizando. Esto significa que la ejecución del subproceso que realiza la llamada se puede bloquear durante un período indefinido mientras espera a que se complete una operación que lleva mucho tiempo. Cuando una función se ejecuta de forma asincrónica, devuelve inmediatamente, incluso si la operación no se ha completado. Esto permite ejecutar una operación que tarda mucho tiempo en ejecutarse en segundo plano, mientras que el subproceso que realiza la llamada es libre para realizar otras tareas.

El uso de E/S asincrónica permite que un servidor de canalización use un bucle que realice los pasos siguientes:

1.  Especifique varios objetos de evento en una llamada a la función wait y espere a que uno de los objetos se establezca en el estado señalado.
2.  Use el valor devuelto de la función wait para determinar qué operación superpuesta ha finalizado.
3.  Realice las tareas necesarias para limpiar la operación completada e iniciar la siguiente operación para ese identificador de canalización. Esto puede implicar iniciar otra operación superpuesta para el mismo identificador de canalización.

Las operaciones superpuestas hacen posible que una canalización lea y escriba datos simultáneamente y que un único subproceso realice operaciones de E/S simultáneas en varios identificadores de canalización. Esto permite que un servidor de canalización de un solo subproceso controle las comunicaciones con varios clientes de canalización de forma eficaz. Para obtener un ejemplo, vea [Servidor de canalización con nombre que usa E/S superpuesta.](named-pipe-server-using-overlapped-i-o.md)

Para que un servidor de canalización use operaciones sincrónicas para comunicarse con más de un cliente, debe crear un subproceso independiente para cada cliente de canalización para que uno o varios subprocesos se puedan ejecutar mientras otros subprocesos están esperando. Para obtener un ejemplo de un servidor de canalización multiproceso que usa operaciones sincrónicas, vea [Servidor de canalización multiproceso](multithreaded-pipe-server.md).

## <a name="enabling-asynchronous-operation"></a>Habilitación de la operación asincrónica

Las funciones [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile,**](/windows/desktop/api/fileapi/nf-fileapi-writefile) [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)y [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) solo se pueden realizar de forma asincrónica si habilita el modo superpuesto para el identificador de canalización especificado y especifica un puntero válido a una [**estructura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Si el **puntero OVERLAPPED** es **NULL,** el valor devuelto de la función puede indicar incorrectamente que se ha completado la operación. Por lo tanto, se recomienda encarecidamente que si crea un identificador con FILE FLAG OVERLAPPED y desea un comportamiento asincrónico, siempre debe especificar una \_ \_ estructura **OVERLAPPED** válida.

El **miembro hEvent** de la estructura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) especificada debe contener un identificador para un objeto de evento de restablecimiento manual. Se trata de un objeto de sincronización creado por la [**función CreateEvent.**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) El subproceso que inicia la operación superpuesta usa el objeto de evento para determinar cuándo ha finalizado la operación. No debe usar el identificador de canalización para la sincronización al realizar operaciones simultáneas en el mismo identificador porque no hay ninguna manera de saber qué finalización de la operación hizo que se señalara el identificador de canalización. La única técnica confiable para realizar operaciones simultáneas en el mismo identificador de canalización es usar una estructura **OVERLAPPED** independiente con su propio objeto de evento para cada operación. Para obtener más información sobre los objetos de evento, vea [Synchronization](/windows/desktop/Sync/synchronization).

Además, se le puede notificar cuando se complete una operación superpuesta mediante las funciones [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) o [**GetQueuedCompletionStatusEx.**](/windows/desktop/FileIO/getqueuedcompletionstatusex-func) En este caso, no es necesario asignar el evento de restablecimiento manual en la estructura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) y la finalización se produce en el identificador de canalización de la misma manera que una operación asincrónica de lectura o escritura. Para obtener más información, vea [Puertos de finalización de E/S.](/windows/desktop/FileIO/i-o-completion-ports)

Cuando [**las operaciones ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile,**](/windows/desktop/api/fileapi/nf-fileapi-writefile) [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)y [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) se realizan de forma asincrónica, se produce una de las siguientes operaciones:

-   Si la operación se completa cuando se devuelve la función, el valor devuelto indica si la operación se ha completado correctamente o no. Si se produce un error, el valor devuelto es cero y la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve algo distinto de ERROR \_ IO \_ PENDING.
-   Si la operación no ha finalizado cuando la función vuelve, el valor devuelto es cero y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR \_ IO \_ PENDING. En este caso, el subproceso que realiza la llamada debe esperar hasta que finalice la operación. A continuación, el subproceso que realiza la llamada debe llamar a la [**función GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) para determinar los resultados.

## <a name="using-completion-routines"></a>Usar rutinas de finalización

Las [**funciones ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) y [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) proporcionan otra forma de E/S superpuesta. A diferencia de las funciones [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) y [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) superpuestas, que usan un objeto de evento para señalar la finalización, las funciones extendidas especifican una *rutina de finalización*. Una rutina de finalización es una función que se pone en cola para su ejecución cuando finaliza la operación de lectura o escritura. La rutina de finalización no se ejecuta hasta que el subproceso que llamó *a* **ReadFileEx** y **WriteFileEx** inicia una operación de espera que se puede alertar mediante una llamada a una de las funciones de espera que se pueden alertar con el parámetro *fAlertable* establecido en **TRUE.** [](/windows/desktop/Sync/wait-functions) En una operación de espera que se puede alertar, las funciones también devuelven cuando una rutina de finalización **ReadFileEx** o **WriteFileEx** se pone en cola para su ejecución. Un servidor de canalización puede usar las funciones extendidas para realizar una secuencia de operaciones de lectura y escritura para cada cliente que se conecta a ella. Cada operación de lectura o escritura de la secuencia especifica una rutina de finalización y cada rutina de finalización inicia el siguiente paso de la secuencia. Para obtener un ejemplo, vea [Servidor de canalización con nombre mediante rutinas de finalización](named-pipe-server-using-completion-routines.md).

 

 
