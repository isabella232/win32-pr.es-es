---
description: Representa el servicio VSS invitado. Se usa para consultar información del clúster invitado desde el host de Hyper-V.
ms.assetid: 82321456-a24e-4f67-9346-f0844e2913dc
title: Msvm_VssService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 298ced09537ffc6e17f98484f600b05155fe0d97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360153"
---
# <a name="msvm_vssservice-class"></a><span data-ttu-id="731d4-104">MSVM \_ VssService (clase)</span><span class="sxs-lookup"><span data-stu-id="731d4-104">Msvm\_VssService class</span></span>

<span data-ttu-id="731d4-105">Representa el servicio VSS invitado.</span><span class="sxs-lookup"><span data-stu-id="731d4-105">Represents the guest VSS service.</span></span> <span data-ttu-id="731d4-106">Se usa para consultar información del clúster invitado desde el host de Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="731d4-106">It is used for querying guest cluster information from the Hyper-V host.</span></span>

<span data-ttu-id="731d4-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="731d4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="731d4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="731d4-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssService : Msvm_GuestService
{
};
```

## <a name="members"></a><span data-ttu-id="731d4-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="731d4-109">Members</span></span>

<span data-ttu-id="731d4-110">La clase **MSVM \_ VssService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="731d4-110">The **Msvm\_VssService** class has these types of members:</span></span>

-   [<span data-ttu-id="731d4-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="731d4-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="731d4-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="731d4-112">Methods</span></span>

<span data-ttu-id="731d4-113">La clase **MSVM \_ VssService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="731d4-113">The **Msvm\_VssService** class has these methods.</span></span>



| <span data-ttu-id="731d4-114">Método</span><span class="sxs-lookup"><span data-stu-id="731d4-114">Method</span></span>                                                                               | <span data-ttu-id="731d4-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="731d4-115">Description</span></span>                                                                 |
|:-------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="731d4-116">**QueryGuestClusterInformation**</span><span class="sxs-lookup"><span data-stu-id="731d4-116">**QueryGuestClusterInformation**</span></span>](msvm-vssservice-queryguestclusterinformation.md) | <span data-ttu-id="731d4-117">Consultar la información del clúster desde el host de Hyper-V hasta el invitado.</span><span class="sxs-lookup"><span data-stu-id="731d4-117">Querying cluster information from the Hyper-V host to the guest.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="731d4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="731d4-118">Requirements</span></span>



| <span data-ttu-id="731d4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="731d4-119">Requirement</span></span> | <span data-ttu-id="731d4-120">Value</span><span class="sxs-lookup"><span data-stu-id="731d4-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="731d4-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="731d4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="731d4-122">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="731d4-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="731d4-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="731d4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="731d4-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="731d4-124">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="731d4-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="731d4-125">Namespace</span></span><br/>                | <span data-ttu-id="731d4-126">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="731d4-126">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="731d4-127">MOF</span><span class="sxs-lookup"><span data-stu-id="731d4-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="731d4-128"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="731d4-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="731d4-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="731d4-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="731d4-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="731d4-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="731d4-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="731d4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="731d4-132">**MSVM \_ GuestService**</span><span class="sxs-lookup"><span data-stu-id="731d4-132">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




