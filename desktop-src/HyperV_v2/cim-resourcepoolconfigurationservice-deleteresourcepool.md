---
description: Inicie un trabajo para eliminar un grupo de recursos.
ms.assetid: af3d9c7c-a825-4568-822d-044b3d92d144
title: Método DeleteResourcePool de la clase CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.DeleteResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9cab27df07a6a3a9679cb5e6595b6ba558d8b05e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666569"
---
# <a name="deleteresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="29984-103">Método DeleteResourcePool de la \_ clase ResourcePoolConfigurationService de CIM</span><span class="sxs-lookup"><span data-stu-id="29984-103">DeleteResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="29984-104">Inicie un trabajo para eliminar un grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="29984-104">Start a job to delete a resource pool.</span></span> <span data-ttu-id="29984-105">No puede haber ninguna asignación pendiente o se producirá un error en la eliminación con "en uso".</span><span class="sxs-lookup"><span data-stu-id="29984-105">No allocations may be outstanding or the delete will fail with "In Use."</span></span> <span data-ttu-id="29984-106">Si el grupo de recursos de servidor es un grupo de recursos raíz, los recursos del host se devuelven al sistema subyacente.</span><span class="sxs-lookup"><span data-stu-id="29984-106">If the resource pool is a root resource pool, any host resources are returned back to the underlying system.</span></span>

## <a name="syntax"></a><span data-ttu-id="29984-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29984-107">Syntax</span></span>


```mof
uint32 DeleteResourcePool(
  [in]  CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="29984-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="29984-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29984-109">*Grupo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="29984-109">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29984-110">[**\_ ResourcePool CIM**](cim-resourcepool.md) que hace referencia al grupo que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="29984-110">A [**CIM\_ResourcePool**](cim-resourcepool.md) that references to the pool to delete.</span></span>

</dd> <dt>

<span data-ttu-id="29984-111">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="29984-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29984-112">Un [**\_ ConcreteJob de CIM**](cim-concretejob.md) que hace referencia al trabajo (puede ser **null** si el trabajo se completó).</span><span class="sxs-lookup"><span data-stu-id="29984-112">A [**CIM\_ConcreteJob**](cim-concretejob.md) that references the job (may be **null** if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29984-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="29984-113">Return value</span></span>

<span data-ttu-id="29984-114">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="29984-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="29984-115">**Trabajo completado sin errores** (0)</span><span class="sxs-lookup"><span data-stu-id="29984-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="29984-116">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="29984-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="29984-117">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="29984-117">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="29984-118">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="29984-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="29984-119">**Error** (4)</span><span class="sxs-lookup"><span data-stu-id="29984-119">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="29984-120">**Parámetro no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="29984-120">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="29984-121">**En uso** (6)</span><span class="sxs-lookup"><span data-stu-id="29984-121">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="29984-122">**Resourcetype incorrecto para el grupo** (7)</span><span class="sxs-lookup"><span data-stu-id="29984-122">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="29984-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="29984-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="29984-124">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="29984-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="29984-125">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="29984-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="29984-126">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="29984-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="29984-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29984-127">Requirements</span></span>



| <span data-ttu-id="29984-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="29984-128">Requirement</span></span> | <span data-ttu-id="29984-129">Value</span><span class="sxs-lookup"><span data-stu-id="29984-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29984-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29984-130">Minimum supported client</span></span><br/> | <span data-ttu-id="29984-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="29984-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="29984-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29984-132">Minimum supported server</span></span><br/> | <span data-ttu-id="29984-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="29984-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="29984-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="29984-134">Namespace</span></span><br/>                | <span data-ttu-id="29984-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="29984-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="29984-136">MOF</span><span class="sxs-lookup"><span data-stu-id="29984-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29984-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29984-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="29984-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="29984-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29984-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="29984-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="29984-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="29984-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29984-141">**\_RESOURCEPOOLCONFIGURATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="29984-141">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




