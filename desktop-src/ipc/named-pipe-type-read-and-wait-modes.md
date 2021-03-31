---
description: El servidor de canalización especifica el modo de tipo de canalización, el modo de lectura y el modo de espera en el parámetro dwPipeMode de la función CreateNamedPipe. Los clientes de canalización pueden especificar estos modos de canalización para los identificadores de canalización mediante la función CreateFile.
ms.assetid: 07cf9d06-6265-47f4-a9f1-c19c06cc5f9f
title: Tipos de canalización con nombre, lectura y modos de espera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b116e5ca9357a65a6d63549b96065843b046d479
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907626"
---
# <a name="named-pipe-type-read-and-wait-modes"></a>Tipos de canalización con nombre, lectura y modos de espera

El servidor de canalización especifica el modo de tipo de canalización, el modo de lectura y el modo de espera en el parámetro *dwPipeMode* de la función [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) . Los clientes de canalización pueden especificar estos modos de canalización para los identificadores de canalización mediante la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

## <a name="type-mode"></a>Modo de tipo

El modo de tipo de una canalización determina el modo en que los datos se escriben en una canalización con nombre. Los datos se pueden transmitir a través de una canalización con nombre como una secuencia de bytes o como una secuencia de mensajes. El servidor de canalización especifica el tipo de canalización cuando se llama a [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) para crear una instancia de una canalización con nombre. Los modos de tipo deben ser los mismos para todas las instancias de una canalización.

Para crear una canalización de tipo byte, especifique \_ el tipo de canalización \_ byte o use el valor predeterminado. Los datos se escriben en la canalización como un flujo de bytes y el sistema no distingue entre los bytes escritos en diferentes operaciones de escritura.

Para crear una canalización de tipo de mensaje, especifique el mensaje de tipo de CANALización \_ \_ . El sistema trata los bytes escritos en cada operación de escritura en la canalización como una unidad de mensaje. El sistema siempre realiza operaciones de escritura en canalizaciones de tipo de mensaje como si estuviera habilitado el modo de escritura a través.

## <a name="read-mode"></a>Modo de lectura

El modo de lectura de una canalización determina cómo se leen los datos de una canalización con nombre. El servidor de canalización especifica el modo de lectura inicial para un identificador de canalización al llamar a [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea). Los datos se pueden leer en modo de lectura de bytes o en modo de lectura de mensaje. Un identificador de una canalización de tipo byte solo puede estar en modo de lectura de bytes. Un identificador de una canalización de tipo de mensaje puede estar en modo de lectura de bytes o de lectura de mensaje. En el caso de una canalización de tipo de mensaje, el modo de lectura puede ser diferente para los identificadores de servidor y de cliente en la misma instancia de canalización.

Para crear el identificador de canalización en modo de lectura de bytes, especifique PIPE \_ READMODE \_ byte o use el valor predeterminado. Los datos se leen de la canalización como un flujo de bytes. Una operación de lectura se completa correctamente cuando se leen todos los bytes disponibles en la canalización o cuando se lee el número de bytes especificado.

Para crear el identificador de canalización en modo de lectura de mensaje, especifique el mensaje de CANALización \_ READMODE \_ . Los datos se leen de la canalización como una secuencia de mensajes. Una operación de lectura se completa correctamente solo cuando se lee todo el mensaje. Si el número especificado de bytes que se van a leer es menor que el tamaño del mensaje siguiente, la función Lee tanto como sea posible el mensaje antes de devolver cero (la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve los datos de error \_ \_ ). El resto del mensaje se puede leer mediante otra operación de lectura.

Para un cliente de canalización, un identificador de canalización devuelto por [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) siempre está en modo de lectura de bytes inicialmente. Ambos clientes de canalización y los servidores de canalización pueden utilizar la función [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) para cambiar el modo de lectura de un identificador de canalización. El identificador de canalización debe tener \_ el \_ derecho de acceso a los atributos de escritura de archivo.

## <a name="wait-mode"></a>Modo de espera

El modo de espera de un identificador de canalización determina cómo las funciones [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)y [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) controlan las operaciones largas. En el modo de bloqueo y espera, las funciones esperan indefinidamente a un proceso en el otro extremo de la canalización para completar una operación. En el modo de espera, las funciones se devuelven inmediatamente en situaciones que, de lo contrario, podrían requerir una espera indefinida.

Una operación [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) se ve afectada por el modo de espera de un identificador de canalización cuando la canalización está vacía. Con un identificador de espera de bloqueo, la operación no se completa correctamente hasta que los datos están disponibles desde un subproceso que escribe en el otro extremo de la canalización. Mediante un identificador de espera de no bloqueo, la función devuelve cero inmediatamente y la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el error \_ no hay \_ datos.

Una operación [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) se ve afectada por el modo de espera de un identificador de canalización cuando no hay suficiente espacio en el búfer de la canalización. Con un identificador de espera de bloqueo, la operación de escritura no puede realizarse hasta que un subproceso que lee el otro extremo de la canalización cree suficiente espacio en el búfer. Con un identificador de espera de bloqueo, la operación de escritura devuelve un valor distinto de cero inmediatamente, sin escribir ningún byte (para una canalización de tipo de mensaje) o después de escribir el número de bytes que contiene el búfer (para una canalización de tipo byte).

Una operación [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) se ve afectada por el modo de espera de un identificador de canalización cuando no hay ningún cliente conectado o en espera para conectarse a la instancia de canalización. Con un identificador de espera de bloqueo, la operación de conexión no se realiza hasta que un cliente de canalización se conecta a la instancia de canalización mediante una llamada a la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) . Con un identificador de espera de bloqueo, la operación de conexión devuelve cero inmediatamente y la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve la \_ escucha de canalización de errores \_ .

De forma predeterminada, todos los identificadores de canalización con nombre devueltos por la función [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) o [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) se crean con el modo de bloqueo y espera habilitado. Para crear la canalización en modo de espera de bloqueo, el servidor de canalización especifica la CANALización de \_ espera al llamar a **CreateNamedPipe**.

Ambos clientes de canalización y los servidores de canalización pueden cambiar el modo de espera de un identificador de canalización especificando \_ la espera de canalización o la canalización \_ nowait en una llamada a la función [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) .

> [!Note]  
> El modo de espera de bloqueo es compatible con la versión 2,0 de Microsoft LAN Manager. Este modo no debe usarse para lograr la entrada y salida superpuestas (e/s) con canalizaciones con nombre. En su lugar, se debe usar la e/s superpuesta, ya que permite que las operaciones que consumen mucho tiempo se ejecuten en segundo plano después de que la función vuelva. Para obtener más información acerca de la e/s superpuesta, vea [entrada y salida de datos sincrónicos y superpuestos](synchronous-and-overlapped-input-and-output.md).

 

 

 
