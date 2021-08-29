---
description: Después de obtener un identificador para una cola de archivos mediante una llamada a la función SetupOpenFileQueue, puede agregar operaciones de archivo a la cola, ya sea archivo por archivo, o mediante la puesta en cola de todos los archivos de una sección INF.
ms.assetid: ba2f40cd-b0df-4768-8080-4fd80c50f2c2
title: Archivos en cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a73a05c9aef71e5707fd7814a4df1fdfa7cce4c1be5bed8a561dd0a0dc6de964
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665435"
---
# <a name="queuing-files"></a>Archivos en cola

Después de obtener un identificador para una cola de archivos mediante una llamada a la función [**SetupOpenFileQueue,**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) puede agregar operaciones de archivo a la cola, ya sea archivo por archivo, o mediante la puesta en cola de todos los archivos de una sección INF.

Para agregar una operación de copia de un archivo individual a la cola de archivos, llame a la [**función SetupQueueCopy.**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya) Si desea poner en cola una operación de copia de archivos mediante los medios de origen predeterminados y los destinos de destino especificados en un archivo INF, puede llamar a la [**función SetupQueueDefaultCopy.**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya)

Puede agregar una operación de eliminación o cambio de nombre de archivo individual a la cola de archivos abiertos mediante una llamada a la [**función SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) o [**SetupQueueRename.**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)

 

 



