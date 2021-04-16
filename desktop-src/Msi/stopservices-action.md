---
description: La acción StopServices detiene los servicios del sistema. Esta acción consulta la tabla ServiceControl.
ms.assetid: 1ad01205-f8b6-400f-be1d-c00a5b71ccfd
title: Acción StopServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb271b99c434a1ac54ab9744697b991e9e1fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677531"
---
# <a name="stopservices-action"></a><span data-ttu-id="c0bdc-104">Acción StopServices</span><span class="sxs-lookup"><span data-stu-id="c0bdc-104">StopServices Action</span></span>

<span data-ttu-id="c0bdc-105">La acción StopServices detiene los servicios del sistema.</span><span class="sxs-lookup"><span data-stu-id="c0bdc-105">The StopServices action stops system services.</span></span> <span data-ttu-id="c0bdc-106">Esta acción consulta la [tabla ServiceControl](servicecontrol-table.md).</span><span class="sxs-lookup"><span data-stu-id="c0bdc-106">This action queries the [ServiceControl table](servicecontrol-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="c0bdc-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="c0bdc-107">Sequence Restrictions</span></span>

<span data-ttu-id="c0bdc-108">Las acciones de servicios se deben usar en la secuencia siguiente:</span><span class="sxs-lookup"><span data-stu-id="c0bdc-108">The services actions must be used in the following sequence:</span></span>

-   <span data-ttu-id="c0bdc-109">StopServices</span><span class="sxs-lookup"><span data-stu-id="c0bdc-109">StopServices</span></span>
-   [<span data-ttu-id="c0bdc-110">DeleteServices</span><span class="sxs-lookup"><span data-stu-id="c0bdc-110">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="c0bdc-111">Cualquiera de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="c0bdc-111">Any of the following actions:</span></span>

-   [<span data-ttu-id="c0bdc-112">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="c0bdc-112">InstallFiles</span></span>](installfiles-action.md)
-   [<span data-ttu-id="c0bdc-113">RemoveFiles</span><span class="sxs-lookup"><span data-stu-id="c0bdc-113">RemoveFiles</span></span>](removefiles-action.md)
-   [<span data-ttu-id="c0bdc-114">DuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="c0bdc-114">DuplicateFiles</span></span>](duplicatefiles-action.md)
-   [<span data-ttu-id="c0bdc-115">MoveFiles</span><span class="sxs-lookup"><span data-stu-id="c0bdc-115">MoveFiles</span></span>](movefiles-action.md)
-   [<span data-ttu-id="c0bdc-116">PatchFiles</span><span class="sxs-lookup"><span data-stu-id="c0bdc-116">PatchFiles</span></span>](patchfiles-action.md)
-   [<span data-ttu-id="c0bdc-117">RemoveDuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="c0bdc-117">RemoveDuplicateFiles</span></span>](removeduplicatefiles-action.md)
-   [<span data-ttu-id="c0bdc-118">InstallServices</span><span class="sxs-lookup"><span data-stu-id="c0bdc-118">InstallServices</span></span>](installservices-action.md)
-   [<span data-ttu-id="c0bdc-119">StartServices</span><span class="sxs-lookup"><span data-stu-id="c0bdc-119">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="c0bdc-120">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="c0bdc-120">ActionData Messages</span></span>



| <span data-ttu-id="c0bdc-121">Campo</span><span class="sxs-lookup"><span data-stu-id="c0bdc-121">Field</span></span> | <span data-ttu-id="c0bdc-122">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="c0bdc-122">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="c0bdc-123">\[1\]</span><span class="sxs-lookup"><span data-stu-id="c0bdc-123">\[1\]</span></span> | <span data-ttu-id="c0bdc-124">Nombre para mostrar del servicio.</span><span class="sxs-lookup"><span data-stu-id="c0bdc-124">Service display name.</span></span>      |
| <span data-ttu-id="c0bdc-125">\[2\]</span><span class="sxs-lookup"><span data-stu-id="c0bdc-125">\[2\]</span></span> | <span data-ttu-id="c0bdc-126">Nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="c0bdc-126">Service name.</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="c0bdc-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c0bdc-127">Remarks</span></span>

<span data-ttu-id="c0bdc-128">Esta acción requiere que el usuario sea administrador o que tenga privilegios elevados con permiso para controlar los servicios o que la aplicación forme parte de una instalación administrada.</span><span class="sxs-lookup"><span data-stu-id="c0bdc-128">This action requires that the user be an administrator or have elevated privileges with permission to control services or that the application be part of a managed installation.</span></span>

 

 



