---
description: Realiza una operación de resincronización en la máquina virtual especificada.
ms.assetid: a3d06780-f43b-45c4-a186-a3544f9c7963
title: Método resynchronize de la clase Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.Resynchronize
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: dcd4865d110843de27f0a242b31253310439e1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360870"
---
# <a name="resynchronize-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="fba8b-103">Método resynchronize de la \_ clase MSVM ReplicationService</span><span class="sxs-lookup"><span data-stu-id="fba8b-103">Resynchronize method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="fba8b-104">Realiza una operación de resincronización en la máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="fba8b-104">Performs a resynchronization operation on the specified virtual machine.</span></span> <span data-ttu-id="fba8b-105">Cuando un cliente llama a este método para una máquina virtual de réplica, se vuelve a sincronizar con la réplica extendida.</span><span class="sxs-lookup"><span data-stu-id="fba8b-105">When a client calls this method for a replica virtual machine, it resynchronizes with extended replica.</span></span>

<span data-ttu-id="fba8b-106">Estos métodos comparan los discos habilitados para la replicación en las máquinas virtuales principal y de recuperación, y corrige los problemas de integridad de los datos de replicación mediante la replicación de los diferentes bloques del servidor principal al de la recuperación.</span><span class="sxs-lookup"><span data-stu-id="fba8b-106">This methods compares the replication enabled disks on the primary and recovery virtual machines, and fixes any replication data integrity issues by replicating the different blocks from the primary to the recovery.</span></span>

## <a name="syntax"></a><span data-ttu-id="fba8b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fba8b-107">Syntax</span></span>


```mof
uint32 Resynchronize(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  datetime               StartTime,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="fba8b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fba8b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fba8b-109">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fba8b-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba8b-110">Referencia a una instancia de un [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual que se va a volver a sincronizar.</span><span class="sxs-lookup"><span data-stu-id="fba8b-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine to be resynchronized.</span></span>

</dd> <dt>

<span data-ttu-id="fba8b-111">*StartTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fba8b-111">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba8b-112">La hora de inicio programada para que se inicie la operación de resincronización.</span><span class="sxs-lookup"><span data-stu-id="fba8b-112">The scheduled start time for the resynchronization operation to begin.</span></span> <span data-ttu-id="fba8b-113">Si este parámetro es **null**, la operación de resincronización se inicia inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="fba8b-113">If this parameter is **Null**, the resynchronization operation starts immediately.</span></span>

</dd> <dt>

<span data-ttu-id="fba8b-114">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fba8b-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fba8b-115">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fba8b-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fba8b-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fba8b-116">Return value</span></span>

<span data-ttu-id="fba8b-117">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="fba8b-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="fba8b-118">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="fba8b-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fba8b-119">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="fba8b-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fba8b-120">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="fba8b-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="fba8b-121">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="fba8b-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="fba8b-122">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="fba8b-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="fba8b-123">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="fba8b-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="fba8b-124">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="fba8b-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="fba8b-125">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="fba8b-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="fba8b-126">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="fba8b-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="fba8b-127">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="fba8b-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="fba8b-128">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="fba8b-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="fba8b-129">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="fba8b-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="fba8b-130">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="fba8b-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="fba8b-131">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="fba8b-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fba8b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fba8b-132">Requirements</span></span>



| <span data-ttu-id="fba8b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="fba8b-133">Requirement</span></span> | <span data-ttu-id="fba8b-134">Value</span><span class="sxs-lookup"><span data-stu-id="fba8b-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fba8b-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fba8b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fba8b-136">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="fba8b-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fba8b-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fba8b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fba8b-138">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="fba8b-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fba8b-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fba8b-139">Namespace</span></span><br/>                | <span data-ttu-id="fba8b-140">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="fba8b-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fba8b-141">MOF</span><span class="sxs-lookup"><span data-stu-id="fba8b-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fba8b-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fba8b-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fba8b-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fba8b-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fba8b-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fba8b-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fba8b-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="fba8b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fba8b-146">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="fba8b-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

