---
description: Inicia la replicación de una máquina virtual.
ms.assetid: 58e89329-1ad4-4473-856d-ebfd7a863fa8
title: Método StartReplication de la clase Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.StartReplication
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4702b5b73a989e2889bf1da9e4d284afdfe5e916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360231"
---
# <a name="startreplication-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="a2937-103">Método StartReplication de la \_ clase ReplicationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="a2937-103">StartReplication method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="a2937-104">Inicia la replicación de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a2937-104">Starts the replication of a virtual machine.</span></span> <span data-ttu-id="a2937-105">Cuando un cliente llama a este método para una máquina virtual de réplica, inicia la replicación con réplica extendida.</span><span class="sxs-lookup"><span data-stu-id="a2937-105">When a client calls this method for a replica virtual machine, it starts the replication with extended replica.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2937-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2937-106">Syntax</span></span>


```mof
uint32 StartReplication(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  uint16                 InitialReplicationType,
  [in]  string                 InitialReplicationExportLocation,
  [in]  datetime               StartTime,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a2937-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a2937-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2937-108">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a2937-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2937-109">Referencia a una instancia de un [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se debe iniciar la replicación.</span><span class="sxs-lookup"><span data-stu-id="a2937-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be started.</span></span>

</dd> <dt>

<span data-ttu-id="a2937-110">*InitialReplicationType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a2937-110">*InitialReplicationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2937-111">Tipo de transferencia que se va a usar para realizar la replicación inicial.</span><span class="sxs-lookup"><span data-stu-id="a2937-111">The type of transfer to be used for performing the initial replication.</span></span>

<dt>

<span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>

<span data-ttu-id="a2937-112"><span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>**Transferencia de red** (1)</span><span class="sxs-lookup"><span data-stu-id="a2937-112"><span id="Network_Transfer"></span><span id="network_transfer"></span><span id="NETWORK_TRANSFER"></span>**Network Transfer** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a2937-113">Transferencia de red.</span><span class="sxs-lookup"><span data-stu-id="a2937-113">Network transfer.</span></span>

</dd> <dt>

<span id="Export"></span><span id="export"></span><span id="EXPORT"></span>

<span data-ttu-id="a2937-114"><span id="Export"></span><span id="export"></span><span id="EXPORT"></span>**Exportar** (2)</span><span class="sxs-lookup"><span data-stu-id="a2937-114"><span id="Export"></span><span id="export"></span><span id="EXPORT"></span>**Export** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a2937-115">Exportación.</span><span class="sxs-lookup"><span data-stu-id="a2937-115">Export.</span></span>

</dd> <dt>

<span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>

<span data-ttu-id="a2937-116"><span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>**Transferencia de red inicial** (3)</span><span class="sxs-lookup"><span data-stu-id="a2937-116"><span id="Seeded_Network_Transfer"></span><span id="seeded_network_transfer"></span><span id="SEEDED_NETWORK_TRANSFER"></span>**Seeded Network Transfer** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a2937-117">Transferencia de red inicializada.</span><span class="sxs-lookup"><span data-stu-id="a2937-117">Seeded network transfer.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a2937-118">*InitialReplicationExportLocation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a2937-118">*InitialReplicationExportLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2937-119">Si *InitialReplicationType* es 2 (Export), este parámetro contiene la ruta de acceso completa del directorio en el que se va a exportar la replicación inicial.</span><span class="sxs-lookup"><span data-stu-id="a2937-119">If *InitialReplicationType* is 2 (Export), this parameter contains the fully qualified path of the directory to which the initial replication is to be exported.</span></span> <span data-ttu-id="a2937-120">Este parámetro no se utiliza para otros valores de *InitialReplicationType* y puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="a2937-120">This parameter is not used for other values of *InitialReplicationType*, and can be **Null**.</span></span> <span data-ttu-id="a2937-121">Este directorio se puede reutilizar para exportar varias replicaciones de máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="a2937-121">This directory can be reused for exporting multiple virtual machine replication.</span></span> <span data-ttu-id="a2937-122">Este método coloca cada replicación de máquina virtual en un subdirectorio independiente en esta ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="a2937-122">This method places each virtual machine replication in a separate subdirectory under this path.</span></span>

</dd> <dt>

<span data-ttu-id="a2937-123">*StartTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a2937-123">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2937-124">La hora de inicio programada para la replicación inicial a través de la conexión de red con el servidor de recuperación.</span><span class="sxs-lookup"><span data-stu-id="a2937-124">The scheduled start time for the initial replication over the network connection to recovery server.</span></span> <span data-ttu-id="a2937-125">Este parámetro se omite cuando *InitialReplicationType* es 2 (Export).</span><span class="sxs-lookup"><span data-stu-id="a2937-125">This parameter is ignored when *InitialReplicationType* is 2 (Export).</span></span> <span data-ttu-id="a2937-126">Si este parámetro es **null**, la replicación inicial se inicia inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="a2937-126">If this parameter is **Null**, the initial replication starts immediately.</span></span>

</dd> <dt>

<span data-ttu-id="a2937-127">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a2937-127">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2937-128">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a2937-128">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2937-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2937-129">Return value</span></span>

<span data-ttu-id="a2937-130">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="a2937-130">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a2937-131">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="a2937-131">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a2937-132">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="a2937-132">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a2937-133">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="a2937-133">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a2937-134">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="a2937-134">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a2937-135">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="a2937-135">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a2937-136">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="a2937-136">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a2937-137">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="a2937-137">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a2937-138">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="a2937-138">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a2937-139">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="a2937-139">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a2937-140">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="a2937-140">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a2937-141">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="a2937-141">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a2937-142">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="a2937-142">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a2937-143">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="a2937-143">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="a2937-144">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="a2937-144">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a2937-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2937-145">Requirements</span></span>



| <span data-ttu-id="a2937-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2937-146">Requirement</span></span> | <span data-ttu-id="a2937-147">Value</span><span class="sxs-lookup"><span data-stu-id="a2937-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2937-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2937-148">Minimum supported client</span></span><br/> | <span data-ttu-id="a2937-149">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="a2937-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a2937-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2937-150">Minimum supported server</span></span><br/> | <span data-ttu-id="a2937-151">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="a2937-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a2937-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a2937-152">Namespace</span></span><br/>                | <span data-ttu-id="a2937-153">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="a2937-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a2937-154">MOF</span><span class="sxs-lookup"><span data-stu-id="a2937-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2937-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2937-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2937-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a2937-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2937-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a2937-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a2937-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2937-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2937-159">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="a2937-159">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

