---
description: Las operaciones de canalización, incluidos los clientes de canalización y los servidores, pueden llamar a una de varias funciones, además de CallNamedPipe, para leer y escribir en una canalización con nombre.
ms.assetid: ae06455e-33bc-433d-be8f-aeb8eeb99b1d
title: Operaciones de canalización con nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 703189a129fc44b956ab65c2f70bbf88bfd22700
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153757"
---
# <a name="named-pipe-operations"></a>Operaciones de canalización con nombre

La primera vez que el servidor de canalizaciones llama a la función [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) , usa el parámetro *nMaxInstances* para especificar el número máximo de instancias de la canalización que pueden existir simultáneamente. El servidor puede llamar a **CreateNamedPipe** repetidamente para crear instancias adicionales de la canalización, siempre que no supere el número máximo de instancias. Si la función se ejecuta correctamente, cada llamada devuelve un identificador al extremo del servidor de una instancia de canalización con nombre.

En cuanto el servidor de canalización crea una instancia de canalización, un cliente de canalización puede conectarse a ella mediante una llamada a la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) . Si hay disponible una instancia de canalización, **CreateFile** devuelve un identificador al extremo de cliente de la instancia de canalización. Si no hay ninguna instancia de la canalización disponible, un cliente de canalización puede utilizar la función [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) para esperar hasta que haya una canalización disponible.

Un servidor de canalización puede determinar cuándo se conecta un cliente de canalización a una instancia de canalización mediante una llamada a la función [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) . Si el identificador de canalización está en modo de espera de bloqueo, **ConnectNamedPipe** no devuelve ningún resultado hasta que se conecta un cliente.

Los clientes y servidores de canalización pueden llamar a una de varias funciones, además de [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) , para leer y escribir en una canalización con nombre. El comportamiento de estas funciones depende del tipo de canalización y de los modos en vigor para el identificador de canalización especificado, como se indica a continuación:

-   Las funciones [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) y [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) se pueden usar con canalizaciones de tipo de byte o de tipo de mensaje.
-   Las funciones [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) y [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) se pueden usar con canalizaciones de tipo de byte o de tipo de mensaje si se abrió el identificador de canalización para las operaciones superpuestas.
-   La función [**PeekNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe) se puede usar para leer sin quitar el contenido de una canalización de tipo byte o de una canalización de tipo de mensaje. **PeekNamedPipe** también puede devolver información adicional sobre la instancia de canalización.
-   La función [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) se puede usar con canalizaciones dúplex de tipo de mensaje si el identificador de canalización del proceso de llamada se establece en modo de lectura de mensaje. La función escribe un mensaje de solicitud y lee un mensaje de respuesta en una sola operación, mejorando el rendimiento de la red.

El servidor de canalización no debe realizar una operación de lectura de bloqueo hasta que se haya iniciado el cliente de canalización. De lo contrario, se puede producir una condición de carrera. Esto suele ocurrir cuando el código de inicialización, como el de la biblioteca en tiempo de ejecución de C, necesita bloquear y examinar los identificadores heredados.

Cuando un cliente y un servidor terminan de usar una instancia de canalización, el servidor debe llamar primero a la función [**FlushFileBuffers**](/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers) para asegurarse de que el cliente Lee todos los bytes o mensajes escritos en la canalización. **FlushFileBuffers** no vuelve hasta que el cliente haya leído todos los datos de la canalización. A continuación, el servidor llama a la función [**DisconnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-disconnectnamedpipe) para cerrar la conexión con el cliente de canalización. Esta función hace que el identificador del cliente no sea válido, si aún no se ha cerrado. Los datos no leídos de la canalización se descartan. Una vez desconectado el cliente, el servidor llama a la función [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) para cerrar su identificador para la instancia de canalización. Como alternativa, el servidor puede usar [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) para permitir que un nuevo cliente se conecte a esta instancia de la canalización.

Un proceso puede recuperar información acerca de una canalización con nombre mediante una llamada a la función [**GetNamedPipeInfo**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-getnamedpipeinfo) , que devuelve el tipo de la canalización, el tamaño de los búferes de entrada y salida, y el número máximo de instancias de canalización que se pueden crear. La función [**GetNamedPipeHandleState**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipehandlestatea) informa de los modos de lectura y espera de un identificador de canalización, el número actual de instancias de canalización e información adicional para las canalizaciones que se comunican a través de una red. La función [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) establece los modos de espera y modo de lectura de un identificador de canalización. En el caso de los clientes de canalización que se comunican con un servidor remoto, la función también controla el número máximo de bytes que se van a recopilar o el tiempo máximo de espera antes de transmitir un mensaje (suponiendo que el identificador del cliente no se ha abierto con el modo de escritura a través habilitado).

 

 
