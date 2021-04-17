---
description: Solicita que el estado de replicación de la relación de replicación de la máquina virtual se cambie al valor especificado.
ms.assetid: 8EC78CCC-2997-4239-A20C-BA56F848ECB6
title: 'Msvm_ComputerSystem:: RequestReplicationStateChangeEx (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestReplicationStateChangeEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d77db9dff90f985991c8e9013ea4f239cb6479f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652803"
---
# <a name="msvm_computersystemrequestreplicationstatechangeex-method"></a><span data-ttu-id="47b58-103">MSVM \_ ComputerSystem:: RequestReplicationStateChangeEx (método)</span><span class="sxs-lookup"><span data-stu-id="47b58-103">Msvm\_ComputerSystem::RequestReplicationStateChangeEx method</span></span>

<span data-ttu-id="47b58-104">Solicita que el estado de replicación de la relación de replicación de la máquina virtual se cambie al valor especificado.</span><span class="sxs-lookup"><span data-stu-id="47b58-104">Requests that the replication state of the replication relationship of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="47b58-105">Mientras el cambio de estado está en curso, la propiedad **ReplicationState** se cambia al valor del parámetro *RequestedState* .</span><span class="sxs-lookup"><span data-stu-id="47b58-105">While the state change is in progress, the **ReplicationState** property is changed to the value of the *RequestedState* parameter.</span></span> <span data-ttu-id="47b58-106">Este método solo se admite para las instancias de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representan una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="47b58-106">This method is only supported for instances of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represent a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="47b58-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47b58-107">Syntax</span></span>


