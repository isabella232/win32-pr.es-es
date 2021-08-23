---
description: Las operaciones superpuestas permiten a un subproceso realizar una operación de E/S lenta en segundo plano, lo que deja al subproceso libre para realizar otras tareas.
ms.assetid: 8c0eb20d-685a-4750-8253-a87089b68509
title: Operaciones superpuestas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ba148d0b2085e2c44e71c4c8d309f9a068223eebe8de8e239f13095c8ddd39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956894"
---
# <a name="overlapped-operations"></a>Operaciones superpuestas

Las operaciones superpuestas permiten a un subproceso realizar una operación de E/S lenta en segundo plano, lo que deja al subproceso libre para realizar otras tareas. Para habilitar las operaciones de E/S superpuestas en un recurso de comunicaciones, el subproceso debe especificar la marca **FILE \_ FLAG \_ OVERLAPPED** en la [**función CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) cuando se abra el identificador. Para ejecutar la [**función ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) o [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) como una operación superpuesta, el subproceso que realiza la llamada debe especificar un puntero a una [**estructura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) La **estructura OVERLAPPED** debe contener un identificador para un objeto de evento de restablecimiento manual (no de restablecimiento automático). El sistema establece el estado del objeto de evento en no señalado cuando se devuelve una llamada a la función de E/S antes de que se haya completado la operación. El sistema establece el estado del objeto de evento en señalado cuando se ha completado la operación. El subproceso usa una función wait para comprobar el estado actual del objeto de evento o para esperar a que se señale su estado.

Las [**funciones ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) [**y WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) solo se pueden realizar como operaciones superpuestas. El subproceso que realiza la llamada especifica un puntero a la función [**FileIOCompletionRoutine,**](/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine) que se realiza cuando se completa la operación superpuesta. La rutina de finalización solo se ejecuta si el subproceso que realiza la llamada realiza una operación que admite alertas.

Para obtener más información sobre los objetos de evento, las funciones de espera, las esperas que se pueden alertar y las rutinas de finalización, vea [Acerca de la sincronización.](/windows/desktop/Sync/about-synchronization)

 

 
