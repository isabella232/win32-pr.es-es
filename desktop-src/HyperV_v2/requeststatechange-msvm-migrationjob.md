---
description: Solicita que el estado del trabajo de migración se cambie al estado especificado.
ms.assetid: f0be5ea8-7e21-407e-b84d-8bd4ca5a6a2c
title: Método RequestStateChange de la clase Msvm_MigrationJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31011de619780ae36f390ee87038300a3b42fef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667161"
---
# <a name="requeststatechange-method-of-the-msvm_migrationjob-class"></a><span data-ttu-id="f79a1-103">Método RequestStateChange de la \_ clase MigrationJob de MSVM</span><span class="sxs-lookup"><span data-stu-id="f79a1-103">RequestStateChange method of the Msvm\_MigrationJob class</span></span>

<span data-ttu-id="f79a1-104">Solicita que el estado del trabajo de migración se cambie al estado especificado.</span><span class="sxs-lookup"><span data-stu-id="f79a1-104">Requests that the state of the migration job be changed to the specified state.</span></span> <span data-ttu-id="f79a1-105">Al invocar el método **RequestStateChange** varias veces, se puede provocar que se sobrescriban o se pierdan solicitudes anteriores.</span><span class="sxs-lookup"><span data-stu-id="f79a1-105">Invoking the **RequestStateChange** method multiple times can result in earlier requests being overwritten or lost.</span></span> <span data-ttu-id="f79a1-106">Si se devuelve 0, la tarea se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f79a1-106">If 0 is returned, then the task completed successfully.</span></span> <span data-ttu-id="f79a1-107">Cualquier otro código de retorno indica una condición de error.</span><span class="sxs-lookup"><span data-stu-id="f79a1-107">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="f79a1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f79a1-108">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="f79a1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f79a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f79a1-110">*RequestedState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f79a1-110">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f79a1-111">Nuevo estado de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="f79a1-111">The new state of a job.</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="f79a1-112"><span id="Start"></span><span id="start"></span><span id="START"></span>**Inicio** (2)</span><span class="sxs-lookup"><span data-stu-id="f79a1-112"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f79a1-113">Cambia el estado a "en ejecución".</span><span class="sxs-lookup"><span data-stu-id="f79a1-113">Changes the state to "Running".</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="f79a1-114"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (3)</span><span class="sxs-lookup"><span data-stu-id="f79a1-114"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f79a1-115">Detiene el trabajo temporalmente.</span><span class="sxs-lookup"><span data-stu-id="f79a1-115">Stops the job temporarily.</span></span> <span data-ttu-id="f79a1-116">La intención es reiniciar posteriormente el trabajo con "Start".</span><span class="sxs-lookup"><span data-stu-id="f79a1-116">The intention is to subsequently restart the job with "Start".</span></span> <span data-ttu-id="f79a1-117">Es posible que se pueda entrar en el estado "servicio" mientras se suspende.</span><span class="sxs-lookup"><span data-stu-id="f79a1-117">It might be possible to enter the "Service" state while suspended.</span></span> <span data-ttu-id="f79a1-118">(Esto es específico del trabajo).</span><span class="sxs-lookup"><span data-stu-id="f79a1-118">(This is job specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="f79a1-119"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Finalizar** (4)</span><span class="sxs-lookup"><span data-stu-id="f79a1-119"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f79a1-120">Detiene el trabajo limpiamente, guarda los datos, conserva el estado y cerrando todos los procesos subyacentes de forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="f79a1-120">Stops the job cleanly, saving data, preserving the state, and shutting down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="f79a1-121"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="f79a1-121"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f79a1-122">Finaliza el trabajo inmediatamente sin necesidad de guardar los datos ni de conservar el estado.</span><span class="sxs-lookup"><span data-stu-id="f79a1-122">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f79a1-123"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servicio** (6)</span><span class="sxs-lookup"><span data-stu-id="f79a1-123"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f79a1-124">Coloca el trabajo en un estado de servicio específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="f79a1-124">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="f79a1-125">Es posible que se pueda reiniciar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f79a1-125">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f79a1-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado**</span><span class="sxs-lookup"><span data-stu-id="f79a1-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="f79a1-127">Reservado.</span><span class="sxs-lookup"><span data-stu-id="f79a1-127">Reserved.</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f79a1-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado**</span><span class="sxs-lookup"><span data-stu-id="f79a1-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="f79a1-129">Reservado.</span><span class="sxs-lookup"><span data-stu-id="f79a1-129">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f79a1-130">*TimeoutPeriod* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f79a1-130">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f79a1-131">Un período de tiempo de espera que especifica la cantidad máxima de tiempo que el cliente espera que se realice la transición al nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="f79a1-131">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="f79a1-132">El formato de intervalo debe usarse para especificar el período de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="f79a1-132">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="f79a1-133">Un valor de 0 o **null** indica que el cliente no tiene ningún requisito de tiempo para la transición.</span><span class="sxs-lookup"><span data-stu-id="f79a1-133">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="f79a1-134">Si esta propiedad no contiene 0 o **null** y la implementación no admite este parámetro, se debe devolver un código de retorno de 4098 (no se admite el uso del parámetro timeout).</span><span class="sxs-lookup"><span data-stu-id="f79a1-134">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (Use Of Timeout Parameter Not Supported) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f79a1-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f79a1-135">Return value</span></span>

