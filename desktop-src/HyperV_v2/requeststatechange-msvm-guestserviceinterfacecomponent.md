---
description: Solicita que el estado del componente de la interfaz de servicio invitado cambie al valor especificado.
ms.assetid: D9F7CD03-0D86-4005-A600-5CC7082A5047
title: 'Msvm_GuestServiceInterfaceComponent:: RequestStateChange (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: de5689968d44277b01d6cb2256d41ddbbe573cd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687472"
---
# <a name="msvm_guestserviceinterfacecomponentrequeststatechange-method"></a><span data-ttu-id="61528-103">MSVM \_ GuestServiceInterfaceComponent:: RequestStateChange (método)</span><span class="sxs-lookup"><span data-stu-id="61528-103">Msvm\_GuestServiceInterfaceComponent::RequestStateChange method</span></span>

<span data-ttu-id="61528-104">Solicita que el estado del componente de la interfaz de servicio invitado cambie al valor especificado.</span><span class="sxs-lookup"><span data-stu-id="61528-104">Requests that the state of the guest service interface component be changed to the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="61528-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61528-105">Syntax</span></span>


```C++
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="61528-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61528-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61528-107">*RequestedState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="61528-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61528-108">Tipo: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61528-108">Type: **uint16**</span></span>

<span data-ttu-id="61528-109">El nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="61528-109">The new state.</span></span> <span data-ttu-id="61528-110">La información se coloca en la propiedad **RequestedState** de la instancia de si el código de retorno del método **RequestStateChange** es 0 o 4096.</span><span class="sxs-lookup"><span data-stu-id="61528-110">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="61528-111">Para obtener más información, vea la descripción de las propiedades **EnabledState** y **RequestedState** del elemento.</span><span class="sxs-lookup"><span data-stu-id="61528-111">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="61528-112">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="61528-112">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="61528-113">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="61528-113">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="61528-114">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="61528-114">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="61528-115">**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="61528-115">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="61528-116">**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="61528-116">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="61528-117">**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="61528-117">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="61528-118">**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="61528-118">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="61528-119">Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="61528-119">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="61528-120">**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="61528-120">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="61528-121">**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="61528-121">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="61528-122">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="61528-122">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="61528-123">**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="61528-123">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="61528-124">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="61528-124">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61528-125">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="61528-125">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="61528-126">Referencia opcional a un objeto [**MSVM \_ ConcreteJob**](msvm-concretejob.md) que se devuelve si la operación se ejecuta de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="61528-126">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="61528-127">Si está presente, la referencia devuelta se puede usar para supervisar el progreso y obtener el resultado del método.</span><span class="sxs-lookup"><span data-stu-id="61528-127">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="61528-128">*TimeoutPeriod* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="61528-128">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61528-129">Tipo: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="61528-129">Type: **datetime**</span></span>

<span data-ttu-id="61528-130">Un período de tiempo de espera que especifica la cantidad máxima de tiempo que el cliente espera que se realice la transición al nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="61528-130">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="61528-131">El formato de intervalo debe usarse para especificar el período de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="61528-131">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="61528-132">Un valor de 0 o **null** indica que el cliente no tiene ningún requisito de tiempo para la transición.</span><span class="sxs-lookup"><span data-stu-id="61528-132">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="61528-133">Si esta propiedad no contiene 0 o **null** y la implementación no admite este parámetro, se debe devolver un código de retorno de 4098 (**no se admite el uso del parámetro timeout**).</span><span class="sxs-lookup"><span data-stu-id="61528-133">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61528-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61528-134">Return value</span></span>

<span data-ttu-id="61528-135">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="61528-135">Type: **uint32**</span></span>

<span data-ttu-id="61528-136">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="61528-136">This method returns one of the following values.</span></span>



| <span data-ttu-id="61528-137">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61528-137">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="61528-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="61528-138">Description</span></span>         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="61528-139"><dt>**Completado sin error**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="61528-139"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                           | <span data-ttu-id="61528-140">Correcto.</span><span class="sxs-lookup"><span data-stu-id="61528-140">Success.</span></span><br/> |
| <dl> <span data-ttu-id="61528-141"><dt>**No compatible**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="61528-141"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>                                     |                     |
| <dl> <span data-ttu-id="61528-142"><dt>**Error desconocido/no especificado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="61528-142"><dt>**Unknown/Unspecified Error**</dt> <dt>2</dt></span></span> </dl>                         |                     |
| <dl> <span data-ttu-id="61528-143"><dt>**No se puede completar en el período de tiempo de espera**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="61528-143"><dt>**Can NOT complete within Timeout Period**</dt> <dt>3</dt></span></span> </dl>            |                     |
| <dl> <span data-ttu-id="61528-144">Con <dt>**error**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="61528-144"><dt>**Failed**</dt> <dt>4</dt></span></span> </dl>                                            |                     |
| <dl> <span data-ttu-id="61528-145"><dt>**Parámetro 5 no válido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="61528-145"><dt>**Invalid Parameter**</dt> <dt>5</dt></span></span> </dl>                                 |                     |
| <dl> <span data-ttu-id="61528-146"><dt>**En uso**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="61528-146"><dt>**In Use**</dt> <dt>6</dt></span></span> </dl>                                            |                     |
| <dl> <span data-ttu-id="61528-147"><dt>**DMTF reservado**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="61528-147"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                                    |                     |
| <dl> <span data-ttu-id="61528-148"><dt>**Parámetros de método con comprobación activada: transición iniciada**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="61528-148"><dt>**Method Parameters Checked - Transition Started**</dt> <dt>4096</dt></span></span> </dl> |                     |
| <dl> <span data-ttu-id="61528-149"><dt>**Transición de estado no válida**</dt> <dt>4097</dt></span><span class="sxs-lookup"><span data-stu-id="61528-149"><dt>**Invalid State Transition**</dt> <dt>4097</dt></span></span> </dl>                       |                     |
| <dl> <span data-ttu-id="61528-150"><dt>**No se admite el uso del parámetro Timeout**</dt> <dt>4098</dt></span><span class="sxs-lookup"><span data-stu-id="61528-150"><dt>**Use of Timeout Parameter Not Supported**</dt> <dt>4098</dt></span></span> </dl>         |                     |
| <dl> <span data-ttu-id="61528-151"><dt>**Ocupado**</dt> <dt>4099</dt></span><span class="sxs-lookup"><span data-stu-id="61528-151"><dt>**Busy**</dt> <dt>4099</dt></span></span> </dl>                                           |                     |
| <dl> <span data-ttu-id="61528-152"><dt>**Método reservado**</dt> <dt>4100.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="61528-152"><dt>**Method Reserved**</dt> <dt>4100..32767</dt></span></span> </dl>                         |                     |
| <dl> <span data-ttu-id="61528-153">32768 <dt>**específico del proveedor**</dt> <dt>... 65535</dt></span><span class="sxs-lookup"><span data-stu-id="61528-153"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl>                        |                     |



 

## <a name="requirements"></a><span data-ttu-id="61528-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61528-154">Requirements</span></span>



| <span data-ttu-id="61528-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="61528-155">Requirement</span></span> | <span data-ttu-id="61528-156">Value</span><span class="sxs-lookup"><span data-stu-id="61528-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61528-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61528-157">Minimum supported client</span></span><br/> | <span data-ttu-id="61528-158">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="61528-158">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="61528-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61528-159">Minimum supported server</span></span><br/> | <span data-ttu-id="61528-160">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="61528-160">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="61528-161">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="61528-161">Namespace</span></span><br/>                | <span data-ttu-id="61528-162">\\\\\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="61528-162">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="61528-163">MOF</span><span class="sxs-lookup"><span data-stu-id="61528-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61528-164"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61528-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="61528-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="61528-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61528-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="61528-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="61528-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="61528-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61528-168">**MSVM \_ GuestServiceInterfaceComponent**</span><span class="sxs-lookup"><span data-stu-id="61528-168">**Msvm\_GuestServiceInterfaceComponent**</span></span>](msvm-guestserviceinterfacecomponent.md)
</dt> </dl>

 

