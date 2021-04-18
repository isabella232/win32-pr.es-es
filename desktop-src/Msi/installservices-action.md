---
description: La acción InstallServices registra un servicio para el sistema. Esta acción consulta la tabla ServiceInstall.
ms.assetid: bb394cdb-1310-44fb-b7e1-2ffbb976d438
title: Acción InstallServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d5964deb08f811e391418211efc6f774261bd87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688449"
---
# <a name="installservices-action"></a><span data-ttu-id="2b19c-104">Acción InstallServices</span><span class="sxs-lookup"><span data-stu-id="2b19c-104">InstallServices Action</span></span>

<span data-ttu-id="2b19c-105">La acción InstallServices registra un servicio para el sistema.</span><span class="sxs-lookup"><span data-stu-id="2b19c-105">The InstallServices action registers a service for the system.</span></span> <span data-ttu-id="2b19c-106">Esta acción consulta la [tabla ServiceInstall](serviceinstall-table.md).</span><span class="sxs-lookup"><span data-stu-id="2b19c-106">This action queries the [ServiceInstall table](serviceinstall-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="2b19c-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="2b19c-107">Sequence Restrictions</span></span>

<span data-ttu-id="2b19c-108">La acción Services debe usarse en la siguiente secuencia.</span><span class="sxs-lookup"><span data-stu-id="2b19c-108">The services action must be used in the following sequence.</span></span>

[<span data-ttu-id="2b19c-109">StopServices</span><span class="sxs-lookup"><span data-stu-id="2b19c-109">StopServices</span></span>](stopservices-action.md)

[<span data-ttu-id="2b19c-110">DeleteServices</span><span class="sxs-lookup"><span data-stu-id="2b19c-110">DeleteServices</span></span>](deleteservices-action.md)

<span data-ttu-id="2b19c-111">Cualquiera de las siguientes acciones: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md)y [RemoveDuplicateFiles](removeduplicatefiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="2b19c-111">Any of the following actions: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md), and [RemoveDuplicateFiles](removeduplicatefiles-action.md) actions.</span></span>

<span data-ttu-id="2b19c-112">InstallServices</span><span class="sxs-lookup"><span data-stu-id="2b19c-112">InstallServices</span></span>

[<span data-ttu-id="2b19c-113">StartServices</span><span class="sxs-lookup"><span data-stu-id="2b19c-113">StartServices</span></span>](startservices-action.md)

## <a name="actiondata-messages"></a><span data-ttu-id="2b19c-114">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="2b19c-114">ActionData Messages</span></span>

<span data-ttu-id="2b19c-115">No hay mensajes ActionData.</span><span class="sxs-lookup"><span data-stu-id="2b19c-115">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b19c-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b19c-116">Remarks</span></span>

<span data-ttu-id="2b19c-117">Esta acción requiere que el usuario sea administrador o que tenga privilegios elevados con permisos para instalar servicios o que la aplicación forme parte de una instalación administrada.</span><span class="sxs-lookup"><span data-stu-id="2b19c-117">This action requires that the user be an administrator or have elevated privileges with permission to install services or that the application be part of a managed installation.</span></span>

 

 



