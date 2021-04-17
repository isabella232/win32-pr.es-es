---
description: Crea una nueva relación de replicación para una máquina virtual. Cuando un cliente llama a este método para una máquina virtual de réplica, extiende la relación de replicación al proveedor especificado.
ms.assetid: 44d3b5aa-46c2-4fe9-9a1d-6ee699d3640d
title: Método CreateReplicationRelationship de la clase Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.CreateReplicationRelationship
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c44628aef9aa278170a1292a74621419bb6256b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667831"
---
# <a name="createreplicationrelationship-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="b15f2-104">Método CreateReplicationRelationship de la \_ clase ReplicationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="b15f2-104">CreateReplicationRelationship method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="b15f2-105">Crea una nueva relación de replicación para una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b15f2-105">Creates a new replication relationship for a virtual machine.</span></span> <span data-ttu-id="b15f2-106">Cuando un cliente llama a este método para una máquina virtual de réplica, extiende la relación de replicación al proveedor especificado.</span><span class="sxs-lookup"><span data-stu-id="b15f2-106">When a client calls this method for a replica virtual machine, it extends the replication relationship to the specified provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="b15f2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b15f2-107">Syntax</span></span>


```mof
uint32 CreateReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b15f2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b15f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b15f2-109">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b15f2-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b15f2-110">Referencia a una instancia de un [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se debe habilitar la replicación.</span><span class="sxs-lookup"><span data-stu-id="b15f2-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be enabled.</span></span>

</dd> <dt>

<span data-ttu-id="b15f2-111">*ReplicationSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b15f2-111">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b15f2-112">Representación de cadena de una instancia de la clase [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) que define la configuración de replicación de la nueva relación de replicación que se va a crear para la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b15f2-112">A string representation of an instance of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the replication settings for the new replication relationship to be created for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="b15f2-113">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b15f2-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b15f2-114">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b15f2-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b15f2-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b15f2-115">Return value</span></span>

<span data-ttu-id="b15f2-116">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="b15f2-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b15f2-117">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="b15f2-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b15f2-118">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="b15f2-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b15f2-119">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="b15f2-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b15f2-120">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="b15f2-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b15f2-121">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="b15f2-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b15f2-122">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="b15f2-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b15f2-123">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="b15f2-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b15f2-124">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="b15f2-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b15f2-125">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="b15f2-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b15f2-126">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="b15f2-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b15f2-127">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="b15f2-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b15f2-128">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="b15f2-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b15f2-129">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="b15f2-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="b15f2-130">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="b15f2-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="b15f2-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b15f2-131">Remarks</span></span>

<span data-ttu-id="b15f2-132">**CreateReplicationRelationship** toma una instancia de [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) (FRSD) como entrada.</span><span class="sxs-lookup"><span data-stu-id="b15f2-132">**CreateReplicationRelationship** takes an [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) instance (FRSD) as input.</span></span> <span data-ttu-id="b15f2-133">La FRSD asociada a la máquina virtual como proveedor de host a host es la opción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b15f2-133">The associated FRSD for the virtual machine as host-to-host provider is the default choice.</span></span> <span data-ttu-id="b15f2-134">La FRSD de entrada se valida para la configuración válida de cada propiedad del proveedor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b15f2-134">Input FRSD is validated for valid settings for each property for the default provider.</span></span> <span data-ttu-id="b15f2-135">En esta tabla se resumen las diferencias de validación con respecto al proveedor externo.</span><span class="sxs-lookup"><span data-stu-id="b15f2-135">This table summarizes the validation differences with respect to the external provider.</span></span>



| <span data-ttu-id="b15f2-136">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b15f2-136">Property</span></span>                                             | <span data-ttu-id="b15f2-137">Proveedores externos</span><span class="sxs-lookup"><span data-stu-id="b15f2-137">External providers</span></span>                                 |
|------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="b15f2-138">ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="b15f2-138">ReplicationProvider</span></span>                                  | <span data-ttu-id="b15f2-139">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b15f2-139">Same as default provider</span></span>                           |
| <span data-ttu-id="b15f2-140">AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="b15f2-140">AuthenticationType</span></span>                                   | <span data-ttu-id="b15f2-141">Omitido</span><span class="sxs-lookup"><span data-stu-id="b15f2-141">Ignored</span></span>                                            |
| <span data-ttu-id="b15f2-142">CertificateThumbPrint</span><span class="sxs-lookup"><span data-stu-id="b15f2-142">CertificateThumbPrint</span></span>                                | <span data-ttu-id="b15f2-143">Omitido</span><span class="sxs-lookup"><span data-stu-id="b15f2-143">Ignored</span></span>                                            |
| <span data-ttu-id="b15f2-144">RootCertificateThumbPrint (RO)</span><span class="sxs-lookup"><span data-stu-id="b15f2-144">RootCertificateThumbPrint (RO)</span></span>                       | <span data-ttu-id="b15f2-145">Omitido</span><span class="sxs-lookup"><span data-stu-id="b15f2-145">Ignored</span></span>                                            |
| <span data-ttu-id="b15f2-146">CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="b15f2-146">CompressionEnabled</span></span>                                   | <span data-ttu-id="b15f2-147">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b15f2-147">Same as default provider</span></span>                           |
| <span data-ttu-id="b15f2-148">BypassProxyServer</span><span class="sxs-lookup"><span data-stu-id="b15f2-148">BypassProxyServer</span></span>                                    | <span data-ttu-id="b15f2-149">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b15f2-149">Same as default provider</span></span>                           |
| <span data-ttu-id="b15f2-150">RecoveryConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="b15f2-150">RecoveryConnectionPoint</span></span>                              | <span data-ttu-id="b15f2-151">\*Se omite (puede cambiar si el proveedor tiene requisitos)</span><span class="sxs-lookup"><span data-stu-id="b15f2-151">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="b15f2-152">RecoveryHostSystem (RO)</span><span class="sxs-lookup"><span data-stu-id="b15f2-152">RecoveryHostSystem (RO)</span></span>                              | <span data-ttu-id="b15f2-153">Omitido</span><span class="sxs-lookup"><span data-stu-id="b15f2-153">Ignored</span></span>                                            |
| <span data-ttu-id="b15f2-154">PrimaryConnectionPoint (RO)</span><span class="sxs-lookup"><span data-stu-id="b15f2-154">PrimaryConnectionPoint (RO)</span></span>                          | <span data-ttu-id="b15f2-155">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b15f2-155">Same as default provider</span></span>                           |
| <span data-ttu-id="b15f2-156">PrimaryHostSystem (RO)</span><span class="sxs-lookup"><span data-stu-id="b15f2-156">PrimaryHostSystem (RO)</span></span>                               | <span data-ttu-id="b15f2-157">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b15f2-157">Same as default provider</span></span>                           |
| <span data-ttu-id="b15f2-158">RecoveryServerPortNumber</span><span class="sxs-lookup"><span data-stu-id="b15f2-158">RecoveryServerPortNumber</span></span>                             | <span data-ttu-id="b15f2-159">\*Se omite (puede cambiar si el proveedor tiene requisitos)</span><span class="sxs-lookup"><span data-stu-id="b15f2-159">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="b15f2-160">ReplicateHostKvpItems</span><span class="sxs-lookup"><span data-stu-id="b15f2-160">ReplicateHostKvpItems</span></span>                                | <span data-ttu-id="b15f2-161">Omitido</span><span class="sxs-lookup"><span data-stu-id="b15f2-161">Ignored</span></span>                                            |
| <span data-ttu-id="b15f2-162">ApplicationConsistentSnapshotInterval</span><span class="sxs-lookup"><span data-stu-id="b15f2-162">ApplicationConsistentSnapshotInterval</span></span>                | <span data-ttu-id="b15f2-163">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b15f2-163">Same as default provider</span></span>                           |
| <span data-ttu-id="b15f2-164">RecoveryHistory</span><span class="sxs-lookup"><span data-stu-id="b15f2-164">RecoveryHistory</span></span>                                      | <span data-ttu-id="b15f2-165">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b15f2-165">Same as default provider</span></span>                           |
| <span data-ttu-id="b15f2-166">IncludedDisks\[\]</span><span class="sxs-lookup"><span data-stu-id="b15f2-166">IncludedDisks\[\]</span></span>                                    | <span data-ttu-id="b15f2-167">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b15f2-167">Same as default provider</span></span>                           |
| <span data-ttu-id="b15f2-168">AutoResynchronizeEnabled</span><span class="sxs-lookup"><span data-stu-id="b15f2-168">AutoResynchronizeEnabled</span></span>                             | <span data-ttu-id="b15f2-169">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b15f2-169">Same as default provider</span></span>                           |
| <span data-ttu-id="b15f2-170">AutoResynchronizeIntervalStart</span><span class="sxs-lookup"><span data-stu-id="b15f2-170">AutoResynchronizeIntervalStart</span></span>                       | <span data-ttu-id="b15f2-171">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b15f2-171">Same as default provider</span></span>                           |
| <span data-ttu-id="b15f2-172">AutoResynchronizeIntervalEnd</span><span class="sxs-lookup"><span data-stu-id="b15f2-172">AutoResynchronizeIntervalEnd</span></span>                         | <span data-ttu-id="b15f2-173">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b15f2-173">Same as default provider</span></span>                           |
| <span data-ttu-id="b15f2-174">EnableWriteOrderPreservationAcrossDisks (desusado)</span><span class="sxs-lookup"><span data-stu-id="b15f2-174">EnableWriteOrderPreservationAcrossDisks (Deprecated)</span></span> | <span data-ttu-id="b15f2-175">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b15f2-175">Same as default provider</span></span>                           |
| <span data-ttu-id="b15f2-176">ReplicationInterval</span><span class="sxs-lookup"><span data-stu-id="b15f2-176">ReplicationInterval</span></span>                                  | <span data-ttu-id="b15f2-177">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="b15f2-177">Same as default provider</span></span>                           |



 

## <a name="requirements"></a><span data-ttu-id="b15f2-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b15f2-178">Requirements</span></span>



| <span data-ttu-id="b15f2-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="b15f2-179">Requirement</span></span> | <span data-ttu-id="b15f2-180">Value</span><span class="sxs-lookup"><span data-stu-id="b15f2-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b15f2-181">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b15f2-181">Minimum supported client</span></span><br/> | <span data-ttu-id="b15f2-182">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="b15f2-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b15f2-183">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b15f2-183">Minimum supported server</span></span><br/> | <span data-ttu-id="b15f2-184">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="b15f2-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b15f2-185">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b15f2-185">Namespace</span></span><br/>                | <span data-ttu-id="b15f2-186">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b15f2-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b15f2-187">MOF</span><span class="sxs-lookup"><span data-stu-id="b15f2-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b15f2-188"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b15f2-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b15f2-189">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b15f2-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b15f2-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b15f2-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b15f2-191">Vea también</span><span class="sxs-lookup"><span data-stu-id="b15f2-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b15f2-192">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="b15f2-192">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="b15f2-193">**RemoveReplicationRelationshipEx**</span><span class="sxs-lookup"><span data-stu-id="b15f2-193">**RemoveReplicationRelationshipEx**</span></span>](removereplicationrelationshipex-msvm-replicationservice.md)
</dt> </dl>

 

