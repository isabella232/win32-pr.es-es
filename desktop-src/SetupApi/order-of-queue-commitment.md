---
description: 'Cuando la función SetupCommitFileQueue confirma la cola de archivos, procesa las operaciones de archivo en el siguiente orden: operaciones de eliminación de archivos, operaciones de cambio de nombre de archivos y, por último, operaciones de copia de archivos.'
ms.assetid: 23aae815-ff1a-435d-b14d-3c62a3355a1b
title: Orden de compromiso de cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f261b1e42631e35146dc3d11f848ff543c999c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910334"
---
# <a name="order-of-queue-commitment"></a><span data-ttu-id="0dbaf-103">Orden de compromiso de cola</span><span class="sxs-lookup"><span data-stu-id="0dbaf-103">Order of Queue Commitment</span></span>

<span data-ttu-id="0dbaf-104">Cuando la función [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) confirma la cola de archivos, procesa las operaciones de archivo en el siguiente orden: operaciones de eliminación de archivos, operaciones de cambio de nombre de archivos y, por último, operaciones de copia de archivos.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-104">When the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function commits the file queue, it processes the file operations in the following order: file deletion operations, then file renaming operations, and finally, file copying operations.</span></span> <span data-ttu-id="0dbaf-105">En el siguiente esquema se muestra el ciclo de vida del proceso de compromiso de una cola.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-105">The following outline illustrates the life cycle of a queue's commitment process.</span></span>

 

-   <span data-ttu-id="0dbaf-106">Inicio de la subcola de eliminación</span><span class="sxs-lookup"><span data-stu-id="0dbaf-106">start the delete subqueue</span></span>
    -   <span data-ttu-id="0dbaf-107">iniciar una operación de eliminación de archivo <--REPEAT para cada</span><span class="sxs-lookup"><span data-stu-id="0dbaf-107">start a file delete operation <-- repeat for each</span></span>
    -   <span data-ttu-id="0dbaf-108">finalizar una operación de eliminación de archivo <--eliminar archivo en cola</span><span class="sxs-lookup"><span data-stu-id="0dbaf-108">finish a file delete operation <-- queued file delete</span></span>
-   <span data-ttu-id="0dbaf-109">finalizar la subcola de eliminación</span><span class="sxs-lookup"><span data-stu-id="0dbaf-109">finish the delete subqueue</span></span>

<!-- -->

-   <span data-ttu-id="0dbaf-110">iniciar la subcola Rename</span><span class="sxs-lookup"><span data-stu-id="0dbaf-110">start the rename subqueue</span></span>
    -   <span data-ttu-id="0dbaf-111">iniciar una operación de cambio de nombre de archivo <--REPEAT para cada</span><span class="sxs-lookup"><span data-stu-id="0dbaf-111">start a file rename operation <-- repeat for each</span></span>
    -   <span data-ttu-id="0dbaf-112">finalizar una operación de eliminación de archivo <: cambio de nombre de archivo en cola</span><span class="sxs-lookup"><span data-stu-id="0dbaf-112">finish a file delete operation <-- queued file rename</span></span>
-   <span data-ttu-id="0dbaf-113">finalizar el cambio de nombre de la subcola</span><span class="sxs-lookup"><span data-stu-id="0dbaf-113">finish the rename subqueue</span></span>

<!-- -->

-   <span data-ttu-id="0dbaf-114">Inicio de la copia subque</span><span class="sxs-lookup"><span data-stu-id="0dbaf-114">start the copy subque</span></span>
    -   <span data-ttu-id="0dbaf-115">iniciar una operación de copia de archivos <--REPEAT para cada</span><span class="sxs-lookup"><span data-stu-id="0dbaf-115">start a file copy operation <-- repeat for each</span></span>
    -   <span data-ttu-id="0dbaf-116">finalizar una operación de copia de archivos <: copia de archivos en cola</span><span class="sxs-lookup"><span data-stu-id="0dbaf-116">finish a file copy operation <-- queued file copy</span></span>
    -   <span data-ttu-id="0dbaf-117">finalizar la subcola de copia</span><span class="sxs-lookup"><span data-stu-id="0dbaf-117">finish the copy subqueue</span></span>
