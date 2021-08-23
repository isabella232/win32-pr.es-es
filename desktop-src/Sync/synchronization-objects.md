---
description: Un objeto de sincronización es un objeto cuyo identificador se puede especificar en una de las funciones de espera para coordinar la ejecución de varios subprocesos.
ms.assetid: 11558ae9-1056-48bf-96f5-94a051df41c3
title: Objetos de sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfd011663e13d8d6992355d99cc643e2f7243f8385ae75f9274367bfc43fe5f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885913"
---
# <a name="synchronization-objects"></a>Objetos de sincronización

Un *objeto de sincronización* es un objeto cuyo identificador se puede especificar en una de las funciones [de](wait-functions.md) espera para coordinar la ejecución de varios subprocesos. Más de un proceso puede tener un identificador para el mismo objeto de sincronización, lo que permite la sincronización entre procesos.

Los siguientes tipos de objeto se proporcionan exclusivamente para la sincronización.



| Tipo           | Descripción                                                                                                                                                                                                      |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Evento          | Notifica que se ha producido un evento a uno o varios subprocesos en espera. Para obtener más información, vea [Objetos de evento](event-objects.md).                                                                                   |
| Mutex          | Solo puede ser propiedad de un subproceso a la vez, lo que permite a los subprocesos coordinar el acceso mutuamente excluyente a un recurso compartido. Para obtener más información, vea [Mutex Objects](mutex-objects.md).                          |
| Semaphore      | Mantiene un recuento entre cero y algún valor máximo, lo que limita el número de subprocesos que acceden simultáneamente a un recurso compartido. Para obtener más información, vea [Semaphore Objects](semaphore-objects.md). |
| Temporizador que se puede esperar | Notifica a uno o varios subprocesos en espera que ha llegado una hora especificada. Para obtener más información, [vea Objetos de temporizador que se pueden esperar.](waitable-timer-objects.md)                                                          |



 

Aunque está disponible para otros usos, también se pueden usar los siguientes objetos para la sincronización.



| Object                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Notificación de cambio          | Creado por [**la función FindFirstChangeNotification,**](/windows/win32/api/fileapi/nf-fileapi-findfirstchangenotificationa) su estado se establece en señalado cuando se produce un tipo de cambio especificado dentro de un directorio o árbol de directorios especificado. Para obtener más información, vea [Obtención de notificaciones de cambio de directorio.](../fileio/obtaining-directory-change-notifications.md)                                                                                                                                   |
| Entrada de la consola                | Se crea cuando se crea una consola. La función [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) devuelve el identificador de la entrada de la consola cuando se especifica CONIN$ o la [**función GetStdHandle.**](/windows/console/getstdhandle) Su estado se establece en señalado cuando hay una entrada no leída en el búfer de entrada de la consola y se establece en sin signo cuando el búfer de entrada está vacío. Para obtener más información sobre las consolas, vea [Aplicaciones en modo de caracteres.](/windows/console/character-mode-applications) |
| Trabajo                          | Se crea mediante una llamada [**a la función CreateJobObject.**](/windows/win32/api/jobapi2/nf-jobapi2-createjobobjectw) El estado de un objeto de trabajo se establece en señalado cuando se finalizan todos sus procesos porque se ha superado el límite de tiempo de fin de trabajo especificado. Para obtener más información sobre los objetos de trabajo, vea [Objetos de trabajo](../procthread/job-objects.md).                                                                                                                                                             |
| Notificación de recursos de memoria | Creado por [**la función CreateMemoryResourceNotification.**](/windows/win32/api/memoryapi/nf-memoryapi-creatememoryresourcenotification) Su estado se establece en señalado cuando se produce un tipo de cambio especificado dentro de la memoria física. Para obtener más información sobre la memoria, vea [Administración de memoria.](../memory/memory-management.md)                                                                                                                                                                                  |
| Proceso                      | Se crea mediante una llamada [**a la función CreateProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) Su estado se establece en nonsignaled mientras se ejecuta el proceso y se establece en signaled cuando finaliza el proceso. Para obtener más información sobre los procesos, vea [Procesos y subprocesos.](../procthread/processes-and-threads.md)                                                                                                                                                                                  |
| Thread                       | Se crea cuando se crea un subproceso mediante una llamada a la [**función CreateProcess,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)o [**CreateRemoteThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) Su estado se establece en nonsignaled mientras se ejecuta el subproceso y se establece en signaled cuando finaliza el subproceso. Para obtener más información sobre los subprocesos, [vea Procesos y subprocesos.](../procthread/processes-and-threads.md)                                                            |



 

En algunas circunstancias, también puede usar un archivo, una canalización con nombre o un dispositivo de comunicaciones como un objeto de sincronización; sin embargo, no se recomienda su uso con este fin. En su lugar, use E/S asincrónica y espere en el objeto de evento establecido en la [**estructura OVERLAPPED.**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Es más seguro usar el objeto de evento debido a la confusión que puede producirse cuando se realizan varias operaciones superpuestas simultáneas en el mismo archivo, canalización con nombre o dispositivo de comunicaciones. En esta situación, no hay ninguna manera de saber qué operación ha provocado que se señale el estado del objeto.

Para obtener información adicional sobre las operaciones de E/S en archivos, canalizaciones con nombre o comunicaciones, vea [Synchronization and Overlapped Input and Output](synchronization-and-overlapped-input-and-output.md).

 

 
