---
description: Una vez que la cola ha terminado de confirmar sus operaciones, debe cerrarse con la función SetupCloseFileQueue con el identificador creado por SetupOpenFileQueue.
ms.assetid: 4cb21699-e476-4832-9678-2bf36f3bda08
title: Cerrar la cola de archivos y el archivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b4005e3ce9d084d759612d70cd9fd256fe9ba4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669880"
---
# <a name="closing-the-file-queue-and-inf-file"></a>Cerrar la cola de archivos y el archivo INF

Una vez que la cola ha terminado de confirmar sus operaciones, debe cerrarse con la función [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) con el identificador creado por [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue). La devolución de llamada de cola predeterminada se debe destruir y volver a crear antes de que se pueda confirmar otra cola.

Si se inició un contexto predeterminado para que lo use la rutina de devolución de llamada predeterminada, también debe terminar llamando a la función [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) . El *contexto* es un puntero a la estructura devuelta por la función [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) .

Cuando ya no se necesite el acceso a la información del archivo INF, llame a la función [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) con el identificador creado por [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) para liberar recursos del sistema.

 

 



