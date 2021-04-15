---
description: Un objeto de sincronización es un objeto cuyo identificador se puede especificar en una de las funciones de espera para coordinar la ejecución de varios subprocesos.
ms.assetid: 11558ae9-1056-48bf-96f5-94a051df41c3
title: Objetos de sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299cbd6225b3cc7629378f5fe500fc36ccbe8e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545662"
---
# <a name="synchronization-objects"></a>Objetos de sincronización

Un *objeto de sincronización* es un objeto cuyo identificador se puede especificar en una de las [funciones de espera](wait-functions.md) para coordinar la ejecución de varios subprocesos. Más de un proceso puede tener un identificador para el mismo objeto de sincronización, lo que permite la sincronización entre procesos.

Los siguientes tipos de objeto se proporcionan exclusivamente para la sincronización.



| Tipo           | Descripción                                                                                                                                                                                                      |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Evento          | Notifica que se ha producido un evento a uno o varios subprocesos en espera. Para obtener más información, vea [objetos de evento](event-objects.md).                                                                                   |
| Mutex          | Solo puede ser propiedad de un subproceso cada vez, lo que permite que los subprocesos coordinen el acceso mutuamente exclusivo a un recurso compartido. Para obtener más información, vea [objetos mutex](mutex-objects.md).                          |
| Semaphore      | Mantiene un recuento entre cero y un valor máximo, limitando el número de subprocesos que están accediendo simultáneamente a un recurso compartido. Para obtener más información, vea [objetos Semaphore](semaphore-objects.md). |
| Temporizador de espera | Notifica a uno o más subprocesos en espera que ha llegado una hora especificada. Para obtener más información, vea [objetos de temporizador](waitable-timer-objects.md)que se van a esperar.                                                          |



 

Aunque está disponible para otros usos, los objetos siguientes también se pueden usar para la sincronización.



| Object                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Notificación de cambios          | Creado por la función [**FindFirstChangeNotification**](/windows/win32/api/fileapi/nf-fileapi-findfirstchangenotificationa) , su estado se establece en señalado cuando se produce un tipo de cambio especificado dentro de un directorio especificado o un árbol de directorios. Para obtener más información, consulte [obtención de notificaciones de cambio de directorio](../fileio/obtaining-directory-change-notifications.md).                                                                                                                                   |
| Entrada de la consola                | Se crea cuando se crea una consola de. La función [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) devuelve el identificador de la entrada de la consola cuando se especifica CONIN $, o bien mediante la función [**GetStdHandle**](/windows/console/getstdhandle) . Su estado se establece en señalizado cuando hay una entrada de datos no leídos en el búfer de entrada de la consola y se establece en no señalizado cuando el búfer de entrada está vacío. Para obtener más información acerca de las consolas, consulte [aplicaciones de modo de carácter](/windows/console/character-mode-applications) |
| Trabajo                          | Se crea mediante una llamada a la función [**CreateJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-createjobobjectw) . El estado de un objeto de trabajo se establece en señalizado cuando todos sus procesos finalizan porque se ha superado el límite de tiempo de final de trabajo especificado. Para obtener más información sobre los objetos de trabajo, vea [objetos de trabajo](../procthread/job-objects.md).                                                                                                                                                             |
| Notificación de recursos de memoria | Creado por la función [**CreateMemoryResourceNotification**](/windows/win32/api/memoryapi/nf-memoryapi-creatememoryresourcenotification) . Su estado se establece en señalado cuando se produce un tipo de cambio especificado en la memoria física. Para obtener más información acerca de la memoria, vea [Administración de memoria](../memory/memory-management.md).                                                                                                                                                                                  |
| Proceso                      | Se crea llamando a la función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) . Su estado se establece en no señalado mientras el proceso se está ejecutando y se establece en señalado cuando finaliza el proceso. Para obtener más información sobre los procesos, vea [procesos y subprocesos](../procthread/processes-and-threads.md).                                                                                                                                                                                  |
| Thread                       | Se crea cuando se crea un nuevo subproceso mediante una llamada a la función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)o [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) . Su estado se establece en no señalado mientras el subproceso se está ejecutando y se establece en señalado cuando finaliza el subproceso. Para obtener más información sobre los subprocesos, vea [procesos y subprocesos](../procthread/processes-and-threads.md).                                                            |



 

En algunas circunstancias, también puede utilizar un archivo, una canalización con nombre o un dispositivo de comunicaciones como objeto de sincronización. sin embargo, no se recomienda su uso para este fin. En su lugar, use la e/s asincrónica y espere al conjunto de objetos de eventos de la estructura [**superpuesta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) . Es más seguro usar el objeto de evento debido a la confusión que puede producirse cuando se realizan varias operaciones superpuestas simultáneamente en el mismo archivo, canalización con nombre o dispositivo de comunicaciones. En esta situación, no hay ninguna manera de saber qué operación hizo que se señalizase el estado del objeto.

Para obtener información adicional sobre las operaciones de e/s en archivos, canalizaciones con nombre o comunicaciones, vea [sincronización y entrada y salida superpuestas](synchronization-and-overlapped-input-and-output.md).

 

 
