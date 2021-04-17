---
description: Quita la relación de replicación de la máquina virtual especificada.
ms.assetid: 0D5013CE-7BAE-4A99-ABF2-F1ECC644A1B2
title: 'Msvm_ReplicationService:: RemoveReplicationRelationshipEx (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RemoveReplicationRelationshipEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c57ed7f9a88789d04a20de0fd199d460b47c1eb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666602"
---
# <a name="msvm_replicationserviceremovereplicationrelationshipex-method"></a><span data-ttu-id="99435-103">MSVM \_ ReplicationService:: RemoveReplicationRelationshipEx (método)</span><span class="sxs-lookup"><span data-stu-id="99435-103">Msvm\_ReplicationService::RemoveReplicationRelationshipEx method</span></span>

<span data-ttu-id="99435-104">Quita la relación de replicación de la máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="99435-104">Removes the specified virtual machine replication relationship.</span></span>

## <a name="syntax"></a><span data-ttu-id="99435-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99435-105">Syntax</span></span>


```C++
uint32 RemoveReplicationRelationshipEx(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="99435-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99435-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99435-107">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99435-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99435-108">Referencia a una instancia de un [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se va a quitar la replicación.</span><span class="sxs-lookup"><span data-stu-id="99435-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to remove the replication.</span></span>

</dd> <dt>

<span data-ttu-id="99435-109">*ReplicationRelationship* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99435-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99435-110">Representación de cadena de una instancia incrustada de la clase [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) que define la relación de replicación que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="99435-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship to remove.</span></span>

</dd> <dt>

<span data-ttu-id="99435-111">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="99435-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99435-112">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="99435-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="99435-113">Esta referencia puede ser **null** si la tarea se ha completado.</span><span class="sxs-lookup"><span data-stu-id="99435-113">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99435-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99435-114">Return value</span></span>

<span data-ttu-id="99435-115">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="99435-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="99435-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="99435-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="99435-117">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="99435-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="99435-118">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="99435-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="99435-119">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="99435-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="99435-120">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="99435-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="99435-121">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="99435-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="99435-122">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="99435-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="99435-123">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="99435-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="99435-124">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="99435-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="99435-125">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="99435-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="99435-126">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="99435-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="99435-127">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="99435-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="99435-128">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="99435-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="99435-129">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="99435-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="99435-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99435-130">Remarks</span></span>

<span data-ttu-id="99435-131">En el caso de una máquina virtual de réplica, no se puede quitar la replicación principal si está habilitada la replicación extendida.</span><span class="sxs-lookup"><span data-stu-id="99435-131">For a replica virtual machine, primary replication can't be removed if extended replication is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="99435-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99435-132">Requirements</span></span>



| <span data-ttu-id="99435-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="99435-133">Requirement</span></span> | <span data-ttu-id="99435-134">Value</span><span class="sxs-lookup"><span data-stu-id="99435-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99435-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99435-135">Minimum supported client</span></span><br/> | <span data-ttu-id="99435-136">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="99435-136">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="99435-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99435-137">Minimum supported server</span></span><br/> | <span data-ttu-id="99435-138">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="99435-138">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="99435-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="99435-139">Namespace</span></span><br/>                | <span data-ttu-id="99435-140">\\\\\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="99435-140">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="99435-141">MOF</span><span class="sxs-lookup"><span data-stu-id="99435-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99435-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="99435-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="99435-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="99435-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99435-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="99435-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="99435-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="99435-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99435-146">**CreateReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="99435-146">**CreateReplicationRelationship**</span></span>](createreplicationrelationship-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="99435-147">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="99435-147">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

