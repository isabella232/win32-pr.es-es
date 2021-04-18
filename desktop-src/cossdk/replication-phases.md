---
description: COMREPL realiza su trabajo en tres fases.
ms.assetid: e9ba8db6-ff6f-4e49-b91b-465e3fa77f27
title: Fases de replicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc180e7864f05eb1be60262ee54dd4b71df53bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714885"
---
# <a name="replication-phases"></a><span data-ttu-id="3495f-103">Fases de replicación</span><span class="sxs-lookup"><span data-stu-id="3495f-103">Replication Phases</span></span>

<span data-ttu-id="3495f-104">COMREPL realiza su trabajo en tres fases.</span><span class="sxs-lookup"><span data-stu-id="3495f-104">COMREPL does its work in three phases.</span></span> <span data-ttu-id="3495f-105">El proceso de replicación se divide en distintas fases por los dos motivos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3495f-105">The replication process is divided into distinct phases for the following two reasons:</span></span>

-   <span data-ttu-id="3495f-106">Para separar el trabajo realizado para preparar el origen a partir del trabajo que se realiza en cada destino</span><span class="sxs-lookup"><span data-stu-id="3495f-106">To separate work done to prepare the source from work that is done on each target</span></span>
-   <span data-ttu-id="3495f-107">Para retrasar la modificación del destino hasta que se hayan adquirido todos los datos desde el origen</span><span class="sxs-lookup"><span data-stu-id="3495f-107">To delay modification of the target until all data has been acquired from the source</span></span>

<span data-ttu-id="3495f-108">Las fases de replicación son las siguientes.</span><span class="sxs-lookup"><span data-stu-id="3495f-108">The replication phases are as follows.</span></span>



| <span data-ttu-id="3495f-109">Fase</span><span class="sxs-lookup"><span data-stu-id="3495f-109">Phase</span></span>         | <span data-ttu-id="3495f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3495f-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3495f-111">Fase de preparación</span><span class="sxs-lookup"><span data-stu-id="3495f-111">Prepare phase</span></span> | <span data-ttu-id="3495f-112">Exporta todas las aplicaciones instaladas localmente en el equipo de origen.</span><span class="sxs-lookup"><span data-stu-id="3495f-112">Exports all the installed applications locally on the source computer.</span></span> <span data-ttu-id="3495f-113">Esta fase no toca la configuración de ningún destino.</span><span class="sxs-lookup"><span data-stu-id="3495f-113">This phase does not touch the configuration of any targets.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="3495f-114">Fase de copia</span><span class="sxs-lookup"><span data-stu-id="3495f-114">Copy phase</span></span>    | <span data-ttu-id="3495f-115">Copia datos en un equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="3495f-115">Copies data to a target computer.</span></span> <span data-ttu-id="3495f-116">Todas las aplicaciones exportadas en el origen se copian en el destino.</span><span class="sxs-lookup"><span data-stu-id="3495f-116">All applications exported on the source are copied to the target.</span></span> <span data-ttu-id="3495f-117">Se trata de una operación de copia de archivos.</span><span class="sxs-lookup"><span data-stu-id="3495f-117">This is a file copy operation.</span></span> <span data-ttu-id="3495f-118">(Consulte [Administración de archivos](file-management.md)). Este paso también adquiere algunos datos del equipo de origen que no se encapsulan en los archivos de aplicación exportados (por ejemplo, las identidades de aplicación).</span><span class="sxs-lookup"><span data-stu-id="3495f-118">(See [File Management](file-management.md).) This step also acquires some data from the source computer that is not encapsulated within exported application files (for example, application identities).</span></span> <span data-ttu-id="3495f-119">Estos datos se almacenan en la memoria de COMREPL.</span><span class="sxs-lookup"><span data-stu-id="3495f-119">This data is held in memory within COMREPL.</span></span> <span data-ttu-id="3495f-120">Esta fase no toca la configuración de ningún equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="3495f-120">This phase does not touch the configuration of any target computers.</span></span>                                                                               |
| <span data-ttu-id="3495f-121">Fase de instalación</span><span class="sxs-lookup"><span data-stu-id="3495f-121">Install phase</span></span> | <span data-ttu-id="3495f-122">Instala el catálogo de origen en un equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="3495f-122">Installs source catalog on a target computer.</span></span> <span data-ttu-id="3495f-123">Cuando se inicia este paso, todos los datos necesarios para volver a configurar el destino se encuentran en los archivos de aplicación del sistema de archivos del destino o se almacenan como datos de instancia en COMREPL.</span><span class="sxs-lookup"><span data-stu-id="3495f-123">When this step is initiated, all data required to reconfigure the target is within application files in the target's file system or is held as instance data within COMREPL.</span></span> <span data-ttu-id="3495f-124">En esta fase se eliminarán todas las aplicaciones instaladas en el destino (excepto las aplicaciones descritas en [lo que se replica](what-gets-replicated.md)) antes de instalar las aplicaciones copiadas desde el origen.</span><span class="sxs-lookup"><span data-stu-id="3495f-124">This phase will delete all the installed applications on the target (except the applications described in [What Gets Replicated](what-gets-replicated.md)) prior to installing the applications copied from the source.</span></span> <span data-ttu-id="3495f-125">COMREPL se instala en varios destinos simultáneamente mediante el uso de un subproceso de instalación por destino.</span><span class="sxs-lookup"><span data-stu-id="3495f-125">COMREPL installs on multiple targets concurrently by using an install thread per target.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3495f-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3495f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3495f-127">Administración de archivos</span><span class="sxs-lookup"><span data-stu-id="3495f-127">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="3495f-128">Registro e informes de errores</span><span class="sxs-lookup"><span data-stu-id="3495f-128">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="3495f-129">Usar COMREPL</span><span class="sxs-lookup"><span data-stu-id="3495f-129">Using COMREPL</span></span>](using-comrepl.md)
</dt> <dt>

[<span data-ttu-id="3495f-130">Lo que se replica</span><span class="sxs-lookup"><span data-stu-id="3495f-130">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 