<dl> <dt>

 <span data-ttu-id="f79a1-136"> (0)</span><span class="sxs-lookup"><span data-stu-id="f79a1-136">(0)</span></span>
</dt> <dt>

 <span data-ttu-id="f79a1-137">(32768)</span><span class="sxs-lookup"><span data-stu-id="f79a1-137">(32768)</span></span>
</dt> <dt>

 <span data-ttu-id="f79a1-138">(32769)</span><span class="sxs-lookup"><span data-stu-id="f79a1-138">(32769)</span></span>
</dt> <dt>

 <span data-ttu-id="f79a1-139">(32770)</span><span class="sxs-lookup"><span data-stu-id="f79a1-139">(32770)</span></span>
</dt> <dt>

 <span data-ttu-id="f79a1-140">(32771)</span><span class="sxs-lookup"><span data-stu-id="f79a1-140">(32771)</span></span>
</dt> <dt>

 <span data-ttu-id="f79a1-141">(32772)</span><span class="sxs-lookup"><span data-stu-id="f79a1-141">(32772)</span></span>
</dt> <dt>

 <span data-ttu-id="f79a1-142">(32773)</span><span class="sxs-lookup"><span data-stu-id="f79a1-142">(32773)</span></span>
</dt> <dt>

 <span data-ttu-id="f79a1-143">(32774)</span><span class="sxs-lookup"><span data-stu-id="f79a1-143">(32774)</span></span>
</dt> <dt>

 <span data-ttu-id="f79a1-144">(32775)</span><span class="sxs-lookup"><span data-stu-id="f79a1-144">(32775)</span></span>
</dt> <dt>

 <span data-ttu-id="f79a1-145">(32776)</span><span class="sxs-lookup"><span data-stu-id="f79a1-145">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="f79a1-146">(32777)</span><span class="sxs-lookup"><span data-stu-id="f79a1-146">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="f79a1-147">(32778)</span><span class="sxs-lookup"><span data-stu-id="f79a1-147">(32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f79a1-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f79a1-148">Requirements</span></span>



| <span data-ttu-id="f79a1-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="f79a1-149">Requirement</span></span> | <span data-ttu-id="f79a1-150">Value</span><span class="sxs-lookup"><span data-stu-id="f79a1-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f79a1-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f79a1-151">Minimum supported client</span></span><br/> | <span data-ttu-id="f79a1-152">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="f79a1-152">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f79a1-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f79a1-153">Minimum supported server</span></span><br/> | <span data-ttu-id="f79a1-154">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="f79a1-154">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f79a1-155">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f79a1-155">Namespace</span></span><br/>                | <span data-ttu-id="f79a1-156">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f79a1-156">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f79a1-157">MOF</span><span class="sxs-lookup"><span data-stu-id="f79a1-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f79a1-158"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f79a1-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f79a1-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f79a1-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f79a1-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f79a1-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f79a1-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="f79a1-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f79a1-162">**MSVM \_ MigrationJob**</span><span class="sxs-lookup"><span data-stu-id="f79a1-162">**Msvm\_MigrationJob**</span></span>](msvm-migrationjob.md)
</dt> </dl>

 

 




