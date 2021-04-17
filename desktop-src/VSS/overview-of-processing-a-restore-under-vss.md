---
description: En el procesamiento de una copia de seguridad en VSS, los solicitantes y escritores trabajaron juntos para generar una imagen de sistema estable desde la que realizar la copia de seguridad de los datos, lo que requería coordinación y la creación de una instantánea del sistema actual.
ms.assetid: 1cefb6ac-f2bb-464b-a62f-05be91ae56f7
title: Información general sobre el procesamiento de una restauración en VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0279888b28af82eb1b4b51093b421b9db5e15d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696986"
---
# <a name="overview-of-processing-a-restore-under-vss"></a><span data-ttu-id="e6f38-103">Información general sobre el procesamiento de una restauración en VSS</span><span class="sxs-lookup"><span data-stu-id="e6f38-103">Overview of Processing a Restore Under VSS</span></span>

<span data-ttu-id="e6f38-104">En el procesamiento de una copia de seguridad en VSS, los solicitantes y escritores trabajaron juntos para generar una imagen de sistema estable desde la que realizar la copia de seguridad de los datos, lo que requería coordinación y la creación de una instantánea del sistema actual.</span><span class="sxs-lookup"><span data-stu-id="e6f38-104">In processing a backup under VSS, requesters and writers worked together to produce a stable system image from which to back up data, which required coordination and the creation of a shadow copy of the current system.</span></span>

<span data-ttu-id="e6f38-105">A diferencia de una copia de seguridad de VSS, en la que el propósito de la coordinación de solicitante y escritores es generar una imagen de sistema estable desde la que copiar los datos, el objetivo de una restauración basada en VSS es devolver los archivos al disco de forma más útil para las aplicaciones (escritores) que se ejecutan actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="e6f38-105">In contrast to a VSS backup, where the purpose of requester and writers coordination is to produce a stable system image from which to copy data, the objective of a VSS-based restore is to return files to disk in a manner most useful to applications (writers) currently running on the system.</span></span> <span data-ttu-id="e6f38-106">Esto no requiere una imagen de sistema estable, por lo que no es necesaria ninguna instantánea.</span><span class="sxs-lookup"><span data-stu-id="e6f38-106">This does not require a stable system image, so no shadow copy is necessary.</span></span>

<span data-ttu-id="e6f38-107">En su lugar, la atención se centra en evitar la interrupción de la actividad del escritor, lo que impide la creación de conjuntos de datos incoherentes en el disco y permite a los escritores el ámbito necesario para evaluar y combinar datos cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="e6f38-107">Instead, attention is focused on avoiding disruption of writer activity, preventing the creation of inconsistent data sets on disk, and allowing writers the necessary scope to evaluate and merge data when necessary.</span></span>

<span data-ttu-id="e6f38-108">Al igual que una operación de copia de seguridad, una restauración de VSS requiere acceso a un documento de componentes de copia de seguridad y a documentos de metadatos de escritura.</span><span class="sxs-lookup"><span data-stu-id="e6f38-108">Like a backup operation, a VSS restore requires access to both a Backup Components Document and to Writer Metadata Documents.</span></span> <span data-ttu-id="e6f38-109">Normalmente, estos documentos no se obtienen mediante la consulta de las aplicaciones en ejecución, sino que se recuperan de las versiones almacenadas como documentos XML en los medios de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="e6f38-109">These documents are not generally obtained by querying running applications, but instead are retrieved from versions stored as XML documents on backup media.</span></span>

<span data-ttu-id="e6f38-110">Como es el caso de las operaciones de copia de seguridad, los documentos de metadatos del escritor siguen siendo objetos de solo lectura y, una vez recuperados, el documento componentes de copia de seguridad todavía se puede modificar.</span><span class="sxs-lookup"><span data-stu-id="e6f38-110">As is the case during backup operations, the Writer Metadata Documents remain read-only objects, and (once retrieved) the Backup Components Document can still be modified.</span></span> <span data-ttu-id="e6f38-111">Las modificaciones del documento componentes de copia de seguridad permiten que los escritores y el solicitante se comuniquen sobre lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e6f38-111">Modifications of the Backup Components Document allow writers and requester to communicate about the following:</span></span>

-   <span data-ttu-id="e6f38-112">Reemplazar [*métodos de restauración*](vssgloss-r.md) con [*destinos de restauración*](vssgloss-r.md)</span><span class="sxs-lookup"><span data-stu-id="e6f38-112">Overriding [*restore methods*](vssgloss-r.md) with [*restore targets*](vssgloss-r.md)</span></span>
-   <span data-ttu-id="e6f38-113">Usar [ *asignaciones de ubicación alternativas*](vssgloss-a.md)</span><span class="sxs-lookup"><span data-stu-id="e6f38-113">Using [*alternate location mappings*](vssgloss-a.md)</span></span>
-   <span data-ttu-id="e6f38-114">Restaurar archivos en nuevas ubicaciones en disco</span><span class="sxs-lookup"><span data-stu-id="e6f38-114">Restoring files to new locations on disk</span></span>
-   <span data-ttu-id="e6f38-115">Usar diferentes reglas de selección de las utilizadas durante la copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="e6f38-115">Using different selection rules from those used during backup</span></span>

<span data-ttu-id="e6f38-116">Para comprender con más detalle las tareas básicas relacionadas con la realización de una restauración, resulta útil dividir esta información general en los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="e6f38-116">To more fully understand the basic tasks involved in performing a restore, it is useful to break down this overview into the following topics:</span></span>

-   [<span data-ttu-id="e6f38-117">Información general de la inicialización de restauración</span><span class="sxs-lookup"><span data-stu-id="e6f38-117">Overview of Restore Initialization</span></span>](overview-of-restore-initialization.md)
-   [<span data-ttu-id="e6f38-118">Información general de la preparación para la restauración</span><span class="sxs-lookup"><span data-stu-id="e6f38-118">Overview of Preparing for Restore</span></span>](overview-of-preparing-for-restore.md)
-   [<span data-ttu-id="e6f38-119">Información general de la restauración de archivos real</span><span class="sxs-lookup"><span data-stu-id="e6f38-119">Overview of Actual File Restoration</span></span>](overview-of-actual-file-restoration.md)
-   [<span data-ttu-id="e6f38-120">Información general sobre la limpieza y la finalización de la restauración</span><span class="sxs-lookup"><span data-stu-id="e6f38-120">Overview of Restore Clean up and Termination</span></span>](overview-of-restore-clean-up-and-termination.md)

 

 



