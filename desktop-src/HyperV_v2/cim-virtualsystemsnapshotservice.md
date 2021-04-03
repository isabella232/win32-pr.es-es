---
description: Representa un servicio que puede crear, aplicar y eliminar instantáneas de sistemas virtuales.
ms.assetid: 8d5d54a2-08f1-4f24-bca3-601dc698d018
title: CIM_VirtualSystemSnapshotService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7ae74f85d1af9867b7a95c23aeda670b8f06f413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913901"
---
# <a name="cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="fab71-103">\_Clase VirtualSystemSnapshotService de CIM</span><span class="sxs-lookup"><span data-stu-id="fab71-103">CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="fab71-104">Representa un servicio que puede crear, aplicar y eliminar instantáneas de sistemas virtuales.</span><span class="sxs-lookup"><span data-stu-id="fab71-104">Represents a service that can create, apply, and delete snapshots of virtual systems.</span></span>

## <a name="syntax"></a><span data-ttu-id="fab71-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fab71-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemSnapshotService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="fab71-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="fab71-106">Members</span></span>

<span data-ttu-id="fab71-107">La clase **CIM \_ VirtualSystemSnapshotService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fab71-107">The **CIM\_VirtualSystemSnapshotService** class has these types of members:</span></span>

-   [<span data-ttu-id="fab71-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="fab71-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fab71-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="fab71-109">Methods</span></span>

<span data-ttu-id="fab71-110">La clase **CIM \_ VirtualSystemSnapshotService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="fab71-110">The **CIM\_VirtualSystemSnapshotService** class has these methods.</span></span>



| <span data-ttu-id="fab71-111">Método</span><span class="sxs-lookup"><span data-stu-id="fab71-111">Method</span></span>                                                                      | <span data-ttu-id="fab71-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="fab71-112">Description</span></span>                                                                                      |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fab71-113">**ApplySnapshot**</span><span class="sxs-lookup"><span data-stu-id="fab71-113">**ApplySnapshot**</span></span>](cim-virtualsystemsnapshotservice-applysnapshot.md)     | <span data-ttu-id="fab71-114">Aplica una instantánea del sistema virtual al sistema virtual de origen.</span><span class="sxs-lookup"><span data-stu-id="fab71-114">Applies a virtual system snapshot to the virtual system to the source virtual system.</span></span><br/> |
| [<span data-ttu-id="fab71-115">**CreateSnapshot**</span><span class="sxs-lookup"><span data-stu-id="fab71-115">**CreateSnapshot**</span></span>](cim-virtualsystemsnapshotservice-createsnapshot.md)   | <span data-ttu-id="fab71-116">Crea una instantánea de un sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="fab71-116">Creates a snapshot of a virtual system.</span></span><br/>                                               |
| [<span data-ttu-id="fab71-117">**DestroySnapshot**</span><span class="sxs-lookup"><span data-stu-id="fab71-117">**DestroySnapshot**</span></span>](cim-virtualsystemsnapshotservice-destroysnapshot.md) | <span data-ttu-id="fab71-118">Elimina una instantánea del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="fab71-118">Deletes a virtual system snapshot.</span></span><br/>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="fab71-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fab71-119">Requirements</span></span>



| <span data-ttu-id="fab71-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fab71-120">Requirement</span></span> | <span data-ttu-id="fab71-121">Value</span><span class="sxs-lookup"><span data-stu-id="fab71-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fab71-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fab71-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fab71-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="fab71-123">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="fab71-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fab71-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fab71-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fab71-125">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="fab71-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fab71-126">Namespace</span></span><br/>                | <span data-ttu-id="fab71-127">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="fab71-127">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fab71-128">MOF</span><span class="sxs-lookup"><span data-stu-id="fab71-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fab71-129"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fab71-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fab71-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fab71-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fab71-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fab71-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fab71-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="fab71-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fab71-133">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="fab71-133">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




