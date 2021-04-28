---
description: 'Método RequestStateChange de la Msvm_StorageJob: solicita un cambio de estado.'
ms.assetid: 2960bc44-f2af-49c6-9c33-5d9e1ad8056c
title: Método RequestStateChange de la Msvm_StorageJob clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e15f28af892e713f8bd6897b2d75b6b227886ad1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111353"
---
# <a name="requeststatechange-method-of-the-msvm_storagejob-class"></a><span data-ttu-id="a9380-103">Método RequestStateChange de la clase StorageJob de Msvm \_</span><span class="sxs-lookup"><span data-stu-id="a9380-103">RequestStateChange method of the Msvm\_StorageJob class</span></span>

<span data-ttu-id="a9380-104">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="a9380-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9380-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9380-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="a9380-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a9380-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9380-107">*RequestedState* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a9380-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9380-108">RequestStateChange cambia el estado de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="a9380-108">RequestStateChange changes the state of a job.</span></span> <span data-ttu-id="a9380-109">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a9380-109">The possible values are as follows:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="a9380-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Inicio** (2)</span><span class="sxs-lookup"><span data-stu-id="a9380-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a9380-111">Cambia el estado a "En ejecución".</span><span class="sxs-lookup"><span data-stu-id="a9380-111">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="a9380-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (3)</span><span class="sxs-lookup"><span data-stu-id="a9380-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a9380-113">Detiene temporalmente el trabajo.</span><span class="sxs-lookup"><span data-stu-id="a9380-113">Stops the job temporarily.</span></span> <span data-ttu-id="a9380-114">La intención es reiniciar posteriormente el trabajo con "Start".</span><span class="sxs-lookup"><span data-stu-id="a9380-114">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="a9380-115">Es posible especificar el estado "Servicio" mientras se suspende.</span><span class="sxs-lookup"><span data-stu-id="a9380-115">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="a9380-116">(Esto es específico del trabajo).</span><span class="sxs-lookup"><span data-stu-id="a9380-116">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="a9380-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span><span class="sxs-lookup"><span data-stu-id="a9380-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a9380-118">Detiene el trabajo correctamente, guarda los datos, conserva el estado y cierra todos los procesos subyacentes de forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="a9380-118">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="a9380-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="a9380-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a9380-120">Finaliza el trabajo inmediatamente sin necesidad de guardar datos o conservar el estado.</span><span class="sxs-lookup"><span data-stu-id="a9380-120">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a9380-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servicio** (6)</span><span class="sxs-lookup"><span data-stu-id="a9380-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a9380-122">Coloca el trabajo en un estado de servicio específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="a9380-122">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="a9380-123">Es posible reiniciar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="a9380-123">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="a9380-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (7..32767)</span><span class="sxs-lookup"><span data-stu-id="a9380-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="a9380-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="a9380-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="a9380-126">*TimeoutPeriod* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a9380-126">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9380-127">Período de tiempo de espera que especifica la cantidad máxima de tiempo que el cliente espera que se lleve la transición al nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="a9380-127">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="a9380-128">El formato de intervalo debe usarse para especificar el período de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="a9380-128">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="a9380-129">Un valor de 0 o **Null** indica que el cliente no tiene requisitos de tiempo para la transición.</span><span class="sxs-lookup"><span data-stu-id="a9380-129">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="a9380-130">Si esta propiedad no contiene 0 o **Null** y la implementación no admite este parámetro, se debe devolver un código de retorno 4098 **(No** se admite el uso del parámetro de tiempo de espera).</span><span class="sxs-lookup"><span data-stu-id="a9380-130">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9380-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a9380-131">Return value</span></span>

<span data-ttu-id="a9380-132">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="a9380-132">This method returns one of the following values:</span></span>

<dl> <dt>

 <span data-ttu-id="a9380-133"> (0)</span><span class="sxs-lookup"><span data-stu-id="a9380-133">(0)</span></span>
</dt> <dt>

 <span data-ttu-id="a9380-134">(32768)</span><span class="sxs-lookup"><span data-stu-id="a9380-134">(32768)</span></span>
</dt> <dt>

 <span data-ttu-id="a9380-135">(32769)</span><span class="sxs-lookup"><span data-stu-id="a9380-135">(32769)</span></span>
</dt> <dt>

 <span data-ttu-id="a9380-136">(32770)</span><span class="sxs-lookup"><span data-stu-id="a9380-136">(32770)</span></span>
</dt> <dt>

 <span data-ttu-id="a9380-137">(32771)</span><span class="sxs-lookup"><span data-stu-id="a9380-137">(32771)</span></span>
</dt> <dt>

 <span data-ttu-id="a9380-138">(32772)</span><span class="sxs-lookup"><span data-stu-id="a9380-138">(32772)</span></span>
</dt> <dt>

 <span data-ttu-id="a9380-139">(32773)</span><span class="sxs-lookup"><span data-stu-id="a9380-139">(32773)</span></span>
</dt> <dt>

 <span data-ttu-id="a9380-140">(32774)</span><span class="sxs-lookup"><span data-stu-id="a9380-140">(32774)</span></span>
</dt> <dt>

 <span data-ttu-id="a9380-141">(32775)</span><span class="sxs-lookup"><span data-stu-id="a9380-141">(32775)</span></span>
</dt> <dt>

 <span data-ttu-id="a9380-142">(32776)</span><span class="sxs-lookup"><span data-stu-id="a9380-142">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="a9380-143">(32777)</span><span class="sxs-lookup"><span data-stu-id="a9380-143">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="a9380-144">(32778)</span><span class="sxs-lookup"><span data-stu-id="a9380-144">(32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a9380-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9380-145">Requirements</span></span>



| <span data-ttu-id="a9380-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9380-146">Requirement</span></span> | <span data-ttu-id="a9380-147">Valor</span><span class="sxs-lookup"><span data-stu-id="a9380-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9380-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9380-148">Minimum supported client</span></span><br/> | <span data-ttu-id="a9380-149">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a9380-149">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="a9380-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9380-150">Minimum supported server</span></span><br/> | <span data-ttu-id="a9380-151">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a9380-151">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="a9380-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a9380-152">Namespace</span></span><br/>                | <span data-ttu-id="a9380-153">Virtualización \\ raíz \\ v2</span><span class="sxs-lookup"><span data-stu-id="a9380-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a9380-154">MOF</span><span class="sxs-lookup"><span data-stu-id="a9380-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9380-155"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9380-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9380-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a9380-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9380-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a9380-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a9380-158">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a9380-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9380-159">**Msvm \_ StorageJob**</span><span class="sxs-lookup"><span data-stu-id="a9380-159">**Msvm\_StorageJob**</span></span>](msvm-storagejob.md)
</dt> </dl>

 

 




