---
description: E/s de canalización sincrónica y e/s de canalización asincrónica. Las funciones ReadFile, WriteFile, TransactNamedPipe y ConnectNamedPipe pueden realizar operaciones de entrada y salida en una canalización de forma sincrónica o asincrónica.
ms.assetid: 5ab9bb7f-1f99-4041-bba8-2863f34dbcaf
title: E/s de canalización sincrónica y superpuesta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3becfb19dfe5fa49d4121246a576fb3200226b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697709"
---
# <a name="synchronous-and-overlapped-pipe-io"></a>E/s de canalización sincrónica y superpuesta

Las funciones [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)y [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) pueden realizar operaciones de entrada y salida en una canalización de forma sincrónica o asincrónica. Cuando una función se ejecuta sincrónicamente, no devuelve ningún resultado hasta que se completa la operación que está realizando. Esto significa que la ejecución del subproceso que realiza la llamada puede bloquearse durante un período indefinido mientras espera a que se complete una operación que consume mucho tiempo. Cuando una función se ejecuta de forma asincrónica, se devuelve inmediatamente, incluso si no se ha completado la operación. Esto permite que una operación que consume mucho tiempo se ejecute en segundo plano, mientras que el subproceso que realiza la llamada puede realizar otras tareas de forma gratuita.

El uso de e/s asincrónica permite que un servidor de canalización use un bucle que realice los pasos siguientes:

1.  Especifique varios objetos de evento en una llamada a la función wait y espere a que uno de los objetos se establezca en el estado señalado.
2.  Use el valor devuelto de la función wait para determinar qué operación superpuesta ha finalizado.
3.  Realice las tareas necesarias para limpiar la operación completada e iniciar la siguiente operación para ese identificador de canalización. Esto puede implicar el inicio de otra operación superpuesta para el mismo identificador de canalización.

Las operaciones superpuestas permiten que una canalización Lea y escriba datos simultáneamente, y que un solo subproceso realice operaciones de e/s simultáneas en varios identificadores de canalización. Esto permite que un servidor de canalización de un solo subproceso controle de forma eficaz las comunicaciones con varios clientes de canalización. Para obtener un ejemplo, vea [servidor de canalización con nombre mediante e/s superpuesta](named-pipe-server-using-overlapped-i-o.md).

Para que un servidor de canalización use operaciones sincrónicas para comunicarse con más de un cliente, debe crear un subproceso independiente para cada cliente de canalización, de modo que se puedan ejecutar uno o más subprocesos mientras otros subprocesos están esperando. Para obtener un ejemplo de un servidor de canalización multiproceso que usa operaciones sincrónicas, vea [servidor de canalización multiproceso](multithreaded-pipe-server.md).

## <a name="enabling-asynchronous-operation"></a>Habilitar la operación asincrónica

Las funciones [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)y [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) solo se pueden realizar de forma asincrónica si se habilita el modo superpuesto para el identificador de canalización especificado y se especifica un puntero válido a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) . Si el puntero **SUPERpuesto** es **null**, el valor devuelto de la función puede indicar incorrectamente que se ha completado la operación. Por lo tanto, se recomienda encarecidamente que, si crea un identificador con la marca de archivo \_ \_ superpuesto y desee el comportamiento asincrónico, siempre debe especificar una estructura **superpuesta** válida.

El miembro **hEvent** de la estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) especificada debe contener un identificador para un objeto de evento de restablecimiento manual. Se trata de un objeto de sincronización creado por la función [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) . El subproceso que inicia la operación superpuesta utiliza el objeto de evento para determinar cuándo ha finalizado la operación. No debe utilizar el controlador de canalización para la sincronización al realizar operaciones simultáneas en el mismo identificador porque no hay ninguna manera de saber la finalización de la operación que provocó la señalización del identificador de canalización. La única técnica confiable para realizar operaciones simultáneas en el mismo identificador de canalización es usar una estructura **superpuesta** independiente con su propio objeto de evento para cada operación. Para obtener más información acerca de los objetos de evento, consulte [Synchronization](/windows/desktop/Sync/synchronization).

Además, se puede recibir una notificación cuando se complete una operación superpuesta mediante las funciones [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) o [**GetQueuedCompletionStatusEx**](/windows/desktop/FileIO/getqueuedcompletionstatusex-func) . En este caso, no es necesario asignar el evento de restablecimiento manual en la estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) y la finalización se produce en el identificador de canalización de la misma manera que una operación de lectura o escritura asincrónica. Para obtener más información, vea [puertos de finalización de e/s](/windows/desktop/FileIO/i-o-completion-ports).

Cuando se realizan operaciones [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)y [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) de forma asincrónica, se produce uno de los siguientes casos:

-   Si la operación se completa cuando la función devuelve, el valor devuelto indica si la operación se ha realizado correctamente o no. Si se produce un error, el valor devuelto es cero y la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve algo distinto del error de \_ e/s \_ pendiente.
-   Si la operación no ha finalizado cuando la función devuelve, el valor devuelto es cero y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el error de \_ e/s \_ pendiente. En este caso, el subproceso de llamada debe esperar hasta que la operación haya finalizado. A continuación, el subproceso que realiza la llamada debe llamar a la función [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) para determinar los resultados.

## <a name="using-completion-routines"></a>Usar rutinas de finalización

Las funciones [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) y [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) proporcionan otra forma de e/s superpuestas. A diferencia de las funciones [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) y [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) superpuestas, que utilizan un objeto de evento para indicar la finalización, las funciones extendidas especifican una *rutina de finalización*. Una rutina de finalización es una función que se pone en cola para su ejecución cuando finaliza la operación de lectura o escritura. La rutina de finalización no se ejecuta hasta que el subproceso que llamó a **ReadFileEx** y **WriteFileEx** inicia una operación de *espera de alerta* mediante una llamada a una de las funciones de [espera de alerta](/windows/desktop/Sync/wait-functions) con el parámetro *fAlertable* establecido en **true**. En una operación de espera de alerta, las funciones también devuelven cuando una rutina de finalización **ReadFileEx** o **WriteFileEx** se pone en cola para su ejecución. Un servidor de canalización puede utilizar las funciones extendidas para realizar una secuencia de operaciones de lectura y escritura para cada cliente que se conecta a ella. Cada operación de lectura o escritura de la secuencia especifica una rutina de finalización y cada rutina de finalización inicia el siguiente paso de la secuencia. Para obtener un ejemplo, vea [servidor de canalización con nombre mediante rutinas de finalización](named-pipe-server-using-completion-routines.md).

 

 
