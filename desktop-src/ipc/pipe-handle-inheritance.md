---
description: El servidor de canalización controla si sus identificadores se pueden heredar de las siguientes maneras.
ms.assetid: 72302f8b-f3a2-4efc-aab1-e596b8323984
title: Herencia de controladores de canalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21cf91d4393b43011a2df632806f96da1e713b96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808402"
---
# <a name="pipe-handle-inheritance"></a>Herencia de controladores de canalización

El servidor de canalización controla si sus identificadores se pueden heredar de las siguientes maneras:

-   La función [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) recibe una estructura de [**\_ atributos de seguridad**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) . Si el servidor de canalización establece el miembro **bInheritHandle** de esta estructura en **true**, los identificadores creados por **CreatePipe** se pueden heredar.
-   El servidor de canalización puede utilizar la función [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) para cambiar la herencia de un identificador de canalización. El servidor de canalización puede crear un duplicado no heredable de un identificador de canalización heredable o un duplicado heredable de un identificador de canalización que no se puede heredar.
-   La función [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) permite que el servidor de canalización especifique si un proceso secundario hereda todos o ninguno de sus identificadores heredables.

Cuando un proceso secundario hereda un identificador de canalización, el sistema permite que el proceso tenga acceso a la canalización. Sin embargo, el proceso primario debe comunicar el valor del identificador al proceso secundario. Normalmente, el proceso primario hace esto redirigiendo el identificador de salida estándar al proceso secundario, tal y como se muestra en los pasos siguientes:

1.  Llame a la función [**GetStdHandle**](/windows/console/getstdhandle) para obtener el identificador de salida estándar actual; Guarde este identificador para poder restaurar el identificador de salida estándar original después de que se haya creado el proceso secundario.
2.  Llame a la función [**SetStdHandle**](/windows/console/setstdhandle) para establecer el identificador de salida estándar en el identificador de escritura en la canalización. Ahora, el proceso primario puede crear el proceso secundario.
3.  Llame a la función [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) para cerrar el identificador de escritura en la canalización. Después de que el proceso secundario hereda el identificador de escritura, el proceso primario ya no necesita su copia.
4.  Llame a [**SetStdHandle**](/windows/console/setstdhandle) para restaurar el identificador de salida estándar original.

El proceso secundario utiliza la función [**GetStdHandle**](/windows/console/getstdhandle) para obtener su identificador de salida estándar, que ahora es un identificador del extremo de escritura de una canalización. A continuación, el proceso secundario utiliza la función [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) para enviar su salida a la canalización. Cuando el elemento secundario ha terminado con la canalización, debe cerrar el identificador de canalización llamando a [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) o finalizando, lo que cierra automáticamente el identificador.

El proceso primario utiliza la función [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) para recibir la entrada de la canalización. Los datos se escriben en una canalización anónima como un flujo de bytes. Esto significa que el proceso primario que lee de una canalización no puede distinguir entre los bytes escritos en operaciones de escritura independientes, a menos que los procesos primarios y secundarios usen un protocolo para indicar dónde finaliza la operación de escritura. Cuando se cierran todos los identificadores de escritura de la canalización, la función **readfile** devuelve cero. Es importante que el proceso primario cierre su identificador hasta el final de escritura de la canalización antes de llamar a **readfile**. Si no se hace esto, la operación **readfile** no puede devolver cero porque el proceso primario tiene un identificador abierto para el extremo de escritura de la canalización.

El procedimiento para redirigir el identificador de entrada estándar es similar al de redirigir el identificador de salida estándar, salvo que el identificador de lectura de la canalización se usa como el identificador de entrada estándar del elemento secundario. En este caso, el proceso primario debe asegurarse de que el proceso secundario no hereda el identificador de escritura de la canalización. Si no se hace esto, la operación [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) realizada por el proceso secundario no puede devolver cero porque el proceso secundario tiene un identificador abierto para el extremo de escritura de la canalización.

Para obtener un programa de ejemplo que usa canalizaciones anónimas para redirigir los identificadores estándar de un proceso secundario, vea [crear un proceso secundario con entrada y salida redirigidas](/windows/desktop/ProcThread/creating-a-child-process-with-redirected-input-and-output).

 

 
