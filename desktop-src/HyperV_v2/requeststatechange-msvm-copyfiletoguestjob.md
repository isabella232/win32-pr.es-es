---
description: Cambia el estado del trabajo.
ms.assetid: 3B11CE45-63E4-43D1-AAF6-02F83C9CBB85
title: 'Msvm_CopyFileToGuestJob:: RequestStateChange (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: adf5d866989f3b3518cf53b52e073239e023e3c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687842"
---
# <a name="msvm_copyfiletoguestjobrequeststatechange-method"></a><span data-ttu-id="f2c1a-103">MSVM \_ CopyFileToGuestJob:: RequestStateChange (método)</span><span class="sxs-lookup"><span data-stu-id="f2c1a-103">Msvm\_CopyFileToGuestJob::RequestStateChange method</span></span>

<span data-ttu-id="f2c1a-104">Cambia el estado del trabajo.</span><span class="sxs-lookup"><span data-stu-id="f2c1a-104">Changes the state of the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2c1a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2c1a-105">Syntax</span></span>


```C++
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="f2c1a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2c1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2c1a-107">*RequestedState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2c1a-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2c1a-108">El nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="f2c1a-108">The new state.</span></span> <span data-ttu-id="f2c1a-109">Estos son los valores posibles:</span><span class="sxs-lookup"><span data-stu-id="f2c1a-109">These are the possible values:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="f2c1a-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Inicio** (2)</span><span class="sxs-lookup"><span data-stu-id="f2c1a-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f2c1a-111">Cambia el estado a "en ejecución".</span><span class="sxs-lookup"><span data-stu-id="f2c1a-111">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="f2c1a-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (3)</span><span class="sxs-lookup"><span data-stu-id="f2c1a-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f2c1a-113">Detiene el trabajo temporalmente.</span><span class="sxs-lookup"><span data-stu-id="f2c1a-113">Stops the job temporarily.</span></span> <span data-ttu-id="f2c1a-114">Después, el cliente puede reiniciar el trabajo con "Start".</span><span class="sxs-lookup"><span data-stu-id="f2c1a-114">The client can then subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="f2c1a-115">Es posible que el cliente pueda entrar en el estado "servicio" mientras está suspendido (es específico del trabajo).</span><span class="sxs-lookup"><span data-stu-id="f2c1a-115">The client can possibly enter the 'Service' state while suspended (this is job-specific).</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="f2c1a-116"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Finalizar** (4)</span><span class="sxs-lookup"><span data-stu-id="f2c1a-116"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f2c1a-117">Detiene el trabajo limpiamente, guarda los datos, conserva el estado y cerrando todos los procesos subyacentes de forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="f2c1a-117">Stops the job cleanly, saving data, preserving the state, and shutting down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="f2c1a-118"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="f2c1a-118"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f2c1a-119">Finaliza el trabajo inmediatamente sin necesidad de guardar los datos ni de conservar el estado.</span><span class="sxs-lookup"><span data-stu-id="f2c1a-119">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f2c1a-120"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servicio** (6)</span><span class="sxs-lookup"><span data-stu-id="f2c1a-120"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f2c1a-121">Coloca el trabajo en un estado de servicio específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="f2c1a-121">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="f2c1a-122">Es posible que el cliente reinicie el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f2c1a-122">The client can possibly restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f2c1a-123"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="f2c1a-123"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f2c1a-124"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="f2c1a-124"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="f2c1a-125">*TimeoutPeriod* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2c1a-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2c1a-126">Un período de tiempo de espera que especifica la cantidad máxima de tiempo que el cliente espera que se realice la transición al nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="f2c1a-126">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="f2c1a-127">El formato de intervalo debe usarse para especificar el período de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="f2c1a-127">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="f2c1a-128">Un valor de 0 o **null** indica que el cliente no tiene ningún requisito de tiempo para la transición.</span><span class="sxs-lookup"><span data-stu-id="f2c1a-128">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="f2c1a-129">Si esta propiedad no contiene 0 o **null** y la implementación no admite este parámetro, se debe devolver un código de retorno de 4098 (**no se admite el uso del parámetro timeout**).</span><span class="sxs-lookup"><span data-stu-id="f2c1a-129">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2c1a-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2c1a-130">Return value</span></span>

<span data-ttu-id="f2c1a-131">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f2c1a-131">This method returns one of the following values.</span></span>



| <span data-ttu-id="f2c1a-132">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2c1a-132">Return code/value</span></span>                                                                                                                                                               | <span data-ttu-id="f2c1a-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="f2c1a-133">Description</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f2c1a-134"><dt>**Completado sin error**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f2c1a-134"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="f2c1a-135">Correcto.</span><span class="sxs-lookup"><span data-stu-id="f2c1a-135">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="f2c1a-136"><dt>**No se admite el uso del parámetro Timeout**</dt> <dt>4098</dt></span><span class="sxs-lookup"><span data-stu-id="f2c1a-136"><dt>**Use of Timeout Parameter Not Supported**</dt> <dt>4098</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="f2c1a-137"><dt>**Error**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="f2c1a-137"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                |                                                                                    |
| <dl> <span data-ttu-id="f2c1a-138"><dt>**Acceso Denegado**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="f2c1a-138"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                         | <span data-ttu-id="f2c1a-139">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="f2c1a-139">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="f2c1a-140"><dt>**No compatible**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="f2c1a-140"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                         |                                                                                    |
| <dl> <span data-ttu-id="f2c1a-141">El <dt>**Estado es desconocido**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="f2c1a-141"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                     |                                                                                    |
| <dl> <span data-ttu-id="f2c1a-142"><dt>**Tiempo de espera**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="f2c1a-142"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                               |                                                                                    |
| <dl> <span data-ttu-id="f2c1a-143"><dt>**Parámetro no válido**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="f2c1a-143"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                     |                                                                                    |
| <dl> <span data-ttu-id="f2c1a-144">El <dt>**sistema está en uso**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="f2c1a-144"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                      |                                                                                    |
| <dl> <span data-ttu-id="f2c1a-145"><dt>**Estado no válido para esta operación**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="f2c1a-145"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>      | <span data-ttu-id="f2c1a-146">No se admite el valor especificado en el parámetro *RequestedState* .</span><span class="sxs-lookup"><span data-stu-id="f2c1a-146">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="f2c1a-147"><dt>**Tipo de datos incorrecto**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="f2c1a-147"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                   |                                                                                    |
| <dl> <span data-ttu-id="f2c1a-148">El <dt>**sistema no está disponible**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="f2c1a-148"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>               |                                                                                    |
| <dl> <span data-ttu-id="f2c1a-149"><dt>**Memoria**</dt> insuficiente <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="f2c1a-149"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                         |                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="f2c1a-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2c1a-150">Requirements</span></span>



| <span data-ttu-id="f2c1a-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2c1a-151">Requirement</span></span> | <span data-ttu-id="f2c1a-152">Value</span><span class="sxs-lookup"><span data-stu-id="f2c1a-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c1a-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2c1a-153">Minimum supported client</span></span><br/> | <span data-ttu-id="f2c1a-154">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="f2c1a-154">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f2c1a-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2c1a-155">Minimum supported server</span></span><br/> | <span data-ttu-id="f2c1a-156">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f2c1a-156">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f2c1a-157">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f2c1a-157">Namespace</span></span><br/>                | <span data-ttu-id="f2c1a-158">\\\\\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f2c1a-158">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="f2c1a-159">MOF</span><span class="sxs-lookup"><span data-stu-id="f2c1a-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2c1a-160"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2c1a-160"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2c1a-161">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f2c1a-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2c1a-162"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f2c1a-162"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f2c1a-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2c1a-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2c1a-164">**MSVM \_ CopyFileToGuestJob**</span><span class="sxs-lookup"><span data-stu-id="f2c1a-164">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




