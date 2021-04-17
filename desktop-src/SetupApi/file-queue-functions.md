---
description: Las siguientes funciones se usan con las colas de archivos.
ms.assetid: f05e2abf-983f-4418-bf92-f5ca6502196e
title: Funciones de cola de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9acaf1fb1fbd2dc4f020577a1ae68d6ec9b2e95c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667878"
---
# <a name="file-queue-functions"></a><span data-ttu-id="7e8b1-103">Funciones de cola de archivos</span><span class="sxs-lookup"><span data-stu-id="7e8b1-103">File Queue Functions</span></span>

<span data-ttu-id="7e8b1-104">Las siguientes funciones se usan con las colas de archivos.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-104">The following functions are used with file queues.</span></span>



| <span data-ttu-id="7e8b1-105">Función</span><span class="sxs-lookup"><span data-stu-id="7e8b1-105">Function</span></span>                                                             | <span data-ttu-id="7e8b1-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e8b1-106">Description</span></span>                                                                                           |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e8b1-107">**SetupCloseFileQueue**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-107">**SetupCloseFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue)                   | <span data-ttu-id="7e8b1-108">Finaliza la cola.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-108">Terminates the queue.</span></span> <span data-ttu-id="7e8b1-109">Las transacciones restantes no se confirman.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-109">Any remaining transactions are not committed.</span></span>                                   |
| [<span data-ttu-id="7e8b1-110">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-110">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)                 | <span data-ttu-id="7e8b1-111">Confirma todas las transacciones en cola.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-111">Commits all queued transactions.</span></span>                                                                      |
| [<span data-ttu-id="7e8b1-112">**SetupOpenFileQueue**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-112">**SetupOpenFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)                     | <span data-ttu-id="7e8b1-113">Inicializa y devuelve un identificador para la cola de archivos.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-113">Initializes and returns a handle to the file queue.</span></span>                                                   |
| [<span data-ttu-id="7e8b1-114">**SetupPromptReboot**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-114">**SetupPromptReboot**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptreboot)                       | <span data-ttu-id="7e8b1-115">Solicita al usuario que reinicie su equipo, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-115">Prompts the user to reboot his or her computer, if necessary.</span></span>                                         |
| [<span data-ttu-id="7e8b1-116">**SetupQueueCopy**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-116">**SetupQueueCopy**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya)                             | <span data-ttu-id="7e8b1-117">Pone en cola una copia de archivos.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-117">Queues a file copy.</span></span>                                                                                   |
| [<span data-ttu-id="7e8b1-118">**SetupQueueCopySection**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-118">**SetupQueueCopySection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona)               | <span data-ttu-id="7e8b1-119">Pone en cola los archivos en una sección de archivos de copia INF.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-119">Queues the files in an INF Copy Files section.</span></span>                                                        |
| [<span data-ttu-id="7e8b1-120">**SetupQueueDefaultCopy**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-120">**SetupQueueDefaultCopy**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya)               | <span data-ttu-id="7e8b1-121">Pone en cola los archivos en una sección de archivos de copia INF con la información predeterminada especificada en un archivo INF.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-121">Queues the files in an INF Copy Files section using the default information specified in an INF file.</span></span> |
| [<span data-ttu-id="7e8b1-122">**SetupQueueDelete**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-122">**SetupQueueDelete**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea)                         | <span data-ttu-id="7e8b1-123">Pone en cola una eliminación de archivos.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-123">Queues a file deletion.</span></span>                                                                               |
| [<span data-ttu-id="7e8b1-124">**SetupQueueDeleteSection**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-124">**SetupQueueDeleteSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)           | <span data-ttu-id="7e8b1-125">Pone en cola los archivos en una sección de archivos INF DELETE.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-125">Queues the files in an INF Delete Files section.</span></span>                                                      |
| [<span data-ttu-id="7e8b1-126">**SetupQueueRename**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-126">**SetupQueueRename**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)                         | <span data-ttu-id="7e8b1-127">Pone en cola un cambio de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-127">Queues a file rename.</span></span>                                                                                 |
| [<span data-ttu-id="7e8b1-128">**SetupQueueRenameSection**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-128">**SetupQueueRenameSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)           | <span data-ttu-id="7e8b1-129">Pone en cola los archivos en una sección de archivos de cambio de nombre de INF.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-129">Queues the files in an INF Rename Files section.</span></span>                                                      |
| [<span data-ttu-id="7e8b1-130">**SetupScanFileQueue**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-130">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)                     | <span data-ttu-id="7e8b1-131">Examina la cola de archivos.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-131">Scans the file queue.</span></span>                                                                                 |
| [<span data-ttu-id="7e8b1-132">**SetupSetPlatformPathOverride**</span><span class="sxs-lookup"><span data-stu-id="7e8b1-132">**SetupSetPlatformPathOverride**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) | <span data-ttu-id="7e8b1-133">Establece la invalidación de la ruta de acceso de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="7e8b1-133">Sets the platform path override.</span></span>                                                                      |



 

 

 



