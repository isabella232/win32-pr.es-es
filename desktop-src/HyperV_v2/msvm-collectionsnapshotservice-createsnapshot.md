---
description: Crea una instantánea de una colección de sistemas virtuales.
ms.assetid: 2512d82f-06b9-4613-b920-d3a9be884a75
title: Método CreateSnapshot de la clase Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 653dae65cc5fe50416b069da6a66e8c678c1b512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812517"
---
# <a name="createsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="fc2cc-103">Método CreateSnapshot de la \_ clase CollectionSnapshotService de MSVM</span><span class="sxs-lookup"><span data-stu-id="fc2cc-103">CreateSnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="fc2cc-104">Crea una instantánea de una colección de sistemas virtuales.</span><span class="sxs-lookup"><span data-stu-id="fc2cc-104">Creates a snapshot of a virtual system collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc2cc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc2cc-105">Syntax</span></span>


```mof
uint32 CreateSnapshot(
  [in]      CIM_CollectionOfMSEs REF Collection,
  [in]      string                   SnapshotSettings,
  [in]      uint16                   SnapshotType,
  [in, out] CIM_Collection       REF ResultingSnapshotCollection,
  [out]     CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="fc2cc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc2cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc2cc-107">*Colección* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="fc2cc-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc2cc-108">Referencia a un [**\_ CollectionOfMSEs de CIM**](cim-collectionofmses.md) que describe la colección de sistemas virtuales afectada.</span><span class="sxs-lookup"><span data-stu-id="fc2cc-108">Reference to a [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) that describes the affected virtual system collection.</span></span>

</dd> <dt>

<span data-ttu-id="fc2cc-109">*SnapshotSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fc2cc-109">*SnapshotSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc2cc-110">Contiene la configuración del parámetro.</span><span class="sxs-lookup"><span data-stu-id="fc2cc-110">Contains the parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="fc2cc-111">*SnapshotType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fc2cc-111">*SnapshotType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc2cc-112">Tipo de instantánea solicitada:</span><span class="sxs-lookup"><span data-stu-id="fc2cc-112">Requested snapshot type:</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fc2cc-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="fc2cc-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>

<span data-ttu-id="fc2cc-114"><span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>**Instantánea estándar** (1)</span><span class="sxs-lookup"><span data-stu-id="fc2cc-114"><span id="Standard_Snapshot"></span><span id="standard_snapshot"></span><span id="STANDARD_SNAPSHOT"></span>**Standard Snapshot** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fc2cc-115">Instantánea estándar del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="fc2cc-115">Standard snapshot of the virtual system.</span></span>

</dd> <dt>

<span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>

<span data-ttu-id="fc2cc-116"><span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>**Instantánea de recuperación** (2)</span><span class="sxs-lookup"><span data-stu-id="fc2cc-116"><span id="Recovery_Snapshot"></span><span id="recovery_snapshot"></span><span id="RECOVERY_SNAPSHOT"></span>**Recovery Snapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fc2cc-117">Instantánea para escenarios de recuperación, incluida la replicación de conmutación por error y la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="fc2cc-117">Snapshot for recovery scenarios including failover replication and backup.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="fc2cc-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="fc2cc-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="fc2cc-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="fc2cc-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="fc2cc-120">*ResultingSnapshotCollection* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fc2cc-120">*ResultingSnapshotCollection* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc2cc-121">Si se ejecuta correctamente, devuelve una referencia de [**\_ colección CIM**](cim-collection.md) que contiene la instantánea del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="fc2cc-121">On success, returns a [**CIM\_Collection**](cim-collection.md) reference containing the virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="fc2cc-122">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fc2cc-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc2cc-123">Referencia opcional que se devuelve si la operación se ejecuta de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="fc2cc-123">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="fc2cc-124">Si está presente, la referencia devuelta a una instancia de [**CIM \_ ConcreteJob**](cim-concretejob.md) se puede usar para supervisar el progreso y obtener el resultado del método.</span><span class="sxs-lookup"><span data-stu-id="fc2cc-124">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc2cc-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc2cc-125">Return value</span></span>

<span data-ttu-id="fc2cc-126">Si se ejecuta correctamente, devuelve 0 (completado) o 4096 (trabajo iniciado); de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="fc2cc-126">On success, returns either 0 (Complete) or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="fc2cc-127">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="fc2cc-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fc2cc-128">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="fc2cc-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fc2cc-129">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="fc2cc-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fc2cc-130">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="fc2cc-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fc2cc-131">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="fc2cc-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fc2cc-132">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="fc2cc-132">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fc2cc-133">**Tipo no válido** (6)</span><span class="sxs-lookup"><span data-stu-id="fc2cc-133">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="fc2cc-134">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="fc2cc-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fc2cc-135">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="fc2cc-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fc2cc-136">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="fc2cc-136">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="fc2cc-137">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="fc2cc-137">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fc2cc-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc2cc-138">Requirements</span></span>



| <span data-ttu-id="fc2cc-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc2cc-139">Requirement</span></span> | <span data-ttu-id="fc2cc-140">Value</span><span class="sxs-lookup"><span data-stu-id="fc2cc-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc2cc-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc2cc-141">Minimum supported client</span></span><br/> | <span data-ttu-id="fc2cc-142">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="fc2cc-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="fc2cc-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc2cc-143">Minimum supported server</span></span><br/> | <span data-ttu-id="fc2cc-144">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fc2cc-144">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="fc2cc-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fc2cc-145">Namespace</span></span><br/>                | <span data-ttu-id="fc2cc-146">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="fc2cc-146">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fc2cc-147">MOF</span><span class="sxs-lookup"><span data-stu-id="fc2cc-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc2cc-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc2cc-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc2cc-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fc2cc-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc2cc-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fc2cc-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fc2cc-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc2cc-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc2cc-152">**MSVM \_ CollectionSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="fc2cc-152">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




