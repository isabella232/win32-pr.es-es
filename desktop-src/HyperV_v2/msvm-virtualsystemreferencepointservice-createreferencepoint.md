---
description: Crea un punto de referencia de un sistema virtual.
ms.assetid: 9cc7665a-9562-4267-bcd0-3162e426fbad
title: Método CreateReferencePoint de la clase Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.CreateReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 08d28970288ba62346894d758ebac5ac156962ff
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105670070"
---
# <a name="createreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="8f1ba-103">Método CreateReferencePoint de la \_ clase VirtualSystemReferencePointService de MSVM</span><span class="sxs-lookup"><span data-stu-id="8f1ba-103">CreateReferencePoint method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="8f1ba-104">Crea un punto de referencia de un sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="8f1ba-104">Creates a reference point of a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f1ba-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f1ba-105">Syntax</span></span>


```mof
uint32 CreateReferencePoint(
  [in]      Msvm_ComputerSystem              REF AffectedSystem,
  [in]      string                               ReferencePointSettings,
  [in]      uint16                               ReferencePointType,
  [in, out] Msvm_VirtualSystemReferencePoint REF ResultingReferencePoint,
  [out]     CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8f1ba-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f1ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f1ba-107">*AffectedSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8f1ba-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f1ba-108">Un [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que hace referencia al sistema virtual afectado.</span><span class="sxs-lookup"><span data-stu-id="8f1ba-108">A [**Msvm\_ComputerSystem**](msvm-computersystem.md) that references the affected virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="8f1ba-109">*ReferencePointSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8f1ba-109">*ReferencePointSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f1ba-110">Contiene la configuración del parámetro.</span><span class="sxs-lookup"><span data-stu-id="8f1ba-110">Contains the parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="8f1ba-111">*ReferencePointType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8f1ba-111">*ReferencePointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f1ba-112">Tipo de punto de referencia solicitado:</span><span class="sxs-lookup"><span data-stu-id="8f1ba-112">Requested reference point type:</span></span>

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="8f1ba-113"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Basado en el registro** (0)</span><span class="sxs-lookup"><span data-stu-id="8f1ba-113"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f1ba-114">Basado en el seguimiento del registro de réplica de Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="8f1ba-114">Based on Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="8f1ba-115"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT basado** (1)</span><span class="sxs-lookup"><span data-stu-id="8f1ba-115"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f1ba-116">Basado en Change Tracking resistente de los discos virtuales.</span><span class="sxs-lookup"><span data-stu-id="8f1ba-116">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8f1ba-117">*ResultingReferencePoint* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8f1ba-117">*ResultingReferencePoint* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f1ba-118">Punto de referencia del sistema virtual resultante</span><span class="sxs-lookup"><span data-stu-id="8f1ba-118">Resulting virtual system reference point</span></span>

</dd> <dt>

<span data-ttu-id="8f1ba-119">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8f1ba-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f1ba-120">Si la operación es de larga ejecución, opcionalmente se puede devolver un trabajo.</span><span class="sxs-lookup"><span data-stu-id="8f1ba-120">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="8f1ba-121">En este caso, la instancia de la [**clase \_ MSVM VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) que representa el nuevo punto de referencia del sistema virtual se presenta a través de la Asociación [**\_ AffectedJobElement CIM**](cim-affectedjobelement.md) con el valor de la propiedad **AffectedElement** que hace referencia a la nueva instancia de la clase **MSVM \_ VirtualSystemReferencePoint** que representa el punto de referencia del sistema virtual y el valor de **ElementEffects** establecido en 5 (Create).</span><span class="sxs-lookup"><span data-stu-id="8f1ba-121">In this case, the instance of the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) class representing the new virtual system reference point is presented via the [**CIM\_AffectedJobElement**](cim-affectedjobelement.md) association with the value of the **AffectedElement** property referring to the new instance of the **Msvm\_VirtualSystemReferencePoint** class representing the virtual system reference point and the value of the **ElementEffects** set to 5 (Create).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f1ba-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f1ba-122">Return value</span></span>

<span data-ttu-id="8f1ba-123">Si se ejecuta correctamente, devuelve 0; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="8f1ba-123">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="8f1ba-124">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="8f1ba-124">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8f1ba-125">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="8f1ba-125">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8f1ba-126">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="8f1ba-126">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8f1ba-127">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="8f1ba-127">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8f1ba-128">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="8f1ba-128">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8f1ba-129">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="8f1ba-129">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8f1ba-130">**Tipo no válido** (6)</span><span class="sxs-lookup"><span data-stu-id="8f1ba-130">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8f1ba-131">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="8f1ba-131">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8f1ba-132">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="8f1ba-132">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8f1ba-133">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="8f1ba-133">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="8f1ba-134">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="8f1ba-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8f1ba-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f1ba-135">Requirements</span></span>



| <span data-ttu-id="8f1ba-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f1ba-136">Requirement</span></span> | <span data-ttu-id="8f1ba-137">Value</span><span class="sxs-lookup"><span data-stu-id="8f1ba-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f1ba-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f1ba-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8f1ba-139">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f1ba-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="8f1ba-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f1ba-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8f1ba-141">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8f1ba-141">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="8f1ba-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8f1ba-142">Namespace</span></span><br/>                | <span data-ttu-id="8f1ba-143">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="8f1ba-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8f1ba-144">MOF</span><span class="sxs-lookup"><span data-stu-id="8f1ba-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f1ba-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f1ba-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f1ba-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8f1ba-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f1ba-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8f1ba-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8f1ba-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f1ba-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f1ba-149">**MSVM \_ VirtualSystemReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="8f1ba-149">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




