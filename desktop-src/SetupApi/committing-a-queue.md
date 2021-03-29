---
description: Una vez que se han puesto en cola todas las operaciones de archivo deseadas, la cola debe estar confirmada. Esto hace que se procesen las operaciones de archivo en cola.
ms.assetid: 536f47f5-785e-4a83-a500-c769442e3e68
title: Confirmar una cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d995f6811dbd19bba9e13f29bc119cdf2f471f74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818078"
---
# <a name="committing-a-queue"></a>Confirmar una cola

Una vez que se han puesto en cola todas las operaciones de archivo deseadas, la cola debe estar confirmada. Esto hace que se procesen las operaciones de archivo en cola.

Una cola de archivos no se puede reutilizar una vez confirmada. El procedimiento recomendado es recopilar todas las operaciones de archivo necesarias para la cola de archivos y confirmar la cola una sola vez. Si se requiere un procesamiento adicional de la cola una vez confirmado, se debe cerrar el identificador de la cola y crear una nueva cola de archivos. Para confirmar la cola de archivos, llame a la función [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) , especificando una rutina de devolución de llamada. La rutina de devolución de llamada recibirá notificaciones de **SetupCommitFileQueue** a medida que se procesen las operaciones de archivo. Si desea utilizar la rutina de devolución de llamada de cola predeterminada, primero debe inicializar el contexto necesario llamando a [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) o [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex). Para obtener más información sobre la rutina de devolución de llamada de cola predeterminada, vea [rutina de devolución de llamada de cola predeterminada](default-queue-callback-routine.md).

> [!Note]  
> Se debe llamar a [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) antes de que se cierre la cola. Las operaciones que no se confirman cuando se llama a [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) no se realizarán.

 

 

 



