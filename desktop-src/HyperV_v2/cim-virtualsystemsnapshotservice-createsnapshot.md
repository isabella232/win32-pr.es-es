---
description: Crea una instantánea de un sistema virtual.
ms.assetid: cad4cb4f-523f-4fda-ac88-8cece7abc227
title: Método CreateSnapshot de la clase CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ee96098477501123cffc1fd59a52734bbbea35d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668087"
---
# <a name="createsnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="8e134-103">Método CreateSnapshot de la \_ clase VirtualSystemSnapshotService de CIM</span><span class="sxs-lookup"><span data-stu-id="8e134-103">CreateSnapshot method of the CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="8e134-104">Crea una instantánea de un sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="8e134-104">Creates a snapshot of a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e134-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e134-105">Syntax</span></span>


```mof
uint32 CreateSnapshot(
  [in]      CIM_ComputerSystem           REF AffectedSystem,
  [in]      string                           SnapshotSettings,
  [in]      uint16                           SnapshotType,
  [in, out] CIM_VirtualSystemSettingData REF ResultingSnapshot,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8e134-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8e134-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e134-107">*AffectedSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e134-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e134-108">Una referencia de [**\_ ComputerSystem de CIM**](cim-computersystem.md) al sistema virtual afectado.</span><span class="sxs-lookup"><span data-stu-id="8e134-108">A [**CIM\_ComputerSystem**](cim-computersystem.md) reference to the affected virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="8e134-109">*SnapshotSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e134-109">*SnapshotSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e134-110">Configuración de parámetros.</span><span class="sxs-lookup"><span data-stu-id="8e134-110">Parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="8e134-111">*SnapshotType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e134-111">*SnapshotType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e134-112">Tipo de instantánea solicitada:</span><span class="sxs-lookup"><span data-stu-id="8e134-112">Requested snapshot type:</span></span>

<dt>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>

<span data-ttu-id="8e134-113"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Instantánea completa** (2)</span><span class="sxs-lookup"><span data-stu-id="8e134-113"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Full Snapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8e134-114">Instantánea completa del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="8e134-114">Complete snapshot of the virtual system.</span></span>

</dd> <dt>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>

<span data-ttu-id="8e134-115"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Instantánea de disco** (3)</span><span class="sxs-lookup"><span data-stu-id="8e134-115"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Disk Snapshot** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8e134-116">Instantánea de discos del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="8e134-116">Snapshot of virtual system disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="8e134-117"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="8e134-117"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="8e134-118"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="8e134-118"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="8e134-119">*ResultingSnapshot* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8e134-119">*ResultingSnapshot* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e134-120">Una [**referencia \_ VirtualSystemSettingData de CIM**](cim-virtualsystemsettingdata.md) a la instantánea del sistema virtual resultante.</span><span class="sxs-lookup"><span data-stu-id="8e134-120">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the resulting virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="8e134-121">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8e134-121">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e134-122">Si la operación es de larga ejecución, opcionalmente se puede devolver un trabajo.</span><span class="sxs-lookup"><span data-stu-id="8e134-122">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="8e134-123">En este caso, la instancia de la [**clase \_ VirtualSystemSettingData de CIM**](cim-virtualsystemsettingdata.md) que representa la nueva instantánea del sistema virtual se presenta a través de la Asociación [**\_ AffectedJobElement de CIM**](cim-affectedjobelement.md) con el valor de la propiedad **AffectedElement** que hace referencia a la nueva instancia de la clase **CIM \_ VirtualSystemSettingData** que representa la instantánea del sistema virtual y el valor de **ElementEffects** establecido en 5 (Create).</span><span class="sxs-lookup"><span data-stu-id="8e134-123">In this case, the instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing the new virtual system snapshot is presented via the [**CIM\_AffectedJobElement**](cim-affectedjobelement.md) association with the value of the **AffectedElement** property referring to the new instance of the **CIM\_VirtualSystemSettingData** class representing the virtual system snapshot and the value of the **ElementEffects** set to 5 (Create).</span></span>

> [!Note]  
> <span data-ttu-id="8e134-124">Este parámetro era de lectura/escritura en Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="8e134-124">This parameter was read/write in Windows 8.1.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e134-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e134-125">Return value</span></span>

<span data-ttu-id="8e134-126">Si se ejecuta correctamente, devuelve 0; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="8e134-126">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="8e134-127">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="8e134-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8e134-128">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="8e134-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8e134-129">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="8e134-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8e134-130">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="8e134-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8e134-131">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="8e134-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8e134-132">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="8e134-132">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8e134-133">**Tipo no válido** (6)</span><span class="sxs-lookup"><span data-stu-id="8e134-133">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8e134-134">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="8e134-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8e134-135">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="8e134-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8e134-136">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="8e134-136">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="8e134-137">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="8e134-137">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8e134-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e134-138">Requirements</span></span>



| <span data-ttu-id="8e134-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e134-139">Requirement</span></span> | <span data-ttu-id="8e134-140">Value</span><span class="sxs-lookup"><span data-stu-id="8e134-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e134-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e134-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8e134-142">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8e134-142">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="8e134-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e134-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8e134-144">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8e134-144">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="8e134-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8e134-145">Namespace</span></span><br/>                | <span data-ttu-id="8e134-146">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="8e134-146">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8e134-147">MOF</span><span class="sxs-lookup"><span data-stu-id="8e134-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e134-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e134-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e134-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8e134-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e134-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8e134-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8e134-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e134-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e134-152">**\_VIRTUALSYSTEMSNAPSHOTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="8e134-152">**CIM\_VirtualSystemSnapshotService**</span></span>](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




