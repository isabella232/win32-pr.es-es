---
description: Agrega recursos a una configuración de sistema virtual.
ms.assetid: c2541571-74f0-48f8-997c-56c152980eea
title: Método AddResourceSettings de la clase CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9563b1e8421dfa6724971450b117780435f6f39e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687341"
---
# <a name="addresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="fb1ba-103">Método AddResourceSettings de la \_ clase VirtualSystemManagementService de CIM</span><span class="sxs-lookup"><span data-stu-id="fb1ba-103">AddResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="fb1ba-104">Agrega recursos a una configuración de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="fb1ba-104">Adds resources to a virtual system configuration.</span></span>

<span data-ttu-id="fb1ba-105">Cuando se aplica a una configuración de sistema virtual "State", se agregan recursos de efectos secundarios al sistema virtual activo.</span><span class="sxs-lookup"><span data-stu-id="fb1ba-105">When applied to a "state" virtual system configuration, as a side effect resources are added to the active virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb1ba-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb1ba-106">Syntax</span></span>


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="fb1ba-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb1ba-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb1ba-108">*AffectedConfiguration* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb1ba-108">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb1ba-109">Una referencia de [**\_ VirtualSystemSettingData de CIM**](cim-virtualsystemsettingdata.md) a la configuración de sistema virtual afectada.</span><span class="sxs-lookup"><span data-stu-id="fb1ba-109">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the affected virtual system configuration.</span></span>

</dd> <dt>

<span data-ttu-id="fb1ba-110">*ResourceSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb1ba-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb1ba-111">Matriz de cadenas que contiene una instancia incrustada de la clase [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que describe los aspectos virtuales de un recurso virtual que se va a agregar al sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="fb1ba-111">Array of strings each containing one embedded instance of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that describes the virtual aspects of a virtual resource to be added to the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="fb1ba-112">*ResultingResourceSettings* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fb1ba-112">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb1ba-113">Matriz de referencias a instancias de la clase [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representan aspectos virtuales de los recursos virtuales agregados.</span><span class="sxs-lookup"><span data-stu-id="fb1ba-113">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing virtual aspects of the added virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="fb1ba-114">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fb1ba-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb1ba-115">Si la operación es de larga ejecución, opcionalmente se puede devolver un trabajo.</span><span class="sxs-lookup"><span data-stu-id="fb1ba-115">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="fb1ba-116">En este caso, las instancias de la clase [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representan la configuración de recursos agregada están disponibles a través de la Asociación **CIM \_ ConreteComponent** desde la instancia de la clase [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa la configuración de sistema virtual afectada.</span><span class="sxs-lookup"><span data-stu-id="fb1ba-116">In this case, the instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing the added resource settings are available via association **CIM\_ConreteComponent** from the instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) representing the affected virtual system configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb1ba-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb1ba-117">Return value</span></span>

<span data-ttu-id="fb1ba-118">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="fb1ba-118">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="fb1ba-119">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="fb1ba-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fb1ba-120">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="fb1ba-120">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fb1ba-121">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="fb1ba-121">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fb1ba-122">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="fb1ba-122">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fb1ba-123">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="fb1ba-123">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fb1ba-124">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="fb1ba-124">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fb1ba-125">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="fb1ba-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fb1ba-126">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="fb1ba-126">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="fb1ba-127">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="fb1ba-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fb1ba-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb1ba-128">Requirements</span></span>



| <span data-ttu-id="fb1ba-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb1ba-129">Requirement</span></span> | <span data-ttu-id="fb1ba-130">Value</span><span class="sxs-lookup"><span data-stu-id="fb1ba-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb1ba-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb1ba-131">Minimum supported client</span></span><br/> | <span data-ttu-id="fb1ba-132">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fb1ba-132">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="fb1ba-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb1ba-133">Minimum supported server</span></span><br/> | <span data-ttu-id="fb1ba-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fb1ba-134">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="fb1ba-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fb1ba-135">Namespace</span></span><br/>                | <span data-ttu-id="fb1ba-136">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="fb1ba-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fb1ba-137">MOF</span><span class="sxs-lookup"><span data-stu-id="fb1ba-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb1ba-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb1ba-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb1ba-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fb1ba-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb1ba-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fb1ba-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fb1ba-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb1ba-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb1ba-142">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="fb1ba-142">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




