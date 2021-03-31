---
description: Quita una relación de replicación de máquina virtual y actúa en la relación de replicación principal de la máquina virtual.
ms.assetid: a9a20aa1-378d-4a2a-9ebc-9786ab2dfda7
title: Método RemoveReplicationRelationship de la clase Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RemoveReplicationRelationship
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bb897ff72cd927390362f076114fc8757baa6c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908131"
---
# <a name="removereplicationrelationship-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="337d5-103">Método RemoveReplicationRelationship de la \_ clase ReplicationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="337d5-103">RemoveReplicationRelationship method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="337d5-104">Quita una relación de replicación de máquina virtual y actúa en la relación de replicación principal de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="337d5-104">Removes a virtual machine replication relationship and acts on the primary replication relationship of the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="337d5-105">A partir de Windows 8.1, se recomienda no usar **RemoveReplicationRelationship** para quitar una relación de replicación de máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="337d5-105">Starting with Windows 8.1, we recommend not to use **RemoveReplicationRelationship** anymore to remove a virtual machine replication relationship.</span></span> <span data-ttu-id="337d5-106">En su lugar, use [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md).</span><span class="sxs-lookup"><span data-stu-id="337d5-106">Instead, use [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="337d5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="337d5-107">Syntax</span></span>


```mof
uint32 RemoveReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="337d5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="337d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="337d5-109">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="337d5-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="337d5-110">Referencia a una instancia de un [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se debe quitar la relación de replicación.</span><span class="sxs-lookup"><span data-stu-id="337d5-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication relationship should be removed.</span></span>

</dd> <dt>

<span data-ttu-id="337d5-111">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="337d5-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="337d5-112">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="337d5-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="337d5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="337d5-113">Return value</span></span>

<span data-ttu-id="337d5-114">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="337d5-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="337d5-115">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="337d5-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="337d5-116">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="337d5-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="337d5-117">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="337d5-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="337d5-118">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="337d5-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="337d5-119">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="337d5-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="337d5-120">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="337d5-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="337d5-121">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="337d5-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="337d5-122">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="337d5-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="337d5-123">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="337d5-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="337d5-124">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="337d5-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="337d5-125">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="337d5-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="337d5-126">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="337d5-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="337d5-127">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="337d5-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="337d5-128">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="337d5-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="337d5-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="337d5-129">Requirements</span></span>



| <span data-ttu-id="337d5-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="337d5-130">Requirement</span></span> | <span data-ttu-id="337d5-131">Value</span><span class="sxs-lookup"><span data-stu-id="337d5-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="337d5-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="337d5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="337d5-133">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="337d5-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="337d5-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="337d5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="337d5-135">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="337d5-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="337d5-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="337d5-136">Namespace</span></span><br/>                | <span data-ttu-id="337d5-137">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="337d5-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="337d5-138">MOF</span><span class="sxs-lookup"><span data-stu-id="337d5-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="337d5-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="337d5-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="337d5-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="337d5-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="337d5-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="337d5-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="337d5-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="337d5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="337d5-143">**CreateReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="337d5-143">**CreateReplicationRelationship**</span></span>](createreplicationrelationship-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="337d5-144">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="337d5-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

