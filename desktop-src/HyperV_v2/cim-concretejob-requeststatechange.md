---
description: Solicita que el estado del trabajo se cambie al valor especificado en el parámetro RequestedState. Invocar varias veces al método RequestStateChange podría provocar que se sobrescriban o se pierdan solicitudes anteriores.
ms.assetid: 64a9d63e-8af4-4ab1-8343-9a0418b951e2
title: Método RequestStateChange de la clase CIM_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6e3efcea0f7ed7d6ecbfef7b543a0e82d90a15b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360425"
---
# <a name="requeststatechange-method-of-the-cim_concretejob-class"></a><span data-ttu-id="79523-104">Método RequestStateChange de la \_ clase ConcreteJob de CIM</span><span class="sxs-lookup"><span data-stu-id="79523-104">RequestStateChange method of the CIM\_ConcreteJob class</span></span>

<span data-ttu-id="79523-105">Solicita que el estado del trabajo se cambie al valor especificado en el parámetro RequestedState.</span><span class="sxs-lookup"><span data-stu-id="79523-105">Requests that the state of the job be changed to the value specified in the RequestedState parameter.</span></span> <span data-ttu-id="79523-106">Invocar varias veces al método RequestStateChange podría provocar que se sobrescriban o se pierdan solicitudes anteriores.</span><span class="sxs-lookup"><span data-stu-id="79523-106">Invoking the RequestStateChange method multiple times could result in earlier requests being overwritten or lost.</span></span>

<span data-ttu-id="79523-107">Si se devuelve 0, la tarea se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="79523-107">If 0 is returned, then the task completed successfully.</span></span> <span data-ttu-id="79523-108">Cualquier otro código de retorno indica una condición de error.</span><span class="sxs-lookup"><span data-stu-id="79523-108">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="79523-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79523-109">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="79523-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79523-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79523-111">*RequestedState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79523-111">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79523-112">Estado que se va a solicitar para un trabajo.</span><span class="sxs-lookup"><span data-stu-id="79523-112">The state to request for a job.</span></span> <span data-ttu-id="79523-113">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="79523-113">The possible values are as follows:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="79523-114"><span id="Start"></span><span id="start"></span><span id="START"></span>**Inicio** (2)</span><span class="sxs-lookup"><span data-stu-id="79523-114"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="79523-115">Cambia el estado a "en ejecución".</span><span class="sxs-lookup"><span data-stu-id="79523-115">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="79523-116"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (3)</span><span class="sxs-lookup"><span data-stu-id="79523-116"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="79523-117">Detiene el trabajo temporalmente.</span><span class="sxs-lookup"><span data-stu-id="79523-117">Stops the job temporarily.</span></span> <span data-ttu-id="79523-118">La intención es reiniciar posteriormente el trabajo con "Start".</span><span class="sxs-lookup"><span data-stu-id="79523-118">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="79523-119">Es posible que se pueda entrar en el estado "servicio" mientras se suspende.</span><span class="sxs-lookup"><span data-stu-id="79523-119">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="79523-120">(Es específico del trabajo).</span><span class="sxs-lookup"><span data-stu-id="79523-120">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="79523-121"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Finalizar** (4)</span><span class="sxs-lookup"><span data-stu-id="79523-121"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="79523-122">Detiene el trabajo correctamente, guarda los datos, conserva el estado y cierra todos los procesos subyacentes de forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="79523-122">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="79523-123"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="79523-123"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="79523-124">Finaliza el trabajo inmediatamente sin necesidad de guardar los datos ni de conservar el estado.</span><span class="sxs-lookup"><span data-stu-id="79523-124">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="79523-125"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servicio** (6)</span><span class="sxs-lookup"><span data-stu-id="79523-125"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="79523-126">Coloca el trabajo en un estado de servicio específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="79523-126">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="79523-127">Es posible que se pueda reiniciar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="79523-127">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="79523-128"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="79523-128"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="79523-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="79523-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="79523-130">*TimeoutPeriod* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79523-130">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79523-131">Un período de tiempo de espera que especifica la cantidad máxima de tiempo que el cliente espera que se realice la transición al nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="79523-131">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="79523-132">El formato de intervalo debe usarse para especificar el período de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="79523-132">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="79523-133">Un valor de 0 o **null** indica que el cliente no tiene ningún requisito de tiempo para la transición.</span><span class="sxs-lookup"><span data-stu-id="79523-133">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="79523-134">Si esta propiedad no contiene 0 o **null** y la implementación no admite este parámetro, se debe devolver un código de retorno de 4098 (**no se admite el uso del parámetro timeout**).</span><span class="sxs-lookup"><span data-stu-id="79523-134">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79523-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79523-135">Return value</span></span>

<span data-ttu-id="79523-136">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="79523-136">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="79523-137">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="79523-137">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="79523-138">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="79523-138">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="79523-139">**Error desconocido o no especificado** (2)</span><span class="sxs-lookup"><span data-stu-id="79523-139">**Unknown/Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="79523-140">**No se puede completar en el período de tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="79523-140">**Can NOT complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="79523-141">**Error** (4)</span><span class="sxs-lookup"><span data-stu-id="79523-141">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="79523-142">**Parámetro no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="79523-142">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="79523-143">**En uso** (6)</span><span class="sxs-lookup"><span data-stu-id="79523-143">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="79523-144">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="79523-144">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="79523-145">**Parámetros de método comprobados: transición iniciada** (4096)</span><span class="sxs-lookup"><span data-stu-id="79523-145">**Method Parameters Checked - Transition Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="79523-146">**Transición de estado no válida** (4097)</span><span class="sxs-lookup"><span data-stu-id="79523-146">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="79523-147">**No se admite el uso de parámetros de tiempo de espera** (4098)</span><span class="sxs-lookup"><span data-stu-id="79523-147">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="79523-148">**Ocupado** (4099)</span><span class="sxs-lookup"><span data-stu-id="79523-148">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="79523-149">**Método reservado** (4100.. 32767)</span><span class="sxs-lookup"><span data-stu-id="79523-149">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="79523-150">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="79523-150">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="79523-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79523-151">Requirements</span></span>



| <span data-ttu-id="79523-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="79523-152">Requirement</span></span> | <span data-ttu-id="79523-153">Value</span><span class="sxs-lookup"><span data-stu-id="79523-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79523-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79523-154">Minimum supported client</span></span><br/> | <span data-ttu-id="79523-155">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="79523-155">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="79523-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79523-156">Minimum supported server</span></span><br/> | <span data-ttu-id="79523-157">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="79523-157">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="79523-158">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="79523-158">Namespace</span></span><br/>                | <span data-ttu-id="79523-159">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="79523-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="79523-160">MOF</span><span class="sxs-lookup"><span data-stu-id="79523-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79523-161"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79523-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="79523-162">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="79523-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79523-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="79523-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="79523-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="79523-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79523-165">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="79523-165">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

 




