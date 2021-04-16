---
description: La participación de un escritor en una operación de copia de seguridad o restauración, y en la que se guardan los datos depende de qué componentes se incluyan explícitamente como parte del documento de componentes de copia de seguridad del solicitante y de la relación entre esos componentes y la ruta de acceso lógica de otros componentes dentro del documento de metadatos del escritor.
ms.assetid: e8920cca-d944-437f-bf6a-7ce8d518746a
title: Trabajar con la selección y las rutas de acceso lógicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42bc29d629df86562bc9b764b1d83bb8bb511d50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696427"
---
# <a name="working-with-selectability-and-logical-paths"></a><span data-ttu-id="8c408-103">Trabajar con la selección y las rutas de acceso lógicas</span><span class="sxs-lookup"><span data-stu-id="8c408-103">Working with Selectability and Logical Paths</span></span>

<span data-ttu-id="8c408-104">La participación de un escritor en una operación de copia de seguridad o restauración, y en la que se guardan los datos depende de qué componentes se [*incluyan explícitamente*](vssgloss-e.md) como parte del documento de componentes de copia de seguridad del solicitante y de la relación entre esos componentes y la ruta de acceso lógica de otros componentes dentro del documento de metadatos del escritor.</span><span class="sxs-lookup"><span data-stu-id="8c408-104">A writer's participation in a backup or restore operation, and which of its data are saved, depends on which of its components are [*explicitly included*](vssgloss-e.md) as part of a requester's Backup Components Document and the relationship between those components and the logical path of other components within the Writer Metadata Document.</span></span>

<span data-ttu-id="8c408-105">Los escritores sin componentes agregados al documento de componentes de copia de seguridad de un solicitante antes de la generación de un evento [*PrepareForBackup*](vssgloss-p.md) (en el caso de las operaciones de copia de seguridad) o de un evento [**prerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) (en el caso de operaciones de restauración) no reciben ningún evento después de este punto y no participarán en la operación de copia de seguridad o restauración.</span><span class="sxs-lookup"><span data-stu-id="8c408-105">Writers with no components added to a requester's Backup Component Document prior to the generation of a [*PrepareForBackup*](vssgloss-p.md) event (in the case of backup operations) or of a [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) event (in the case of restore operations) receive no events after this point and will not participate in the backup or restore operation.</span></span>

<span data-ttu-id="8c408-106">Sin embargo, la libertad del solicitante de incluir o excluir un componente determinado en una copia de seguridad o restauración se rige por lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8c408-106">However, a requester's freedom to include or exclude any given component in a backup or restore is governed by the following:</span></span>

-   <span data-ttu-id="8c408-107">Cualquier jerarquía que existe entre los componentes administrados por un escritor y que se expresan mediante rutas de acceso [ *lógicas*](vssgloss-l.md)</span><span class="sxs-lookup"><span data-stu-id="8c408-107">Any hierarchy that exists between the components managed by a writer and expressed by [*logical paths*](vssgloss-l.md)</span></span>
-   <span data-ttu-id="8c408-108">Si el componente se designa como [ *seleccionable para la copia de seguridad*](vssgloss-s.md)</span><span class="sxs-lookup"><span data-stu-id="8c408-108">Whether the component is designated as being [*selectable for backup*](vssgloss-s.md)</span></span>
-   <span data-ttu-id="8c408-109">Si se designa como [ *seleccionable para la restauración*](vssgloss-s.md)</span><span class="sxs-lookup"><span data-stu-id="8c408-109">Whether it is designated as being [*selectable for restore*](vssgloss-s.md)</span></span>
-   <span data-ttu-id="8c408-110">Si existe una dependencia explícita entre un componente determinado de un escritor determinado y otros componentes de otros escritores</span><span class="sxs-lookup"><span data-stu-id="8c408-110">Whether an explicit dependency exists between a given component in a given writer and other components in other writers</span></span>

<span data-ttu-id="8c408-111">En los temas siguientes encontrará más información sobre estos problemas:</span><span class="sxs-lookup"><span data-stu-id="8c408-111">More information on these issues is in the following topics:</span></span>

-   [<span data-ttu-id="8c408-112">Acciones lógicas de los componentes</span><span class="sxs-lookup"><span data-stu-id="8c408-112">Logical Pathing of Components</span></span>](logical-pathing-of-components.md)
-   [<span data-ttu-id="8c408-113">Trabajar con la selección para la copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="8c408-113">Working with Selectability for Backup</span></span>](working-with-selectability-for-backup.md)
-   [<span data-ttu-id="8c408-114">Trabajar con la selección para restaurar y subcomponentes</span><span class="sxs-lookup"><span data-stu-id="8c408-114">Working with Selectability For Restore and Subcomponents</span></span>](working-with-selectability-for-restore-and-subcomponents.md)
-   [<span data-ttu-id="8c408-115">Selección y trabajo con propiedades de componentes</span><span class="sxs-lookup"><span data-stu-id="8c408-115">Selectability and Working with Component Properties</span></span>](selectability-and-working-with-component-properties.md)
-   [<span data-ttu-id="8c408-116">Dependencias entre los componentes administrados por escritores diferentes</span><span class="sxs-lookup"><span data-stu-id="8c408-116">Dependencies between Components Managed by Different Writers</span></span>](dependencies-between-components-managed-by-different-writers.md)

 

 



