---
description: Operaciones de canalización anónimas, incluida la creación de canalizar, la escritura en una canalización y los identificadores de canalización.
ms.assetid: df81471c-1072-4456-a877-304e76ade4bd
title: Operaciones de canalización anónimas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963d7127c51859b05e570d00291470a49be5ba66
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172330"
---
# <a name="anonymous-pipe-operations"></a>Operaciones de canalización anónimas

La [**función CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) crea una canalización anónima y devuelve dos identificadores: un identificador de lectura a la canalización y un identificador de escritura a la canalización. El identificador de lectura tiene acceso de solo lectura a la canalización y el identificador de escritura tiene acceso de solo escritura a la canalización. Para comunicarse mediante la canalización, el servidor de canalización debe pasar un identificador de canalización a otro proceso. Normalmente, esto se hace a través de la herencia; es decir, el proceso permite que un proceso secundario herede el identificador. El proceso también puede duplicar un identificador de canalización mediante la función [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) y enviarlo a un proceso no relacionado mediante algún tipo de comunicación entre procesos, como DDE o memoria compartida.

Un servidor de canalización puede enviar el identificador de lectura o el identificador de escritura al cliente de canalización, en función de si el cliente debe usar la canalización anónima para enviar información o recibir información. Para leer desde la canalización, use el identificador de lectura de la canalización en una llamada a la [**función ReadFile.**](/windows/desktop/api/fileapi/nf-fileapi-readfile) La **llamada a ReadFile** devuelve cuando otro proceso ha escrito en la canalización. La **llamada a ReadFile** también puede devolver si se han cerrado todos los identificadores de escritura de la canalización o si se produce un error antes de que se haya completado la operación de lectura.

Para escribir en la canalización, use el identificador de escritura de la canalización en una llamada a la [**función WriteFile.**](/windows/desktop/api/fileapi/nf-fileapi-writefile) La **llamada WriteFile** no se devuelve hasta que ha escrito el número especificado de bytes en la canalización o se produce un error. Si el búfer de canalización está lleno y hay más bytes que escribir, **WriteFile** no devuelve hasta que otro proceso lee de la canalización, lo que hace que haya más espacio disponible en el búfer. El servidor de canalización especifica el tamaño de búfer de la canalización cuando llama a [**CreatePipe.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe)

Las canalizaciones anónimas no admiten las operaciones de lectura y escritura asincrónicas (superpuestas). Esto significa que no puede usar las funciones [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) y [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) con canalizaciones anónimas. Además, el parámetro *lpOverlapped* de [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) y [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) se omite cuando estas funciones se usan con canalizaciones anónimas.

Existe una canalización anónima hasta que se han cerrado todos los identificadores de canalización, tanto de lectura como de escritura. Un proceso puede cerrar sus identificadores de canalización mediante la [**función CloseHandle.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) Todos los identificadores de canalización también se cierran cuando finaliza el proceso.

Las canalizaciones anónimas se implementan mediante una canalización con nombre con un nombre único. Por lo tanto, a menudo puede pasar un identificador a una canalización anónima a una función que requiere un identificador a una canalización con nombre.

 

 
