---
description: 'Método RequestStateChange de la Msvm_ReplicationService clase : solicita un cambio de estado.'
ms.assetid: ae799e76-5177-42a5-8591-ceaf15dd7eaf
title: Método RequestStateChange de la Msvm_ReplicationService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e2955bd278742c2a8e152c83ddd61292277baa70
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111533"
---
# <a name="requeststatechange-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="13864-103">Método RequestStateChange de la clase ReplicationService de \_ Msvm</span><span class="sxs-lookup"><span data-stu-id="13864-103">RequestStateChange method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="13864-104">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="13864-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="13864-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13864-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="13864-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13864-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13864-107">*RequestedState* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="13864-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13864-108">El nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="13864-108">The new state.</span></span> <span data-ttu-id="13864-109">La información se coloca en la **propiedad RequestedState** de la instancia si el código de retorno del método **RequestStateChange** es 0 o 4096.</span><span class="sxs-lookup"><span data-stu-id="13864-109">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="13864-110">Para obtener más información, vea la descripción de las propiedades **EnabledState** y **RequestedState** del elemento.</span><span class="sxs-lookup"><span data-stu-id="13864-110">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="13864-111">Debe ser uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="13864-111">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="13864-112">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="13864-112">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="13864-113">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="13864-113">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="13864-114">**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="13864-114">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="13864-115">**Sin** conexión (6)</span><span class="sxs-lookup"><span data-stu-id="13864-115">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="13864-116">**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="13864-116">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="13864-117">**Aplazar** (8)</span><span class="sxs-lookup"><span data-stu-id="13864-117">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="13864-118">**Quiesce** (9)</span><span class="sxs-lookup"><span data-stu-id="13864-118">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="13864-119">**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="13864-119">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="13864-120">**Restablecimiento** (11)</span><span class="sxs-lookup"><span data-stu-id="13864-120">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="13864-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="13864-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="13864-122">**Vendor Reserved** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="13864-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="13864-123">*Trabajo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="13864-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13864-124">Puede contener una referencia al [**\_ objeto ConcreteJob de CIM**](cim-concretejob.md) creado para realizar un seguimiento de la transición de estado iniciada por la invocación del método.</span><span class="sxs-lookup"><span data-stu-id="13864-124">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="13864-125">*TimeoutPeriod* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="13864-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13864-126">Período de tiempo de espera que especifica la cantidad máxima de tiempo que el cliente espera que se lleve la transición al nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="13864-126">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="13864-127">El formato de intervalo debe usarse para especificar el período de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="13864-127">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="13864-128">Un valor de 0 o **Null** indica que el cliente no tiene requisitos de tiempo para la transición.</span><span class="sxs-lookup"><span data-stu-id="13864-128">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="13864-129">Si esta propiedad no contiene 0 o **Null** y la implementación no admite este parámetro, se debe devolver un código de retorno 4098 **(No** se admite el uso del parámetro de tiempo de espera).</span><span class="sxs-lookup"><span data-stu-id="13864-129">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13864-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13864-130">Return value</span></span>

<span data-ttu-id="13864-131">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="13864-131">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="13864-132">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="13864-132">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="13864-133">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="13864-133">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="13864-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13864-134">Requirements</span></span>



| <span data-ttu-id="13864-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="13864-135">Requirement</span></span> | <span data-ttu-id="13864-136">Valor</span><span class="sxs-lookup"><span data-stu-id="13864-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13864-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13864-137">Minimum supported client</span></span><br/> | <span data-ttu-id="13864-138">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="13864-138">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="13864-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13864-139">Minimum supported server</span></span><br/> | <span data-ttu-id="13864-140">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="13864-140">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="13864-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="13864-141">Namespace</span></span><br/>                | <span data-ttu-id="13864-142">Virtualización \\ raíz \\ v2</span><span class="sxs-lookup"><span data-stu-id="13864-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="13864-143">MOF</span><span class="sxs-lookup"><span data-stu-id="13864-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13864-144"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="13864-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="13864-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="13864-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13864-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="13864-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="13864-147">Consulte también</span><span class="sxs-lookup"><span data-stu-id="13864-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13864-148">**ReplicationService de Msvm \_**</span><span class="sxs-lookup"><span data-stu-id="13864-148">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

 




