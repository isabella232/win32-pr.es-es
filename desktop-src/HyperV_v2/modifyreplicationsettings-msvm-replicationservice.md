---
description: Modifica la configuración de replicación de una máquina virtual. Cuando un cliente llama a este método para una máquina virtual de réplica, modifica la configuración de replicación de la relación de replicación con la réplica extendida.
ms.assetid: e68514a5-f508-4047-8dcc-6a95f3e3353e
title: Método ModifyReplicationSettings de la clase Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyReplicationSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d1c932f06350324e0d84559724f7ba0412dfb3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688062"
---
# <a name="modifyreplicationsettings-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="aacef-104">Método ModifyReplicationSettings de la \_ clase ReplicationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="aacef-104">ModifyReplicationSettings method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="aacef-105">Modifica la configuración de replicación de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="aacef-105">Modifies the replication settings for a virtual machine.</span></span> <span data-ttu-id="aacef-106">Cuando un cliente llama a este método para una máquina virtual de réplica, modifica la configuración de replicación de la relación de replicación con la réplica extendida.</span><span class="sxs-lookup"><span data-stu-id="aacef-106">When a client calls this method for a replica virtual machine, it modifies the replication settings of the replication relationship with the extended replica.</span></span>

## <a name="syntax"></a><span data-ttu-id="aacef-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aacef-107">Syntax</span></span>


