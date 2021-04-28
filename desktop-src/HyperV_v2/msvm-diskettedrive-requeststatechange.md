---
description: 'Método RequestStateChange de la Msvm_DisketteDrive clase : solicita un cambio de estado.'
ms.assetid: 349081c0-65d8-470d-8d84-7c616c0f81b6
title: Método RequestStateChange de la Msvm_DisketteDrive clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteDrive.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 06d61557ca765721660937592f59667f5e6b3fc9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119173"
---
# <a name="requeststatechange-method-of-the-msvm_diskettedrive-class"></a><span data-ttu-id="c92b1-103">Método RequestStateChange de la clase \_ DisketteDrive de Msvm</span><span class="sxs-lookup"><span data-stu-id="c92b1-103">RequestStateChange method of the Msvm\_DisketteDrive class</span></span>

<span data-ttu-id="c92b1-104">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="c92b1-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="c92b1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c92b1-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="c92b1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c92b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c92b1-107">*RequestedState* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c92b1-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c92b1-108">Estado solicitado para el elemento.</span><span class="sxs-lookup"><span data-stu-id="c92b1-108">The state requested for the element.</span></span> <span data-ttu-id="c92b1-109">Esta información se colocará en la propiedad RequestedState de la instancia si el código devuelto del método RequestStateChange es 0 ('Completed with No Error') o 4096 (0x1000) ('Job Started').</span><span class="sxs-lookup"><span data-stu-id="c92b1-109">This information will be placed into the RequestedState property of the instance if the return code of the RequestStateChange method is 0 ('Completed with No Error'), or 4096 (0x1000) ('Job Started').</span></span> <span data-ttu-id="c92b1-110">Consulte la descripción de las propiedades EnabledState y RequestedState para obtener explicaciones detalladas de los valores RequestedState.</span><span class="sxs-lookup"><span data-stu-id="c92b1-110">Refer to the description of the EnabledState and RequestedState properties for the detailed explanations of the RequestedState values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c92b1-111">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="c92b1-111">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c92b1-112">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="c92b1-112">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="c92b1-113">**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="c92b1-113">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="c92b1-114">**Sin** conexión (6)</span><span class="sxs-lookup"><span data-stu-id="c92b1-114">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="c92b1-115">**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="c92b1-115">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="c92b1-116">**Aplazar** (8)</span><span class="sxs-lookup"><span data-stu-id="c92b1-116">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="c92b1-117">**Quiesce** (9)</span><span class="sxs-lookup"><span data-stu-id="c92b1-117">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="c92b1-118">**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="c92b1-118">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="c92b1-119">**Restablecimiento** (11)</span><span class="sxs-lookup"><span data-stu-id="c92b1-119">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c92b1-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="c92b1-120">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="c92b1-121">**Vendor Reserved** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="c92b1-121">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="c92b1-122">*Trabajo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c92b1-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c92b1-123">Puede contener una referencia al Trabajo concreto creado para realizar un seguimiento de la transición de estado iniciada por la invocación del método .</span><span class="sxs-lookup"><span data-stu-id="c92b1-123">May contain a reference to the ConcreteJob created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="c92b1-124">*TimeoutPeriod* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c92b1-124">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c92b1-125">Período de tiempo de espera que especifica la cantidad máxima de tiempo que el cliente espera que se lleve la transición al nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="c92b1-125">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="c92b1-126">El formato de intervalo debe usarse para especificar timeoutPeriod.</span><span class="sxs-lookup"><span data-stu-id="c92b1-126">The interval format must be used to specify the TimeoutPeriod.</span></span> <span data-ttu-id="c92b1-127">Un valor de 0 o un parámetro NULL indica que el cliente no tiene requisitos de tiempo para la transición.</span><span class="sxs-lookup"><span data-stu-id="c92b1-127">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

<span data-ttu-id="c92b1-128">Si esta propiedad no contiene 0 o NULL y la implementación no admite este parámetro, se devolverá un código de retorno de "No se admite el uso del parámetro de tiempo de espera".</span><span class="sxs-lookup"><span data-stu-id="c92b1-128">If this property does not contain 0 or null and the implementation does not support this parameter, a return code of 'Use Of Timeout Parameter Not Supported' shall be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c92b1-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c92b1-129">Return value</span></span>

<span data-ttu-id="c92b1-130">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="c92b1-130">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="c92b1-131">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="c92b1-131">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c92b1-132">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="c92b1-132">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c92b1-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c92b1-133">Requirements</span></span>



| <span data-ttu-id="c92b1-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c92b1-134">Requirement</span></span> | <span data-ttu-id="c92b1-135">Valor</span><span class="sxs-lookup"><span data-stu-id="c92b1-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c92b1-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c92b1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c92b1-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c92b1-137">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="c92b1-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c92b1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c92b1-139">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c92b1-139">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="c92b1-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c92b1-140">Namespace</span></span><br/>                | <span data-ttu-id="c92b1-141">Virtualización \\ raíz \\ v2</span><span class="sxs-lookup"><span data-stu-id="c92b1-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c92b1-142">MOF</span><span class="sxs-lookup"><span data-stu-id="c92b1-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c92b1-143"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="c92b1-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c92b1-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c92b1-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c92b1-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c92b1-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c92b1-146">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c92b1-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c92b1-147">**Msvm \_ DisketteDrive**</span><span class="sxs-lookup"><span data-stu-id="c92b1-147">**Msvm\_DisketteDrive**</span></span>](msvm-diskettedrive.md)
</dt> </dl>

 

 




