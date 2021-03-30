---
description: Restablece las estadísticas de replicación que están asociadas a la relación de replicación especificada de la máquina virtual especificada.
ms.assetid: 6E49A7C0-2F60-444E-964E-420470EE1538
title: 'Msvm_ReplicationService:: ResetReplicationStatisticsEx (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ResetReplicationStatisticsEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c1acb234660e71636b4a69a697b11385d65cf1ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911002"
---
# <a name="msvm_replicationserviceresetreplicationstatisticsex-method"></a><span data-ttu-id="74b28-103">MSVM \_ ReplicationService:: ResetReplicationStatisticsEx (método)</span><span class="sxs-lookup"><span data-stu-id="74b28-103">Msvm\_ReplicationService::ResetReplicationStatisticsEx method</span></span>

<span data-ttu-id="74b28-104">Restablece las estadísticas de replicación que están asociadas a la relación de replicación especificada de la máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="74b28-104">Resets replication statistics that are associated with the specified replication relationship of the specified virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="74b28-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74b28-105">Syntax</span></span>


```C++
uint32 ResetReplicationStatisticsEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="74b28-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74b28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74b28-107">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74b28-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74b28-108">Referencia a una instancia de un [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual habilitada para réplicas.</span><span class="sxs-lookup"><span data-stu-id="74b28-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the replica-enabled virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="74b28-109">*ReplicationRelationship* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74b28-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74b28-110">Representación de cadena de una instancia incrustada de la clase [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) que define la relación de replicación para la que se restablecen las estadísticas de replicación.</span><span class="sxs-lookup"><span data-stu-id="74b28-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship for which to reset the replication statistics.</span></span>

</dd> <dt>

<span data-ttu-id="74b28-111">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="74b28-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74b28-112">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="74b28-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="74b28-113">Esta referencia puede ser **null** si la tarea se ha completado.</span><span class="sxs-lookup"><span data-stu-id="74b28-113">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74b28-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74b28-114">Return value</span></span>

<span data-ttu-id="74b28-115">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="74b28-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="74b28-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="74b28-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="74b28-117">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="74b28-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="74b28-118">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="74b28-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="74b28-119">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="74b28-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="74b28-120">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="74b28-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="74b28-121">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="74b28-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="74b28-122">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="74b28-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="74b28-123">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="74b28-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="74b28-124">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="74b28-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="74b28-125">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="74b28-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="74b28-126">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="74b28-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="74b28-127">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="74b28-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="74b28-128">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="74b28-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="74b28-129">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="74b28-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="74b28-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74b28-130">Requirements</span></span>



| <span data-ttu-id="74b28-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="74b28-131">Requirement</span></span> | <span data-ttu-id="74b28-132">Value</span><span class="sxs-lookup"><span data-stu-id="74b28-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74b28-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74b28-133">Minimum supported client</span></span><br/> | <span data-ttu-id="74b28-134">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="74b28-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="74b28-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74b28-135">Minimum supported server</span></span><br/> | <span data-ttu-id="74b28-136">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="74b28-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="74b28-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="74b28-137">Namespace</span></span><br/>                | <span data-ttu-id="74b28-138">\\\\\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="74b28-138">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="74b28-139">MOF</span><span class="sxs-lookup"><span data-stu-id="74b28-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74b28-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74b28-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="74b28-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="74b28-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74b28-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="74b28-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="74b28-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="74b28-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74b28-144">**GetReplicationStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="74b28-144">**GetReplicationStatisticsEx**</span></span>](getreplicationstatisticsex-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="74b28-145">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="74b28-145">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

