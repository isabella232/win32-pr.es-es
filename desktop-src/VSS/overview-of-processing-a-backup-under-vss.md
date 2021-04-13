---
description: Al procesar una copia de seguridad, un solicitante y una coordenada de escritores para proporcionar una imagen de sistema estable desde la que realizar copias de seguridad de los datos (el volumen de copia sombra), agrupar los archivos en función de su uso y almacenar información sobre los datos guardados.
ms.assetid: d7acb2a2-bb58-47e3-a950-d32f663ae36d
title: Información general sobre el procesamiento de una copia de seguridad en VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a11aeab87b503241acefdd15a153c9e417e537
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360603"
---
# <a name="overview-of-processing-a-backup-under-vss"></a><span data-ttu-id="d5c73-103">Información general sobre el procesamiento de una copia de seguridad en VSS</span><span class="sxs-lookup"><span data-stu-id="d5c73-103">Overview of Processing a Backup Under VSS</span></span>

<span data-ttu-id="d5c73-104">Al procesar una copia de seguridad, un solicitante y una coordenada de escritores para proporcionar una imagen de sistema estable desde la que realizar copias de seguridad de los datos (el volumen de copia sombra), agrupar los archivos en función de su uso y almacenar información sobre los datos guardados.</span><span class="sxs-lookup"><span data-stu-id="d5c73-104">In processing a backup, requester and writers coordinate to provide a stable system image from which to back up data (the shadow copied volume), to group files together on the basis of their usage, and to store information on the saved data.</span></span> <span data-ttu-id="d5c73-105">Todo esto debe realizarse al crear solo una interrupción mínima en el flujo de trabajo normal del escritor.</span><span class="sxs-lookup"><span data-stu-id="d5c73-105">This must all be done while creating only minimal interruption to the writer's normal work flow.</span></span>

<span data-ttu-id="d5c73-106">Un solicitante consulta a los escritores sus metadatos, procesa estos datos, notifica a los escritores antes del inicio de la instantánea y de las operaciones de copia de seguridad y, a continuación, notifica a los escritores de nuevo después de que finalicen las operaciones de instantáneas y de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d5c73-106">A requester queries writers for their metadata, processes this data, notifies the writers prior to the beginning of the shadow copy and of the backup operations, and then notifies the writers again after the shadow copy and backup operations end.</span></span>

<span data-ttu-id="d5c73-107">En respuesta a estas notificaciones, el escritor proporciona información acerca de los archivos de los que se va a hacer una copia de seguridad, incluida la especificación de grupos de archivos para coordinar ([*componentes*](vssgloss-c.md)), las pausas en sus operaciones de e/s antes de una instantánea y, a continuación, vuelve al funcionamiento normal después de la finalización de una instantánea o al final de la copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="d5c73-107">In response to these notifications, the writer provides information about files to be backed up—including specifying groups of files to coordinate ([*components*](vssgloss-c.md))—pauses in its I/O operations prior to a shadow copy, and then returns to normal operation following the completion of a shadow copy or at the end of the backup.</span></span>

<span data-ttu-id="d5c73-108">Durante el procesamiento de la copia de seguridad, un escritor especifica los archivos de los que es responsable a través de sus metadatos de solo lectura, el documento de metadatos de escritor (consulte [metadatos de VSS: trabajar con el documento de metadatos del escritor](working-with-the-writer-metadata-document.md)).</span><span class="sxs-lookup"><span data-stu-id="d5c73-108">In the course of processing the backup, a writer specifies the files it is responsible for through its read-only metadata—the Writer Metadata Document (see [VSS Metadata: Working with the Writer Metadata Document](working-with-the-writer-metadata-document.md)).</span></span> <span data-ttu-id="d5c73-109">A continuación, el solicitante interpreta estos metadatos, elige qué hacer para realizar la copia de seguridad y almacena estas decisiones en su propio objeto de metadatos, en el documento componentes de copia de seguridad (vea [metadatos de VSS: trabajar con el documento componentes de copia de seguridad](working-with-the-backup-components-document.md)).</span><span class="sxs-lookup"><span data-stu-id="d5c73-109">The requester then interprets this metadata, chooses what to back up, and stores these decisions in its own metadata object, the Backup Components Document (see [VSS Metadata: Working with the Backup Components Document](working-with-the-backup-components-document.md)).</span></span> <span data-ttu-id="d5c73-110">Este documento de componentes de copia de seguridad está disponible para la inspección y modificación del escritor durante las operaciones de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="d5c73-110">This Backup Components Document is available for writer inspection and modification during both the backup and restore operations.</span></span>

<span data-ttu-id="d5c73-111">En este diagrama se muestran las interacciones entre el solicitante, el servicio VSS, la compatibilidad con el kernel de VSS, cualquier Escritor VSS implicado y cualquier proveedor de hardware VSS.</span><span class="sxs-lookup"><span data-stu-id="d5c73-111">This diagram shows the interactions between the requester, the VSS service, the VSS kernel support, any VSS writers involved, and any VSS hardware providers.</span></span>

![interacciones entre el solicitante, los componentes de copia de seguridad, los escritores y los proveedores](images/vssimpl.png)

<span data-ttu-id="d5c73-113">Para comprender con más detalle las tareas básicas relacionadas con la realización de una copia de seguridad, resulta útil dividir esta información general en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="d5c73-113">To more fully understand the basic tasks involved in performing a backup, it is useful to break down this overview into the following topics:</span></span>

-   [<span data-ttu-id="d5c73-114">Información general sobre la inicialización de copias de seguridad</span><span class="sxs-lookup"><span data-stu-id="d5c73-114">Overview of Backup Initialization</span></span>](overview-of-backup-initialization.md)
-   [<span data-ttu-id="d5c73-115">Información general de la fase de detección de copias de seguridad</span><span class="sxs-lookup"><span data-stu-id="d5c73-115">Overview of the Backup Discovery Phase</span></span>](overview-of-the-backup-discovery-phase.md)
-   [<span data-ttu-id="d5c73-116">Información general de las tareas anteriores a la copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="d5c73-116">Overview of Pre-Backup Tasks</span></span>](overview-of-pre-backup-tasks.md)
-   [<span data-ttu-id="d5c73-117">Información general sobre la copia de seguridad real de archivos</span><span class="sxs-lookup"><span data-stu-id="d5c73-117">Overview of Actual Backup Of Files</span></span>](overview-of-actual-backup-of-files.md)
-   [<span data-ttu-id="d5c73-118">Información general sobre la terminación de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="d5c73-118">Overview of Backup Termination</span></span>](overview-of-backup-termination.md)

 

 



