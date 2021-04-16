---
description: Recupera las estadísticas de replicación que están asociadas a la relación de replicación especificada de la máquina virtual.
ms.assetid: AB46894A-CBED-40DF-86B9-B578603B0341
title: 'Msvm_ReplicationService:: GetReplicationStatisticsEx (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatisticsEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7fdb60addc94094082fe83e70af06a2f5ae11f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686886"
---
# <a name="msvm_replicationservicegetreplicationstatisticsex-method"></a><span data-ttu-id="158e6-103">MSVM \_ ReplicationService:: GetReplicationStatisticsEx (método)</span><span class="sxs-lookup"><span data-stu-id="158e6-103">Msvm\_ReplicationService::GetReplicationStatisticsEx method</span></span>

<span data-ttu-id="158e6-104">Recupera las estadísticas de replicación que están asociadas a la relación de replicación especificada de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="158e6-104">Retrieves the replication statistics that are associated with the specified replication relationship of the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="158e6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="158e6-105">Syntax</span></span>


```C++
uint32 GetReplicationStatisticsEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="158e6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="158e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="158e6-107">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="158e6-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="158e6-108">Referencia a una instancia de un [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se van a recuperar las estadísticas de replicación.</span><span class="sxs-lookup"><span data-stu-id="158e6-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to retrieve the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="158e6-109">*ReplicationRelationship* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="158e6-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="158e6-110">Representación de cadena de una instancia incrustada de la clase [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) que define la relación de replicación para la que se van a recuperar las estadísticas de replicación.</span><span class="sxs-lookup"><span data-stu-id="158e6-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship for which to retrieve the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="158e6-111">*ReplicationStatistics* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="158e6-111">*ReplicationStatistics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="158e6-112">Si es correcto, recibe una instancia incrustada de la clase [**MSVM \_ ReplicationStatistics**](msvm-replicationstatistics.md) que contiene las estadísticas de replicación de la relación de replicación solicitada.</span><span class="sxs-lookup"><span data-stu-id="158e6-112">If successful, receives an embedded instance of the [**Msvm\_ReplicationStatistics**](msvm-replicationstatistics.md) class that contains the replication statistics for the requested replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="158e6-113">*ReplicationHealthIssues* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="158e6-113">*ReplicationHealthIssues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="158e6-114">Si se realiza correctamente, recibe una matriz de instancias incrustadas de la clase de [**\_ error MSVM**](msvm-error.md) que indican cualquier advertencia o error de replicación de la máquina virtual solicitada.</span><span class="sxs-lookup"><span data-stu-id="158e6-114">If successful, receives an array of embedded instances of the [**Msvm\_Error**](msvm-error.md) class that indicate any replication warnings or errors for the requested virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="158e6-115">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="158e6-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="158e6-116">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="158e6-116">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="158e6-117">Esta referencia puede ser **null** si la tarea se ha completado.</span><span class="sxs-lookup"><span data-stu-id="158e6-117">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="158e6-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="158e6-118">Return value</span></span>

<span data-ttu-id="158e6-119">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="158e6-119">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="158e6-120">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="158e6-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="158e6-121">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="158e6-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="158e6-122">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="158e6-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="158e6-123">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="158e6-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="158e6-124">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="158e6-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="158e6-125">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="158e6-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="158e6-126">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="158e6-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="158e6-127">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="158e6-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="158e6-128">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="158e6-128">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="158e6-129">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="158e6-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="158e6-130">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="158e6-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="158e6-131">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="158e6-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="158e6-132">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="158e6-132">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="158e6-133">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="158e6-133">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="158e6-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="158e6-134">Requirements</span></span>



| <span data-ttu-id="158e6-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="158e6-135">Requirement</span></span> | <span data-ttu-id="158e6-136">Value</span><span class="sxs-lookup"><span data-stu-id="158e6-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="158e6-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="158e6-137">Minimum supported client</span></span><br/> | <span data-ttu-id="158e6-138">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="158e6-138">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="158e6-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="158e6-139">Minimum supported server</span></span><br/> | <span data-ttu-id="158e6-140">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="158e6-140">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="158e6-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="158e6-141">Namespace</span></span><br/>                | <span data-ttu-id="158e6-142">\\\\\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="158e6-142">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="158e6-143">MOF</span><span class="sxs-lookup"><span data-stu-id="158e6-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="158e6-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="158e6-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="158e6-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="158e6-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="158e6-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="158e6-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="158e6-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="158e6-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="158e6-148">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="158e6-148">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="158e6-149">**ResetReplicationStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="158e6-149">**ResetReplicationStatisticsEx**</span></span>](resetreplicationstatisticsex-msvm-replicationservice.md)
</dt> </dl>

 

