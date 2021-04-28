---
description: 'Método RemoveResourceSettings de la clase CIM_VirtualSystemManagementService: quita la configuración de recursos virtuales de una configuración del sistema virtual.'
ms.assetid: 7934a5e4-f54c-43fd-9ec3-d1fc1aad0acd
title: Método RemoveResourceSettings de la CIM_VirtualSystemManagementService clase
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
ms.openlocfilehash: e5c7daabcdcd732c3a5693664e1768ebf66668d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112263"
---
# <a name="removeresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="f269e-103">Método RemoveResourceSettings de la clase \_ CIM VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="f269e-103">RemoveResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="f269e-104">Quita la configuración de recursos virtuales de una configuración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="f269e-104">Removes virtual resource settings from a virtual system configuration.</span></span>

<span data-ttu-id="f269e-105">Cuando se aplica a partes de una configuración del sistema virtual "actual", como efecto secundario se pueden quitar los recursos del sistema virtual activo.</span><span class="sxs-lookup"><span data-stu-id="f269e-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f269e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f269e-106">Syntax</span></span>


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f269e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f269e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f269e-108">*ResourceSettings* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f269e-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f269e-109">Matriz de referencias a instancias de la clase [**\_ CIM ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) donde cada instancia representa la configuración de un recurso virtual dentro de una configuración del sistema virtual que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="f269e-109">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) where each instance represents the settings of a virtual resource within a virtual system configuration that are to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="f269e-110">*Trabajo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f269e-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f269e-111">Si la operación es de larga duración, opcionalmente se puede devolver [**un \_ ConcreteJob cim**](cim-concretejob.md) que representa el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f269e-111">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f269e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f269e-112">Return value</span></span>

<span data-ttu-id="f269e-113">Devuelve un 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="f269e-113">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="f269e-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="f269e-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f269e-115">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="f269e-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f269e-116">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="f269e-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f269e-117">**Tiempo de** espera (3)</span><span class="sxs-lookup"><span data-stu-id="f269e-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f269e-118">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="f269e-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f269e-119">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="f269e-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f269e-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="f269e-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f269e-121">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="f269e-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f269e-122">**Método reservado** (4097..32767)</span><span class="sxs-lookup"><span data-stu-id="f269e-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="f269e-123">**Específico del** proveedor (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="f269e-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f269e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f269e-124">Requirements</span></span>



| <span data-ttu-id="f269e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f269e-125">Requirement</span></span> | <span data-ttu-id="f269e-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f269e-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f269e-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f269e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f269e-128">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f269e-128">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f269e-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f269e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f269e-130">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f269e-130">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f269e-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f269e-131">Namespace</span></span><br/>                | <span data-ttu-id="f269e-132">Virtualización \\ raíz \\ v2</span><span class="sxs-lookup"><span data-stu-id="f269e-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f269e-133">MOF</span><span class="sxs-lookup"><span data-stu-id="f269e-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f269e-134"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="f269e-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f269e-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f269e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f269e-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f269e-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f269e-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f269e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f269e-138">**CIM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="f269e-138">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




