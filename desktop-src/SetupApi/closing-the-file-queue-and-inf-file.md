---
description: Una vez que la cola ha terminado de confirmar sus operaciones, se debe cerrar mediante la función SetupCloseFileQueue con el identificador creado por SetupOpenFileQueue.
ms.assetid: 4cb21699-e476-4832-9678-2bf36f3bda08
title: Cerrar la cola de archivos y el archivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce5c81c75f7515acfb346b4277e416b0cb2c2a9be6e40464dcfdfc21c3b23bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887580"
---
# <a name="closing-the-file-queue-and-inf-file"></a>Cerrar la cola de archivos y el archivo INF

Una vez que la cola haya terminado de confirmar sus operaciones, debe cerrarse mediante la función [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) con el identificador creado por [**SetupOpenFileQueue.**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) La devolución de llamada de cola predeterminada se debe destruir y volver a crear antes de que se pueda confirma otra cola.

Si se inició un contexto predeterminado para su uso por la rutina de devolución de llamada predeterminada, también debe terminarse llamando a la función [**SetupTermDefaultQueueCallback.**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) Context *es* un puntero a la estructura devuelta por la [**función SetupInitDefaultQueueCallback.**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback)

Cuando ya no se necesite acceso a la información inf, llame a la función [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) con el identificador creado por [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) para liberar recursos del sistema.

 

 



