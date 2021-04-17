---
description: Recupera las estadísticas de replicación de una máquina virtual y actúa en la relación de replicación principal de la máquina virtual.
ms.assetid: 24f3f572-fa85-4680-be77-7e835e6471c5
title: Método GetReplicationStatistics de la clase Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetReplicationStatistics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9dff711830ccdb805c362961671dff28f5bf0b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666550"
---
# <a name="getreplicationstatistics-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="415ef-103">Método GetReplicationStatistics de la \_ clase ReplicationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="415ef-103">GetReplicationStatistics method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="415ef-104">Recupera las estadísticas de replicación de una máquina virtual y actúa en la relación de replicación principal de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="415ef-104">Retrieves replication statistics for a virtual machine and acts on the primary replication relationship of the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="415ef-105">A partir de Windows 8.1, se recomienda no usar **GetReplicationStatistics** para recuperar las estadísticas de replicación.</span><span class="sxs-lookup"><span data-stu-id="415ef-105">Starting with Windows 8.1, we recommend not to use **GetReplicationStatistics** anymore to retrieve replication statistics.</span></span> <span data-ttu-id="415ef-106">En su lugar, use [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md).</span><span class="sxs-lookup"><span data-stu-id="415ef-106">Instead, use [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="415ef-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="415ef-107">Syntax</span></span>


```mof
uint32 GetReplicationStatistics(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 ReplicationStatistics[],
  [out] string                 ReplicationHealthIssues[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="415ef-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="415ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="415ef-109">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="415ef-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="415ef-110">Referencia a una instancia de un [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se van a recuperar las estadísticas de replicación.</span><span class="sxs-lookup"><span data-stu-id="415ef-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to retrieve the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="415ef-111">*ReplicationStatistics* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="415ef-111">*ReplicationStatistics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="415ef-112">Si se realiza correctamente, recibe una instancia incrustada de la clase [**MSVM \_ ReplicationStatistics**](msvm-replicationstatistics.md) que contiene las estadísticas de replicación de la máquina virtual solicitada.</span><span class="sxs-lookup"><span data-stu-id="415ef-112">If successful, receives an embedded instance of the [**Msvm\_ReplicationStatistics**](msvm-replicationstatistics.md) class that contains the replication statistics for the requested virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="415ef-113">*ReplicationHealthIssues* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="415ef-113">*ReplicationHealthIssues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="415ef-114">Si se realiza correctamente, recibe una matriz de instancias incrustadas de la clase de [**\_ error MSVM**](msvm-error.md) que indican cualquier advertencia o error de replicación de la máquina virtual solicitada.</span><span class="sxs-lookup"><span data-stu-id="415ef-114">If successful, receives an array of embedded instances of the [**Msvm\_Error**](msvm-error.md) class that indicate any replication warnings or errors for the requested virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="415ef-115">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="415ef-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="415ef-116">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="415ef-116">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="415ef-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="415ef-117">Return value</span></span>

<span data-ttu-id="415ef-118">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="415ef-118">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="415ef-119">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="415ef-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="415ef-120">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="415ef-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="415ef-121">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="415ef-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="415ef-122">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="415ef-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="415ef-123">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="415ef-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="415ef-124">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="415ef-124">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="415ef-125">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="415ef-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="415ef-126">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="415ef-126">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="415ef-127">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="415ef-127">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="415ef-128">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="415ef-128">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="415ef-129">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="415ef-129">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="415ef-130">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="415ef-130">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="415ef-131">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="415ef-131">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="415ef-132">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="415ef-132">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="415ef-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="415ef-133">Requirements</span></span>



| <span data-ttu-id="415ef-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="415ef-134">Requirement</span></span> | <span data-ttu-id="415ef-135">Value</span><span class="sxs-lookup"><span data-stu-id="415ef-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="415ef-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="415ef-136">Minimum supported client</span></span><br/> | <span data-ttu-id="415ef-137">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="415ef-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="415ef-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="415ef-138">Minimum supported server</span></span><br/> | <span data-ttu-id="415ef-139">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="415ef-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="415ef-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="415ef-140">Namespace</span></span><br/>                | <span data-ttu-id="415ef-141">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="415ef-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="415ef-142">MOF</span><span class="sxs-lookup"><span data-stu-id="415ef-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="415ef-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="415ef-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="415ef-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="415ef-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="415ef-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="415ef-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="415ef-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="415ef-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="415ef-147">**ResetReplicationStatistics**</span><span class="sxs-lookup"><span data-stu-id="415ef-147">**ResetReplicationStatistics**</span></span>](resetreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="415ef-148">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="415ef-148">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

