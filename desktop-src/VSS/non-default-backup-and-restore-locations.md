---
description: Las operaciones de copia de seguridad y restauración suelen copiar archivos de una ubicación predeterminada determinada en el disco en un medio de copia de seguridad y, a continuación, restaurar desde ese medio a la misma ubicación predeterminada en el disco.
ms.assetid: 7609c392-d5f8-48c2-8e7e-f35f56cf94f8
title: Ubicaciones de copia de seguridad y restauración no predeterminadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c809b886886c1d84de1cc3960163a7cc94179cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696996"
---
# <a name="non-default-backup-and-restore-locations"></a><span data-ttu-id="95f57-103">Ubicaciones de copia de seguridad y restauración no predeterminadas</span><span class="sxs-lookup"><span data-stu-id="95f57-103">Non-Default Backup and Restore Locations</span></span>

<span data-ttu-id="95f57-104">Las operaciones de copia de seguridad y restauración suelen copiar archivos de una ubicación predeterminada determinada en el disco en un medio de copia de seguridad y, a continuación, restaurar desde ese medio a la misma ubicación predeterminada en el disco.</span><span class="sxs-lookup"><span data-stu-id="95f57-104">Backup and restore operations typically copy files from a given, default location on disk to backup media and then restore from that media to the same default location on disk.</span></span>

<span data-ttu-id="95f57-105">Hay muchas razones, especialmente cuando se trabaja con procesos en ejecución, no para seguir este modelo simple.</span><span class="sxs-lookup"><span data-stu-id="95f57-105">There are many reasons, particularly when dealing with running processes, not to follow this simple model.</span></span> <span data-ttu-id="95f57-106">VSS admite el uso de orígenes no estándar para la restauración de copias de seguridad y destinos alternativos, e incluye mecanismos para trabajar con subconjuntos de archivos y reasignar archivos.</span><span class="sxs-lookup"><span data-stu-id="95f57-106">VSS supports using nonstandard sources for backup and alternate destinations for restore, and includes mechanisms to work with subsets of files and to remap files.</span></span>

-   [<span data-ttu-id="95f57-107">Trabajar con rutas de acceso alternativas durante la copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="95f57-107">Working with Alternate Paths during Backup</span></span>](working-with-alternate-paths-during-backup.md)
-   [<span data-ttu-id="95f57-108">Trabajar con ubicaciones alternativas durante la restauración</span><span class="sxs-lookup"><span data-stu-id="95f57-108">Working with Alternate Locations during Restore</span></span>](working-with-alternate-locations-during-restore.md)
-   [<span data-ttu-id="95f57-109">Trabajar con nuevos destinos durante la restauración</span><span class="sxs-lookup"><span data-stu-id="95f57-109">Working with New Targets during Restore</span></span>](working-with-new-targets-during-restore.md)
-   [<span data-ttu-id="95f57-110">Trabajar con archivos parciales</span><span class="sxs-lookup"><span data-stu-id="95f57-110">Working with Partial Files</span></span>](working-with-partial-files.md)
-   [<span data-ttu-id="95f57-111">Trabajar con destinos dirigidos</span><span class="sxs-lookup"><span data-stu-id="95f57-111">Working with Directed Targets</span></span>](working-with-directed-targets.md)

 

 



