---
description: Operaciones de canalización anónimas, incluida la creación de canalizaciones, escritura en una canalización, identificadores de canalización.
ms.assetid: df81471c-1072-4456-a877-304e76ade4bd
title: Operaciones de canalización anónimas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963d7127c51859b05e570d00291470a49be5ba66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687384"
---
# <a name="anonymous-pipe-operations"></a>Operaciones de canalización anónimas

La función [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) crea una canalización anónima y devuelve dos identificadores: un identificador de lectura para la canalización y un identificador de escritura para la canalización. El identificador de lectura tiene acceso de solo lectura a la canalización, y el identificador de escritura tiene acceso de solo escritura a la canalización. Para comunicarse mediante la canalización, el servidor de canalización debe pasar un identificador de canalización a otro proceso. Normalmente, esto se hace a través de la herencia; es decir, el proceso permite que un proceso secundario herede el identificador. El proceso también puede duplicar un identificador de canalización mediante la función [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) y enviarlo a un proceso no relacionado mediante algún tipo de comunicación entre procesos, como DDE o la memoria compartida.

Un servidor de canalización puede enviar el identificador de lectura o el identificador de escritura al cliente de canalización, dependiendo de si el cliente debe usar la canalización anónima para enviar información o recibir información. Para leer de la canalización, use el identificador de lectura de la canalización en una llamada a la función [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) . La llamada **readfile** devuelve cuando otro proceso ha escrito en la canalización. La llamada **readfile** también puede devolver si se han cerrado todos los identificadores de escritura de la canalización o si se produce un error antes de que se haya completado la operación de lectura.

Para escribir en la canalización, use el identificador de escritura de la canalización en una llamada a la función [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) . La llamada **WriteFile** no vuelve hasta que ha escrito el número especificado de bytes en la canalización o se produce un error. Si el búfer de canalización está lleno y hay más bytes que se van a escribir, **WriteFile** no devuelve ningún resultado hasta que otro proceso Lee de la canalización, lo que hace que haya más espacio en búfer disponible. El servidor de canalización especifica el tamaño del búfer de la canalización cuando llama a [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe).

Las canalizaciones anónimas no admiten las operaciones de lectura y escritura asincrónicas (superpuestas). Esto significa que no puede usar las funciones [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) y [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) con canalizaciones anónimas. Además, el parámetro *lpOverlapped* de [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) y [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) se omite cuando estas funciones se usan con canalizaciones anónimas.

Existe una canalización anónima hasta que se hayan cerrado todos los identificadores de canalización, tanto de lectura como de escritura. Un proceso puede cerrar los identificadores de canalización mediante la función [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) . También se cierran todos los identificadores de canalización cuando finaliza el proceso.

Las canalizaciones anónimas se implementan mediante una canalización con nombre con un nombre único. Por lo tanto, a menudo puede pasar un identificador a una canalización anónima a una función que requiera un identificador a una canalización con nombre.

 

 
