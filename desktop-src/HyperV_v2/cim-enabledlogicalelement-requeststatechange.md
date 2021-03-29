---
description: Solicita que el estado del elemento se cambie al valor especificado en el parámetro RequestedState.
ms.assetid: 6d0061ad-ca14-400a-b813-af920f231eeb
title: Método RequestStateChange de la clase CIM_EnabledLogicalElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElement.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5b28a2c33b61893be24eacc882b29b5a2be18b14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360758"
---
# <a name="requeststatechange-method-of-the-cim_enabledlogicalelement-class"></a><span data-ttu-id="3dcff-103">Método RequestStateChange de la \_ clase EnabledLogicalElement de CIM</span><span class="sxs-lookup"><span data-stu-id="3dcff-103">RequestStateChange method of the CIM\_EnabledLogicalElement class</span></span>

<span data-ttu-id="3dcff-104">Solicita que el estado del elemento se cambie al valor especificado en el parámetro RequestedState.</span><span class="sxs-lookup"><span data-stu-id="3dcff-104">Requests that the state of the element be changed to the value specified in the RequestedState parameter.</span></span> <span data-ttu-id="3dcff-105">Cuando se produce el cambio de estado solicitado, los EnabledState y RequestedState del elemento serán los mismos.</span><span class="sxs-lookup"><span data-stu-id="3dcff-105">When the requested state change takes place, the EnabledState and RequestedState of the element will be the same.</span></span> <span data-ttu-id="3dcff-106">Invocar varias veces al método RequestStateChange podría provocar que se sobrescriban o se pierdan solicitudes anteriores.</span><span class="sxs-lookup"><span data-stu-id="3dcff-106">Invoking the RequestStateChange method multiple times could result in earlier requests being overwritten or lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dcff-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3dcff-107">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="3dcff-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3dcff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dcff-109">*RequestedState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3dcff-109">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dcff-110">Estado solicitado para el elemento.</span><span class="sxs-lookup"><span data-stu-id="3dcff-110">The state requested for the element.</span></span> <span data-ttu-id="3dcff-111">Esta información se colocará en la propiedad **RequestedState** de la instancia si el código de retorno del método **RequestStateChange** es 0 (' completado sin Error ') o 4096 (0X1000) (' Job Started ').</span><span class="sxs-lookup"><span data-stu-id="3dcff-111">This information will be placed into the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 ('Completed with No Error'), or 4096 (0x1000) ('Job Started').</span></span> <span data-ttu-id="3dcff-112">Consulte la descripción de las propiedades **EnabledState** y **RequestedState** para obtener una explicación detallada de los valores de **requestedstate** .</span><span class="sxs-lookup"><span data-stu-id="3dcff-112">Refer to the description of the **EnabledState** and **RequestedState** properties for the detailed explanations of the **RequestedState** values.</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="3dcff-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Inicio** (2)</span><span class="sxs-lookup"><span data-stu-id="3dcff-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3dcff-114">Cambia el estado a "en ejecución".</span><span class="sxs-lookup"><span data-stu-id="3dcff-114">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="3dcff-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (3)</span><span class="sxs-lookup"><span data-stu-id="3dcff-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3dcff-116">Detiene el trabajo temporalmente.</span><span class="sxs-lookup"><span data-stu-id="3dcff-116">Stops the job temporarily.</span></span> <span data-ttu-id="3dcff-117">La intención es reiniciar posteriormente el trabajo con "Start".</span><span class="sxs-lookup"><span data-stu-id="3dcff-117">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="3dcff-118">Es posible que se pueda entrar en el estado "servicio" mientras se suspende.</span><span class="sxs-lookup"><span data-stu-id="3dcff-118">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="3dcff-119">(Es específico del trabajo).</span><span class="sxs-lookup"><span data-stu-id="3dcff-119">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="3dcff-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Finalizar** (4)</span><span class="sxs-lookup"><span data-stu-id="3dcff-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3dcff-121">Detiene el trabajo correctamente, guarda los datos, conserva el estado y cierra todos los procesos subyacentes de forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="3dcff-121">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="3dcff-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="3dcff-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="3dcff-123">Finaliza el trabajo inmediatamente sin necesidad de guardar los datos ni de conservar el estado.</span><span class="sxs-lookup"><span data-stu-id="3dcff-123">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3dcff-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servicio** (6)</span><span class="sxs-lookup"><span data-stu-id="3dcff-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="3dcff-125">Coloca el trabajo en un estado de servicio específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="3dcff-125">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="3dcff-126">Es posible que se pueda reiniciar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="3dcff-126">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3dcff-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="3dcff-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="3dcff-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="3dcff-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="3dcff-129">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3dcff-129">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3dcff-130">Puede contener una referencia al [**\_ ConcreteJob de CIM**](cim-concretejob.md) creado para realizar el seguimiento de la transición de estado iniciada por la invocación del método.</span><span class="sxs-lookup"><span data-stu-id="3dcff-130">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="3dcff-131">*TimeoutPeriod* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3dcff-131">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dcff-132">Un período de tiempo de espera que especifica la cantidad máxima de tiempo que el cliente espera que se realice la transición al nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="3dcff-132">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="3dcff-133">El formato de intervalo debe usarse para especificar el período de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="3dcff-133">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="3dcff-134">Un valor de 0 o **null** indica que el cliente no tiene ningún requisito de tiempo para la transición.</span><span class="sxs-lookup"><span data-stu-id="3dcff-134">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="3dcff-135">Si esta propiedad no contiene 0 o **null** y la implementación no admite este parámetro, se debe devolver un código de retorno de 4098 (**no se admite el uso del parámetro timeout**).</span><span class="sxs-lookup"><span data-stu-id="3dcff-135">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dcff-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3dcff-136">Return value</span></span>

