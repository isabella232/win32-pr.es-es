---
description: 'Método RequestStateChange de la Msvm_CollectionReferencePointExportJob clase : solicita un cambio de estado.'
ms.assetid: 34d70ff2-4545-4ab7-8c84-6532c342768b
title: Método RequestStateChange de la Msvm_CollectionReferencePointExportJob clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 84956e206654de022c3151aa5a442651f9c2375a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119243"
---
# <a name="requeststatechange-method-of-the-msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="d6333-103">Método RequestStateChange de la clase \_ CollectionReferencePointExportJob de Msvm</span><span class="sxs-lookup"><span data-stu-id="d6333-103">RequestStateChange method of the Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="d6333-104">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="d6333-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6333-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6333-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="d6333-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d6333-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6333-107">*RequestedState* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d6333-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6333-108">RequestStateChange cambia el estado de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="d6333-108">RequestStateChange changes the state of a job.</span></span> <span data-ttu-id="d6333-109">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="d6333-109">The possible values are as follows:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="d6333-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Inicio** (2)</span><span class="sxs-lookup"><span data-stu-id="d6333-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d6333-111">Cambia el estado a "En ejecución".</span><span class="sxs-lookup"><span data-stu-id="d6333-111">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="d6333-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (3)</span><span class="sxs-lookup"><span data-stu-id="d6333-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d6333-113">Detiene temporalmente el trabajo.</span><span class="sxs-lookup"><span data-stu-id="d6333-113">Stops the job temporarily.</span></span> <span data-ttu-id="d6333-114">La intención es reiniciar posteriormente el trabajo con "Start".</span><span class="sxs-lookup"><span data-stu-id="d6333-114">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="d6333-115">Es posible especificar el estado "Servicio" mientras se suspende.</span><span class="sxs-lookup"><span data-stu-id="d6333-115">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="d6333-116">(Esto es específico del trabajo).</span><span class="sxs-lookup"><span data-stu-id="d6333-116">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="d6333-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span><span class="sxs-lookup"><span data-stu-id="d6333-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d6333-118">Detiene el trabajo correctamente, guarda los datos, conserva el estado y cierra todos los procesos subyacentes de forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="d6333-118">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="d6333-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="d6333-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d6333-120">Finaliza el trabajo inmediatamente sin necesidad de guardar datos o conservar el estado.</span><span class="sxs-lookup"><span data-stu-id="d6333-120">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d6333-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servicio** (6)</span><span class="sxs-lookup"><span data-stu-id="d6333-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d6333-122">Coloca el trabajo en un estado de servicio específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="d6333-122">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="d6333-123">Es posible reiniciar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="d6333-123">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="d6333-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (7..32767)</span><span class="sxs-lookup"><span data-stu-id="d6333-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="d6333-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="d6333-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="d6333-126">*TimeoutPeriod* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d6333-126">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6333-127">Período de tiempo de espera que especifica la cantidad máxima de tiempo que el cliente espera que se lleve la transición al nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="d6333-127">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="d6333-128">El formato de intervalo debe usarse para especificar el período de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="d6333-128">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="d6333-129">Un valor de 0 o **Null** indica que el cliente no tiene requisitos de tiempo para la transición.</span><span class="sxs-lookup"><span data-stu-id="d6333-129">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="d6333-130">Si esta propiedad no contiene 0 o **Null** y la implementación no admite este parámetro, se debe devolver un código de retorno 4098 **(No** se admite el uso del parámetro de tiempo de espera).</span><span class="sxs-lookup"><span data-stu-id="d6333-130">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6333-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d6333-131">Return value</span></span>

<span data-ttu-id="d6333-132">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve uno de los errores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d6333-132">Returns 0 on success; otherwise, returns one of the following errors.</span></span>

<dl> <dt>

 <span data-ttu-id="d6333-133"> (0)</span><span class="sxs-lookup"><span data-stu-id="d6333-133">(0)</span></span>
</dt> <dt>

 <span data-ttu-id="d6333-134">(32768)</span><span class="sxs-lookup"><span data-stu-id="d6333-134">(32768)</span></span>
</dt> <dt>

 <span data-ttu-id="d6333-135">(32769)</span><span class="sxs-lookup"><span data-stu-id="d6333-135">(32769)</span></span>
</dt> <dt>

 <span data-ttu-id="d6333-136">(32770)</span><span class="sxs-lookup"><span data-stu-id="d6333-136">(32770)</span></span>
</dt> <dt>

 <span data-ttu-id="d6333-137">(32771)</span><span class="sxs-lookup"><span data-stu-id="d6333-137">(32771)</span></span>
</dt> <dt>

 <span data-ttu-id="d6333-138">(32772)</span><span class="sxs-lookup"><span data-stu-id="d6333-138">(32772)</span></span>
</dt> <dt>

 <span data-ttu-id="d6333-139">(32773)</span><span class="sxs-lookup"><span data-stu-id="d6333-139">(32773)</span></span>
</dt> <dt>

 <span data-ttu-id="d6333-140">(32774)</span><span class="sxs-lookup"><span data-stu-id="d6333-140">(32774)</span></span>
</dt> <dt>

 <span data-ttu-id="d6333-141">(32775)</span><span class="sxs-lookup"><span data-stu-id="d6333-141">(32775)</span></span>
</dt> <dt>

 <span data-ttu-id="d6333-142">(32776)</span><span class="sxs-lookup"><span data-stu-id="d6333-142">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="d6333-143">(32777)</span><span class="sxs-lookup"><span data-stu-id="d6333-143">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="d6333-144">(32778)</span><span class="sxs-lookup"><span data-stu-id="d6333-144">(32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d6333-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6333-145">Requirements</span></span>



| <span data-ttu-id="d6333-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6333-146">Requirement</span></span> | <span data-ttu-id="d6333-147">Valor</span><span class="sxs-lookup"><span data-stu-id="d6333-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6333-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6333-148">Minimum supported client</span></span><br/> | <span data-ttu-id="d6333-149">Windows 10, solo aplicaciones de escritorio de la versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="d6333-149">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d6333-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6333-150">Minimum supported server</span></span><br/> | <span data-ttu-id="d6333-151">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d6333-151">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d6333-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d6333-152">Namespace</span></span><br/>                | <span data-ttu-id="d6333-153">Virtualización \\ raíz \\ v2</span><span class="sxs-lookup"><span data-stu-id="d6333-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d6333-154">MOF</span><span class="sxs-lookup"><span data-stu-id="d6333-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6333-155"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6333-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6333-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d6333-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6333-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d6333-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d6333-158">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d6333-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6333-159">**Colección de \_ MsvmReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="d6333-159">**Msvm\_CollectionReferencePointExportJob**</span></span>](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




