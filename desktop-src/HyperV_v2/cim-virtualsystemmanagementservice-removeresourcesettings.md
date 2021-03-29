---
description: Quita la configuración de recursos virtuales de una configuración de sistema virtual.
ms.assetid: 7934a5e4-f54c-43fd-9ec3-d1fc1aad0acd
title: Método RemoveResourceSettings de la clase CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1f5b3ac1cc53f23d0d899a4c6b5d17408bca3b9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812728"
---
# <a name="removeresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="614bf-103">Método RemoveResourceSettings de la \_ clase VirtualSystemManagementService de CIM</span><span class="sxs-lookup"><span data-stu-id="614bf-103">RemoveResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="614bf-104">Quita la configuración de recursos virtuales de una configuración de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="614bf-104">Removes virtual resource settings from a virtual system configuration.</span></span>

<span data-ttu-id="614bf-105">Cuando se aplica a partes de una configuración de sistema virtual "actual", es posible que se eliminen los recursos secundarios del sistema virtual activo.</span><span class="sxs-lookup"><span data-stu-id="614bf-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="614bf-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="614bf-106">Syntax</span></span>


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="614bf-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="614bf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="614bf-108">*ResourceSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="614bf-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="614bf-109">Matriz de referencias a instancias de la clase [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) donde cada instancia representa la configuración de un recurso virtual dentro de una configuración de sistema virtual que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="614bf-109">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) where each instance represents the settings of a virtual resource within a virtual system configuration that are to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="614bf-110">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="614bf-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="614bf-111">Si la operación es de larga ejecución, opcionalmente se puede devolver un [**\_ ConcreteJob de CIM**](cim-concretejob.md) que represente el trabajo.</span><span class="sxs-lookup"><span data-stu-id="614bf-111">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="614bf-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="614bf-112">Return value</span></span>

<span data-ttu-id="614bf-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="614bf-113">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="614bf-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="614bf-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="614bf-115">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="614bf-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="614bf-116">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="614bf-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="614bf-117">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="614bf-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="614bf-118">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="614bf-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="614bf-119">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="614bf-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="614bf-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="614bf-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="614bf-121">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="614bf-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="614bf-122">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="614bf-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="614bf-123">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="614bf-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="614bf-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="614bf-124">Requirements</span></span>



| <span data-ttu-id="614bf-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="614bf-125">Requirement</span></span> | <span data-ttu-id="614bf-126">Value</span><span class="sxs-lookup"><span data-stu-id="614bf-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="614bf-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="614bf-127">Minimum supported client</span></span><br/> | <span data-ttu-id="614bf-128">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="614bf-128">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="614bf-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="614bf-129">Minimum supported server</span></span><br/> | <span data-ttu-id="614bf-130">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="614bf-130">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="614bf-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="614bf-131">Namespace</span></span><br/>                | <span data-ttu-id="614bf-132">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="614bf-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="614bf-133">MOF</span><span class="sxs-lookup"><span data-stu-id="614bf-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="614bf-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="614bf-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="614bf-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="614bf-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="614bf-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="614bf-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="614bf-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="614bf-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="614bf-138">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="614bf-138">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




