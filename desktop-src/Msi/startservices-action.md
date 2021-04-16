---
description: La acción StartServices inicia servicios del sistema. Esta acción consulta la tabla ServiceControl.
ms.assetid: 53791b1c-5fd5-45d8-817b-098566ab4f9c
title: Acción StartServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c150a8970c5852d9cfc53581290e792c00b628
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677653"
---
# <a name="startservices-action"></a><span data-ttu-id="9f649-104">Acción StartServices</span><span class="sxs-lookup"><span data-stu-id="9f649-104">StartServices Action</span></span>

<span data-ttu-id="9f649-105">La acción StartServices inicia servicios del sistema.</span><span class="sxs-lookup"><span data-stu-id="9f649-105">The StartServices action starts system services.</span></span> <span data-ttu-id="9f649-106">Esta acción consulta la [tabla ServiceControl](servicecontrol-table.md).</span><span class="sxs-lookup"><span data-stu-id="9f649-106">This action queries the [ServiceControl table](servicecontrol-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="9f649-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="9f649-107">Sequence Restrictions</span></span>

<span data-ttu-id="9f649-108">Las acciones de servicios se deben usar en la secuencia siguiente:</span><span class="sxs-lookup"><span data-stu-id="9f649-108">The services actions must be used in the following sequence:</span></span>

-   [<span data-ttu-id="9f649-109">StopServices</span><span class="sxs-lookup"><span data-stu-id="9f649-109">StopServices</span></span>](stopservices-action.md)
-   [<span data-ttu-id="9f649-110">DeleteServices</span><span class="sxs-lookup"><span data-stu-id="9f649-110">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="9f649-111">Cualquiera de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="9f649-111">Any of the following actions:</span></span>

-   [<span data-ttu-id="9f649-112">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="9f649-112">InstallFiles</span></span>](installfiles-action.md)
-   [<span data-ttu-id="9f649-113">RemoveFiles</span><span class="sxs-lookup"><span data-stu-id="9f649-113">RemoveFiles</span></span>](removefiles-action.md)
-   [<span data-ttu-id="9f649-114">DuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="9f649-114">DuplicateFiles</span></span>](duplicatefiles-action.md)
-   [<span data-ttu-id="9f649-115">MoveFiles</span><span class="sxs-lookup"><span data-stu-id="9f649-115">MoveFiles</span></span>](movefiles-action.md)
-   [<span data-ttu-id="9f649-116">PatchFiles</span><span class="sxs-lookup"><span data-stu-id="9f649-116">PatchFiles</span></span>](patchfiles-action.md)
-   [<span data-ttu-id="9f649-117">RemoveDuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="9f649-117">RemoveDuplicateFiles</span></span>](removeduplicatefiles-action.md)
-   [<span data-ttu-id="9f649-118">InstallServices</span><span class="sxs-lookup"><span data-stu-id="9f649-118">InstallServices</span></span>](installservices-action.md)
-   <span data-ttu-id="9f649-119">StartServices</span><span class="sxs-lookup"><span data-stu-id="9f649-119">StartServices</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="9f649-120">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="9f649-120">ActionData Messages</span></span>



| <span data-ttu-id="9f649-121">Campo</span><span class="sxs-lookup"><span data-stu-id="9f649-121">Field</span></span> | <span data-ttu-id="9f649-122">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="9f649-122">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="9f649-123">\[1\]</span><span class="sxs-lookup"><span data-stu-id="9f649-123">\[1\]</span></span> | <span data-ttu-id="9f649-124">Nombre para mostrar del servicio.</span><span class="sxs-lookup"><span data-stu-id="9f649-124">Service display name.</span></span>      |
| <span data-ttu-id="9f649-125">\[2\]</span><span class="sxs-lookup"><span data-stu-id="9f649-125">\[2\]</span></span> | <span data-ttu-id="9f649-126">Nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="9f649-126">Service name.</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="9f649-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f649-127">Remarks</span></span>

<span data-ttu-id="9f649-128">Esta acción requiere que el usuario sea administrador o que tenga privilegios elevados con permiso para controlar los servicios o que la aplicación forme parte de una instalación administrada.</span><span class="sxs-lookup"><span data-stu-id="9f649-128">This action requires that the user be an administrator or have elevated privileges with permission to control services or that the application be part of a managed installation.</span></span>

 

 