-   <span data-ttu-id="0dbaf-118">finalizar la cola</span><span class="sxs-lookup"><span data-stu-id="0dbaf-118">finish the queue</span></span>

 

<span data-ttu-id="0dbaf-119">En cada paso, o si se produce un error, la función [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) envía una notificación a la rutina de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-119">At each step, or if an error occurs, the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function sends a notification to the callback routine.</span></span> <span data-ttu-id="0dbaf-120">La rutina de devolución de llamada puede usar la información enviada por la cola para realizar el seguimiento del progreso de la instalación y, si es necesario, interactuar con el usuario.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-120">The callback routine can use the information sent by the queue to track the installation progress and, if necessary, interact with the user.</span></span>

<span data-ttu-id="0dbaf-121">Por ejemplo, si una operación de copia de archivos necesita un archivo de código fuente que no estaba disponible en la ruta de acceso actual, [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) enviaría una \_ notificación SPFILENOTIFY NEEDMEDIA a la rutina de devolución de llamada, junto con información sobre el archivo y los medios necesarios.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-121">For example, if a file copy operation needed a source file that was not available at the current path, [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) would send a SPFILENOTIFY\_NEEDMEDIA notification to the callback routine, along with information about the file and media required.</span></span> <span data-ttu-id="0dbaf-122">La rutina de devolución de llamada podría usar esta información para generar un cuadro de diálogo que pide al usuario que inserte el siguiente disco mediante una llamada a [ **SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)</span><span class="sxs-lookup"><span data-stu-id="0dbaf-122">The callback routine could use this information to generate a dialog box that prompts the user to insert the next disk by calling [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)</span></span>

<span data-ttu-id="0dbaf-123">Una rutina de devolución de llamada de cola predeterminada, [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka), se incluye con la API de instalación.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-123">A default queue callback routine, [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka), is included with the Setup API.</span></span> <span data-ttu-id="0dbaf-124">Esta rutina controla las notificaciones de cola y genera cuadros de diálogo de error y barras de progreso para la instalación.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-124">This routine handles queue notifications and generates error dialog boxes and progress bars for the installation.</span></span> <span data-ttu-id="0dbaf-125">Puede usar la rutina de devolución de llamada de cola predeterminada tal como está, o escribir una rutina de devolución de llamada de filtro para controlar un subconjunto de las notificaciones y pasar las demás a la rutina de devolución de llamada de cola predeterminada.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-125">You can use the default queue callback routine as it is, or write a filter callback routine to handle a subset of the notifications and pass the others on to the default queue callback routine.</span></span>

<span data-ttu-id="0dbaf-126">Si ninguna de las funciones de la rutina de devolución de llamada se adapta a sus necesidades, puede escribir una rutina de devolución de llamada personalizada independiente que no llame a la rutina de devolución de llamada de cola predeterminada.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-126">If none of the functionality of the callback routine suits your needs, you can write a self-contained custom callback routine that does not call the default queue callback routine.</span></span>

<span data-ttu-id="0dbaf-127">Para obtener más información sobre las rutinas de devolución de llamada de cola, vea [rutina de devolución de llamada de cola predeterminada](default-queue-callback-routine.md)y [crear una rutina de devolución de llamada de cola personalizada](creating-a-custom-queue-callback-routine.md).</span><span class="sxs-lookup"><span data-stu-id="0dbaf-127">For more information about queue callback routines, see [Default Queue Callback Routine](default-queue-callback-routine.md), and [Creating a Custom Queue Callback Routine](creating-a-custom-queue-callback-routine.md).</span></span>

 

 



