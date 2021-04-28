---
description: 'Método ModifyResourceSettings de la clase CIM_VirtualSystemManagementService: modifica la configuración de recursos virtuales.'
ms.assetid: 4942f167-0e53-4ae2-b973-4a06b636b44a
title: Método ModifyResourceSettings de la CIM_VirtualSystemManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 26971c80ce6f7d0ffcdcef069d76aef5fdc15138
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112293"
---
# <a name="modifyresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="3552f-103">Método ModifyResourceSettings de la clase \_ CIM VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="3552f-103">ModifyResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="3552f-104">Modifica la configuración de recursos virtuales.</span><span class="sxs-lookup"><span data-stu-id="3552f-104">Modifies virtual resource settings.</span></span>

<span data-ttu-id="3552f-105">Cuando se aplica a partes de una configuración del sistema virtual "actual", como efecto secundario se pueden modificar los recursos del sistema virtual activo.</span><span class="sxs-lookup"><span data-stu-id="3552f-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="3552f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3552f-106">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3552f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3552f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3552f-108">*ResourceSettings* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="3552f-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3552f-109">Matriz de cadenas que contiene una instancia incrustada de la clase [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que describe las modificaciones en los aspectos virtuales de un recurso virtual existente.</span><span class="sxs-lookup"><span data-stu-id="3552f-109">Array of strings each containing an embedded instance of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that describes modifications to the virtual aspects of an existing virtual resource.</span></span> <span data-ttu-id="3552f-110">Todas las instancias deben tener un **instanceID** válido para identificar la configuración del recurso virtual que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="3552f-110">All instances must have a valid **InstanceID** in order to identify the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="3552f-111">*ResultingResourceSettings* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3552f-111">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3552f-112">Matriz de referencias a instancias de la clase [**CIM \_ ResourceAllocationSettingData que**](cim-resourceallocationsettingdata.md) representa aspectos virtuales de los recursos virtuales modificados.</span><span class="sxs-lookup"><span data-stu-id="3552f-112">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="3552f-113">*Trabajo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3552f-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3552f-114">Si la operación es de larga duración, opcionalmente se devuelve un trabajo.</span><span class="sxs-lookup"><span data-stu-id="3552f-114">If the operation is long running, then optionally a job be returned.</span></span> <span data-ttu-id="3552f-115">En este caso, las instancias de la clase [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representan la configuración de recursos modificada están disponibles a través de la asociación **CIM \_ ConreteComponent** desde la instancia de la clase [**CIM \_ VirtualSystemSettingData que representa**](cim-virtualsystemsettingdata.md) la configuración del sistema virtual afectada.</span><span class="sxs-lookup"><span data-stu-id="3552f-115">In this case, the instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing the modified resource settings are available via association **CIM\_ConreteComponent** from the instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) representing the affected virtual system configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3552f-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3552f-116">Return value</span></span>

<span data-ttu-id="3552f-117">Devuelve un valor 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="3552f-117">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="3552f-118">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="3552f-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3552f-119">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="3552f-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3552f-120">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="3552f-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3552f-121">**Tiempo de** espera (3)</span><span class="sxs-lookup"><span data-stu-id="3552f-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3552f-122">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="3552f-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3552f-123">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="3552f-123">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3552f-124">**Parámetros incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="3552f-124">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3552f-125">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3552f-125">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3552f-126">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="3552f-126">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3552f-127">**Método reservado** (4097..32767)</span><span class="sxs-lookup"><span data-stu-id="3552f-127">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="3552f-128">**Específico del** proveedor (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="3552f-128">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3552f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3552f-129">Requirements</span></span>



| <span data-ttu-id="3552f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3552f-130">Requirement</span></span> | <span data-ttu-id="3552f-131">Valor</span><span class="sxs-lookup"><span data-stu-id="3552f-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3552f-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3552f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3552f-133">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3552f-133">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="3552f-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3552f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3552f-135">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3552f-135">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="3552f-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3552f-136">Namespace</span></span><br/>                | <span data-ttu-id="3552f-137">Virtualización \\ raíz \\ v2</span><span class="sxs-lookup"><span data-stu-id="3552f-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3552f-138">MOF</span><span class="sxs-lookup"><span data-stu-id="3552f-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3552f-139"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="3552f-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3552f-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3552f-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3552f-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3552f-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3552f-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3552f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3552f-143">**CIM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="3552f-143">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




