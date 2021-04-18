---
description: Crea un grupo de recursos secundarios.
ms.assetid: 30a70231-f1b7-4f0e-ac47-cf5a79ddb8ab
title: Método CreatePool de la clase Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.CreatePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fb29a4b5a47d88232a6b0df6a828d482030b3f1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687851"
---
# <a name="createpool-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="beb8a-103">Método CreatePool de la \_ clase ResourcePoolConfigurationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="beb8a-103">CreatePool method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="beb8a-104">Crea un grupo de recursos secundarios.</span><span class="sxs-lookup"><span data-stu-id="beb8a-104">Creates a child resource pool.</span></span> <span data-ttu-id="beb8a-105">El grupo de recursos de servidor se limitará al mismo sistema que este servicio.</span><span class="sxs-lookup"><span data-stu-id="beb8a-105">The resource pool will be scoped to the same System as this Service.</span></span> <span data-ttu-id="beb8a-106">El grupo resultante será un grupo secundario.</span><span class="sxs-lookup"><span data-stu-id="beb8a-106">The resulting pool will be a child pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="beb8a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="beb8a-107">Syntax</span></span>


```mof
uint32 CreatePool(
  [in]  string               PoolSettings,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="beb8a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="beb8a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beb8a-109">*PoolSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="beb8a-109">*PoolSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beb8a-110">Instancia insertada de la clase [**MSVM \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) que se usa para especificar la configuración del grupo que no está relacionada con la asignación.</span><span class="sxs-lookup"><span data-stu-id="beb8a-110">An embedded instance of the [**Msvm\_ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) class that is used to specify the pool settings that are not allocation related.</span></span>

</dd> <dt>

<span data-ttu-id="beb8a-111">*ParentPools* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="beb8a-111">*ParentPools* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beb8a-112">Una matriz de referencias de [**\_ ResourcePool de MSVM**](msvm-resourcepool.md) que representan el grupo o los grupos de los que se va a crear el nuevo grupo.</span><span class="sxs-lookup"><span data-stu-id="beb8a-112">An array of [**Msvm\_ResourcePool**](msvm-resourcepool.md) references that represent the pool or pools from which to create the new pool.</span></span>

</dd> <dt>

<span data-ttu-id="beb8a-113">*AllocationSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="beb8a-113">*AllocationSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beb8a-114">Una matriz de una o varias instancias incrustadas de la clase [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) que se usan para especificar la configuración relacionada con la asignación del grupo.</span><span class="sxs-lookup"><span data-stu-id="beb8a-114">An array of one or more embedded instances of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that are used to specify the pool allocation related settings.</span></span> <span data-ttu-id="beb8a-115">Esta matriz debe contener un elemento para cada elemento de la matriz *ParentPools* o exactamente un elemento.</span><span class="sxs-lookup"><span data-stu-id="beb8a-115">This array must contain either one element for each element in the *ParentPools* array, or exactly one element.</span></span> <span data-ttu-id="beb8a-116">Si esta matriz contiene un elemento y *ParentPools* contiene más de un elemento, *AlllocationSettings* especifica una asignación de capacidad compartida que puede satisfacer cualquiera de los grupos primarios.</span><span class="sxs-lookup"><span data-stu-id="beb8a-116">If this array contains one element and *ParentPools* contains more than one element, *AlllocationSettings* specifies a shared capacity allocation that can be satisfied by any of the parent pools.</span></span>

<span data-ttu-id="beb8a-117">Se usa para restringir los recursos que se pueden asignar desde el elemento secundario al grupo a un límite inferior al de la capacidad agregada proporcionada por sus elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="beb8a-117">This is used to restrict the resources that can be allocated from the child to the pool to a lower limit than the aggregate capacity provided by its parents.</span></span> <span data-ttu-id="beb8a-118">Esta opción no es compatible con todos los tipos de recursos.</span><span class="sxs-lookup"><span data-stu-id="beb8a-118">This option is not supported by all resource types.</span></span> <span data-ttu-id="beb8a-119">Si un tipo de recurso no admite la asignación de capacidad compartida, este método devolverá 32770 (no se admite).</span><span class="sxs-lookup"><span data-stu-id="beb8a-119">If a resource type does not support shared capacity allocation, this method will return 32770 (Not Supported).</span></span>

</dd> <dt>

<span data-ttu-id="beb8a-120">*Grupo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="beb8a-120">*Pool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="beb8a-121">Referencia al grupo resultante.</span><span class="sxs-lookup"><span data-stu-id="beb8a-121">A reference to the resulting pool.</span></span>

</dd> <dt>

<span data-ttu-id="beb8a-122">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="beb8a-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="beb8a-123">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="beb8a-123">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beb8a-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="beb8a-124">Return value</span></span>

<span data-ttu-id="beb8a-125">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="beb8a-125">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="beb8a-126">**Trabajo completado sin errores** (0)</span><span class="sxs-lookup"><span data-stu-id="beb8a-126">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="beb8a-127">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="beb8a-127">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="beb8a-128">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="beb8a-128">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="beb8a-129">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="beb8a-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="beb8a-130">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="beb8a-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="beb8a-131">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="beb8a-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="beb8a-132">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="beb8a-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="beb8a-133">**Desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="beb8a-133">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="beb8a-134">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="beb8a-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="beb8a-135">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="beb8a-135">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="beb8a-136">**En uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="beb8a-136">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="beb8a-137">**Estado no válido** (32775)</span><span class="sxs-lookup"><span data-stu-id="beb8a-137">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="beb8a-138">**Tipo de recurso incorrecto para el grupo** (32776)</span><span class="sxs-lookup"><span data-stu-id="beb8a-138">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="beb8a-139">**No disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="beb8a-139">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="beb8a-140">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="beb8a-140">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="beb8a-141">**Proveedor reservado** (32779)</span><span class="sxs-lookup"><span data-stu-id="beb8a-141">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="beb8a-142">**Recursos insuficientes** (32780)</span><span class="sxs-lookup"><span data-stu-id="beb8a-142">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="beb8a-143">**No se encontró el objeto** (32781.. 32787)</span><span class="sxs-lookup"><span data-stu-id="beb8a-143">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="beb8a-144">**Existe el objeto** (32788)</span><span class="sxs-lookup"><span data-stu-id="beb8a-144">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="beb8a-145">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="beb8a-145">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="beb8a-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="beb8a-146">Requirements</span></span>



| <span data-ttu-id="beb8a-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="beb8a-147">Requirement</span></span> | <span data-ttu-id="beb8a-148">Value</span><span class="sxs-lookup"><span data-stu-id="beb8a-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="beb8a-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="beb8a-149">Minimum supported client</span></span><br/> | <span data-ttu-id="beb8a-150">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="beb8a-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="beb8a-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="beb8a-151">Minimum supported server</span></span><br/> | <span data-ttu-id="beb8a-152">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="beb8a-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="beb8a-153">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="beb8a-153">Namespace</span></span><br/>                | <span data-ttu-id="beb8a-154">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="beb8a-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="beb8a-155">MOF</span><span class="sxs-lookup"><span data-stu-id="beb8a-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="beb8a-156"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="beb8a-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="beb8a-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="beb8a-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="beb8a-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="beb8a-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="beb8a-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="beb8a-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beb8a-160">**MSVM \_ ResourcePoolConfigurationService**</span><span class="sxs-lookup"><span data-stu-id="beb8a-160">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

