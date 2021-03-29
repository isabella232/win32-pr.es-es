---
description: La acción DeleteServices detiene un servicio y quita su registro del sistema. Esta acción consulta la tabla ServiceControl.
ms.assetid: c7976de9-65f4-4552-8f8c-e7a32ef4821d
title: Acción DeleteServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c5fc22bbb0c11cd546f1ffbb9f3ad98e06efae3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360868"
---
# <a name="deleteservices-action"></a><span data-ttu-id="8cdae-104">Acción DeleteServices</span><span class="sxs-lookup"><span data-stu-id="8cdae-104">DeleteServices Action</span></span>

<span data-ttu-id="8cdae-105">La acción DeleteServices detiene un servicio y quita su registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="8cdae-105">The DeleteServices action stops a service and removes its registration from the system.</span></span> <span data-ttu-id="8cdae-106">Esta acción consulta la [tabla ServiceControl](servicecontrol-table.md).</span><span class="sxs-lookup"><span data-stu-id="8cdae-106">This action queries the [ServiceControl table](servicecontrol-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="8cdae-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="8cdae-107">Sequence Restrictions</span></span>

<span data-ttu-id="8cdae-108">Las acciones de servicios se deben usar en la secuencia siguiente:</span><span class="sxs-lookup"><span data-stu-id="8cdae-108">The services actions must be used in the following sequence:</span></span>

1.  [<span data-ttu-id="8cdae-109">StopServices</span><span class="sxs-lookup"><span data-stu-id="8cdae-109">StopServices</span></span>](stopservices-action.md)
2.  <span data-ttu-id="8cdae-110">DeleteServices</span><span class="sxs-lookup"><span data-stu-id="8cdae-110">DeleteServices</span></span>
3.  <span data-ttu-id="8cdae-111">Cualquiera de las siguientes acciones: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md)y [RemoveDuplicateFiles](removeduplicatefiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="8cdae-111">Any of the following actions: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md), and [RemoveDuplicateFiles](removeduplicatefiles-action.md) actions.</span></span>
4.  [<span data-ttu-id="8cdae-112">Acción InstallServices</span><span class="sxs-lookup"><span data-stu-id="8cdae-112">InstallServices action</span></span>](installservices-action.md)
5.  [<span data-ttu-id="8cdae-113">StartServices</span><span class="sxs-lookup"><span data-stu-id="8cdae-113">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="8cdae-114">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="8cdae-114">ActionData Messages</span></span>



| <span data-ttu-id="8cdae-115">Campo</span><span class="sxs-lookup"><span data-stu-id="8cdae-115">Field</span></span> | <span data-ttu-id="8cdae-116">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="8cdae-116">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="8cdae-117">\[1\]</span><span class="sxs-lookup"><span data-stu-id="8cdae-117">\[1\]</span></span> | <span data-ttu-id="8cdae-118">Nombre para mostrar del servicio.</span><span class="sxs-lookup"><span data-stu-id="8cdae-118">Service display name.</span></span>      |
| <span data-ttu-id="8cdae-119">\[2\]</span><span class="sxs-lookup"><span data-stu-id="8cdae-119">\[2\]</span></span> | <span data-ttu-id="8cdae-120">Nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="8cdae-120">Service name.</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="8cdae-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8cdae-121">Remarks</span></span>

<span data-ttu-id="8cdae-122">Esta acción requiere que el usuario sea administrador o que tenga privilegios elevados con permiso para eliminar servicios o que la aplicación forme parte de una instalación administrada.</span><span class="sxs-lookup"><span data-stu-id="8cdae-122">This action requires the user be an administrator or have elevated privileges with permission to delete services or that the application be part of a managed installation.</span></span>

 

 



