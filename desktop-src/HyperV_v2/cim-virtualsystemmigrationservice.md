---
description: Representa un servicio que controla la migración de sistemas virtuales entre sistemas host. Esta clase también comprueba si es probable que una migración pendiente sea correcta.
ms.assetid: 28948a36-3b92-4d52-9a48-aaa155e7fad5
title: CIM_VirtualSystemMigrationService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6343cec0573a97656368d66426ec9b46c7255e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909190"
---
# <a name="cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="15c04-104">\_Clase VirtualSystemMigrationService de CIM</span><span class="sxs-lookup"><span data-stu-id="15c04-104">CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="15c04-105">Representa un servicio que controla la migración de sistemas virtuales entre sistemas host.</span><span class="sxs-lookup"><span data-stu-id="15c04-105">Represents a service that controls the migration of virtual systems between host systems.</span></span> <span data-ttu-id="15c04-106">Esta clase también comprueba si es probable que una migración pendiente sea correcta.</span><span class="sxs-lookup"><span data-stu-id="15c04-106">This class also verifies whether a pending migration is likely to succeed.</span></span>

## <a name="syntax"></a><span data-ttu-id="15c04-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15c04-107">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.17.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="15c04-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="15c04-108">Members</span></span>

<span data-ttu-id="15c04-109">La clase **CIM \_ VirtualSystemMigrationService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="15c04-109">The **CIM\_VirtualSystemMigrationService** class has these types of members:</span></span>

-   [<span data-ttu-id="15c04-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="15c04-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="15c04-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="15c04-111">Methods</span></span>

<span data-ttu-id="15c04-112">La clase **CIM \_ VirtualSystemMigrationService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="15c04-112">The **CIM\_VirtualSystemMigrationService** class has these methods.</span></span>



| <span data-ttu-id="15c04-113">Método</span><span class="sxs-lookup"><span data-stu-id="15c04-113">Method</span></span>                                                                                                                     | <span data-ttu-id="15c04-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="15c04-114">Description</span></span>                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15c04-115">**CheckVirtualSystemIsMigratableToHost**</span><span class="sxs-lookup"><span data-stu-id="15c04-115">**CheckVirtualSystemIsMigratableToHost**</span></span>](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md)     | <span data-ttu-id="15c04-116">Comprueba si es probable que se realice correctamente una migración de sistema virtual pendiente a un host.</span><span class="sxs-lookup"><span data-stu-id="15c04-116">Verifies whether a pending virtual system migration to a host is likely to succeed.</span></span><br/>   |
| [<span data-ttu-id="15c04-117">**CheckVirtualSystemIsMigratableToSystem**</span><span class="sxs-lookup"><span data-stu-id="15c04-117">**CheckVirtualSystemIsMigratableToSystem**</span></span>](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletosystem.md) | <span data-ttu-id="15c04-118">Comprueba si es probable que se realice correctamente una migración de sistema virtual pendiente a un sistema.</span><span class="sxs-lookup"><span data-stu-id="15c04-118">Verifies whether a pending virtual system migration to a system is likely to succeed.</span></span><br/> |
| [<span data-ttu-id="15c04-119">**MigrateVirtualSystemToHost**</span><span class="sxs-lookup"><span data-stu-id="15c04-119">**MigrateVirtualSystemToHost**</span></span>](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md)                         | <span data-ttu-id="15c04-120">Migra un sistema virtual a un host de destino.</span><span class="sxs-lookup"><span data-stu-id="15c04-120">Migrates a virtual system to a target host.</span></span><br/>                                           |
| [<span data-ttu-id="15c04-121">**MigrateVirtualSystemToSystem**</span><span class="sxs-lookup"><span data-stu-id="15c04-121">**MigrateVirtualSystemToSystem**</span></span>](cim-virtualsystemmigrationservice-migratevirtualsystemtosystem.md)                     | <span data-ttu-id="15c04-122">Migra un sistema virtual a un sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="15c04-122">Migrates a virtual system to target system.</span></span><br/>                                           |



 

## <a name="requirements"></a><span data-ttu-id="15c04-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15c04-123">Requirements</span></span>



| <span data-ttu-id="15c04-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="15c04-124">Requirement</span></span> | <span data-ttu-id="15c04-125">Value</span><span class="sxs-lookup"><span data-stu-id="15c04-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15c04-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15c04-126">Minimum supported client</span></span><br/> | <span data-ttu-id="15c04-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="15c04-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="15c04-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15c04-128">Minimum supported server</span></span><br/> | <span data-ttu-id="15c04-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="15c04-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="15c04-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="15c04-130">Namespace</span></span><br/>                | <span data-ttu-id="15c04-131">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="15c04-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="15c04-132">MOF</span><span class="sxs-lookup"><span data-stu-id="15c04-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15c04-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15c04-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="15c04-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="15c04-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15c04-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="15c04-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="15c04-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="15c04-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15c04-137">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="15c04-137">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




