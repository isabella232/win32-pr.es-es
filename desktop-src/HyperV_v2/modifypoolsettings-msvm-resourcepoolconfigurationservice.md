---
description: Cambia la configuración de un grupo secundario que no está relacionado con la asignación.
ms.assetid: f60068e0-f333-41e2-8f11-78aa48dfa260
title: Método ModifyPoolSettings de la clase Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.ModifyPoolSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: edc5f48dabfb84554954cc80d9c4e8a20678d34f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277991"
---
# <a name="modifypoolsettings-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="3f6a7-103">Método ModifyPoolSettings de la \_ clase ResourcePoolConfigurationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="3f6a7-103">ModifyPoolSettings method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="3f6a7-104">Cambia la configuración de un grupo secundario que no está relacionado con la asignación.</span><span class="sxs-lookup"><span data-stu-id="3f6a7-104">Changes the settings of a child pool that are not allocation related.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f6a7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f6a7-105">Syntax</span></span>


```mof
uint32 ModifyPoolSettings(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  string               PoolSettings,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3f6a7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f6a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f6a7-107">*ChildPool* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f6a7-107">*ChildPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f6a7-108">Referencia a una instancia de la clase [**\_ ResourcePool de CIM**](cim-resourcepool.md) que representa el grupo secundario que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="3f6a7-108">A reference to an instance of the [**CIM\_ResourcePool**](cim-resourcepool.md) class that represents the child pool to modify.</span></span>

</dd> <dt>

<span data-ttu-id="3f6a7-109">*PoolSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f6a7-109">*PoolSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f6a7-110">Instancia insertada de la clase [**MSVM \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) que se usa para especificar la nueva configuración para el grupo.</span><span class="sxs-lookup"><span data-stu-id="3f6a7-110">An embedded instance of the [**Msvm\_ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) class that is used to specify the new settings for the pool.</span></span>

</dd> <dt>

<span data-ttu-id="3f6a7-111">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3f6a7-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f6a7-112">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3f6a7-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f6a7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f6a7-113">Return value</span></span>

<span data-ttu-id="3f6a7-114">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3f6a7-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3f6a7-115">**Trabajo completado sin errores** (0)</span><span class="sxs-lookup"><span data-stu-id="3f6a7-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3f6a7-116">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3f6a7-116">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3f6a7-117">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="3f6a7-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3f6a7-118">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="3f6a7-118">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="3f6a7-119">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="3f6a7-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3f6a7-120">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="3f6a7-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3f6a7-121">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="3f6a7-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3f6a7-122">**Desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="3f6a7-122">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3f6a7-123">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="3f6a7-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3f6a7-124">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="3f6a7-124">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3f6a7-125">**En uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="3f6a7-125">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3f6a7-126">**Estado no válido** (32775)</span><span class="sxs-lookup"><span data-stu-id="3f6a7-126">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3f6a7-127">**Tipo de recurso incorrecto para el grupo** (32776)</span><span class="sxs-lookup"><span data-stu-id="3f6a7-127">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3f6a7-128">**No disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="3f6a7-128">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3f6a7-129">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="3f6a7-129">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="3f6a7-130">**Proveedor reservado** (32779)</span><span class="sxs-lookup"><span data-stu-id="3f6a7-130">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="3f6a7-131">**Recursos insuficientes** (32780)</span><span class="sxs-lookup"><span data-stu-id="3f6a7-131">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="3f6a7-132">**No se encontró el objeto** (32781.. 32787)</span><span class="sxs-lookup"><span data-stu-id="3f6a7-132">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="3f6a7-133">**Existe el objeto** (32788)</span><span class="sxs-lookup"><span data-stu-id="3f6a7-133">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="3f6a7-134">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="3f6a7-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3f6a7-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f6a7-135">Requirements</span></span>



| <span data-ttu-id="3f6a7-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f6a7-136">Requirement</span></span> | <span data-ttu-id="3f6a7-137">Value</span><span class="sxs-lookup"><span data-stu-id="3f6a7-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f6a7-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f6a7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="3f6a7-139">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="3f6a7-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3f6a7-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f6a7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="3f6a7-141">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="3f6a7-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3f6a7-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3f6a7-142">Namespace</span></span><br/>                | <span data-ttu-id="3f6a7-143">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="3f6a7-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3f6a7-144">MOF</span><span class="sxs-lookup"><span data-stu-id="3f6a7-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f6a7-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3f6a7-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3f6a7-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3f6a7-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f6a7-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3f6a7-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3f6a7-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f6a7-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f6a7-149">**MSVM \_ ResourcePoolConfigurationService**</span><span class="sxs-lookup"><span data-stu-id="3f6a7-149">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

