---
description: El servidor de canalización especifica el modo de tipo de canalización, el modo de lectura y el modo de espera en el parámetro dwPipeMode de la función CreateNamedPipe. Los clientes de canalización pueden especificar estos modos de canalización para sus identificadores de canalización mediante la función CreateFile.
ms.assetid: 07cf9d06-6265-47f4-a9f1-c19c06cc5f9f
title: Modos de tipo de canalización con nombre, lectura y espera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3b8ba69ef0d795747070072511c84abf5a3950db3b9c03ec18973f4d29bbd51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014895"
---
# <a name="named-pipe-type-read-and-wait-modes"></a>Modos de tipo de canalización con nombre, lectura y espera

El servidor de canalización especifica el modo de tipo de canalización, el modo de lectura y el modo de espera en el *parámetro dwPipeMode* de la [**función CreateNamedPipe.**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) Los clientes de canalización pueden especificar estos modos de canalización para sus identificadores de canalización mediante la [**función CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

## <a name="type-mode"></a>Modo de tipo

El modo de tipo de una canalización determina cómo se escriben los datos en una canalización con nombre. Los datos se pueden transmitir a través de una canalización con nombre como una secuencia de bytes o como una secuencia de mensajes. El servidor de canalización especifica el tipo de canalización al llamar a [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) para crear una instancia de una canalización con nombre. Los modos de tipo deben ser los mismos para todas las instancias de una canalización.

Para crear una canalización de tipo byte, especifique PIPE \_ TYPE BYTE o use el valor \_ predeterminado. Los datos se escriben en la canalización como una secuencia de bytes y el sistema no diferencia entre los bytes escritos en diferentes operaciones de escritura.

Para crear una canalización de tipo de mensaje, especifique PIPE \_ TYPE \_ MESSAGE. El sistema trata los bytes escritos en cada operación de escritura en la canalización como una unidad de mensaje. El sistema siempre realiza operaciones de escritura en canalizaciones de tipo mensaje como si se habilitara el modo de escritura a través.

## <a name="read-mode"></a>Modo de lectura

El modo de lectura de una canalización determina cómo se leen los datos de una canalización con nombre. El servidor de canalización especifica el modo de lectura inicial para un identificador de canalización al llamar a [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea). Los datos se pueden leer en modo de lectura de bytes o en modo de lectura de mensajes. Un identificador de una canalización de tipo byte solo puede estar en modo de lectura de bytes. Un identificador de una canalización de tipo de mensaje puede estar en modo de lectura de bytes o de lectura de mensajes. Para una canalización de tipo mensaje, el modo de lectura puede ser diferente para los identificadores de servidor y cliente a la misma instancia de canalización.

Para crear el identificador de canalización en modo de lectura de bytes, especifique PIPE \_ READMODE \_ BYTE o use el valor predeterminado. Los datos se leen de la canalización como una secuencia de bytes. Una operación de lectura se completa correctamente cuando se leen todos los bytes disponibles en la canalización o cuando se lee el número especificado de bytes.

Para crear el identificador de canalización en modo de lectura de mensajes, especifique PIPE \_ READMODE \_ MESSAGE. Los datos se leen desde la canalización como una secuencia de mensajes. Una operación de lectura se completa correctamente solo cuando se lee todo el mensaje. Si el número de bytes especificado para leer es menor que el tamaño del mensaje siguiente, la función lee la mayor parte del mensaje posible antes de devolver cero (la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR \_ MORE \_ DATA). El resto del mensaje se puede leer mediante otra operación de lectura.

Para un cliente de canalización, un identificador de canalización devuelto por [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) siempre está en modo de lectura de bytes inicialmente. Tanto los clientes de canalización como los servidores de canalización pueden usar la función [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) para cambiar el modo de lectura de un identificador de canalización. El identificador de canalización debe tener el derecho de acceso FILE \_ WRITE \_ ATTRIBUTES.

## <a name="wait-mode"></a>Modo de espera

El modo de espera de un identificador de canalización determina cómo las funciones [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)y [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) controlan operaciones largas. En el modo de bloqueo y espera, las funciones esperan indefinidamente a que un proceso en el otro extremo de la canalización complete una operación. En el modo de espera sin bloqueo, las funciones se devuelven inmediatamente en situaciones que, de lo contrario, requerirían una espera indefinida.

Una [**operación ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) se ve afectada por el modo de espera de un identificador de canalización cuando la canalización está vacía. Con un identificador de bloqueo y espera, la operación no se completa correctamente hasta que los datos están disponibles desde un subproceso que escribe en el otro extremo de la canalización. Con un identificador de espera sin bloqueo, la función devuelve cero inmediatamente y la [**función GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR \_ NO \_ DATA.

Una [**operación WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) se ve afectada por el modo de espera de un identificador de canalización cuando no hay suficiente espacio en el búfer de la canalización. Con un identificador de bloqueo y espera, la operación de escritura no se puede realizar correctamente hasta que un subproceso lea el otro extremo de la canalización para crear espacio suficiente en el búfer. Con un identificador de espera sin bloqueo, la operación de escritura devuelve un valor distinto de cero inmediatamente, sin escribir bytes (para una canalización de tipo de mensaje) o después de escribir tantos bytes como el búfer contiene (para una canalización de tipo byte).

Una [**operación ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) se ve afectada por el modo de espera de un identificador de canalización cuando no hay ningún cliente conectado o esperando conectarse a la instancia de canalización. Con un identificador de bloqueo y espera, la operación de conexión no se realiza correctamente hasta que un cliente de canalización se conecta a la instancia de canalización mediante una llamada a la [**función CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o [**CallNamedPipe.**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) Con un identificador de espera sin bloqueo, la operación de conexión devuelve cero inmediatamente y la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR \_ PIPE \_ LISTENING.

De forma predeterminada, todos los identificadores de canalización con nombre devueltos por la [**función CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) o [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) se crean con el modo de bloqueo y espera habilitado. Para crear la canalización en modo de espera sin bloqueo, el servidor de canalización especifica PIPE \_ NOWAIT al llamar a **CreateNamedPipe**.

Tanto los clientes de canalización como los servidores de canalización pueden cambiar el modo de espera de un identificador de canalización especificando PIPE WAIT o PIPE NOWAIT en una llamada a la función \_ \_ [**SetNamedPipeHandleState.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate)

> [!Note]  
> El modo de espera de no bloqueo es compatible con la versión 2.0 de Microsoft LAN Manager. Este modo no debe usarse para lograr entradas y salidas superpuestas (E/S) con canalizaciones con nombre. En su lugar, se debe usar E/S superpuesta, ya que permite que las operaciones que tardan mucho tiempo se ejecuten en segundo plano después de que se devuelva la función. Para obtener más información sobre la E/S superpuesta, vea Entrada y salida [superpuestas y sincrónicas.](synchronous-and-overlapped-input-and-output.md)

 

 

 
