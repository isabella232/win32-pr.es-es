---
description: Revierte la conmutación por error actual para una máquina virtual descartando el disco de conmutación por error actual.
ms.assetid: 99d3a3d3-49e4-4410-b979-47b62ebc6aa6
title: Método RevertFailover de la clase Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RevertFailover
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: db20abf34fdad2e0eba499fd1b4cc390bf93b754
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669939"
---
# <a name="revertfailover-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="3b63b-103">Método RevertFailover de la \_ clase ReplicationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="3b63b-103">RevertFailover method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="3b63b-104">Revierte la conmutación por error actual para una máquina virtual descartando el disco de conmutación por error actual.</span><span class="sxs-lookup"><span data-stu-id="3b63b-104">Reverts the current failover for a virtual machine by discarding the current failover disk.</span></span> <span data-ttu-id="3b63b-105">Después de esta operación, se puede volver a llamar a [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3b63b-105">After this operation, [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) can be called again.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b63b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b63b-106">Syntax</span></span>


```mof
uint32 RevertFailover(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3b63b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b63b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b63b-108">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3b63b-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b63b-109">Referencia a una instancia de un [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se va a revertir la conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="3b63b-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to revert the failover.</span></span>

</dd> <dt>

<span data-ttu-id="3b63b-110">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3b63b-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b63b-111">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3b63b-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b63b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b63b-112">Return value</span></span>

<span data-ttu-id="3b63b-113">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3b63b-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3b63b-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="3b63b-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3b63b-115">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="3b63b-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3b63b-116">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="3b63b-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3b63b-117">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="3b63b-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3b63b-118">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="3b63b-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3b63b-119">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="3b63b-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3b63b-120">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="3b63b-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3b63b-121">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="3b63b-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3b63b-122">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="3b63b-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3b63b-123">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="3b63b-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3b63b-124">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="3b63b-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3b63b-125">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="3b63b-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3b63b-126">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="3b63b-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="3b63b-127">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="3b63b-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3b63b-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b63b-128">Requirements</span></span>



| <span data-ttu-id="3b63b-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b63b-129">Requirement</span></span> | <span data-ttu-id="3b63b-130">Value</span><span class="sxs-lookup"><span data-stu-id="3b63b-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b63b-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b63b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3b63b-132">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b63b-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3b63b-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b63b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3b63b-134">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b63b-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3b63b-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3b63b-135">Namespace</span></span><br/>                | <span data-ttu-id="3b63b-136">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="3b63b-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3b63b-137">MOF</span><span class="sxs-lookup"><span data-stu-id="3b63b-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b63b-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b63b-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b63b-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3b63b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b63b-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3b63b-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3b63b-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b63b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b63b-142">**InitiateFailover**</span><span class="sxs-lookup"><span data-stu-id="3b63b-142">**InitiateFailover**</span></span>](initiatefailover-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="3b63b-143">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="3b63b-143">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="3b63b-144">**SetFailoverNetworkAdapterSettings**</span><span class="sxs-lookup"><span data-stu-id="3b63b-144">**SetFailoverNetworkAdapterSettings**</span></span>](setfailovernetworkadaptersettings-msvm-replicationservice.md)
</dt> </dl>

 

