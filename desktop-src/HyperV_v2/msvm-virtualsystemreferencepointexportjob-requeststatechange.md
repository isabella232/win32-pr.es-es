---
description: 'Método RequestStateChange de la clase Msvm_VirtualSystemReferencePointExportJob: solicita un cambio de estado.'
ms.assetid: 53c24e17-2b59-4439-a6d1-e971c189d223
title: Método RequestStateChange de la Msvm_VirtualSystemReferencePointExportJob clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bd12d7cd5b79e38260e671bf1408304390985dac
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109313"
---
# <a name="requeststatechange-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="75be6-103">Método RequestStateChange de la clase Msvm \_ VirtualSystemReferencePointExportJob</span><span class="sxs-lookup"><span data-stu-id="75be6-103">RequestStateChange method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="75be6-104">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="75be6-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="75be6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75be6-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="75be6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75be6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75be6-107">*RequestedState* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="75be6-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75be6-108">Cambia el estado de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="75be6-108">Changes the state of a job.</span></span> <span data-ttu-id="75be6-109">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="75be6-109">The possible values are as follows:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="75be6-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Inicio** (2)</span><span class="sxs-lookup"><span data-stu-id="75be6-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="75be6-111">Cambia el estado a "En ejecución".</span><span class="sxs-lookup"><span data-stu-id="75be6-111">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="75be6-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (3)</span><span class="sxs-lookup"><span data-stu-id="75be6-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="75be6-113">Detiene temporalmente el trabajo.</span><span class="sxs-lookup"><span data-stu-id="75be6-113">Stops the job temporarily.</span></span> <span data-ttu-id="75be6-114">La intención es reiniciar posteriormente el trabajo con "Start".</span><span class="sxs-lookup"><span data-stu-id="75be6-114">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="75be6-115">Es posible especificar el estado "Servicio" mientras se suspende.</span><span class="sxs-lookup"><span data-stu-id="75be6-115">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="75be6-116">(Esto es específico del trabajo).</span><span class="sxs-lookup"><span data-stu-id="75be6-116">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="75be6-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span><span class="sxs-lookup"><span data-stu-id="75be6-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="75be6-118">Detiene el trabajo correctamente, guarda los datos, conserva el estado y cierra todos los procesos subyacentes de forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="75be6-118">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="75be6-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="75be6-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="75be6-120">Finaliza el trabajo inmediatamente sin necesidad de guardar datos o conservar el estado.</span><span class="sxs-lookup"><span data-stu-id="75be6-120">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="75be6-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servicio** (6)</span><span class="sxs-lookup"><span data-stu-id="75be6-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="75be6-122">Coloca el trabajo en un estado de servicio específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="75be6-122">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="75be6-123">Es posible reiniciar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="75be6-123">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="75be6-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (7..32767)</span><span class="sxs-lookup"><span data-stu-id="75be6-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="75be6-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="75be6-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="75be6-126">*TimeoutPeriod* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="75be6-126">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75be6-127">Período de tiempo de espera que especifica la cantidad máxima de tiempo que el cliente espera que se lleve la transición al nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="75be6-127">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="75be6-128">El formato de intervalo debe usarse para especificar el período de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="75be6-128">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="75be6-129">Un valor de 0 o **Null** indica que el cliente no tiene ningún requisito de tiempo para la transición.</span><span class="sxs-lookup"><span data-stu-id="75be6-129">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="75be6-130">Si esta propiedad no contiene 0 o **Null** y la implementación no admite este parámetro, se debe devolver un código de retorno 4098 (**Use Of Timeout Parameter Not Supported**).</span><span class="sxs-lookup"><span data-stu-id="75be6-130">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75be6-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75be6-131">Return value</span></span>

<span data-ttu-id="75be6-132">Devuelve un 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="75be6-132">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

 <span data-ttu-id="75be6-133"> (0)</span><span class="sxs-lookup"><span data-stu-id="75be6-133">(0)</span></span>
</dt> <dt>

 <span data-ttu-id="75be6-134">(32768)</span><span class="sxs-lookup"><span data-stu-id="75be6-134">(32768)</span></span>
</dt> <dt>

 <span data-ttu-id="75be6-135">(32769)</span><span class="sxs-lookup"><span data-stu-id="75be6-135">(32769)</span></span>
</dt> <dt>

 <span data-ttu-id="75be6-136">(32770)</span><span class="sxs-lookup"><span data-stu-id="75be6-136">(32770)</span></span>
</dt> <dt>

 <span data-ttu-id="75be6-137">(32771)</span><span class="sxs-lookup"><span data-stu-id="75be6-137">(32771)</span></span>
</dt> <dt>

 <span data-ttu-id="75be6-138">(32772)</span><span class="sxs-lookup"><span data-stu-id="75be6-138">(32772)</span></span>
</dt> <dt>

 <span data-ttu-id="75be6-139">(32773)</span><span class="sxs-lookup"><span data-stu-id="75be6-139">(32773)</span></span>
</dt> <dt>

 <span data-ttu-id="75be6-140">(32774)</span><span class="sxs-lookup"><span data-stu-id="75be6-140">(32774)</span></span>
</dt> <dt>

 <span data-ttu-id="75be6-141">(32775)</span><span class="sxs-lookup"><span data-stu-id="75be6-141">(32775)</span></span>
</dt> <dt>

 <span data-ttu-id="75be6-142">(32776)</span><span class="sxs-lookup"><span data-stu-id="75be6-142">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="75be6-143">(32777)</span><span class="sxs-lookup"><span data-stu-id="75be6-143">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="75be6-144">(32778)</span><span class="sxs-lookup"><span data-stu-id="75be6-144">(32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="75be6-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75be6-145">Requirements</span></span>



| <span data-ttu-id="75be6-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="75be6-146">Requirement</span></span> | <span data-ttu-id="75be6-147">Valor</span><span class="sxs-lookup"><span data-stu-id="75be6-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75be6-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75be6-148">Minimum supported client</span></span><br/> | <span data-ttu-id="75be6-149">Windows 10, solo aplicaciones de escritorio de la versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="75be6-149">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="75be6-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75be6-150">Minimum supported server</span></span><br/> | <span data-ttu-id="75be6-151">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="75be6-151">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="75be6-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="75be6-152">Namespace</span></span><br/>                | <span data-ttu-id="75be6-153">Virtualización \\ raíz \\ v2</span><span class="sxs-lookup"><span data-stu-id="75be6-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="75be6-154">MOF</span><span class="sxs-lookup"><span data-stu-id="75be6-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75be6-155"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="75be6-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="75be6-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="75be6-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75be6-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="75be6-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="75be6-158">Consulte también</span><span class="sxs-lookup"><span data-stu-id="75be6-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75be6-159">**Msvm \_ VirtualSystemReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="75be6-159">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 