```C++
uint32 RequestReplicationStateChangeEx(
  [in]  string              ReplicationRelationship,
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="47b58-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47b58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47b58-109">*ReplicationRelationship* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="47b58-109">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47b58-110">Representación de cadena de una instancia incrustada de la clase [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) que define la relación de replicación para la solicitud de cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="47b58-110">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the replication relationship for state change request.</span></span> <span data-ttu-id="47b58-111">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="47b58-111">This parameter is optional.</span></span> <span data-ttu-id="47b58-112">Cuando no se especifica, la solicitud se ejecuta en la relación de replicación principal.</span><span class="sxs-lookup"><span data-stu-id="47b58-112">When it's unspecified, the request runs on the primary replication relationship.</span></span>

</dd> <dt>

<span data-ttu-id="47b58-113">*RequestedState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="47b58-113">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47b58-114">Nuevo estado de replicación.</span><span class="sxs-lookup"><span data-stu-id="47b58-114">The new replication state.</span></span> <span data-ttu-id="47b58-115">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="47b58-115">The must be one of the following values.</span></span>

<dt>

<span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>

<span data-ttu-id="47b58-116"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Listo para iniciar la replicación inicial** (1)</span><span class="sxs-lookup"><span data-stu-id="47b58-116"><span id="Ready_to_start_initial_replication"></span><span id="ready_to_start_initial_replication"></span><span id="READY_TO_START_INITIAL_REPLICATION"></span>**Ready to start initial replication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="47b58-117">Listo para iniciar la replicación inicial.</span><span class="sxs-lookup"><span data-stu-id="47b58-117">Ready to start initial replication.</span></span>

</dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="47b58-118"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Esperando para completar la replicación inicial** (2)</span><span class="sxs-lookup"><span data-stu-id="47b58-118"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="47b58-119">Esperando para completar la replicación inicial.</span><span class="sxs-lookup"><span data-stu-id="47b58-119">Waiting to complete initial replication.</span></span>

</dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="47b58-120"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicando** (3)</span><span class="sxs-lookup"><span data-stu-id="47b58-120"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd>

<span data-ttu-id="47b58-121">Replicating.</span><span class="sxs-lookup"><span data-stu-id="47b58-121">Replicating.</span></span>

</dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="47b58-122"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Replicación sincronizada completa** (4)</span><span class="sxs-lookup"><span data-stu-id="47b58-122"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd>

<span data-ttu-id="47b58-123">Replicación sincronizada completada.</span><span class="sxs-lookup"><span data-stu-id="47b58-123">Synced replication complete.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="47b58-124"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (7)</span><span class="sxs-lookup"><span data-stu-id="47b58-124"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (7)</span></span>


</dt> <dd>

<span data-ttu-id="47b58-125">Suspende la replicación.</span><span class="sxs-lookup"><span data-stu-id="47b58-125">Suspend replication.</span></span>

</dd> <dt>

<span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>

<span data-ttu-id="47b58-126"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Cancelar resincronización** (9)</span><span class="sxs-lookup"><span data-stu-id="47b58-126"><span id="Cancel_Resynchronize"></span><span id="cancel_resynchronize"></span><span id="CANCEL_RESYNCHRONIZE"></span>**Cancel Resynchronize** (9)</span></span>


</dt> <dd>

<span data-ttu-id="47b58-127">Cancelar la resincronización.</span><span class="sxs-lookup"><span data-stu-id="47b58-127">Cancel resynchronization.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="47b58-128">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="47b58-128">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47b58-129">Referencia opcional a un objeto [**MSVM \_ ConcreteJob**](msvm-concretejob.md) que se devuelve si la operación se ejecuta de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="47b58-129">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="47b58-130">Si está presente, la referencia devuelta se puede usar para supervisar el progreso y obtener el resultado del método.</span><span class="sxs-lookup"><span data-stu-id="47b58-130">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="47b58-131">*TimeoutPeriod* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="47b58-131">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47b58-132">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="47b58-132">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47b58-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47b58-133">Return value</span></span>

<span data-ttu-id="47b58-134">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="47b58-134">This method returns one of the following values.</span></span>



| <span data-ttu-id="47b58-135">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47b58-135">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="47b58-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="47b58-136">Description</span></span>                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="47b58-137"><dt>**Completado sin error**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="47b58-137"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="47b58-138">Correcto</span><span class="sxs-lookup"><span data-stu-id="47b58-138">Success</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="47b58-139"><dt>**Parámetros de método comprobados: trabajo iniciado**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="47b58-139"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="47b58-140">La transición es asincrónica.</span><span class="sxs-lookup"><span data-stu-id="47b58-140">The transition is asynchronous.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="47b58-141"><dt>**Error**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="47b58-141"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 |                                                                                                                             |
| <dl> <span data-ttu-id="47b58-142"><dt>**Acceso Denegado**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="47b58-142"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="47b58-143"><dt>**No compatible**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="47b58-143"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="47b58-144">El <dt>**Estado es desconocido**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="47b58-144"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      |                                                                                                                             |
| <dl> <span data-ttu-id="47b58-145"><dt>**Tiempo de espera**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="47b58-145"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                |                                                                                                                             |
| <dl> <span data-ttu-id="47b58-146"><dt>**Parámetro no válido**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="47b58-146"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="47b58-147">No se admite el valor especificado en uno de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="47b58-147">The value specified in one of the parameters is not supported.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="47b58-148">El <dt>**sistema está en uso**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="47b58-148"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       |                                                                                                                             |
| <dl> <span data-ttu-id="47b58-149"><dt>**Estado no válido para esta operación**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="47b58-149"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="47b58-150">El valor especificado en el parámetro *RequestedState* no se admite en el estado o el modo de replicación actual.</span><span class="sxs-lookup"><span data-stu-id="47b58-150">The value specified in the *RequestedState* parameter is not supported in the current replication mode or state.</span></span><br/> |
| <dl> <span data-ttu-id="47b58-151"><dt>**Tipo de datos incorrecto**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="47b58-151"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    |                                                                                                                             |
| <dl> <span data-ttu-id="47b58-152">El <dt>**sistema no está disponible**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="47b58-152"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                |                                                                                                                             |
| <dl> <span data-ttu-id="47b58-153"><dt>**Memoria**</dt> insuficiente <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="47b58-153"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          |                                                                                                                             |
| <dl> <span data-ttu-id="47b58-154"><dt>**No se encontró el archivo**</dt> <dt>32779</dt></span><span class="sxs-lookup"><span data-stu-id="47b58-154"><dt>**File not found**</dt> <dt>32779</dt></span></span> </dl>                         |                                                                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="47b58-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47b58-155">Requirements</span></span>



| <span data-ttu-id="47b58-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="47b58-156">Requirement</span></span> | <span data-ttu-id="47b58-157">Value</span><span class="sxs-lookup"><span data-stu-id="47b58-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47b58-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47b58-158">Minimum supported client</span></span><br/> | <span data-ttu-id="47b58-159">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="47b58-159">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="47b58-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47b58-160">Minimum supported server</span></span><br/> | <span data-ttu-id="47b58-161">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="47b58-161">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="47b58-162">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="47b58-162">Namespace</span></span><br/>                | <span data-ttu-id="47b58-163">\\\\\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="47b58-163">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="47b58-164">MOF</span><span class="sxs-lookup"><span data-stu-id="47b58-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47b58-165"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47b58-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="47b58-166">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="47b58-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47b58-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="47b58-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="47b58-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="47b58-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47b58-169">**MSVM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="47b58-169">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

 




