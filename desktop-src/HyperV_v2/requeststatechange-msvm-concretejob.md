---
description: Solicita que el estado del trabajo se cambie al estado especificado.
ms.assetid: 5D7D7D20-4BB9-4375-BBBF-7AA64FEE6D13
title: Método RequestStateChange de la clase Msvm_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0e7abf5f4bf78ac469e528ab72bb5786130e9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667818"
---
# <a name="requeststatechange-method-of-the-msvm_concretejob-class"></a><span data-ttu-id="c5b36-103">Método RequestStateChange de la \_ clase ConcreteJob de MSVM</span><span class="sxs-lookup"><span data-stu-id="c5b36-103">RequestStateChange method of the Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="c5b36-104">Solicita que el estado del trabajo se cambie al estado especificado.</span><span class="sxs-lookup"><span data-stu-id="c5b36-104">Requests that the state of the job be changed to the specified state.</span></span> <span data-ttu-id="c5b36-105">Al invocar el método **RequestStateChange** varias veces, se puede provocar que se sobrescriban o se pierdan solicitudes anteriores.</span><span class="sxs-lookup"><span data-stu-id="c5b36-105">Invoking the **RequestStateChange** method multiple times can result in earlier requests being overwritten or lost.</span></span> <span data-ttu-id="c5b36-106">Si se devuelve 0, la tarea se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c5b36-106">If 0 is returned, then the task completed successfully.</span></span> <span data-ttu-id="c5b36-107">Cualquier otro código de retorno indica una condición de error.</span><span class="sxs-lookup"><span data-stu-id="c5b36-107">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5b36-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5b36-108">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="c5b36-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5b36-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5b36-110">*RequestedState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5b36-110">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5b36-111">Tipo: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5b36-111">Type: **uint16**</span></span>

