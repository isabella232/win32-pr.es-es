---
description: Confirma la instantánea de recuperación que el método InitiateFailover ha usado para una conmutación por error.
ms.assetid: 05c27211-adc7-400a-83e2-81792ae7577f
title: Método CommitFailover de la clase Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.CommitFailover
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 04687ea29f39645c2407de44faf6bba6ecc75832
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687708"
---
# <a name="commitfailover-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="f102f-103">Método CommitFailover de la \_ clase ReplicationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="f102f-103">CommitFailover method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="f102f-104">Confirma la instantánea de recuperación que el método [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) ha usado para una conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="f102f-104">Commits the recovery snapshot that the [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) method has used for a failover.</span></span>

<span data-ttu-id="f102f-105">Este método simplifica los puntos de recuperación en la máquina virtual de recuperación aplicando la instantánea de recuperación.</span><span class="sxs-lookup"><span data-stu-id="f102f-105">This method flattens the recovery points on the recovery virtual machine by applying the recovery snapshot.</span></span> <span data-ttu-id="f102f-106">Una vez hecho esto, no se puede cancelar la operación de conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="f102f-106">After this is done, the failover operation cannot be canceled.</span></span> <span data-ttu-id="f102f-107">Normalmente, los usuarios realizarán esta ejecución cuando el punto de replicación utilizado para la conmutación por error sea satisfactorio y la máquina virtual de recuperación pueda cambiar el rol para que sea principal.</span><span class="sxs-lookup"><span data-stu-id="f102f-107">Users will typically perform this when the replication point used for failover is satisfactory and the recovery virtual machine can change role to be primary.</span></span>

## <a name="syntax"></a><span data-ttu-id="f102f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f102f-108">Syntax</span></span>


```mof
uint32 CommitFailover(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f102f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f102f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f102f-110">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f102f-110">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f102f-111">Referencia a una instancia de un [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se va a confirmar la conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="f102f-111">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to commit the failover.</span></span>

</dd> <dt>

<span data-ttu-id="f102f-112">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f102f-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f102f-113">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f102f-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f102f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f102f-114">Return value</span></span>

<span data-ttu-id="f102f-115">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f102f-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f102f-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="f102f-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f102f-117">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="f102f-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f102f-118">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="f102f-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f102f-119">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="f102f-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f102f-120">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="f102f-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f102f-121">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="f102f-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f102f-122">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="f102f-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f102f-123">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="f102f-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f102f-124">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="f102f-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f102f-125">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="f102f-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f102f-126">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="f102f-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f102f-127">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="f102f-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f102f-128">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="f102f-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="f102f-129">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="f102f-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f102f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f102f-130">Requirements</span></span>



| <span data-ttu-id="f102f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f102f-131">Requirement</span></span> | <span data-ttu-id="f102f-132">Value</span><span class="sxs-lookup"><span data-stu-id="f102f-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f102f-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f102f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f102f-134">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="f102f-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f102f-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f102f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f102f-136">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="f102f-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f102f-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f102f-137">Namespace</span></span><br/>                | <span data-ttu-id="f102f-138">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f102f-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f102f-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f102f-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f102f-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f102f-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f102f-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f102f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f102f-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f102f-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f102f-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="f102f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f102f-144">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="f102f-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

