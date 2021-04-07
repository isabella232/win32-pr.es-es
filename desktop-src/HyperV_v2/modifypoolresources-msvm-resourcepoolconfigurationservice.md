---
description: Cambia la configuración de recursos del grupo primario para los recursos asignados a un grupo secundario.
ms.assetid: 419fca70-5f15-4593-80ac-ef2af2c3dde5
title: Método ModifyPoolResources de la clase Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.ModifyPoolResources
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2efffdbcc34577f675556874c4153eea2670768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911689"
---
# <a name="modifypoolresources-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="0a04d-103">Método ModifyPoolResources de la \_ clase ResourcePoolConfigurationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="0a04d-103">ModifyPoolResources method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="0a04d-104">Cambia la configuración de recursos del grupo primario para los recursos asignados a un grupo secundario.</span><span class="sxs-lookup"><span data-stu-id="0a04d-104">Changes the parent pool resource settings for resources assigned to a child pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a04d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a04d-105">Syntax</span></span>


```mof
uint32 ModifyPoolResources(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0a04d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a04d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a04d-107">*ChildPool* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0a04d-107">*ChildPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a04d-108">Referencia a una instancia de la clase [**\_ ResourcePool de CIM**](cim-resourcepool.md) que representa el grupo secundario que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="0a04d-108">A reference to an instance of the [**CIM\_ResourcePool**](cim-resourcepool.md) class that represents the child pool to modify.</span></span>

</dd> <dt>

<span data-ttu-id="0a04d-109">*ParentPools* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0a04d-109">*ParentPools* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a04d-110">Una matriz de [**referencias \_ ResourcePool CIM**](cim-resourcepool.md) que representan los nuevos grupos primarios que se asignarán al grupo secundario.</span><span class="sxs-lookup"><span data-stu-id="0a04d-110">An array of [**CIM\_ResourcePool**](cim-resourcepool.md) references that represent the new parent pools to assign to the child pool.</span></span>

</dd> <dt>

<span data-ttu-id="0a04d-111">*AllocationSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0a04d-111">*AllocationSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a04d-112">Una matriz opcional de una o varias instancias incrustadas de la clase [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) que se usan para especificar la configuración relacionada con la asignación del grupo.</span><span class="sxs-lookup"><span data-stu-id="0a04d-112">An optional array of one or more embedded instances of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that are used to specify the pool allocation related settings.</span></span>

</dd> <dt>

<span data-ttu-id="0a04d-113">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0a04d-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a04d-114">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0a04d-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a04d-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a04d-115">Return value</span></span>

<span data-ttu-id="0a04d-116">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0a04d-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0a04d-117">**Trabajo completado sin errores** (0)</span><span class="sxs-lookup"><span data-stu-id="0a04d-117">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0a04d-118">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0a04d-118">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0a04d-119">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="0a04d-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0a04d-120">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="0a04d-120">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="0a04d-121">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="0a04d-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="0a04d-122">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="0a04d-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0a04d-123">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="0a04d-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="0a04d-124">**Desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="0a04d-124">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="0a04d-125">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="0a04d-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="0a04d-126">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="0a04d-126">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0a04d-127">**En uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="0a04d-127">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="0a04d-128">**Estado no válido** (32775)</span><span class="sxs-lookup"><span data-stu-id="0a04d-128">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0a04d-129">**Tipo de recurso incorrecto para el grupo** (32776)</span><span class="sxs-lookup"><span data-stu-id="0a04d-129">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="0a04d-130">**No disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="0a04d-130">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="0a04d-131">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="0a04d-131">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="0a04d-132">**Proveedor reservado** (32779)</span><span class="sxs-lookup"><span data-stu-id="0a04d-132">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="0a04d-133">**Recursos insuficientes** (32780)</span><span class="sxs-lookup"><span data-stu-id="0a04d-133">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="0a04d-134">**No se encontró el objeto** (32781.. 32787)</span><span class="sxs-lookup"><span data-stu-id="0a04d-134">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="0a04d-135">**Existe el objeto** (32788)</span><span class="sxs-lookup"><span data-stu-id="0a04d-135">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="0a04d-136">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="0a04d-136">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0a04d-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a04d-137">Requirements</span></span>



| <span data-ttu-id="0a04d-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a04d-138">Requirement</span></span> | <span data-ttu-id="0a04d-139">Value</span><span class="sxs-lookup"><span data-stu-id="0a04d-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a04d-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a04d-140">Minimum supported client</span></span><br/> | <span data-ttu-id="0a04d-141">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="0a04d-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0a04d-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a04d-142">Minimum supported server</span></span><br/> | <span data-ttu-id="0a04d-143">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="0a04d-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0a04d-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0a04d-144">Namespace</span></span><br/>                | <span data-ttu-id="0a04d-145">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="0a04d-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0a04d-146">MOF</span><span class="sxs-lookup"><span data-stu-id="0a04d-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a04d-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0a04d-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a04d-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0a04d-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a04d-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0a04d-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0a04d-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a04d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a04d-151">**MSVM \_ ResourcePoolConfigurationService**</span><span class="sxs-lookup"><span data-stu-id="0a04d-151">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

