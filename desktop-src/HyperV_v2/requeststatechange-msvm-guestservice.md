---
description: Solicita que el estado del servicio invitado cambie al valor especificado.
ms.assetid: F2853BB3-4074-431C-9E10-26AA0757FE99
title: 'Msvm_GuestService:: RequestStateChange (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1360c36b58c96b7e621e5f339bd503ce4f1390b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815222"
---
# <a name="msvm_guestservicerequeststatechange-method"></a><span data-ttu-id="b17bf-103">MSVM \_ GuestService:: RequestStateChange (método)</span><span class="sxs-lookup"><span data-stu-id="b17bf-103">Msvm\_GuestService::RequestStateChange method</span></span>

<span data-ttu-id="b17bf-104">Solicita que el estado del servicio invitado cambie al valor especificado.</span><span class="sxs-lookup"><span data-stu-id="b17bf-104">Requests that the state of the guest service be changed to the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b17bf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b17bf-105">Syntax</span></span>


```C++
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="b17bf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b17bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b17bf-107">*RequestedState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b17bf-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b17bf-108">El nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="b17bf-108">The new state.</span></span> <span data-ttu-id="b17bf-109">La información se coloca en la propiedad **RequestedState** de la instancia de si el código de retorno del método **RequestStateChange** es 0 o 4096.</span><span class="sxs-lookup"><span data-stu-id="b17bf-109">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="b17bf-110">Para obtener más información, vea la descripción de las propiedades **EnabledState** y **RequestedState** del elemento.</span><span class="sxs-lookup"><span data-stu-id="b17bf-110">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="b17bf-111">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="b17bf-111">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b17bf-112">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="b17bf-112">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b17bf-113">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="b17bf-113">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="b17bf-114">**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="b17bf-114">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="b17bf-115">**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="b17bf-115">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="b17bf-116">**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="b17bf-116">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="b17bf-117">**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="b17bf-117">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="b17bf-118">Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="b17bf-118">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="b17bf-119">**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="b17bf-119">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="b17bf-120">**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="b17bf-120">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="b17bf-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="b17bf-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="b17bf-122">**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="b17bf-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="b17bf-123">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b17bf-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b17bf-124">Referencia opcional a un objeto [**\_ ConcreteJob de CIM**](cim-concretejob.md) que se devuelve si la operación se ejecuta de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b17bf-124">An optional reference to a [**CIM\_ConcreteJob**](cim-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="b17bf-125">Si está presente, la referencia devuelta se puede usar para supervisar el progreso y obtener el resultado del método.</span><span class="sxs-lookup"><span data-stu-id="b17bf-125">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="b17bf-126">*TimeoutPeriod* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b17bf-126">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b17bf-127">Un período de tiempo de espera que especifica la cantidad máxima de tiempo que el cliente espera que se realice la transición al nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="b17bf-127">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="b17bf-128">El formato de intervalo debe usarse para especificar el período de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="b17bf-128">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="b17bf-129">Un valor de 0 o **null** indica que el cliente no tiene ningún requisito de tiempo para la transición.</span><span class="sxs-lookup"><span data-stu-id="b17bf-129">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="b17bf-130">Si esta propiedad no contiene 0 o **null** y la implementación no admite este parámetro, se debe devolver un código de retorno de 4098 (**no se admite el uso del parámetro timeout**).</span><span class="sxs-lookup"><span data-stu-id="b17bf-130">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b17bf-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b17bf-131">Return value</span></span>

<span data-ttu-id="b17bf-132">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="b17bf-132">This method returns one of the following values.</span></span>



| <span data-ttu-id="b17bf-133">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b17bf-133">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="b17bf-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="b17bf-134">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b17bf-135"><dt>**Completado sin error**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b17bf-135"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                           | <span data-ttu-id="b17bf-136">Correcto.</span><span class="sxs-lookup"><span data-stu-id="b17bf-136">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="b17bf-137"><dt>**No compatible**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b17bf-137"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>                                     |                                                                                    |
| <dl> <span data-ttu-id="b17bf-138"><dt>**Parámetros de método con comprobación activada: transición iniciada**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="b17bf-138"><dt>**Method Parameters Checked - Transition Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="b17bf-139">La transición es asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b17bf-139">The transition is asynchronous.</span></span><br/>                                         |
| <dl> <span data-ttu-id="b17bf-140"><dt>**No se admite el uso del parámetro Timeout**</dt> <dt>4098</dt></span><span class="sxs-lookup"><span data-stu-id="b17bf-140"><dt>**Use of Timeout Parameter Not Supported**</dt> <dt>4098</dt></span></span> </dl>         |                                                                                    |
| <dl> <span data-ttu-id="b17bf-141"><dt>**Acceso Denegado**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="b17bf-141"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="b17bf-142">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="b17bf-142">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="b17bf-143"><dt>**Estado no válido para esta operación**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="b17bf-143"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>              | <span data-ttu-id="b17bf-144">No se admite el valor especificado en el parámetro *RequestedState* .</span><span class="sxs-lookup"><span data-stu-id="b17bf-144">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b17bf-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b17bf-145">Requirements</span></span>



| <span data-ttu-id="b17bf-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="b17bf-146">Requirement</span></span> | <span data-ttu-id="b17bf-147">Value</span><span class="sxs-lookup"><span data-stu-id="b17bf-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b17bf-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b17bf-148">Minimum supported client</span></span><br/> | <span data-ttu-id="b17bf-149">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="b17bf-149">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b17bf-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b17bf-150">Minimum supported server</span></span><br/> | <span data-ttu-id="b17bf-151">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b17bf-151">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b17bf-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b17bf-152">Namespace</span></span><br/>                | <span data-ttu-id="b17bf-153">\\\\\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b17bf-153">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="b17bf-154">MOF</span><span class="sxs-lookup"><span data-stu-id="b17bf-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b17bf-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b17bf-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b17bf-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b17bf-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b17bf-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b17bf-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b17bf-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="b17bf-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b17bf-159">**MSVM \_ GuestService**</span><span class="sxs-lookup"><span data-stu-id="b17bf-159">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




