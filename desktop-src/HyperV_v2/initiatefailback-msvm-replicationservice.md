---
description: Inicia la conmutación por recuperación para una máquina virtual de recuperación.
ms.assetid: F4AE1911-46B2-4412-A17F-3CA7D388276F
title: 'Msvm_ReplicationService:: InitiateFailback (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.InitiateFailback
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b356982296427212287ea11b528a7878dc166245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666813"
---
# <a name="msvm_replicationserviceinitiatefailback-method"></a><span data-ttu-id="3fc6a-103">MSVM \_ ReplicationService:: InitiateFailback (método)</span><span class="sxs-lookup"><span data-stu-id="3fc6a-103">Msvm\_ReplicationService::InitiateFailback method</span></span>

<span data-ttu-id="3fc6a-104">Inicia la conmutación por recuperación para una máquina virtual de recuperación.</span><span class="sxs-lookup"><span data-stu-id="3fc6a-104">Initiates the failback for a recovery virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fc6a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3fc6a-105">Syntax</span></span>


```C++
uint32 InitiateFailback(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [in]  string                 RecoveryPointIdentifier,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="3fc6a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3fc6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fc6a-107">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3fc6a-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fc6a-108">Referencia a una instancia de un equipo [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual para la que se va a iniciar una conmutación por recuperación.</span><span class="sxs-lookup"><span data-stu-id="3fc6a-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to initiate a failback.</span></span>

</dd> <dt>

<span data-ttu-id="3fc6a-109">*ReplicationSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3fc6a-109">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fc6a-110">Representación de cadena de una instancia incrustada de la clase [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) que define la configuración de replicación para la conmutación por recuperación.</span><span class="sxs-lookup"><span data-stu-id="3fc6a-110">A string representation of an embedded instance of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the replication settings for the failback.</span></span>

</dd> <dt>

<span data-ttu-id="3fc6a-111">*RecoveryPointIdentifier* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3fc6a-111">*RecoveryPointIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fc6a-112">Entrada opcional que identifica el punto de recuperación en el que se solicita la conmutación por recuperación.</span><span class="sxs-lookup"><span data-stu-id="3fc6a-112">Optional input that identifies the recovery point to which failback is requested.</span></span>

</dd> <dt>

<span data-ttu-id="3fc6a-113">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3fc6a-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3fc6a-114">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3fc6a-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="3fc6a-115">Esta referencia se puede usar para supervisar el progreso y obtener el resultado del método.</span><span class="sxs-lookup"><span data-stu-id="3fc6a-115">This reference can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fc6a-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3fc6a-116">Return value</span></span>

<span data-ttu-id="3fc6a-117">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3fc6a-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3fc6a-118">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="3fc6a-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3fc6a-119">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="3fc6a-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3fc6a-120">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="3fc6a-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3fc6a-121">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="3fc6a-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3fc6a-122">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="3fc6a-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3fc6a-123">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="3fc6a-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3fc6a-124">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="3fc6a-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3fc6a-125">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="3fc6a-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3fc6a-126">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="3fc6a-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3fc6a-127">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="3fc6a-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3fc6a-128">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="3fc6a-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3fc6a-129">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="3fc6a-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3fc6a-130">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="3fc6a-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="3fc6a-131">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="3fc6a-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="3fc6a-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3fc6a-132">Remarks</span></span>

<span data-ttu-id="3fc6a-133">**InitiateFailback** funciona en una máquina virtual de recuperación y toma el estado *WaitingForFailback* de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3fc6a-133">**InitiateFailback** works on a recovery virtual machine and takes the virtual machine to *WaitingForFailback* state.</span></span> <span data-ttu-id="3fc6a-134">**InitiateFailback** reenvía la solicitud de conmutación por recuperación al proveedor correspondiente, que resincroniza de nuevo el punto de recuperación del lado principal nuevo.</span><span class="sxs-lookup"><span data-stu-id="3fc6a-134">**InitiateFailback** forwards the failback request to the corresponding provider, which reverse-resyncs the recovery point from new-primary side.</span></span> <span data-ttu-id="3fc6a-135">Una vez finalizada la conmutación por recuperación del punto de recuperación solicitado, el estado de replicación se mueve al estado *FailbackCompleted* .</span><span class="sxs-lookup"><span data-stu-id="3fc6a-135">After failback of the requested recovery point completes, the replication state moves to *FailbackCompleted* state.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fc6a-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fc6a-136">Requirements</span></span>



| <span data-ttu-id="3fc6a-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fc6a-137">Requirement</span></span> | <span data-ttu-id="3fc6a-138">Value</span><span class="sxs-lookup"><span data-stu-id="3fc6a-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fc6a-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3fc6a-139">Minimum supported client</span></span><br/> | <span data-ttu-id="3fc6a-140">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="3fc6a-140">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="3fc6a-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3fc6a-141">Minimum supported server</span></span><br/> | <span data-ttu-id="3fc6a-142">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3fc6a-142">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3fc6a-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3fc6a-143">Namespace</span></span><br/>                | <span data-ttu-id="3fc6a-144">\\\\\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="3fc6a-144">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="3fc6a-145">MOF</span><span class="sxs-lookup"><span data-stu-id="3fc6a-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3fc6a-146"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3fc6a-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3fc6a-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3fc6a-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fc6a-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3fc6a-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3fc6a-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="3fc6a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fc6a-150">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="3fc6a-150">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

