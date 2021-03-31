---
description: La restauración de archivos en un sistema en ejecución puede ser problemática. Es importante que las aplicaciones en ejecución (escritores) indiquen qué hacer cuando surjan dificultades durante las restauraciones, por ejemplo, si el archivo que se está restaurando está actualmente en uso.
ms.assetid: 2cb963a8-7077-4419-96d8-cba0fd011e4f
title: Configuraciones de restauración de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f13acfc59f250a859e9c62f2df2e1b1b982608ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154334"
---
# <a name="vss-restore-configurations"></a><span data-ttu-id="0b4ac-104">Configuraciones de restauración de VSS</span><span class="sxs-lookup"><span data-stu-id="0b4ac-104">VSS Restore Configurations</span></span>

<span data-ttu-id="0b4ac-105">La restauración de archivos en un sistema en ejecución puede ser problemática.</span><span class="sxs-lookup"><span data-stu-id="0b4ac-105">File restoration on a running system can be problematic.</span></span> <span data-ttu-id="0b4ac-106">Es importante que las aplicaciones en ejecución (escritores) indiquen qué hacer cuando surjan dificultades durante las restauraciones, por ejemplo, si el archivo que se está restaurando está actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="0b4ac-106">It is important that running applications (writers) indicate what to do when difficulties arise during restores, for instance, if the file being restored is currently in use.</span></span>

<span data-ttu-id="0b4ac-107">En VSS, los escritores tienen dos maneras complementarias de administrar restauraciones:[*métodos de restauración*](vssgloss-r.md) y destinos de [*restauración*](vssgloss-r.md).</span><span class="sxs-lookup"><span data-stu-id="0b4ac-107">Under VSS, writers have two complementary ways of managing restores—[*restore methods*](vssgloss-r.md) and [*restore targets*](vssgloss-r.md).</span></span>

<span data-ttu-id="0b4ac-108">Además, los solicitantes pueden optar por restaurar archivos en ubicaciones previamente no especificadas y notificar a los escritores (consulte [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)).</span><span class="sxs-lookup"><span data-stu-id="0b4ac-108">In addition, requesters can choose to restore files to previously unspecified locations and notify writers (see [**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)).</span></span>

<span data-ttu-id="0b4ac-109">El método restore (también llama al destino de restauración original) se especifica mediante un escritor en el momento de la copia de seguridad y establece una definición para todo el escritor del método que se va a usar para restaurar todos sus componentes en el futuro.</span><span class="sxs-lookup"><span data-stu-id="0b4ac-109">The restore method (also call the original restore target) is specified by a writer at a backup time, and sets a writer-wide definition of the method to be used to restore all its components in the future.</span></span> <span data-ttu-id="0b4ac-110">Todos los archivos y componentes administrados por un escritor comparten el mismo método de restauración.</span><span class="sxs-lookup"><span data-stu-id="0b4ac-110">All files and components managed by a writer share the same restore method.</span></span>

<span data-ttu-id="0b4ac-111">Los destinos de restauración permiten a los escritores cambiar el modo en que se restaurarán los componentes específicos en el momento de la restauración.</span><span class="sxs-lookup"><span data-stu-id="0b4ac-111">Restore targets allow writers to change how specific components are to be restored at restore time.</span></span> <span data-ttu-id="0b4ac-112">A diferencia de los métodos de restauración, los destinos de restauración se definen para un conjunto de componentes.</span><span class="sxs-lookup"><span data-stu-id="0b4ac-112">Unlike restore methods, restore targets are defined for a component set.</span></span>

<span data-ttu-id="0b4ac-113">En los temas que se enumeran a continuación se muestra una explicación detallada del uso de los métodos de restauración y los destinos de restauración:</span><span class="sxs-lookup"><span data-stu-id="0b4ac-113">A detailed discussion of the usage of restore methods and restore targets is found in the topics listed below:</span></span>

-   [<span data-ttu-id="0b4ac-114">Estado de restauración de VSS</span><span class="sxs-lookup"><span data-stu-id="0b4ac-114">VSS Restore State</span></span>](vss-restore-state.md)
-   [<span data-ttu-id="0b4ac-115">Definición de los métodos de restauración de VSS</span><span class="sxs-lookup"><span data-stu-id="0b4ac-115">Setting VSS Restore Methods</span></span>](setting-vss-restore-methods.md)
-   [<span data-ttu-id="0b4ac-116">Establecimiento de destinos de restauración de VSS</span><span class="sxs-lookup"><span data-stu-id="0b4ac-116">Setting VSS Restore Targets</span></span>](setting-vss-restore-targets.md)
-   [<span data-ttu-id="0b4ac-117">Establecer opciones de restauración de VSS</span><span class="sxs-lookup"><span data-stu-id="0b4ac-117">Setting VSS Restore Options</span></span>](setting-vss-restore-options.md)

<span data-ttu-id="0b4ac-118">(Para obtener información sobre las restauraciones que no usan estos mecanismos, vea [restauraciones sin participación del escritor](restores-without-writer-participation.md)).</span><span class="sxs-lookup"><span data-stu-id="0b4ac-118">(For information on restores that do not use these mechanisms, see [Restores without Writer Participation](restores-without-writer-participation.md).)</span></span>

 

 



