---
description: Cambia la relación de replicación extendida a la relación principal de una máquina virtual de réplica. La máquina virtual de réplica debe estar en un estado de conmutación por error confirmada.
ms.assetid: B593A155-B5E6-44E5-8835-09DEB1FF868E
title: 'Msvm_ReplicationService:: ChangeReplicationModeToPrimary (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ChangeReplicationModeToPrimary
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0a18b3c9f1003ff7b263f5c6b7cc89abedccfd1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666341"
---
# <a name="msvm_replicationservicechangereplicationmodetoprimary-method"></a><span data-ttu-id="f47d1-104">MSVM \_ ReplicationService:: ChangeReplicationModeToPrimary (método)</span><span class="sxs-lookup"><span data-stu-id="f47d1-104">Msvm\_ReplicationService::ChangeReplicationModeToPrimary method</span></span>

<span data-ttu-id="f47d1-105">Cambia la relación de replicación extendida a la relación principal de una máquina virtual de réplica.</span><span class="sxs-lookup"><span data-stu-id="f47d1-105">Changes the extended replication relationship to the primary relationship for a replica virtual machine.</span></span> <span data-ttu-id="f47d1-106">La máquina virtual de réplica debe estar en un estado de conmutación por error confirmada.</span><span class="sxs-lookup"><span data-stu-id="f47d1-106">The replica virtual machine must be in a failover committed state.</span></span>

## <a name="syntax"></a><span data-ttu-id="f47d1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f47d1-107">Syntax</span></span>


```C++
uint32 ChangeReplicationModeToPrimary(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="f47d1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f47d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f47d1-109">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f47d1-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f47d1-110">Referencia a una instancia de un equipo de [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que este método cambia la relación de replicación extendida a la relación principal.</span><span class="sxs-lookup"><span data-stu-id="f47d1-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which this method changes the extended replication relationship to the primary relationship.</span></span>

</dd> <dt>

<span data-ttu-id="f47d1-111">*ReplicationRelationship* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f47d1-111">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f47d1-112">Representación de cadena de una instancia incrustada de la clase [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) que define la relación de replicación extendida que este método cambia a la relación principal.</span><span class="sxs-lookup"><span data-stu-id="f47d1-112">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the extended replication relationship that this method changes to the primary relationship.</span></span>

</dd> <dt>

<span data-ttu-id="f47d1-113">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f47d1-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f47d1-114">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f47d1-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="f47d1-115">Esta referencia puede ser **null** si la tarea se ha completado.</span><span class="sxs-lookup"><span data-stu-id="f47d1-115">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f47d1-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f47d1-116">Return value</span></span>

<span data-ttu-id="f47d1-117">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f47d1-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f47d1-118">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="f47d1-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f47d1-119">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="f47d1-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f47d1-120">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="f47d1-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f47d1-121">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="f47d1-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f47d1-122">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="f47d1-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f47d1-123">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="f47d1-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f47d1-124">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="f47d1-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f47d1-125">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="f47d1-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f47d1-126">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="f47d1-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f47d1-127">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="f47d1-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f47d1-128">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="f47d1-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f47d1-129">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="f47d1-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f47d1-130">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="f47d1-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="f47d1-131">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="f47d1-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f47d1-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f47d1-132">Requirements</span></span>



| <span data-ttu-id="f47d1-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f47d1-133">Requirement</span></span> | <span data-ttu-id="f47d1-134">Value</span><span class="sxs-lookup"><span data-stu-id="f47d1-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f47d1-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f47d1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f47d1-136">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="f47d1-136">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f47d1-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f47d1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f47d1-138">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f47d1-138">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f47d1-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f47d1-139">Namespace</span></span><br/>                | <span data-ttu-id="f47d1-140">\\\\\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f47d1-140">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="f47d1-141">MOF</span><span class="sxs-lookup"><span data-stu-id="f47d1-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f47d1-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f47d1-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f47d1-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f47d1-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f47d1-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f47d1-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f47d1-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="f47d1-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f47d1-146">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="f47d1-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

