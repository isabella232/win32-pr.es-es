---
description: Iniciar un trabajo para cambiar un grupo primario con la configuración de asignación especificada.
ms.assetid: 2eea1a60-fbf0-49a7-8f79-52c62c295316
title: Método ChangeParentResourcePool de la clase CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.ChangeParentResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6ef852d6af8f0973b6b3f29fca5fcd90e9ce726a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686908"
---
# <a name="changeparentresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="a9ba3-103">Método ChangeParentResourcePool de la \_ clase ResourcePoolConfigurationService de CIM</span><span class="sxs-lookup"><span data-stu-id="a9ba3-103">ChangeParentResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="a9ba3-104">Iniciar un trabajo para cambiar un grupo primario con la configuración de asignación especificada.</span><span class="sxs-lookup"><span data-stu-id="a9ba3-104">Start a job to change a parent pool using the specified allocation settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9ba3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9ba3-105">Syntax</span></span>


```mof
uint32 ChangeParentResourcePool(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  CIM_ResourcePool REF ParentPool[],
  [in]  string               Settings[],
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a9ba3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a9ba3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9ba3-107">*ChildPool* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a9ba3-107">*ChildPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9ba3-108">[**\_ ResourcePool CIM**](cim-resourcepool.md) que hace referencia al grupo secundario.</span><span class="sxs-lookup"><span data-stu-id="a9ba3-108">A [**CIM\_ResourcePool**](cim-resourcepool.md) that references the child pool.</span></span>

</dd> <dt>

<span data-ttu-id="a9ba3-109">*ParentPool* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a9ba3-109">*ParentPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9ba3-110">Una [**matriz \_ ResourcePool de CIM**](cim-resourcepool.md) que hace referencia a los grupos primarios.</span><span class="sxs-lookup"><span data-stu-id="a9ba3-110">A [**CIM\_ResourcePool**](cim-resourcepool.md) array that references the parent pool(s).</span></span>

</dd> <dt>

<span data-ttu-id="a9ba3-111">*Configuración* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a9ba3-111">*Settings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9ba3-112">Cadena opcional que contiene una representación de una instancia de [**\_ SettingData de CIM**](cim-settingdata.md) que se usa para especificar la configuración del grupo primario.</span><span class="sxs-lookup"><span data-stu-id="a9ba3-112">Optional string containing a representation of a [**CIM\_SettingData**](cim-settingdata.md) instance that is used to specify the settings for the parent pool.</span></span>

</dd> <dt>

<span data-ttu-id="a9ba3-113">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a9ba3-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9ba3-114">Un [**\_ ConcreteJob de CIM**](cim-concretejob.md) que hace referencia al trabajo (puede ser **null** si el trabajo se completó).</span><span class="sxs-lookup"><span data-stu-id="a9ba3-114">A [**CIM\_ConcreteJob**](cim-concretejob.md) that references the job (may be **null** if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9ba3-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a9ba3-115">Return value</span></span>

<span data-ttu-id="a9ba3-116">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="a9ba3-116">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="a9ba3-117">**Trabajo completado sin errores** (0)</span><span class="sxs-lookup"><span data-stu-id="a9ba3-117">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a9ba3-118">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="a9ba3-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a9ba3-119">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="a9ba3-119">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a9ba3-120">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="a9ba3-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a9ba3-121">**Error** (4)</span><span class="sxs-lookup"><span data-stu-id="a9ba3-121">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a9ba3-122">**Parámetro no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="a9ba3-122">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a9ba3-123">**En uso** (6)</span><span class="sxs-lookup"><span data-stu-id="a9ba3-123">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a9ba3-124">**Resourcetype incorrecto para el grupo** (7)</span><span class="sxs-lookup"><span data-stu-id="a9ba3-124">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a9ba3-125">**Recursos insuficientes** (8)</span><span class="sxs-lookup"><span data-stu-id="a9ba3-125">**Insufficient Resources** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a9ba3-126">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a9ba3-126">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a9ba3-127">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="a9ba3-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a9ba3-128">**Tamaño no compatible** (4097)</span><span class="sxs-lookup"><span data-stu-id="a9ba3-128">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="a9ba3-129">**Método reservado** (4098.. 32767)</span><span class="sxs-lookup"><span data-stu-id="a9ba3-129">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="a9ba3-130">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="a9ba3-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a9ba3-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9ba3-131">Requirements</span></span>



| <span data-ttu-id="a9ba3-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9ba3-132">Requirement</span></span> | <span data-ttu-id="a9ba3-133">Value</span><span class="sxs-lookup"><span data-stu-id="a9ba3-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9ba3-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9ba3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a9ba3-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a9ba3-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="a9ba3-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9ba3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a9ba3-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a9ba3-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="a9ba3-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a9ba3-138">Namespace</span></span><br/>                | <span data-ttu-id="a9ba3-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="a9ba3-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a9ba3-140">MOF</span><span class="sxs-lookup"><span data-stu-id="a9ba3-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9ba3-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9ba3-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9ba3-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a9ba3-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9ba3-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a9ba3-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a9ba3-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9ba3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9ba3-145">**\_RESOURCEPOOLCONFIGURATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="a9ba3-145">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




