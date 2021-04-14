---
description: Las operaciones superpuestas permiten que un subproceso realice una operación de e/s que consuma mucho tiempo en segundo plano, lo que permite que el subproceso pueda realizar otras tareas.
ms.assetid: 8c0eb20d-685a-4750-8253-a87089b68509
title: Operaciones superpuestas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d8dc9e39386e25129d3e7d7a5281a8299d54ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496205"
---
# <a name="overlapped-operations"></a>Operaciones superpuestas

Las operaciones superpuestas permiten que un subproceso realice una operación de e/s que consuma mucho tiempo en segundo plano, lo que permite que el subproceso pueda realizar otras tareas. Para habilitar las operaciones de e/s superpuestas en un recurso de comunicaciones, el subproceso debe especificar la marca de superposición de **\_ marca \_ de archivo** en la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) cuando se abre el controlador. Para ejecutar la función [**readfile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) o [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) como una operación superpuesta, el subproceso que realiza la llamada debe especificar un puntero a una estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) . La estructura **superpuesta** debe contener un identificador de un objeto de evento de restablecimiento manual (no un restablecimiento automático). El sistema establece el estado del objeto de evento como no señalizado cuando una llamada a la función de e/s se devuelve antes de que se haya completado la operación. El sistema establece el estado del objeto de evento en señalado cuando se ha completado la operación. El subproceso utiliza una función wait para comprobar el estado actual del objeto de evento o para esperar a que se señalice su estado.

Las funciones [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) y [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) solo se pueden realizar como operaciones superpuestas. El subproceso de llamada especifica un puntero a la función [**FileIOCompletionRoutine**](/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine) , que se realiza cuando se completa la operación superpuesta. La rutina de finalización se ejecuta solo si el subproceso de llamada realiza una operación de alerta.

Para obtener más información sobre los objetos de eventos, las funciones de espera, las esperas de alertas y las rutinas de finalización, consulte [acerca de la sincronización](/windows/desktop/Sync/about-synchronization).

 

 
