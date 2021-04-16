---
description: Iniciar un trabajo para crear un grupo secundario a partir de un grupo primario con la configuración de asignación especificada.
ms.assetid: 9b09221a-7c4e-4648-a2a8-012df1818c3e
title: Método CreateChildResourcePool de la clase CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateChildResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e4e709fd240c849581f6dcd343001a9b1dee7003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666570"
---
# <a name="createchildresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="6d2c8-103">Método CreateChildResourcePool de la \_ clase ResourcePoolConfigurationService de CIM</span><span class="sxs-lookup"><span data-stu-id="6d2c8-103">CreateChildResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="6d2c8-104">Iniciar un trabajo para crear un grupo secundario a partir de un grupo primario con la configuración de asignación especificada.</span><span class="sxs-lookup"><span data-stu-id="6d2c8-104">Start a job to create a sub-pool from a parent pool using the specified allocation settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d2c8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6d2c8-105">Syntax</span></span>


```mof
uint32 CreateChildResourcePool(
  [in]  string               ElementName,
  [in]  string               Settings[],
  [in]  CIM_ResourcePool REF ParentPool[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6d2c8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6d2c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d2c8-107">*ElementName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6d2c8-107">*ElementName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2c8-108">Nombre relevante del usuario final para el grupo que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="6d2c8-108">A end user relevant name for the pool being created.</span></span> <span data-ttu-id="6d2c8-109">Si **es null**, se puede usar un nombre predeterminado proporcionado por el sistema.</span><span class="sxs-lookup"><span data-stu-id="6d2c8-109">If **NULL**, then a system supplied default name can be used.</span></span> <span data-ttu-id="6d2c8-110">El valor se almacenará en la propiedad **ElementName** del elemento creado.</span><span class="sxs-lookup"><span data-stu-id="6d2c8-110">The value will be stored in the **ElementName** property for the created element.</span></span>

</dd> <dt>

<span data-ttu-id="6d2c8-111">*Configuración* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6d2c8-111">*Settings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2c8-112">Cadena que contiene una representación de una instancia de [**\_ SettingData de CIM**](cim-settingdata.md) que se usa para especificar la configuración del grupo secundario.</span><span class="sxs-lookup"><span data-stu-id="6d2c8-112">String containing a representation of a [**CIM\_SettingData**](cim-settingdata.md) instance that is used to specify the settings for the child Pool.</span></span>

</dd> <dt>

<span data-ttu-id="6d2c8-113">*ParentPool* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6d2c8-113">*ParentPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2c8-114">Un [**\_ ResourcePool CIM**](cim-resourcepool.md) a partir del cual se creará el nuevo grupo.</span><span class="sxs-lookup"><span data-stu-id="6d2c8-114">A [**CIM\_ResourcePool**](cim-resourcepool.md) from which to create the new Pool.</span></span>

</dd> <dt>

<span data-ttu-id="6d2c8-115">*Grupo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6d2c8-115">*Pool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2c8-116">[**\_ ResourcePool CIM**](cim-resourcepool.md) que hace referencia al grupo resultante.</span><span class="sxs-lookup"><span data-stu-id="6d2c8-116">A [**CIM\_ResourcePool**](cim-resourcepool.md) that references the resulting pool.</span></span>

</dd> <dt>

<span data-ttu-id="6d2c8-117">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6d2c8-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2c8-118">Referencia al trabajo (puede ser null si el trabajo se completó).</span><span class="sxs-lookup"><span data-stu-id="6d2c8-118">Reference to the job (may be null if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d2c8-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6d2c8-119">Return value</span></span>

<span data-ttu-id="6d2c8-120">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="6d2c8-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="6d2c8-121">**Trabajo completado sin errores** (0)</span><span class="sxs-lookup"><span data-stu-id="6d2c8-121">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6d2c8-122">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="6d2c8-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6d2c8-123">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="6d2c8-123">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6d2c8-124">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="6d2c8-124">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6d2c8-125">**Error** (4)</span><span class="sxs-lookup"><span data-stu-id="6d2c8-125">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6d2c8-126">**Parámetro no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="6d2c8-126">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6d2c8-127">**En uso** (6)</span><span class="sxs-lookup"><span data-stu-id="6d2c8-127">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6d2c8-128">**Resourcetype incorrecto para el grupo** (7)</span><span class="sxs-lookup"><span data-stu-id="6d2c8-128">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="6d2c8-129">**Recursos insuficientes** (8)</span><span class="sxs-lookup"><span data-stu-id="6d2c8-129">**Insufficient Resources** (8)</span></span>
</dt> <dt>

<span data-ttu-id="6d2c8-130">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="6d2c8-130">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6d2c8-131">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="6d2c8-131">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6d2c8-132">**Tamaño no compatible** (4097)</span><span class="sxs-lookup"><span data-stu-id="6d2c8-132">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="6d2c8-133">**Método reservado** (4098.. 32767)</span><span class="sxs-lookup"><span data-stu-id="6d2c8-133">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="6d2c8-134">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="6d2c8-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6d2c8-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d2c8-135">Requirements</span></span>



| <span data-ttu-id="6d2c8-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d2c8-136">Requirement</span></span> | <span data-ttu-id="6d2c8-137">Value</span><span class="sxs-lookup"><span data-stu-id="6d2c8-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d2c8-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d2c8-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6d2c8-139">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6d2c8-139">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="6d2c8-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d2c8-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6d2c8-141">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6d2c8-141">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="6d2c8-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6d2c8-142">Namespace</span></span><br/>                | <span data-ttu-id="6d2c8-143">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="6d2c8-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6d2c8-144">MOF</span><span class="sxs-lookup"><span data-stu-id="6d2c8-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d2c8-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d2c8-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d2c8-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6d2c8-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d2c8-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6d2c8-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6d2c8-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d2c8-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d2c8-149">**\_RESOURCEPOOLCONFIGURATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="6d2c8-149">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




