---
description: Poner en cola las operaciones de archivo es útil porque le permite procesar la instalación en conjunto, en lugar de en la sección INF.
ms.assetid: 6519c2fb-142d-4071-865f-c00a98c2fe35
title: Creación de una cola y operaciones de archivo de colas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f344e9d1c36ecac2d3cd3293196e1d08ff81a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667658"
---
# <a name="creating-a-queue-and-queuing-file-operations"></a><span data-ttu-id="cf03c-103">Creación de una cola y operaciones de archivo de colas</span><span class="sxs-lookup"><span data-stu-id="cf03c-103">Creating a Queue and Queuing File Operations</span></span>

<span data-ttu-id="cf03c-104">Poner en cola las operaciones de archivo es útil porque le permite procesar la instalación en conjunto, en lugar de en la sección INF.</span><span class="sxs-lookup"><span data-stu-id="cf03c-104">Queuing the file operations is useful because it enables you to process the installation as a whole, instead of by INF section.</span></span>

<span data-ttu-id="cf03c-105">Para crear una cola de archivos, declare una variable para almacenar el identificador de la cola y, a continuación, llame a la función [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) .</span><span class="sxs-lookup"><span data-stu-id="cf03c-105">To create a file queue, declare a variable to store the queue handle, then call the [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) function.</span></span> <span data-ttu-id="cf03c-106">Una vez creada la cola, puede poner en cola las operaciones de copia, cambio de nombre y eliminación, así como examinar la cola de archivos para comprobar las operaciones en cola.</span><span class="sxs-lookup"><span data-stu-id="cf03c-106">After the queue is created, you can queue copy, rename, and delete operations, as well as scan the file queue to verify enqueued operations.</span></span>

<span data-ttu-id="cf03c-107">Para agregar operaciones de archivo único a la cola, use las funciones [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya), [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)y [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) .</span><span class="sxs-lookup"><span data-stu-id="cf03c-107">To add single file operations to the queue, use the [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya), [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea), and [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) functions.</span></span>

<span data-ttu-id="cf03c-108">Todas las operaciones de archivo enumeradas en una sección **copiar archivos**, **eliminar archivos** o **cambiar nombre de archivos** se pueden agregar a la cola mediante [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona), [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)o [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="cf03c-108">All the file operations listed in a **Copy Files**, **Delete Files**, or **Rename Files** section can be added to the queue by using [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona), [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona), or [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona), respectively.</span></span>

<span data-ttu-id="cf03c-109">Otra manera de poner en cola todos los archivos de las secciones **Copy files** enumeradas en una sección **install** de un archivo INF es usar la función [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona).</span><span class="sxs-lookup"><span data-stu-id="cf03c-109">Another way to queue all the files in the **Copy Files** sections listed in an **Install** section of an INF is to use the function, [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona).</span></span>

<span data-ttu-id="cf03c-110">En el ejemplo siguiente se usa la función [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona) para poner en cola las operaciones de copia de todos los archivos enumerados en una sección **Copy files** de un archivo INF.</span><span class="sxs-lookup"><span data-stu-id="cf03c-110">The following example uses the [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona) function to enqueue copy operations for all the files listed in a **Copy Files** section of an INF file.</span></span>

``` syntax
test = SetupQueueCopySection(
     MyQueue,                  \\Handle to the open queue
     "A:\",                    \\Source root path
     MyInf,                    \\Inf containing the source info
     NULL,                     \\specifies that MyInf contains 
                               \\  the section to copy as well
     MySection,                \\the name of the section to queue
  
                               \\flags specifying the copy style
     SP_COPY_NOSKIP | SP_COPY_NOBROWSE,
);
```

<span data-ttu-id="cf03c-111">En el ejemplo, la cola es la cola a la que se agregan las operaciones de copia, "A: \\ " especifica la ruta de acceso al origen y MyInf es el identificador del archivo INF abierto.</span><span class="sxs-lookup"><span data-stu-id="cf03c-111">In the example, MyQueue is the queue to add copy operations to, "A:\\" specifies the path to the source, and MyInf is the handle to the open INF file.</span></span> <span data-ttu-id="cf03c-112">El parámetro *ListInfHandle* se establece en **null**, lo que indica que la sección para copiar está en MyInf.</span><span class="sxs-lookup"><span data-stu-id="cf03c-112">The parameter *ListInfHandle* is set to **NULL**, indicating that the section for copying is in MyInf.</span></span> <span data-ttu-id="cf03c-113">Mi sección es la sección de MyInf que contiene los archivos que se van a poner en cola para copiarlos.</span><span class="sxs-lookup"><span data-stu-id="cf03c-113">MySection is the section in MyInf containing the files to queue for copying.</span></span>

<span data-ttu-id="cf03c-114">Las marcas de SP \_ Copy \_ noskip y SP \_ Copy \_ nobrowse se han combinado con un operador OR para indicar que no se deben ofrecer opciones al usuario para omitir o buscar archivos si se producen errores.</span><span class="sxs-lookup"><span data-stu-id="cf03c-114">The flags SP\_COPY\_NOSKIP and SP\_COPY\_NOBROWSE have been combined using an OR operator to indicate that the user should not be offered options to skip or browse for files if errors occur.</span></span>

 

 



