---
description: 'Método RequestStateChange de la Msvm_Ps2Mouse: solicita un cambio de estado.'
ms.assetid: a61c17a8-f89d-47aa-8c4f-46ccf478103e
title: Método RequestStateChange de la Msvm_Ps2Mouse clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 878b0977a244d4b098dfa449f3c778c33e909111
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118823"
---
# <a name="requeststatechange-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="94d74-103">Método RequestStateChange de la clase \_ Ps2Mouse de Msvm</span><span class="sxs-lookup"><span data-stu-id="94d74-103">RequestStateChange method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="94d74-104">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="94d74-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="94d74-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94d74-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="94d74-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94d74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94d74-107">*RequestedState* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="94d74-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94d74-108">Estado solicitado para el elemento.</span><span class="sxs-lookup"><span data-stu-id="94d74-108">The state requested for the element.</span></span> <span data-ttu-id="94d74-109">Esta información se colocará en la propiedad RequestedState de la instancia si el código de retorno del método RequestStateChange es 0 ('Completed with No Error') o 4096 (0x1000) ('Job Started').</span><span class="sxs-lookup"><span data-stu-id="94d74-109">This information will be placed into the RequestedState property of the instance if the return code of the RequestStateChange method is 0 ('Completed with No Error'), or 4096 (0x1000) ('Job Started').</span></span> <span data-ttu-id="94d74-110">Consulte la descripción de las propiedades EnabledState y RequestedState para obtener explicaciones detalladas de los valores requestedState.</span><span class="sxs-lookup"><span data-stu-id="94d74-110">Refer to the description of the EnabledState and RequestedState properties for the detailed explanations of the RequestedState values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="94d74-111">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="94d74-111">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="94d74-112">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="94d74-112">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="94d74-113">**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="94d74-113">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="94d74-114">**Sin** conexión (6)</span><span class="sxs-lookup"><span data-stu-id="94d74-114">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="94d74-115">**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="94d74-115">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="94d74-116">**Aplazar** (8)</span><span class="sxs-lookup"><span data-stu-id="94d74-116">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="94d74-117">**Quiesce** (9)</span><span class="sxs-lookup"><span data-stu-id="94d74-117">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="94d74-118">**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="94d74-118">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="94d74-119">**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="94d74-119">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="94d74-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="94d74-120">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="94d74-121">**Vendor Reserved** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="94d74-121">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="94d74-122">*Trabajo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="94d74-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94d74-123">Puede contener una referencia a la instancia de ConcreteJob creada para realizar un seguimiento de la transición de estado iniciada por la invocación del método.</span><span class="sxs-lookup"><span data-stu-id="94d74-123">May contain a reference to the ConcreteJob created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="94d74-124">*TimeoutPeriod* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="94d74-124">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94d74-125">Período de tiempo de espera que especifica la cantidad máxima de tiempo que el cliente espera que se lleve la transición al nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="94d74-125">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="94d74-126">El formato de intervalo debe usarse para especificar timeoutPeriod.</span><span class="sxs-lookup"><span data-stu-id="94d74-126">The interval format must be used to specify the TimeoutPeriod.</span></span> <span data-ttu-id="94d74-127">Un valor de 0 o un parámetro null indica que el cliente no tiene ningún requisito de tiempo para la transición.</span><span class="sxs-lookup"><span data-stu-id="94d74-127">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

<span data-ttu-id="94d74-128">Si esta propiedad no contiene 0 o NULL y la implementación no admite este parámetro, se devolverá un código de retorno "Use Of Timeout Parameter Not Supported" (No se admite el parámetro de tiempo de espera).</span><span class="sxs-lookup"><span data-stu-id="94d74-128">If this property does not contain 0 or null and the implementation does not support this parameter, a return code of 'Use Of Timeout Parameter Not Supported' shall be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94d74-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94d74-129">Return value</span></span>

<span data-ttu-id="94d74-130">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="94d74-130">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="94d74-131">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="94d74-131">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="94d74-132">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="94d74-132">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="94d74-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94d74-133">Requirements</span></span>



| <span data-ttu-id="94d74-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="94d74-134">Requirement</span></span> | <span data-ttu-id="94d74-135">Valor</span><span class="sxs-lookup"><span data-stu-id="94d74-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94d74-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94d74-136">Minimum supported client</span></span><br/> | <span data-ttu-id="94d74-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="94d74-137">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="94d74-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94d74-138">Minimum supported server</span></span><br/> | <span data-ttu-id="94d74-139">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="94d74-139">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="94d74-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="94d74-140">Namespace</span></span><br/>                | <span data-ttu-id="94d74-141">Virtualización \\ raíz \\ v2</span><span class="sxs-lookup"><span data-stu-id="94d74-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="94d74-142">MOF</span><span class="sxs-lookup"><span data-stu-id="94d74-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94d74-143"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="94d74-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="94d74-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="94d74-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94d74-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="94d74-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="94d74-146">Consulte también</span><span class="sxs-lookup"><span data-stu-id="94d74-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94d74-147">**Msvm \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="94d74-147">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

 




