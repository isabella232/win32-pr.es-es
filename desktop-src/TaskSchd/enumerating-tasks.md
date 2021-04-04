---
title: Enumerar tareas
description: Programador de tareas 1,0 proporciona un objeto de enumeración para enumerar las tareas de la carpeta tareas programadas.
ms.assetid: ccd140a1-06f6-4e6b-afa6-f7ac9b9ff904
keywords:
- enumerar tareas Programador de tareas
- enumerar tareas Programador de tareas, descritas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dda98cf40bc1ea360d20bcf13084faa692aa22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076017"
---
# <a name="enumerating-tasks"></a><span data-ttu-id="d63ee-105">Enumerar tareas</span><span class="sxs-lookup"><span data-stu-id="d63ee-105">Enumerating Tasks</span></span>

<span data-ttu-id="d63ee-106">Programador de tareas 1,0 proporciona un objeto de enumeración para enumerar las tareas de la [*carpeta tareas programadas*](s.md).</span><span class="sxs-lookup"><span data-stu-id="d63ee-106">Task Scheduler 1.0 provides an enumeration object for enumerating the tasks in the [*Scheduled Tasks folder*](s.md).</span></span>

> [!Note]  
> <span data-ttu-id="d63ee-107">Para un equipo con Windows Server 2003, Windows XP o Windows 2000 para crear, supervisar o controlar tareas en un equipo con Windows Vista, se deben completar ciertas operaciones en el equipo de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d63ee-107">For a Windows Server 2003, Windows XP, or Windows 2000 computer to create, monitor, or control tasks on a Windows Vista computer, certain operations must be completed on the Windows Vista computer.</span></span> <span data-ttu-id="d63ee-108">Para obtener más información, consulte [Tareas](tasks.md).</span><span class="sxs-lookup"><span data-stu-id="d63ee-108">For more information, see [Tasks](tasks.md).</span></span>

 

## <a name="using-the-enumeration-object"></a><span data-ttu-id="d63ee-109">Usar el objeto de enumeración</span><span class="sxs-lookup"><span data-stu-id="d63ee-109">Using the Enumeration Object</span></span>

<span data-ttu-id="d63ee-110">La interfaz [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) de este objeto proporciona métodos para enumerar las tareas de la carpeta, restablecer la secuencia de enumeración al principio de la lista, omitir las tareas y realizar una copia del objeto de enumeración actual para su uso posterior.</span><span class="sxs-lookup"><span data-stu-id="d63ee-110">The [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) interface of this object provides methods for enumerating the tasks in the folder, resetting the enumeration sequence to the start of the list, skipping tasks, and making a copy of the current enumeration object for later use.</span></span>

<span data-ttu-id="d63ee-111">Para obtener información sobre cómo enumerar las tareas en la carpeta tareas programadas, vea [**IEnumWorkItems:: Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next).</span><span class="sxs-lookup"><span data-stu-id="d63ee-111">For information about enumerating the tasks in the Scheduled tasks folder, see [**IEnumWorkItems::Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next).</span></span>

<span data-ttu-id="d63ee-112">Para obtener información sobre cómo restablecer la enumeración al principio de la lista, vea [**IEnumWorkItems:: RESET**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-reset).</span><span class="sxs-lookup"><span data-stu-id="d63ee-112">For information about resetting the enumeration to the start of the list, see [**IEnumWorkItems::Reset**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-reset).</span></span>

<span data-ttu-id="d63ee-113">Para obtener información sobre cómo omitir las tareas, vea [**IEnumWorkItems:: Skip**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-skip).</span><span class="sxs-lookup"><span data-stu-id="d63ee-113">For information about skipping tasks, see [**IEnumWorkItems::Skip**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-skip).</span></span>

<span data-ttu-id="d63ee-114">Para obtener información sobre cómo crear una copia del objeto de enumeración actual, vea [**IEnumWorkItems:: Clone**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-clone).</span><span class="sxs-lookup"><span data-stu-id="d63ee-114">For information about making a copy of the current enumeration object, see [**IEnumWorkItems::Clone**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-clone).</span></span>

<span data-ttu-id="d63ee-115">Para obtener un ejemplo de cómo enumerar las tareas de la carpeta tareas programadas, vea [ejemplo de enumeración de tareas](enumerating-tasks-example.md).</span><span class="sxs-lookup"><span data-stu-id="d63ee-115">For an example of enumerating the tasks in the Scheduled Tasks folder, see [Enumerating Tasks Example](enumerating-tasks-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d63ee-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d63ee-116">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d63ee-117">**Vista**</span><span class="sxs-lookup"><span data-stu-id="d63ee-117">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d63ee-118">Programador de tareas información de la tarea 1,0</span><span class="sxs-lookup"><span data-stu-id="d63ee-118">Task Scheduler 1.0 Task Information</span></span>](task-scheduler-1-0-task-informatation.md)
</dt> </dl>

 

 




