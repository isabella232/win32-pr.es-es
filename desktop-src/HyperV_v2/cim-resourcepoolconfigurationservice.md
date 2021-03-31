---
description: Administra la configuración de grupos de recursos mediante el uso de trabajos.
ms.assetid: cc0f0236-2335-4dd9-9132-51b3e6b9fcf4
title: CIM_ResourcePoolConfigurationService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e8dbbce21f7749b7f436e2f49acb7ce6c7340faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908098"
---
# <a name="cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="37789-103">\_Clase ResourcePoolConfigurationService de CIM</span><span class="sxs-lookup"><span data-stu-id="37789-103">CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="37789-104">Administra la configuración de grupos de recursos mediante el uso de trabajos.</span><span class="sxs-lookup"><span data-stu-id="37789-104">Manages the configuration of resource pools by using jobs.</span></span>

## <a name="syntax"></a><span data-ttu-id="37789-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37789-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_ResourcePoolConfigurationService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="37789-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="37789-106">Members</span></span>

<span data-ttu-id="37789-107">La clase **CIM \_ ResourcePoolConfigurationService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="37789-107">The **CIM\_ResourcePoolConfigurationService** class has these types of members:</span></span>

-   [<span data-ttu-id="37789-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="37789-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="37789-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="37789-109">Methods</span></span>

<span data-ttu-id="37789-110">La clase **CIM \_ ResourcePoolConfigurationService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="37789-110">The **CIM\_ResourcePoolConfigurationService** class has these methods.</span></span>



| <span data-ttu-id="37789-111">Método</span><span class="sxs-lookup"><span data-stu-id="37789-111">Method</span></span>                                                                                                          | <span data-ttu-id="37789-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="37789-112">Description</span></span>                                                                   |
|:----------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="37789-113">**AddResourcesToResourcePool**</span><span class="sxs-lookup"><span data-stu-id="37789-113">**AddResourcesToResourcePool**</span></span>](cim-resourcepoolconfigurationservice-addresourcestoresourcepool.md)           | <span data-ttu-id="37789-114">Inicia un trabajo para agregar recursos a un grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="37789-114">Starts a job to add resources to a resource pool.</span></span><br/>                  |
| [<span data-ttu-id="37789-115">**ChangeParentResourcePool**</span><span class="sxs-lookup"><span data-stu-id="37789-115">**ChangeParentResourcePool**</span></span>](cim-resourcepoolconfigurationservice-changeparentresourcepool.md)               | <span data-ttu-id="37789-116">Iniciar un trabajo para cambiar el grupo de recursos primarios de un grupo de recursos de sitio.</span><span class="sxs-lookup"><span data-stu-id="37789-116">Start a job to change the parent resource pool of a resource pool.</span></span><br/> |
| [<span data-ttu-id="37789-117">**CreateChildResourcePool**</span><span class="sxs-lookup"><span data-stu-id="37789-117">**CreateChildResourcePool**</span></span>](cim-resourcepoolconfigurationservice-createchildresourcepool.md)                 | <span data-ttu-id="37789-118">Iniciar un trabajo para crear un grupo de recursos de un grupo de recursos primario.</span><span class="sxs-lookup"><span data-stu-id="37789-118">Start a job to create a resource pool from a parent resource pool.</span></span><br/> |
| [<span data-ttu-id="37789-119">**CreateResourcePool**</span><span class="sxs-lookup"><span data-stu-id="37789-119">**CreateResourcePool**</span></span>](cim-resourcepoolconfigurationservice-createresourcepool.md)                           | <span data-ttu-id="37789-120">Inicia un trabajo para crear un grupo de recursos raíz.</span><span class="sxs-lookup"><span data-stu-id="37789-120">Starts a job to create a root resource pool.</span></span><br/>                       |
| [<span data-ttu-id="37789-121">**DeleteResourcePool**</span><span class="sxs-lookup"><span data-stu-id="37789-121">**DeleteResourcePool**</span></span>](cim-resourcepoolconfigurationservice-deleteresourcepool.md)                           | <span data-ttu-id="37789-122">Inicie un trabajo para eliminar un grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="37789-122">Start a job to delete a resource pool.</span></span><br/>                             |
| [<span data-ttu-id="37789-123">**RemoveResourcesFromResourcePool**</span><span class="sxs-lookup"><span data-stu-id="37789-123">**RemoveResourcesFromResourcePool**</span></span>](cim-resourcepoolconfigurationservice-removeresourcesfromresourcepool.md) | <span data-ttu-id="37789-124">Inicia un trabajo para quitar recursos de un grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="37789-124">Starts a job to remove resources from a resource pool.</span></span><br/>             |



 

## <a name="requirements"></a><span data-ttu-id="37789-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37789-125">Requirements</span></span>



| <span data-ttu-id="37789-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="37789-126">Requirement</span></span> | <span data-ttu-id="37789-127">Value</span><span class="sxs-lookup"><span data-stu-id="37789-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37789-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37789-128">Minimum supported client</span></span><br/> | <span data-ttu-id="37789-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="37789-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="37789-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37789-130">Minimum supported server</span></span><br/> | <span data-ttu-id="37789-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="37789-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="37789-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="37789-132">Namespace</span></span><br/>                | <span data-ttu-id="37789-133">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="37789-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="37789-134">MOF</span><span class="sxs-lookup"><span data-stu-id="37789-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37789-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37789-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="37789-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="37789-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37789-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="37789-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="37789-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="37789-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37789-139">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="37789-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




