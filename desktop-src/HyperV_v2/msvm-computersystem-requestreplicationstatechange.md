---
description: Solicita que el estado de replicación de la máquina virtual se cambie al valor especificado y actúe en la relación de replicación principal de la máquina virtual.
ms.assetid: 65FCDADD-1C50-4816-B10B-A951D1FC9C3B
title: Método RequestReplicationStateChange de la clase Msvm_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestReplicationStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 32f0136662f043627a5fad152ee0e0aaa1845e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544734"
---
# <a name="requestreplicationstatechange-method-of-the-msvm_computersystem-class"></a><span data-ttu-id="f876c-103">Método RequestReplicationStateChange de la \_ clase MSVM ComputerSystem</span><span class="sxs-lookup"><span data-stu-id="f876c-103">RequestReplicationStateChange method of the Msvm\_ComputerSystem class</span></span>

<span data-ttu-id="f876c-104">Solicita que el estado de replicación de la máquina virtual se cambie al valor especificado y actúe en la relación de replicación principal de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f876c-104">Requests that the replication state of the virtual machine be changed to the specified value and acts on the primary replication relationship of the virtual machine.</span></span> <span data-ttu-id="f876c-105">Mientras el cambio de estado está en curso, la propiedad **ReplicationState** se cambia al valor del parámetro *RequestedState* .</span><span class="sxs-lookup"><span data-stu-id="f876c-105">While the state change is in progress, the **ReplicationState** property is changed to the value of the *RequestedState* parameter.</span></span> <span data-ttu-id="f876c-106">Este método solo se admite para las instancias de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representan una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f876c-106">This method is only supported for instances of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represent a virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="f876c-107">A partir de Windows 8.1, se recomienda no usar **RequestReplicationStateChange** ya para solicitar el cambio de estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="f876c-107">Starting with Windows 8.1, we recommend not to use **RequestReplicationStateChange** anymore to request changing of replication state.</span></span> <span data-ttu-id="f876c-108">En su lugar, use [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md).</span><span class="sxs-lookup"><span data-stu-id="f876c-108">Instead, use [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f876c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f876c-109">Syntax</span></span>


```mof
uint32 RequestReplicationStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="f876c-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f876c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f876c-111">*RequestedState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f876c-111">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f876c-112">Nuevo estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="f876c-112">The new replication state.</span></span> <span data-ttu-id="f876c-113">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f876c-113">The must be one of the following values.</span></span>

<dt>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>

<span data-ttu-id="f876c-114"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Listo para iniciar la replicación inicial** (1)</span><span class="sxs-lookup"><span data-stu-id="f876c-114"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Ready to start initial replication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f876c-115">Listo para iniciar la replicación inicial.</span><span class="sxs-lookup"><span data-stu-id="f876c-115">Ready to start initial replication.</span></span>

</dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="f876c-116"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Esperando para completar la replicación inicial** (2)</span><span class="sxs-lookup"><span data-stu-id="f876c-116"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f876c-117">Esperando para completar la replicación inicial.</span><span class="sxs-lookup"><span data-stu-id="f876c-117">Waiting to complete initial replication.</span></span>

</dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="f876c-118"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicando** (3)</span><span class="sxs-lookup"><span data-stu-id="f876c-118"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f876c-119">Replicating.</span><span class="sxs-lookup"><span data-stu-id="f876c-119">Replicating.</span></span>

</dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="f876c-120"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Replicación sincronizada completa** (4)</span><span class="sxs-lookup"><span data-stu-id="f876c-120"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f876c-121">Replicación sincronizada completada.</span><span class="sxs-lookup"><span data-stu-id="f876c-121">Synced replication complete.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="f876c-122"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (7)</span><span class="sxs-lookup"><span data-stu-id="f876c-122"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f876c-123">Suspende la replicación.</span><span class="sxs-lookup"><span data-stu-id="f876c-123">Suspend replication.</span></span>

</dd> <dt>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>

<span data-ttu-id="f876c-124"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Cancelar resincronización** (9)</span><span class="sxs-lookup"><span data-stu-id="f876c-124"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Cancel Resynchronize** (9)</span></span>


</dt> <dd>

<span data-ttu-id="f876c-125">Cancelar la resincronización.</span><span class="sxs-lookup"><span data-stu-id="f876c-125">Cancel resynchronization.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f876c-126">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f876c-126">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f876c-127">Referencia opcional a un objeto [**MSVM \_ ConcreteJob**](msvm-concretejob.md) que se devuelve si la operación se ejecuta de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="f876c-127">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="f876c-128">Si está presente, la referencia devuelta se puede usar para supervisar el progreso y obtener el resultado del método.</span><span class="sxs-lookup"><span data-stu-id="f876c-128">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="f876c-129">*TimeoutPeriod* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f876c-129">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f876c-130">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f876c-130">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f876c-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f876c-131">Return value</span></span>

<span data-ttu-id="f876c-132">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f876c-132">This method returns one of the following values.</span></span>



| <span data-ttu-id="f876c-133">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f876c-133">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="f876c-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="f876c-134">Description</span></span>                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f876c-135"><dt>**Completado sin error**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f876c-135"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="f876c-136">Correcto</span><span class="sxs-lookup"><span data-stu-id="f876c-136">Success</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="f876c-137"><dt>**Parámetros de método comprobados: trabajo iniciado**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="f876c-137"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="f876c-138">La transición es asincrónica.</span><span class="sxs-lookup"><span data-stu-id="f876c-138">The transition is asynchronous.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="f876c-139"><dt>**Error**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="f876c-139"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 |                                                                                                                             |
| <dl> <span data-ttu-id="f876c-140"><dt>**Acceso Denegado**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="f876c-140"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="f876c-141"><dt>**No compatible**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="f876c-141"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="f876c-142">El <dt>**Estado es desconocido**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="f876c-142"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      |                                                                                                                             |
| <dl> <span data-ttu-id="f876c-143"><dt>**Tiempo de espera**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="f876c-143"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                |                                                                                                                             |
| <dl> <span data-ttu-id="f876c-144"><dt>**Parámetro no válido**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="f876c-144"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="f876c-145">No se admite el valor especificado en uno de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="f876c-145">The value specified in one of the parameters is not supported.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="f876c-146">El <dt>**sistema está en uso**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="f876c-146"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       |                                                                                                                             |
| <dl> <span data-ttu-id="f876c-147"><dt>**Estado no válido para esta operación**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="f876c-147"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="f876c-148">El valor especificado en el parámetro *RequestedState* no se admite en el estado o el modo de replicación actual.</span><span class="sxs-lookup"><span data-stu-id="f876c-148">The value specified in the *RequestedState* parameter is not supported in the current replication mode or state.</span></span><br/> |
| <dl> <span data-ttu-id="f876c-149"><dt>**Tipo de datos incorrecto**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="f876c-149"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    |                                                                                                                             |
| <dl> <span data-ttu-id="f876c-150">El <dt>**sistema no está disponible**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="f876c-150"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                |                                                                                                                             |
| <dl> <span data-ttu-id="f876c-151"><dt>**Memoria**</dt> insuficiente <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="f876c-151"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="f876c-152"><dt>**No se encontró el archivo**</dt> <dt>32779</dt></span><span class="sxs-lookup"><span data-stu-id="f876c-152"><dt>**File not found**</dt> <dt>32779</dt></span></span> </dl>                         |                                                                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="f876c-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f876c-153">Requirements</span></span>



| <span data-ttu-id="f876c-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="f876c-154">Requirement</span></span> | <span data-ttu-id="f876c-155">Value</span><span class="sxs-lookup"><span data-stu-id="f876c-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f876c-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f876c-156">Minimum supported client</span></span><br/> | <span data-ttu-id="f876c-157">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="f876c-157">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f876c-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f876c-158">Minimum supported server</span></span><br/> | <span data-ttu-id="f876c-159">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="f876c-159">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f876c-160">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f876c-160">Namespace</span></span><br/>                | <span data-ttu-id="f876c-161">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f876c-161">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f876c-162">MOF</span><span class="sxs-lookup"><span data-stu-id="f876c-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f876c-163"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f876c-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f876c-164">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f876c-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f876c-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f876c-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f876c-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="f876c-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f876c-167">**MSVM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="f876c-167">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

 