<span data-ttu-id="c5b36-112">Nuevo estado de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="c5b36-112">The new state of a job.</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="c5b36-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Inicio** (2)</span><span class="sxs-lookup"><span data-stu-id="c5b36-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c5b36-114">Cambia el estado a "en ejecución".</span><span class="sxs-lookup"><span data-stu-id="c5b36-114">Changes the state to "Running".</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="c5b36-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (3)</span><span class="sxs-lookup"><span data-stu-id="c5b36-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c5b36-116">Detiene el trabajo temporalmente.</span><span class="sxs-lookup"><span data-stu-id="c5b36-116">Stops the job temporarily.</span></span> <span data-ttu-id="c5b36-117">La intención es reiniciar posteriormente el trabajo con "Start".</span><span class="sxs-lookup"><span data-stu-id="c5b36-117">The intention is to subsequently restart the job with "Start".</span></span> <span data-ttu-id="c5b36-118">Es posible que se pueda entrar en el estado "servicio" mientras se suspende.</span><span class="sxs-lookup"><span data-stu-id="c5b36-118">It might be possible to enter the "Service" state while suspended.</span></span> <span data-ttu-id="c5b36-119">(Esto es específico del trabajo).</span><span class="sxs-lookup"><span data-stu-id="c5b36-119">(This is job specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="c5b36-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Finalizar** (4)</span><span class="sxs-lookup"><span data-stu-id="c5b36-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c5b36-121">Detiene el trabajo limpiamente, guarda los datos, conserva el estado y cerrando todos los procesos subyacentes de forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="c5b36-121">Stops the job cleanly, saving data, preserving the state, and shutting down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="c5b36-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="c5b36-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c5b36-123">Finaliza el trabajo inmediatamente sin necesidad de guardar los datos ni de conservar el estado.</span><span class="sxs-lookup"><span data-stu-id="c5b36-123">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c5b36-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servicio** (6)</span><span class="sxs-lookup"><span data-stu-id="c5b36-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c5b36-125">Coloca el trabajo en un estado de servicio específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="c5b36-125">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="c5b36-126">Es posible que se pueda reiniciar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="c5b36-126">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c5b36-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado**</span><span class="sxs-lookup"><span data-stu-id="c5b36-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="c5b36-128">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c5b36-128">Reserved.</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="c5b36-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado**</span><span class="sxs-lookup"><span data-stu-id="c5b36-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="c5b36-130">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c5b36-130">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c5b36-131">*TimeoutPeriod* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5b36-131">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5b36-132">Tipo: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c5b36-132">Type: **datetime**</span></span>

<span data-ttu-id="c5b36-133">Un período de tiempo de espera que especifica la cantidad máxima de tiempo que el cliente espera que se realice la transición al nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="c5b36-133">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="c5b36-134">El formato de intervalo debe usarse para especificar el período de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="c5b36-134">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="c5b36-135">Un valor de 0 o **null** indica que el cliente no tiene ningún requisito de tiempo para la transición.</span><span class="sxs-lookup"><span data-stu-id="c5b36-135">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="c5b36-136">Si esta propiedad no contiene 0 o **null** y la implementación no admite este parámetro, se debe devolver un código de retorno de 4098 (no se admite el uso del parámetro timeout).</span><span class="sxs-lookup"><span data-stu-id="c5b36-136">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (Use Of Timeout Parameter Not Supported) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5b36-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5b36-137">Return value</span></span>

<span data-ttu-id="c5b36-138">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c5b36-138">Type: **uint32**</span></span>

<span data-ttu-id="c5b36-139">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c5b36-139">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c5b36-140">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="c5b36-140">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c5b36-141">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="c5b36-141">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c5b36-142">**Error desconocido o no especificado** (2)</span><span class="sxs-lookup"><span data-stu-id="c5b36-142">**Unknown/Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c5b36-143">**No se puede completar en el período de tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="c5b36-143">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c5b36-144">**Error** (4)</span><span class="sxs-lookup"><span data-stu-id="c5b36-144">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c5b36-145">**Parámetro no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="c5b36-145">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c5b36-146">**En uso** (6)</span><span class="sxs-lookup"><span data-stu-id="c5b36-146">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c5b36-147">**DMTF reservado** (7 4095)</span><span class="sxs-lookup"><span data-stu-id="c5b36-147">**DMTF Reserved** (7 4095)</span></span>
</dt> <dt>

<span data-ttu-id="c5b36-148">**Parámetros de método comprobados: transición iniciada** (4096)</span><span class="sxs-lookup"><span data-stu-id="c5b36-148">**Method Parameters Checked - Transition Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c5b36-149">**Transición de estado no válida** (4097)</span><span class="sxs-lookup"><span data-stu-id="c5b36-149">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="c5b36-150">**No se admite el uso de parámetros de tiempo de espera** (4098)</span><span class="sxs-lookup"><span data-stu-id="c5b36-150">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="c5b36-151">**Ocupado** (4099)</span><span class="sxs-lookup"><span data-stu-id="c5b36-151">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="c5b36-152">**Método reservado** (4100 32767)</span><span class="sxs-lookup"><span data-stu-id="c5b36-152">**Method Reserved** (4100 32767)</span></span>
</dt> <dt>

<span data-ttu-id="c5b36-153">**Específico del proveedor** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="c5b36-153">**Vendor Specific** (32768 65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="c5b36-154">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5b36-154">Remarks</span></span>

<span data-ttu-id="c5b36-155">El acceso a la clase [**MSVM \_ ConcreteJob**](msvm-concretejob.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="c5b36-155">Access to the [**Msvm\_ConcreteJob**](msvm-concretejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c5b36-156">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c5b36-156">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5b36-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5b36-157">Requirements</span></span>



| <span data-ttu-id="c5b36-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5b36-158">Requirement</span></span> | <span data-ttu-id="c5b36-159">Value</span><span class="sxs-lookup"><span data-stu-id="c5b36-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5b36-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5b36-160">Minimum supported client</span></span><br/> | <span data-ttu-id="c5b36-161">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="c5b36-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c5b36-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5b36-162">Minimum supported server</span></span><br/> | <span data-ttu-id="c5b36-163">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="c5b36-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c5b36-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c5b36-164">Namespace</span></span><br/>                | <span data-ttu-id="c5b36-165">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="c5b36-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c5b36-166">MOF</span><span class="sxs-lookup"><span data-stu-id="c5b36-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5b36-167"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5b36-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5b36-168">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c5b36-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5b36-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c5b36-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c5b36-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5b36-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5b36-171">**MSVM \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="c5b36-171">**Msvm\_ConcreteJob**</span></span>](msvm-concretejob.md)
</dt> </dl>

 

