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
# <a name="queuing-files"></a><span data-ttu-id="0ad87-103">Archivos de colas</span><span class="sxs-lookup"><span data-stu-id="0ad87-103">Queuing Files</span></span>

<span data-ttu-id="0ad87-104">Una vez que haya obtenido un identificador de una cola de archivos mediante una llamada a la función [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) , puede Agregar operaciones de archivo a la cola, ya sea archivo a archivo, o bien poniendo en cola todos los archivos de una sección INF.</span><span class="sxs-lookup"><span data-stu-id="0ad87-104">After you have obtained a handle to a file queue by calling the [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) function, you can add file operations to the queue, either file-by-file, or by queuing all the files in an INF section.</span></span>

<span data-ttu-id="0ad87-105">Para agregar una operación de copia de un archivo individual a la cola de archivos, llame a la función [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya) .</span><span class="sxs-lookup"><span data-stu-id="0ad87-105">To add a copy operation for an individual file to the file queue, call the [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya) function.</span></span> <span data-ttu-id="0ad87-106">Si desea poner en cola una operación de copia de archivos mediante los medios de origen y destinos de destino predeterminados especificados en un archivo INF, puede llamar a la función [**SetupQueueDefaultCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya) .</span><span class="sxs-lookup"><span data-stu-id="0ad87-106">If you want to queue a file copy operation using the default source media and target destinations specified in an INF file, you can call the [**SetupQueueDefaultCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya) function.</span></span>

<span data-ttu-id="0ad87-107">Puede Agregar una operación individual de eliminación o cambio de nombre de un archivo a la cola de archivos abierta, llamando a la función [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) o [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea) .</span><span class="sxs-lookup"><span data-stu-id="0ad87-107">You can add an individual file delete or rename operation to the open file queue, by calling the [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) or [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea) function.</span></span>

 

 



