---
description: El servidor de canalización controla si sus identificadores se pueden heredar de las maneras siguientes.
ms.assetid: 72302f8b-f3a2-4efc-aab1-e596b8323984
title: Herencia de identificadores de canalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c5c2a5abc19164e0bf71f325f1d6e76b46de75e22513061f7f9634ef7212f26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829315"
---
# <a name="pipe-handle-inheritance"></a>Herencia de identificadores de canalización

El servidor de canalización controla si sus identificadores se pueden heredar de las maneras siguientes:

-   La [**función CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) recibe una [**estructura SECURITY \_ ATTRIBUTES.**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) Si el servidor de canalización establece el miembro **bInheritHandle** de esta estructura en **TRUE,** se pueden heredar los identificadores creados por **CreatePipe.**
-   El servidor de canalización puede usar la [**función DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) para cambiar la herencia de un identificador de canalización. El servidor de canalización puede crear un duplicado no heredable de un identificador de canalización heredable o un duplicado heredable de un identificador de canalización no heredable.
-   La [**función CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) permite al servidor de canalización especificar si un proceso secundario hereda todos o ninguno de sus identificadores heredables.

Cuando un proceso secundario hereda un identificador de canalización, el sistema permite que el proceso acceda a la canalización. Sin embargo, el proceso primario debe comunicar el valor del identificador al proceso secundario. Normalmente, el proceso primario lo hace redirija el identificador de salida estándar al proceso secundario, como se muestra en los pasos siguientes:

1.  Llame a [**la función GetStdHandle**](/windows/console/getstdhandle) para obtener el identificador de salida estándar actual; guarde este identificador para que pueda restaurar el identificador de salida estándar original una vez creado el proceso secundario.
2.  Llame a [**la función SetStdHandle**](/windows/console/setstdhandle) para establecer el identificador de salida estándar en el identificador de escritura en la canalización. Ahora el proceso primario puede crear el proceso secundario.
3.  Llame a [**la función CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) para cerrar el identificador de escritura a la canalización. Una vez que el proceso secundario hereda el identificador de escritura, el proceso primario ya no necesita su copia.
4.  Llame [**a SetStdHandle para**](/windows/console/setstdhandle) restaurar el identificador de salida estándar original.

El proceso secundario usa la [**función GetStdHandle**](/windows/console/getstdhandle) para obtener su identificador de salida estándar, que ahora es un identificador para el final de escritura de una canalización. A continuación, el proceso secundario usa [**la función WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) para enviar su salida a la canalización. Cuando el elemento secundario haya terminado con la canalización, debe cerrar el identificador de canalización llamando a [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) o terminando, lo que cierra automáticamente el identificador.

El proceso primario usa la [**función ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) para recibir la entrada de la canalización. Los datos se escriben en una canalización anónima como una secuencia de bytes. Esto significa que el proceso primario que lee de una canalización no puede distinguir entre los bytes escritos en operaciones de escritura independientes, a menos que los procesos primarios y secundarios usen un protocolo para indicar dónde finaliza la operación de escritura. Cuando se cierran todos los identificadores de escritura de la canalización, la **función ReadFile** devuelve cero. Es importante que el proceso primario cierre su identificador al final de escritura de la canalización antes de llamar a **ReadFile**. Si esto no se hace, la operación **ReadFile** no puede devolver cero porque el proceso primario tiene un identificador abierto para el final de escritura de la canalización.

El procedimiento para redirigir el identificador de entrada estándar es similar al de redirigir el identificador de salida estándar, salvo que el identificador de lectura de la canalización se usa como identificador de entrada estándar del elemento secundario. En este caso, el proceso primario debe asegurarse de que el proceso secundario no hereda el identificador de escritura de la canalización. Si esto no se hace, la operación [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) realizada por el proceso secundario no puede devolver cero porque el proceso secundario tiene un identificador abierto para el final de escritura de la canalización.

Para obtener un programa de ejemplo que usa canalizaciones anónimas para redirigir los identificadores estándar de un proceso secundario, vea [Creating a Child Process with Redirected Input and Output](/windows/desktop/ProcThread/creating-a-child-process-with-redirected-input-and-output).

 

 
