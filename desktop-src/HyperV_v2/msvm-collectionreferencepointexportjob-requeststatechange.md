---
description: Solicita un cambio de estado.
ms.assetid: 34d70ff2-4545-4ab7-8c84-6532c342768b
title: Método RequestStateChange de la clase Msvm_CollectionReferencePointExportJob
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
ms.openlocfilehash: a3e8b3f3a7249896f023734d049fa3fa772514f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688365"
---
# <a name="requeststatechange-method-of-the-msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="80fec-103">Método RequestStateChange de la \_ clase CollectionReferencePointExportJob de MSVM</span><span class="sxs-lookup"><span data-stu-id="80fec-103">RequestStateChange method of the Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="80fec-104">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="80fec-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="80fec-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80fec-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="80fec-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="80fec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80fec-107">*RequestedState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="80fec-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80fec-108">RequestStateChange cambia el estado de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="80fec-108">RequestStateChange changes the state of a job.</span></span> <span data-ttu-id="80fec-109">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="80fec-109">The possible values are as follows:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="80fec-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Inicio** (2)</span><span class="sxs-lookup"><span data-stu-id="80fec-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="80fec-111">Cambia el estado a "en ejecución".</span><span class="sxs-lookup"><span data-stu-id="80fec-111">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="80fec-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (3)</span><span class="sxs-lookup"><span data-stu-id="80fec-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="80fec-113">Detiene el trabajo temporalmente.</span><span class="sxs-lookup"><span data-stu-id="80fec-113">Stops the job temporarily.</span></span> <span data-ttu-id="80fec-114">La intención es reiniciar posteriormente el trabajo con "Start".</span><span class="sxs-lookup"><span data-stu-id="80fec-114">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="80fec-115">Es posible que se pueda entrar en el estado "servicio" mientras se suspende.</span><span class="sxs-lookup"><span data-stu-id="80fec-115">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="80fec-116">(Es específico del trabajo).</span><span class="sxs-lookup"><span data-stu-id="80fec-116">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="80fec-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Finalizar** (4)</span><span class="sxs-lookup"><span data-stu-id="80fec-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="80fec-118">Detiene el trabajo correctamente, guarda los datos, conserva el estado y cierra todos los procesos subyacentes de forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="80fec-118">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="80fec-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="80fec-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="80fec-120">Finaliza el trabajo inmediatamente sin necesidad de guardar los datos ni de conservar el estado.</span><span class="sxs-lookup"><span data-stu-id="80fec-120">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="80fec-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servicio** (6)</span><span class="sxs-lookup"><span data-stu-id="80fec-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="80fec-122">Coloca el trabajo en un estado de servicio específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="80fec-122">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="80fec-123">Es posible que se pueda reiniciar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="80fec-123">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="80fec-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="80fec-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="80fec-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="80fec-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="80fec-126">*TimeoutPeriod* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="80fec-126">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80fec-127">Un período de tiempo de espera que especifica la cantidad máxima de tiempo que el cliente espera que se realice la transición al nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="80fec-127">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="80fec-128">El formato de intervalo debe usarse para especificar el período de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="80fec-128">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="80fec-129">Un valor de 0 o **null** indica que el cliente no tiene ningún requisito de tiempo para la transición.</span><span class="sxs-lookup"><span data-stu-id="80fec-129">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="80fec-130">Si esta propiedad no contiene 0 o **null** y la implementación no admite este parámetro, se debe devolver un código de retorno de 4098 (**no se admite el uso del parámetro timeout**).</span><span class="sxs-lookup"><span data-stu-id="80fec-130">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80fec-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80fec-131">Return value</span></span>

<span data-ttu-id="80fec-132">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve uno de los siguientes errores.</span><span class="sxs-lookup"><span data-stu-id="80fec-132">Returns 0 on success; otherwise, returns one of the following errors.</span></span>

<dl> <dt>

 <span data-ttu-id="80fec-133"> (0)</span><span class="sxs-lookup"><span data-stu-id="80fec-133">(0)</span></span>
</dt> <dt>

 <span data-ttu-id="80fec-134">(32768)</span><span class="sxs-lookup"><span data-stu-id="80fec-134">(32768)</span></span>
</dt> <dt>

 <span data-ttu-id="80fec-135">(32769)</span><span class="sxs-lookup"><span data-stu-id="80fec-135">(32769)</span></span>
</dt> <dt>

 <span data-ttu-id="80fec-136">(32770)</span><span class="sxs-lookup"><span data-stu-id="80fec-136">(32770)</span></span>
</dt> <dt>

 <span data-ttu-id="80fec-137">(32771)</span><span class="sxs-lookup"><span data-stu-id="80fec-137">(32771)</span></span>
</dt> <dt>

 <span data-ttu-id="80fec-138">(32772)</span><span class="sxs-lookup"><span data-stu-id="80fec-138">(32772)</span></span>
</dt> <dt>

 <span data-ttu-id="80fec-139">(32773)</span><span class="sxs-lookup"><span data-stu-id="80fec-139">(32773)</span></span>
</dt> <dt>

 <span data-ttu-id="80fec-140">(32774)</span><span class="sxs-lookup"><span data-stu-id="80fec-140">(32774)</span></span>
</dt> <dt>

 <span data-ttu-id="80fec-141">(32775)</span><span class="sxs-lookup"><span data-stu-id="80fec-141">(32775)</span></span>
</dt> <dt>

 <span data-ttu-id="80fec-142">(32776)</span><span class="sxs-lookup"><span data-stu-id="80fec-142">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="80fec-143">(32777)</span><span class="sxs-lookup"><span data-stu-id="80fec-143">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="80fec-144">(32778)</span><span class="sxs-lookup"><span data-stu-id="80fec-144">(32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="80fec-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80fec-145">Requirements</span></span>



| <span data-ttu-id="80fec-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="80fec-146">Requirement</span></span> | <span data-ttu-id="80fec-147">Value</span><span class="sxs-lookup"><span data-stu-id="80fec-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80fec-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80fec-148">Minimum supported client</span></span><br/> | <span data-ttu-id="80fec-149">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="80fec-149">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="80fec-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80fec-150">Minimum supported server</span></span><br/> | <span data-ttu-id="80fec-151">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="80fec-151">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="80fec-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="80fec-152">Namespace</span></span><br/>                | <span data-ttu-id="80fec-153">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="80fec-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="80fec-154">MOF</span><span class="sxs-lookup"><span data-stu-id="80fec-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80fec-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80fec-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="80fec-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="80fec-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80fec-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="80fec-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="80fec-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="80fec-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80fec-159">**MSVM \_ CollectionReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="80fec-159">**Msvm\_CollectionReferencePointExportJob**</span></span>](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