<span data-ttu-id="3dcff-137">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="3dcff-137">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="3dcff-138">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="3dcff-138">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3dcff-139">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="3dcff-139">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3dcff-140">**Error desconocido o no especificado** (2)</span><span class="sxs-lookup"><span data-stu-id="3dcff-140">**Unknown or Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3dcff-141">**No se puede completar en el período de tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="3dcff-141">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3dcff-142">**Error** (4)</span><span class="sxs-lookup"><span data-stu-id="3dcff-142">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3dcff-143">**Parámetro no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="3dcff-143">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3dcff-144">**En uso** (6)</span><span class="sxs-lookup"><span data-stu-id="3dcff-144">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3dcff-145">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3dcff-145">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3dcff-146">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="3dcff-146">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3dcff-147">**Transición de estado no válida** (4097)</span><span class="sxs-lookup"><span data-stu-id="3dcff-147">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="3dcff-148">**No se admite el uso de parámetros de tiempo de espera** (4098)</span><span class="sxs-lookup"><span data-stu-id="3dcff-148">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="3dcff-149">**Ocupado** (4099)</span><span class="sxs-lookup"><span data-stu-id="3dcff-149">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="3dcff-150">**Método reservado** (4100.. 32767)</span><span class="sxs-lookup"><span data-stu-id="3dcff-150">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="3dcff-151">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="3dcff-151">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3dcff-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3dcff-152">Requirements</span></span>



| <span data-ttu-id="3dcff-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dcff-153">Requirement</span></span> | <span data-ttu-id="3dcff-154">Value</span><span class="sxs-lookup"><span data-stu-id="3dcff-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dcff-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3dcff-155">Minimum supported client</span></span><br/> | <span data-ttu-id="3dcff-156">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3dcff-156">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="3dcff-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3dcff-157">Minimum supported server</span></span><br/> | <span data-ttu-id="3dcff-158">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3dcff-158">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="3dcff-159">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3dcff-159">Namespace</span></span><br/>                | <span data-ttu-id="3dcff-160">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="3dcff-160">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3dcff-161">MOF</span><span class="sxs-lookup"><span data-stu-id="3dcff-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3dcff-162"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3dcff-162"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3dcff-163">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3dcff-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3dcff-164"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3dcff-164"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3dcff-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="3dcff-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dcff-166">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3dcff-166">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

 




