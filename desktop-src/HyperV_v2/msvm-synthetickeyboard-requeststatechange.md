---
description: Solicita un cambio de estado.
ms.assetid: 984e8a68-bc95-4a8b-99d6-ac248e96c45e
title: Método RequestStateChange de la clase Msvm_SyntheticKeyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticKeyboard.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9d3527f380bec783bd6305f2ec4fa57c15684dc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652378"
---
# <a name="requeststatechange-method-of-the-msvm_synthetickeyboard-class"></a><span data-ttu-id="42a43-103">Método RequestStateChange de la \_ clase SyntheticKeyboard de MSVM</span><span class="sxs-lookup"><span data-stu-id="42a43-103">RequestStateChange method of the Msvm\_SyntheticKeyboard class</span></span>

<span data-ttu-id="42a43-104">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="42a43-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="42a43-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42a43-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="42a43-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42a43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42a43-107">*RequestedState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="42a43-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42a43-108">Estado solicitado para el elemento.</span><span class="sxs-lookup"><span data-stu-id="42a43-108">The state requested for the element.</span></span> <span data-ttu-id="42a43-109">Esta información se colocará en la propiedad **RequestedState** de la instancia si el código de retorno del método RequestStateChange es 0 (' completado sin error ') o 4096 (0x1000) (' Job Started ').</span><span class="sxs-lookup"><span data-stu-id="42a43-109">This information will be placed into the **RequestedState** property of the instance if the return code of the RequestStateChange method is 0 ('Completed with No Error'), or 4096 (0x1000) ('Job Started').</span></span> <span data-ttu-id="42a43-110">Consulte la descripción de las propiedades **EnabledState** y **RequestedState** para obtener una explicación detallada de los valores de *requestedstate* .</span><span class="sxs-lookup"><span data-stu-id="42a43-110">Refer to the description of the **EnabledState** and **RequestedState** properties for the detailed explanations of the *RequestedState* values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="42a43-111">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="42a43-111">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="42a43-112">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="42a43-112">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="42a43-113">**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="42a43-113">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="42a43-114">**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="42a43-114">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="42a43-115">**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="42a43-115">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="42a43-116">**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="42a43-116">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="42a43-117">Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="42a43-117">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="42a43-118">**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="42a43-118">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="42a43-119">**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="42a43-119">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="42a43-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="42a43-120">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="42a43-121">**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="42a43-121">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="42a43-122">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="42a43-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42a43-123">Puede contener una referencia al [**\_ ConcreteJob de CIM**](cim-concretejob.md) creado para realizar el seguimiento de la transición de estado iniciada por la invocación del método.</span><span class="sxs-lookup"><span data-stu-id="42a43-123">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="42a43-124">*TimeoutPeriod* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="42a43-124">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42a43-125">Un período de tiempo de espera que especifica la cantidad máxima de tiempo que el cliente espera que se realice la transición al nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="42a43-125">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="42a43-126">El formato de intervalo debe usarse para especificar el TimeoutPeriod.</span><span class="sxs-lookup"><span data-stu-id="42a43-126">The interval format must be used to specify the TimeoutPeriod.</span></span> <span data-ttu-id="42a43-127">Un valor de 0 o un parámetro null indica que el cliente no tiene ningún requisito de tiempo para la transición.</span><span class="sxs-lookup"><span data-stu-id="42a43-127">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

<span data-ttu-id="42a43-128">Si esta propiedad no contiene 0 o NULL y la implementación no admite este parámetro, se devolverá el código de retorno "uso del parámetro de tiempo de espera no admitido".</span><span class="sxs-lookup"><span data-stu-id="42a43-128">If this property does not contain 0 or null and the implementation does not support this parameter, a return code of 'Use Of Timeout Parameter Not Supported' shall be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42a43-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42a43-129">Return value</span></span>

<span data-ttu-id="42a43-130">Si se ejecuta correctamente, devuelve 0; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="42a43-130">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="42a43-131">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="42a43-131">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="42a43-132">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="42a43-132">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="42a43-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42a43-133">Requirements</span></span>



| <span data-ttu-id="42a43-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="42a43-134">Requirement</span></span> | <span data-ttu-id="42a43-135">Value</span><span class="sxs-lookup"><span data-stu-id="42a43-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42a43-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42a43-136">Minimum supported client</span></span><br/> | <span data-ttu-id="42a43-137">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="42a43-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="42a43-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42a43-138">Minimum supported server</span></span><br/> | <span data-ttu-id="42a43-139">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="42a43-139">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="42a43-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="42a43-140">Namespace</span></span><br/>                | <span data-ttu-id="42a43-141">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="42a43-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="42a43-142">MOF</span><span class="sxs-lookup"><span data-stu-id="42a43-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42a43-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="42a43-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="42a43-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="42a43-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42a43-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="42a43-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="42a43-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="42a43-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a43-147">**MSVM \_ SyntheticKeyboard**</span><span class="sxs-lookup"><span data-stu-id="42a43-147">**Msvm\_SyntheticKeyboard**</span></span>](msvm-synthetickeyboard.md)
</dt> </dl>

 

 