```mof
uint32 ModifyReplicationSettings(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="aacef-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aacef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aacef-109">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aacef-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aacef-110">Referencia a una instancia de un [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se debe modificar la configuración de replicación.</span><span class="sxs-lookup"><span data-stu-id="aacef-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication settings should be modified.</span></span>

</dd> <dt>

<span data-ttu-id="aacef-111">*ReplicationSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aacef-111">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aacef-112">Representación de cadena de la clase [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) que define la nueva configuración de replicación.</span><span class="sxs-lookup"><span data-stu-id="aacef-112">A string representation of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the new replication settings.</span></span>

</dd> <dt>

<span data-ttu-id="aacef-113">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="aacef-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aacef-114">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="aacef-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aacef-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aacef-115">Return value</span></span>

<span data-ttu-id="aacef-116">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="aacef-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="aacef-117">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="aacef-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="aacef-118">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="aacef-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="aacef-119">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="aacef-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="aacef-120">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="aacef-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="aacef-121">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="aacef-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="aacef-122">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="aacef-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="aacef-123">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="aacef-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="aacef-124">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="aacef-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="aacef-125">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="aacef-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="aacef-126">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="aacef-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="aacef-127">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="aacef-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="aacef-128">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="aacef-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="aacef-129">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="aacef-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="aacef-130">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="aacef-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="aacef-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aacef-131">Remarks</span></span>

<span data-ttu-id="aacef-132">**ModifyReplicationSettings** toma una instancia de [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) (FRSD) como entrada.</span><span class="sxs-lookup"><span data-stu-id="aacef-132">**ModifyReplicationSettings** takes an [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) instance (FRSD) as input.</span></span> <span data-ttu-id="aacef-133">La FRSD asociada a la máquina virtual como proveedor de host a host es la opción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="aacef-133">The associated FRSD for the virtual machine as host-to-host provider is the default choice.</span></span> <span data-ttu-id="aacef-134">La FRSD de entrada se valida para la configuración válida de cada propiedad del proveedor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="aacef-134">Input FRSD is validated for valid settings for each property for the default provider.</span></span> <span data-ttu-id="aacef-135">En esta tabla se resumen las diferencias de validación con respecto al proveedor externo.</span><span class="sxs-lookup"><span data-stu-id="aacef-135">This table summarizes the validation differences with respect to the external provider.</span></span>



| <span data-ttu-id="aacef-136">Propiedad</span><span class="sxs-lookup"><span data-stu-id="aacef-136">Property</span></span>                                             | <span data-ttu-id="aacef-137">Proveedores externos</span><span class="sxs-lookup"><span data-stu-id="aacef-137">External providers</span></span>                                 |
|------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="aacef-138">ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="aacef-138">ReplicationProvider</span></span>                                  | <span data-ttu-id="aacef-139">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aacef-139">Same as default provider</span></span>                           |
| <span data-ttu-id="aacef-140">AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="aacef-140">AuthenticationType</span></span>                                   | <span data-ttu-id="aacef-141">Omitido</span><span class="sxs-lookup"><span data-stu-id="aacef-141">Ignored</span></span>                                            |
| <span data-ttu-id="aacef-142">CertificateThumbPrint</span><span class="sxs-lookup"><span data-stu-id="aacef-142">CertificateThumbPrint</span></span>                                | <span data-ttu-id="aacef-143">Omitido</span><span class="sxs-lookup"><span data-stu-id="aacef-143">Ignored</span></span>                                            |
| <span data-ttu-id="aacef-144">RootCertificateThumbPrint (RO)</span><span class="sxs-lookup"><span data-stu-id="aacef-144">RootCertificateThumbPrint (RO)</span></span>                       | <span data-ttu-id="aacef-145">Omitido</span><span class="sxs-lookup"><span data-stu-id="aacef-145">Ignored</span></span>                                            |
| <span data-ttu-id="aacef-146">CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="aacef-146">CompressionEnabled</span></span>                                   | <span data-ttu-id="aacef-147">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aacef-147">Same as default provider</span></span>                           |
| <span data-ttu-id="aacef-148">BypassProxyServer</span><span class="sxs-lookup"><span data-stu-id="aacef-148">BypassProxyServer</span></span>                                    | <span data-ttu-id="aacef-149">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aacef-149">Same as default provider</span></span>                           |
| <span data-ttu-id="aacef-150">RecoveryConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="aacef-150">RecoveryConnectionPoint</span></span>                              | <span data-ttu-id="aacef-151">\*Se omite (puede cambiar si el proveedor tiene requisitos)</span><span class="sxs-lookup"><span data-stu-id="aacef-151">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="aacef-152">RecoveryHostSystem (RO)</span><span class="sxs-lookup"><span data-stu-id="aacef-152">RecoveryHostSystem (RO)</span></span>                              | <span data-ttu-id="aacef-153">Omitido</span><span class="sxs-lookup"><span data-stu-id="aacef-153">Ignored</span></span>                                            |
| <span data-ttu-id="aacef-154">PrimaryConnectionPoint (RO)</span><span class="sxs-lookup"><span data-stu-id="aacef-154">PrimaryConnectionPoint (RO)</span></span>                          | <span data-ttu-id="aacef-155">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aacef-155">Same as default provider</span></span>                           |
| <span data-ttu-id="aacef-156">PrimaryHostSystem (RO)</span><span class="sxs-lookup"><span data-stu-id="aacef-156">PrimaryHostSystem (RO)</span></span>                               | <span data-ttu-id="aacef-157">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aacef-157">Same as default provider</span></span>                           |
| <span data-ttu-id="aacef-158">RecoveryServerPortNumber</span><span class="sxs-lookup"><span data-stu-id="aacef-158">RecoveryServerPortNumber</span></span>                             | <span data-ttu-id="aacef-159">\*Se omite (puede cambiar si el proveedor tiene requisitos)</span><span class="sxs-lookup"><span data-stu-id="aacef-159">Ignored\* (may change if provider has requirement)</span></span> |
| <span data-ttu-id="aacef-160">ReplicateHostKvpItems</span><span class="sxs-lookup"><span data-stu-id="aacef-160">ReplicateHostKvpItems</span></span>                                | <span data-ttu-id="aacef-161">Omitido</span><span class="sxs-lookup"><span data-stu-id="aacef-161">Ignored</span></span>                                            |
| <span data-ttu-id="aacef-162">ApplicationConsistentSnapshotInterval</span><span class="sxs-lookup"><span data-stu-id="aacef-162">ApplicationConsistentSnapshotInterval</span></span>                | <span data-ttu-id="aacef-163">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aacef-163">Same as default provider</span></span>                           |
| <span data-ttu-id="aacef-164">RecoveryHistory</span><span class="sxs-lookup"><span data-stu-id="aacef-164">RecoveryHistory</span></span>                                      | <span data-ttu-id="aacef-165">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aacef-165">Same as default provider</span></span>                           |
| <span data-ttu-id="aacef-166">IncludedDisks\[\]</span><span class="sxs-lookup"><span data-stu-id="aacef-166">IncludedDisks\[\]</span></span>                                    | <span data-ttu-id="aacef-167">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aacef-167">Same as default provider</span></span>                           |
| <span data-ttu-id="aacef-168">AutoResynchronizeEnabled</span><span class="sxs-lookup"><span data-stu-id="aacef-168">AutoResynchronizeEnabled</span></span>                             | <span data-ttu-id="aacef-169">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aacef-169">Same as default provider</span></span>                           |
| <span data-ttu-id="aacef-170">AutoResynchronizeIntervalStart</span><span class="sxs-lookup"><span data-stu-id="aacef-170">AutoResynchronizeIntervalStart</span></span>                       | <span data-ttu-id="aacef-171">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aacef-171">Same as default provider</span></span>                           |
| <span data-ttu-id="aacef-172">AutoResynchronizeIntervalEnd</span><span class="sxs-lookup"><span data-stu-id="aacef-172">AutoResynchronizeIntervalEnd</span></span>                         | <span data-ttu-id="aacef-173">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aacef-173">Same as default provider</span></span>                           |
| <span data-ttu-id="aacef-174">EnableWriteOrderPreservationAcrossDisks (desusado)</span><span class="sxs-lookup"><span data-stu-id="aacef-174">EnableWriteOrderPreservationAcrossDisks (Deprecated)</span></span> | <span data-ttu-id="aacef-175">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aacef-175">Same as default provider</span></span>                           |
| <span data-ttu-id="aacef-176">ReplicationInterval</span><span class="sxs-lookup"><span data-stu-id="aacef-176">ReplicationInterval</span></span>                                  | <span data-ttu-id="aacef-177">Igual que el proveedor predeterminado</span><span class="sxs-lookup"><span data-stu-id="aacef-177">Same as default provider</span></span>                           |



 

## <a name="requirements"></a><span data-ttu-id="aacef-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aacef-178">Requirements</span></span>



| <span data-ttu-id="aacef-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="aacef-179">Requirement</span></span> | <span data-ttu-id="aacef-180">Value</span><span class="sxs-lookup"><span data-stu-id="aacef-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aacef-181">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aacef-181">Minimum supported client</span></span><br/> | <span data-ttu-id="aacef-182">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="aacef-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="aacef-183">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aacef-183">Minimum supported server</span></span><br/> | <span data-ttu-id="aacef-184">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="aacef-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aacef-185">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="aacef-185">Namespace</span></span><br/>                | <span data-ttu-id="aacef-186">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="aacef-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="aacef-187">MOF</span><span class="sxs-lookup"><span data-stu-id="aacef-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aacef-188"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aacef-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="aacef-189">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aacef-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aacef-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="aacef-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="aacef-191">Vea también</span><span class="sxs-lookup"><span data-stu-id="aacef-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aacef-192">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="aacef-192">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

