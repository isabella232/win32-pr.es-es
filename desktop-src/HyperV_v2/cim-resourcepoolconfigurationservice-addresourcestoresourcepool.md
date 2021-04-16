---
description: Inicia un trabajo para agregar recursos a un grupo de recursos.
ms.assetid: b163619a-19bd-43d7-ba35-ec4bd8192100
title: Método AddResourcesToResourcePool de la clase CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.AddResourcesToResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d3aed59267bd064e95b62431064fbd54bb9168aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686909"
---
# <a name="addresourcestoresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="8b48a-103">Método AddResourcesToResourcePool de la \_ clase ResourcePoolConfigurationService de CIM</span><span class="sxs-lookup"><span data-stu-id="8b48a-103">AddResourcesToResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="8b48a-104">Inicia un trabajo para agregar recursos a un grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8b48a-104">Starts a job to add resources to a resource pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b48a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b48a-105">Syntax</span></span>


```mof
uint32 AddResourcesToResourcePool(
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8b48a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b48a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b48a-107">*HostResources* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8b48a-107">*HostResources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b48a-108">Matriz de instancias de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que se va a agregar al grupo.</span><span class="sxs-lookup"><span data-stu-id="8b48a-108">Array of [**CIM\_LogicalDevice**](cim-logicaldevice.md) instances to add to the pool.</span></span>

</dd> <dt>

<span data-ttu-id="8b48a-109">*Grupo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8b48a-109">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b48a-110">[**\_ ResourcePool CIM**](cim-resourcepool.md) que representa el grupo al que se van a agregar los recursos.</span><span class="sxs-lookup"><span data-stu-id="8b48a-110">A [**CIM\_ResourcePool**](cim-resourcepool.md) that represents the pool to add the resources to.</span></span>

</dd> <dt>

<span data-ttu-id="8b48a-111">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8b48a-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b48a-112">Un [**\_ ConcreteJob de CIM**](cim-concretejob.md) que hace referencia al trabajo (puede ser **null** si el trabajo se completó).</span><span class="sxs-lookup"><span data-stu-id="8b48a-112">A [**CIM\_ConcreteJob**](cim-concretejob.md) that references the job (may be **null** if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b48a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b48a-113">Return value</span></span>

<span data-ttu-id="8b48a-114">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="8b48a-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="8b48a-115">**Trabajo completado sin errores** (0)</span><span class="sxs-lookup"><span data-stu-id="8b48a-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8b48a-116">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="8b48a-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8b48a-117">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="8b48a-117">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8b48a-118">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="8b48a-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8b48a-119">**Error** (4)</span><span class="sxs-lookup"><span data-stu-id="8b48a-119">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8b48a-120">**Parámetro no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="8b48a-120">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8b48a-121">**En uso** (6)</span><span class="sxs-lookup"><span data-stu-id="8b48a-121">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8b48a-122">**Resourcetype incorrecto para el grupo** (7)</span><span class="sxs-lookup"><span data-stu-id="8b48a-122">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="8b48a-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="8b48a-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8b48a-124">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="8b48a-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8b48a-125">**Tamaño no compatible** (4097)</span><span class="sxs-lookup"><span data-stu-id="8b48a-125">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="8b48a-126">**Método reservado** (4098.. 32767)</span><span class="sxs-lookup"><span data-stu-id="8b48a-126">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="8b48a-127">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="8b48a-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8b48a-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b48a-128">Requirements</span></span>



| <span data-ttu-id="8b48a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b48a-129">Requirement</span></span> | <span data-ttu-id="8b48a-130">Value</span><span class="sxs-lookup"><span data-stu-id="8b48a-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b48a-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b48a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8b48a-132">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8b48a-132">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="8b48a-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b48a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8b48a-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8b48a-134">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="8b48a-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8b48a-135">Namespace</span></span><br/>                | <span data-ttu-id="8b48a-136">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="8b48a-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8b48a-137">MOF</span><span class="sxs-lookup"><span data-stu-id="8b48a-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b48a-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b48a-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b48a-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8b48a-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b48a-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8b48a-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8b48a-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b48a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b48a-142">**\_RESOURCEPOOLCONFIGURATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="8b48a-142">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




