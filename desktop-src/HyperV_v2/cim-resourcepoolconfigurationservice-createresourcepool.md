---
description: Inicia un trabajo para crear un ResourcePool raíz. El ámbito del ResourcePool se establecerá en el mismo sistema que este servicio.
ms.assetid: 357880dc-125a-452c-89f5-44cd17684436
title: Método CreateResourcePool de la clase CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ca339eb2e2a4ec0fb441c5ed1a657608d71248bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810334"
---
# <a name="createresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="0d3da-104">Método CreateResourcePool de la \_ clase ResourcePoolConfigurationService de CIM</span><span class="sxs-lookup"><span data-stu-id="0d3da-104">CreateResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="0d3da-105">Inicia un trabajo para crear un ResourcePool raíz.</span><span class="sxs-lookup"><span data-stu-id="0d3da-105">Starts a job to create a root ResourcePool.</span></span> <span data-ttu-id="0d3da-106">El ámbito del ResourcePool se establecerá en el mismo sistema que este servicio.</span><span class="sxs-lookup"><span data-stu-id="0d3da-106">The ResourcePool will be scoped to the same System as this Service.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d3da-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d3da-107">Syntax</span></span>


```mof
uint32 CreateResourcePool(
  [in]  string                ElementName,
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  string                ResourceType,
  [out] CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0d3da-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d3da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d3da-109">*ElementName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d3da-109">*ElementName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d3da-110">Nombre relevante del usuario final para el grupo que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="0d3da-110">A end user relevant name for the pool being created.</span></span> <span data-ttu-id="0d3da-111">Si **es null**, se puede usar un nombre predeterminado proporcionado por el sistema.</span><span class="sxs-lookup"><span data-stu-id="0d3da-111">If **NULL**, then a system supplied default name can be used.</span></span> <span data-ttu-id="0d3da-112">El valor se almacenará en la propiedad **ElementName** del grupo creado.</span><span class="sxs-lookup"><span data-stu-id="0d3da-112">The value will be stored in the **ElementName** property for the created pool.</span></span>

</dd> <dt>

<span data-ttu-id="0d3da-113">*HostResources* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d3da-113">*HostResources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d3da-114">Matriz de cero o más [**dispositivos \_ lógicos de CIM**](cim-logicaldevice.md) que se usan para crear el grupo o modificar las extensiones de origen.</span><span class="sxs-lookup"><span data-stu-id="0d3da-114">Array of zero or more [**CIM\_LogicalDevice**](cim-logicaldevice.md) devices that are used to create the Pool or modify the source extents.</span></span> <span data-ttu-id="0d3da-115">Todos los elementos de la matriz deben ser del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="0d3da-115">All elements in the array must be of the same type.</span></span>

</dd> <dt>

<span data-ttu-id="0d3da-116">*ResourceType* \[in\]</span><span class="sxs-lookup"><span data-stu-id="0d3da-116">*ResourceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d3da-117">El tipo de recursos que el grupo creado administrará.</span><span class="sxs-lookup"><span data-stu-id="0d3da-117">The type of resources the created pool will manage.</span></span> <span data-ttu-id="0d3da-118">Si *HostResources* contiene elementos, esta propiedad debe Machar su tipo.</span><span class="sxs-lookup"><span data-stu-id="0d3da-118">If *HostResources* contains elements, this property must mach their type.</span></span>

</dd> <dt>

<span data-ttu-id="0d3da-119">*Grupo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0d3da-119">*Pool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d3da-120">Si se ejecuta correctamente, devuelve una referencia a [**la \_ ResourcePool CIM**](cim-resourcepool.md)resultante.</span><span class="sxs-lookup"><span data-stu-id="0d3da-120">On success, returns a reference to the resulting [**CIM\_ResourcePool**](cim-resourcepool.md).</span></span> <span data-ttu-id="0d3da-121">Cuando se devuelve un trabajo, esto puede ser **null**, en cuyo caso, el cliente debe usar el trabajo para buscar el ResourcePool resultante una vez completado el trabajo.</span><span class="sxs-lookup"><span data-stu-id="0d3da-121">When a Job is returned, this may be **NULL**, in which case, the client must use the Job to find the resulting ResourcePool once the Job completes.</span></span>

</dd> <dt>

<span data-ttu-id="0d3da-122">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0d3da-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d3da-123">Referencia a un [**\_ ConcreteJob de CIM**](cim-concretejob.md) que representa el trabajo (puede ser null si el trabajo se completó).</span><span class="sxs-lookup"><span data-stu-id="0d3da-123">Reference to a [**CIM\_ConcreteJob**](cim-concretejob.md) that represents the job (may be null if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d3da-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d3da-124">Return value</span></span>

<span data-ttu-id="0d3da-125">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="0d3da-125">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="0d3da-126">**Trabajo completado sin errores** (0)</span><span class="sxs-lookup"><span data-stu-id="0d3da-126">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0d3da-127">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="0d3da-127">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0d3da-128">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="0d3da-128">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0d3da-129">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="0d3da-129">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0d3da-130">**Error** (4)</span><span class="sxs-lookup"><span data-stu-id="0d3da-130">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0d3da-131">**Parámetro no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="0d3da-131">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0d3da-132">**En uso** (6)</span><span class="sxs-lookup"><span data-stu-id="0d3da-132">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0d3da-133">**Resourcetype incorrecto para el grupo** (7)</span><span class="sxs-lookup"><span data-stu-id="0d3da-133">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="0d3da-134">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0d3da-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0d3da-135">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="0d3da-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0d3da-136">**Tamaño no compatible** (4097)</span><span class="sxs-lookup"><span data-stu-id="0d3da-136">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="0d3da-137">**Método reservado** (4098.. 32767)</span><span class="sxs-lookup"><span data-stu-id="0d3da-137">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="0d3da-138">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="0d3da-138">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0d3da-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d3da-139">Requirements</span></span>



| <span data-ttu-id="0d3da-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d3da-140">Requirement</span></span> | <span data-ttu-id="0d3da-141">Value</span><span class="sxs-lookup"><span data-stu-id="0d3da-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d3da-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d3da-142">Minimum supported client</span></span><br/> | <span data-ttu-id="0d3da-143">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0d3da-143">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="0d3da-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d3da-144">Minimum supported server</span></span><br/> | <span data-ttu-id="0d3da-145">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0d3da-145">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="0d3da-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0d3da-146">Namespace</span></span><br/>                | <span data-ttu-id="0d3da-147">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="0d3da-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0d3da-148">MOF</span><span class="sxs-lookup"><span data-stu-id="0d3da-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d3da-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d3da-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d3da-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0d3da-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d3da-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0d3da-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0d3da-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d3da-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d3da-153">**\_RESOURCEPOOLCONFIGURATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="0d3da-153">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




