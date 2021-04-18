---
description: Elimina un grupo de recursos.
ms.assetid: bc3111a4-9687-49ec-890e-190358230c53
title: Método DeletePool de la clase Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.DeletePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 84273daa0aa30dca8722d90d4fcec22b88325bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668085"
---
# <a name="deletepool-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="831b0-103">Método DeletePool de la \_ clase ResourcePoolConfigurationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="831b0-103">DeletePool method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="831b0-104">Elimina un grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="831b0-104">Deletes a resource pool.</span></span> <span data-ttu-id="831b0-105">Para eliminar correctamente un grupo de recursos, no puede haber ninguna asignación pendiente o se producirá un error en la eliminación con 32774 (en uso).</span><span class="sxs-lookup"><span data-stu-id="831b0-105">To successfully delete a resource pool, no allocations can be outstanding or the delete will fail with 32774 (In Use).</span></span> <span data-ttu-id="831b0-106">Si el grupo de recursos de servidor es un grupo de recursos raíz, los recursos del host se devuelven al sistema subyacente.</span><span class="sxs-lookup"><span data-stu-id="831b0-106">If the resource pool is a root resource pool, any host resources are returned back to the underlying system.</span></span>

## <a name="syntax"></a><span data-ttu-id="831b0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="831b0-107">Syntax</span></span>


```mof
uint32 DeletePool(
  [in]  CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="831b0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="831b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="831b0-109">*Grupo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="831b0-109">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="831b0-110">Referencia a una instancia de la clase [**\_ ResourcePool de CIM**](cim-resourcepool.md) que representa el grupo que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="831b0-110">A reference to an instance of the [**CIM\_ResourcePool**](cim-resourcepool.md) class that represents the pool to delete.</span></span>

</dd> <dt>

<span data-ttu-id="831b0-111">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="831b0-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="831b0-112">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="831b0-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="831b0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="831b0-113">Return value</span></span>

<span data-ttu-id="831b0-114">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="831b0-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="831b0-115">**Trabajo completado sin errores** (0)</span><span class="sxs-lookup"><span data-stu-id="831b0-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="831b0-116">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="831b0-116">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="831b0-117">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="831b0-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="831b0-118">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="831b0-118">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="831b0-119">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="831b0-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="831b0-120">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="831b0-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="831b0-121">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="831b0-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="831b0-122">**Desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="831b0-122">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="831b0-123">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="831b0-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="831b0-124">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="831b0-124">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="831b0-125">**En uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="831b0-125">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="831b0-126">**Estado no válido** (32775)</span><span class="sxs-lookup"><span data-stu-id="831b0-126">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="831b0-127">**Tipo de recurso incorrecto para el grupo** (32776)</span><span class="sxs-lookup"><span data-stu-id="831b0-127">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="831b0-128">**No disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="831b0-128">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="831b0-129">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="831b0-129">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="831b0-130">**Proveedor reservado** (32779)</span><span class="sxs-lookup"><span data-stu-id="831b0-130">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="831b0-131">**Recursos insuficientes** (32780)</span><span class="sxs-lookup"><span data-stu-id="831b0-131">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="831b0-132">**No se encontró el objeto** (32781.. 32787)</span><span class="sxs-lookup"><span data-stu-id="831b0-132">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="831b0-133">**Existe el objeto** (32788)</span><span class="sxs-lookup"><span data-stu-id="831b0-133">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="831b0-134">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="831b0-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="831b0-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="831b0-135">Requirements</span></span>



| <span data-ttu-id="831b0-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="831b0-136">Requirement</span></span> | <span data-ttu-id="831b0-137">Value</span><span class="sxs-lookup"><span data-stu-id="831b0-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="831b0-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="831b0-138">Minimum supported client</span></span><br/> | <span data-ttu-id="831b0-139">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="831b0-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="831b0-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="831b0-140">Minimum supported server</span></span><br/> | <span data-ttu-id="831b0-141">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="831b0-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="831b0-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="831b0-142">Namespace</span></span><br/>                | <span data-ttu-id="831b0-143">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="831b0-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="831b0-144">MOF</span><span class="sxs-lookup"><span data-stu-id="831b0-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="831b0-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="831b0-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="831b0-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="831b0-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="831b0-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="831b0-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="831b0-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="831b0-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="831b0-149">**MSVM \_ ResourcePoolConfigurationService**</span><span class="sxs-lookup"><span data-stu-id="831b0-149">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

