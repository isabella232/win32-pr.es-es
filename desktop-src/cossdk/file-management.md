---
description: Para habilitar la transferencia de archivos de aplicación, COMREPL administra automáticamente los conjuntos de carpetas del sistema de archivos en el origen y el destino. Todas estas carpetas COMREPL tienen la raíz en% systemdir% de la \\ \\ replicación com.
ms.assetid: 8c59577b-34ea-4675-aaea-a2732fd5ce14
title: Administración de archivos (servicios de componentes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e785b8fd39d94bcf623810bca950862d22ec8762
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538722"
---
# <a name="file-management"></a><span data-ttu-id="11a3e-104">Administración de archivos</span><span class="sxs-lookup"><span data-stu-id="11a3e-104">File Management</span></span>

<span data-ttu-id="11a3e-105">Para habilitar la transferencia de archivos de aplicación, COMREPL administra automáticamente los conjuntos de carpetas del sistema de archivos en el origen y el destino.</span><span class="sxs-lookup"><span data-stu-id="11a3e-105">To enable the transfer of application files, COMREPL automatically manages sets of file system folders on the source and target.</span></span> <span data-ttu-id="11a3e-106">Todas estas carpetas COMREPL tienen la raíz en% systemdir% de la \\ \\ replicación com.</span><span class="sxs-lookup"><span data-stu-id="11a3e-106">These COMREPL folders are all rooted in %systemdir%\\com\\replication.</span></span>

## <a name="source-folders"></a><span data-ttu-id="11a3e-107">Carpetas de origen</span><span class="sxs-lookup"><span data-stu-id="11a3e-107">Source folders</span></span>



| <span data-ttu-id="11a3e-108">Carpeta</span><span class="sxs-lookup"><span data-stu-id="11a3e-108">Folder</span></span>                   | <span data-ttu-id="11a3e-109">Propósito</span><span class="sxs-lookup"><span data-stu-id="11a3e-109">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11a3e-110">ReplicaSource</span><span class="sxs-lookup"><span data-stu-id="11a3e-110">ReplicaSource</span></span><br/> | <span data-ttu-id="11a3e-111">Las aplicaciones exportadas durante la fase de preparación se almacenan aquí.</span><span class="sxs-lookup"><span data-stu-id="11a3e-111">Applications exported during the prepare phase are stored here.</span></span><br/> <span data-ttu-id="11a3e-112">Esta carpeta se sobrescribe cada vez que se ejecuta la fase de preparación en un determinado equipo de origen.</span><span class="sxs-lookup"><span data-stu-id="11a3e-112">This folder is overwritten each time the prepare phase is executed against a given source computer.</span></span> <span data-ttu-id="11a3e-113">Esta carpeta nunca se elimina explícitamente, por lo que la replicación en destinos puede tener lugar en cualquier momento después de preparar el origen.</span><span class="sxs-lookup"><span data-stu-id="11a3e-113">This folder is never explicitly deleted, so replication to targets can take place at any time after the source is prepared.</span></span><br/> <span data-ttu-id="11a3e-114">Cada aplicación se almacena en su propia subcarpeta denominada <appName> + <appID> .</span><span class="sxs-lookup"><span data-stu-id="11a3e-114">Each application is stored in its own subfolder named <appName>+<appID>.</span></span><br/> |



 

## <a name="target-folders"></a><span data-ttu-id="11a3e-115">Carpetas de destino</span><span class="sxs-lookup"><span data-stu-id="11a3e-115">Target folders</span></span>



| <span data-ttu-id="11a3e-116">Carpeta</span><span class="sxs-lookup"><span data-stu-id="11a3e-116">Folder</span></span>                    | <span data-ttu-id="11a3e-117">Propósito</span><span class="sxs-lookup"><span data-stu-id="11a3e-117">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11a3e-118">ReplicaNew</span><span class="sxs-lookup"><span data-stu-id="11a3e-118">ReplicaNew</span></span><br/>     | <span data-ttu-id="11a3e-119">La fase de copia copia todos los archivos y subcarpetas de ReplicaSource del origen en ReplicaNew en el destino.</span><span class="sxs-lookup"><span data-stu-id="11a3e-119">The copy phase copies all files and subfolders from ReplicaSource on the source to ReplicaNew on the target.</span></span> <span data-ttu-id="11a3e-120">Cualquier contenido anterior de ReplicaNew se elimina cada vez que se ejecuta la fase de copia en un destino determinado.</span><span class="sxs-lookup"><span data-stu-id="11a3e-120">Any previous contents of ReplicaNew are deleted each time the copy phase is run against a given target.</span></span><br/> <span data-ttu-id="11a3e-121">Esta carpeta solo existe mientras se ejecuta el proceso de replicación.</span><span class="sxs-lookup"><span data-stu-id="11a3e-121">This folder exists only while the replication process is running.</span></span> <span data-ttu-id="11a3e-122">(Consulte ReplicaCurrent).</span><span class="sxs-lookup"><span data-stu-id="11a3e-122">(See ReplicaCurrent.)</span></span><br/>           |
| <span data-ttu-id="11a3e-123">ReplicaCurrent</span><span class="sxs-lookup"><span data-stu-id="11a3e-123">ReplicaCurrent</span></span><br/> | <span data-ttu-id="11a3e-124">Las aplicaciones replicadas actualmente instaladas en el destino se almacenan aquí.</span><span class="sxs-lookup"><span data-stu-id="11a3e-124">The replicated applications currently installed on the target are stored here.</span></span><br/> <span data-ttu-id="11a3e-125">Cuando se inicia la fase de instalación, se cambia el nombre de la carpeta ReplicaNew a ReplicaCurrent.</span><span class="sxs-lookup"><span data-stu-id="11a3e-125">When the install phase is started, the ReplicaNew folder is renamed to ReplicaCurrent.</span></span> <span data-ttu-id="11a3e-126">Si hay una carpeta ReplicaCurrent existente, se le cambia el nombre a ReplicaOld.</span><span class="sxs-lookup"><span data-stu-id="11a3e-126">If there is an existing ReplicaCurrent folder, it is renamed to ReplicaOld.</span></span> <span data-ttu-id="11a3e-127">Si hay una carpeta ReplicaOld existente, se elimina su contenido.</span><span class="sxs-lookup"><span data-stu-id="11a3e-127">If there is an existing ReplicaOld folder, its contents are deleted.</span></span><br/> |
| <span data-ttu-id="11a3e-128">ReplicaOld</span><span class="sxs-lookup"><span data-stu-id="11a3e-128">ReplicaOld</span></span><br/>     | <span data-ttu-id="11a3e-129">Guarda los archivos de aplicación instalados durante el siguiente a la última replicación.</span><span class="sxs-lookup"><span data-stu-id="11a3e-129">Saves the application files installed during the next to last replication.</span></span> <span data-ttu-id="11a3e-130">Estos archivos se guardan solo con fines de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="11a3e-130">These files are saved for backup purposes only.</span></span><br/>                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="11a3e-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="11a3e-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11a3e-132">Registro e informes de errores</span><span class="sxs-lookup"><span data-stu-id="11a3e-132">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="11a3e-133">Fases de replicación</span><span class="sxs-lookup"><span data-stu-id="11a3e-133">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="11a3e-134">Usar COMREPL</span><span class="sxs-lookup"><span data-stu-id="11a3e-134">Using COMREPL</span></span>](using-comrepl.md)
</dt> <dt>

[<span data-ttu-id="11a3e-135">Lo que se replica</span><span class="sxs-lookup"><span data-stu-id="11a3e-135">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 




