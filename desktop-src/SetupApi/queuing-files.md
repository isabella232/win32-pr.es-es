---
description: Una vez que haya obtenido un identificador de una cola de archivos mediante una llamada a la función SetupOpenFileQueue, puede Agregar operaciones de archivo a la cola, ya sea archivo a archivo, o bien poniendo en cola todos los archivos de una sección INF.
ms.assetid: ba2f40cd-b0df-4768-8080-4fd80c50f2c2
title: Archivos de colas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7b5ab9a9be136e50547076c8daf9bd519ade72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910038"
---
# <a name="queuing-files"></a>Archivos de colas

Una vez que haya obtenido un identificador de una cola de archivos mediante una llamada a la función [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) , puede Agregar operaciones de archivo a la cola, ya sea archivo a archivo, o bien poniendo en cola todos los archivos de una sección INF.

Para agregar una operación de copia de un archivo individual a la cola de archivos, llame a la función [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya) . Si desea poner en cola una operación de copia de archivos mediante los medios de origen y destinos de destino predeterminados especificados en un archivo INF, puede llamar a la función [**SetupQueueDefaultCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya) .

Puede Agregar una operación individual de eliminación o cambio de nombre de un archivo a la cola de archivos abierta, llamando a la función [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) o [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea) .

 

 



