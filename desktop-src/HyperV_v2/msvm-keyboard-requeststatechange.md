---
description: Solicita que se cambie el estado del elemento.
ms.assetid: D1742588-D932-4FE1-8D2A-E410BEE371FF
title: Método RequestStateChange de la clase Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c3358c6c9907717e536466466dd074faf3a038a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001250"
---
# <a name="requeststatechange-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="29930-103">Método RequestStateChange de la \_ clase de teclado MSVM</span><span class="sxs-lookup"><span data-stu-id="29930-103">RequestStateChange method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="29930-104">Solicita que se cambie el estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="29930-104">Requests that the state of the element be changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="29930-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29930-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="29930-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="29930-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29930-107">*RequestedState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="29930-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29930-108">Nuevo estado solicitado para el elemento.</span><span class="sxs-lookup"><span data-stu-id="29930-108">The new state requested for the element.</span></span> <span data-ttu-id="29930-109">Esta información se colocará en la propiedad **RequestedState** de la instancia si el código de retorno es 0 (' completado sin error '), 3 (' timeout ') o 4096 (0x1000) (' Job Started ').</span><span class="sxs-lookup"><span data-stu-id="29930-109">This information will be placed into the **RequestedState** property of the instance if the return code is 0 ('Completed with No Error'), 3 ('Timeout'), or 4096 (0x1000) ('Job Started').</span></span> <span data-ttu-id="29930-110">Para obtener explicaciones detalladas de los valores de *RequestedState* , consulte la descripción de las propiedades **EnabledState** y **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="29930-110">For detailed explanations of the *RequestedState* values, see the description of the **EnabledState** and **RequestedState** properties.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="29930-111">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="29930-111">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="29930-112">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="29930-112">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="29930-113">**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="29930-113">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="29930-114">**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="29930-114">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="29930-115">**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="29930-115">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="29930-116">**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="29930-116">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="29930-117">Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="29930-117">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="29930-118">**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="29930-118">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="29930-119">**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="29930-119">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="29930-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="29930-120">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="29930-121">**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="29930-121">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="29930-122">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="29930-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29930-123">Referencia al trabajo.</span><span class="sxs-lookup"><span data-stu-id="29930-123">A reference to the job.</span></span> <span data-ttu-id="29930-124">Este parámetro puede ser **null** si la tarea se ha completado.</span><span class="sxs-lookup"><span data-stu-id="29930-124">This parameter can be **Null** if the task is completed.</span></span>

</dd> <dt>

<span data-ttu-id="29930-125">*TimeoutPeriod* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="29930-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29930-126">Cantidad máxima de tiempo que el cliente espera que se lleve a cabo la transición al nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="29930-126">The maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="29930-127">El formato de intervalo debe usarse para especificar este período de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="29930-127">The interval format must be used to specify this time-out period.</span></span> <span data-ttu-id="29930-128">Un valor de 0 o **null** indica que el cliente no tiene ningún requisito de tiempo para la transición.</span><span class="sxs-lookup"><span data-stu-id="29930-128">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="29930-129">Si esta propiedad no contiene 0 o **null**, y la implementación no admite este parámetro, se devuelve un código de retorno de 4098 ("se ha utilizado el parámetro de tiempo de espera no compatible").</span><span class="sxs-lookup"><span data-stu-id="29930-129">If this property does not contain 0 or **Null**, and the implementation does not support this parameter, a return code of 4098 ("Use Of Timeout Parameter Not Supported") is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29930-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="29930-130">Return value</span></span>

<dl> <dt>

<span data-ttu-id="29930-131">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="29930-131">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="29930-132">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="29930-132">**Not supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="29930-133">**Error desconocido o no especificado** (2)</span><span class="sxs-lookup"><span data-stu-id="29930-133">**Unknown or Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="29930-134">**No se puede completar en el período de tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="29930-134">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="29930-135">**Error** (4)</span><span class="sxs-lookup"><span data-stu-id="29930-135">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="29930-136">**Parámetro no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="29930-136">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="29930-137">**En uso** (6)</span><span class="sxs-lookup"><span data-stu-id="29930-137">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="29930-138">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="29930-138">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="29930-139">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="29930-139">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="29930-140">**Transición de estado no válida** (4097)</span><span class="sxs-lookup"><span data-stu-id="29930-140">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="29930-141">**No se admite el uso de parámetros de tiempo de espera** (4098)</span><span class="sxs-lookup"><span data-stu-id="29930-141">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="29930-142">**Ocupado** (4099)</span><span class="sxs-lookup"><span data-stu-id="29930-142">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="29930-143">**Método reservado** (4100.. 32767)</span><span class="sxs-lookup"><span data-stu-id="29930-143">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="29930-144">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="29930-144">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="29930-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29930-145">Requirements</span></span>



| <span data-ttu-id="29930-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="29930-146">Requirement</span></span> | <span data-ttu-id="29930-147">Value</span><span class="sxs-lookup"><span data-stu-id="29930-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29930-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29930-148">Minimum supported client</span></span><br/> | <span data-ttu-id="29930-149">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="29930-149">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="29930-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29930-150">Minimum supported server</span></span><br/> | <span data-ttu-id="29930-151">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="29930-151">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="29930-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="29930-152">Namespace</span></span><br/>                | <span data-ttu-id="29930-153">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="29930-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="29930-154">MOF</span><span class="sxs-lookup"><span data-stu-id="29930-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29930-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29930-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="29930-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="29930-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29930-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="29930-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="29930-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="29930-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29930-159">**\_Teclado MSVM**</span><span class="sxs-lookup"><span data-stu-id="29930-159">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

 




