---
description: Solicita que el estado de la máquina virtual se cambie al valor especificado.
ms.assetid: 87BE4C7D-604B-4F8D-B4DC-89BD563E3999
title: Método RequestStateChange de la clase Msvm_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 291d72797b1ee765507a3d23921cd518cf605354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279661"
---
# <a name="requeststatechange-method-of-the-msvm_computersystem-class"></a><span data-ttu-id="b0274-103">Método RequestStateChange de la \_ clase MSVM ComputerSystem</span><span class="sxs-lookup"><span data-stu-id="b0274-103">RequestStateChange method of the Msvm\_ComputerSystem class</span></span>

<span data-ttu-id="b0274-104">Solicita que el estado de la máquina virtual se cambie al valor especificado.</span><span class="sxs-lookup"><span data-stu-id="b0274-104">Requests that the state of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="b0274-105">Invocar varias veces al método **RequestStateChange** podría provocar que se sobrescriban o se pierdan solicitudes anteriores.</span><span class="sxs-lookup"><span data-stu-id="b0274-105">Invoking the **RequestStateChange** method multiple times could result in earlier requests being overwritten or lost.</span></span> <span data-ttu-id="b0274-106">Este método solo se admite para las instancias de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representan una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b0274-106">This method is only supported for instances of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represent a virtual machine.</span></span>

<span data-ttu-id="b0274-107">Mientras el cambio de estado está en curso, la propiedad **requestedstate** cambia al valor del parámetro *RequestedState* .</span><span class="sxs-lookup"><span data-stu-id="b0274-107">While the state change is in progress, the **RequestedState** property is changed to the value of the *RequestedState* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0274-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0274-108">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="b0274-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0274-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0274-110">*RequestedState* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b0274-110">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0274-111">Tipo: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0274-111">Type: **uint16**</span></span>

<span data-ttu-id="b0274-112">El nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="b0274-112">The new state.</span></span> <span data-ttu-id="b0274-113">Los valores mayores que 32767 son los valores propuestos de **DMTF** y están sujetos a cambios.</span><span class="sxs-lookup"><span data-stu-id="b0274-113">Values that are greater than 32767 are **DMTF** proposed values and are subject to change.</span></span>

<span data-ttu-id="b0274-114">Estos son los valores posibles:</span><span class="sxs-lookup"><span data-stu-id="b0274-114">Here are possible values:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b0274-115"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="b0274-115"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b0274-116">Corresponde a [**CIM \_ EnabledLogicalElement. EnabledState**](/previous-versions//cc136818(v=vs.85)) = Other.</span><span class="sxs-lookup"><span data-stu-id="b0274-116">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Other.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b0274-117"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="b0274-117"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b0274-118">Corresponde a [**CIM \_ EnabledLogicalElement. EnabledState**](/previous-versions//cc136818(v=vs.85)) = enabled.</span><span class="sxs-lookup"><span data-stu-id="b0274-118">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Enabled.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b0274-119"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="b0274-119"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b0274-120">Corresponde a [**CIM \_ EnabledLogicalElement. EnabledState**](/previous-versions//cc136818(v=vs.85)) = Disabled.</span><span class="sxs-lookup"><span data-stu-id="b0274-120">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Disabled.</span></span>

</dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="b0274-121"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Apagar** (4)</span><span class="sxs-lookup"><span data-stu-id="b0274-121"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b0274-122">Válido solo en la versión 1 (V1) de Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="b0274-122">Valid in version 1 (V1) of Hyper-V only.</span></span> <span data-ttu-id="b0274-123">La máquina virtual se está cerrando a través del servicio de cierre.</span><span class="sxs-lookup"><span data-stu-id="b0274-123">The virtual machine is shutting down via the shutdown service.</span></span> <span data-ttu-id="b0274-124">Corresponde a [**CIM \_ EnabledLogicalElement. EnabledState**](/previous-versions//cc136818(v=vs.85)) = ShuttingDown.</span><span class="sxs-lookup"><span data-stu-id="b0274-124">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = ShuttingDown.</span></span>

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="b0274-125"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="b0274-125"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b0274-126">Corresponde a [**CIM \_ EnabledLogicalElement. EnabledState**](/previous-versions//cc136818(v=vs.85)) = Enabled pero sin conexión.</span><span class="sxs-lookup"><span data-stu-id="b0274-126">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Enabled but offline.</span></span>

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="b0274-127"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Prueba** (7)</span><span class="sxs-lookup"><span data-stu-id="b0274-127"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="b0274-128"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Diferir** (8)</span><span class="sxs-lookup"><span data-stu-id="b0274-128"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="b0274-129"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="b0274-129"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>


</dt> <dd>

<span data-ttu-id="b0274-130">Corresponde a [**CIM \_ EnabledLogicalElement. EnabledState**](/previous-versions//cc136818(v=vs.85)) = reposo, habilitado pero en pausa.</span><span class="sxs-lookup"><span data-stu-id="b0274-130">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Quiesce, Enabled but paused.</span></span>

</dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="b0274-131"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicio** (10)</span><span class="sxs-lookup"><span data-stu-id="b0274-131"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>


</dt> <dd>

<span data-ttu-id="b0274-132">Transición de estado desde **OFF** o **guardado** a en **ejecución**.</span><span class="sxs-lookup"><span data-stu-id="b0274-132">State transition from **Off** or **Saved** to **Running**.</span></span>

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="b0274-133"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Restablecer** (11)</span><span class="sxs-lookup"><span data-stu-id="b0274-133"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>


</dt> <dd>

<span data-ttu-id="b0274-134">Restablezca la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b0274-134">Reset the virtual machine.</span></span> <span data-ttu-id="b0274-135">Corresponde a [**CIM \_ EnabledLogicalElement. EnabledState**](/previous-versions//cc136818(v=vs.85)) = RESET.</span><span class="sxs-lookup"><span data-stu-id="b0274-135">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Reset.</span></span>

</dd> <dt>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>

<span data-ttu-id="b0274-136"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Guardar** (32773)</span><span class="sxs-lookup"><span data-stu-id="b0274-136"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Saving** (32773)</span></span>


</dt> <dd>

<span data-ttu-id="b0274-137">En la versión 1 (V1) de Hyper-V, corresponde a **EnabledStateSaving**.</span><span class="sxs-lookup"><span data-stu-id="b0274-137">In version 1 (V1) of Hyper-V, corresponds to **EnabledStateSaving**.</span></span>

</dd> <dt>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>

<span data-ttu-id="b0274-138"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Pausar** (32776)</span><span class="sxs-lookup"><span data-stu-id="b0274-138"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Pausing** (32776)</span></span>


</dt> <dd>

<span data-ttu-id="b0274-139">En la versión 1 (V1) de Hyper-V, corresponde a **EnabledStatePausing**.</span><span class="sxs-lookup"><span data-stu-id="b0274-139">In version 1 (V1) of Hyper-V, corresponds to **EnabledStatePausing**.</span></span>

</dd> <dt>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>

<span data-ttu-id="b0274-140"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Reanudar** (32777)</span><span class="sxs-lookup"><span data-stu-id="b0274-140"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Resuming** (32777)</span></span>


</dt> <dd>

<span data-ttu-id="b0274-141">En la versión 1 (V1) de Hyper-V, corresponde a **EnabledStateResuming**.</span><span class="sxs-lookup"><span data-stu-id="b0274-141">In version 1 (V1) of Hyper-V, corresponds to **EnabledStateResuming**.</span></span> <span data-ttu-id="b0274-142">Transición de estado de **pausa** a en **ejecución**.</span><span class="sxs-lookup"><span data-stu-id="b0274-142">State transition from **Paused** to **Running**.</span></span>

</dd> <dt>

<span id="FastSaved"></span><span id="fastsaved"></span><span id="FASTSAVED"></span>

<span data-ttu-id="b0274-143"><span id="FastSaved"></span><span id="fastsaved"></span><span id="FASTSAVED"></span>**FastSaved** (32779)</span><span class="sxs-lookup"><span data-stu-id="b0274-143"><span id="FastSaved"></span><span id="fastsaved"></span><span id="FASTSAVED"></span>**FastSaved** (32779)</span></span>


</dt> <dd>

<span data-ttu-id="b0274-144">Corresponde a **EnabledStateFastSuspend**.</span><span class="sxs-lookup"><span data-stu-id="b0274-144">Corresponds to **EnabledStateFastSuspend**.</span></span>

</dd> <dt>

<span id="FastSaving"></span><span id="fastsaving"></span><span id="FASTSAVING"></span>

<span data-ttu-id="b0274-145"><span id="FastSaving"></span><span id="fastsaving"></span><span id="FASTSAVING"></span>**FastSaving** (32780)</span><span class="sxs-lookup"><span data-stu-id="b0274-145"><span id="FastSaving"></span><span id="fastsaving"></span><span id="FASTSAVING"></span>**FastSaving** (32780)</span></span>


</dt> <dd>

<span data-ttu-id="b0274-146">Corresponde a **EnabledStateFastSuspending**.</span><span class="sxs-lookup"><span data-stu-id="b0274-146">Corresponds to **EnabledStateFastSuspending**.</span></span> <span data-ttu-id="b0274-147">Transición de estado de **ejecución** a **FastSaved**.</span><span class="sxs-lookup"><span data-stu-id="b0274-147">State transition from **Running** to **FastSaved**.</span></span>

</dd> </dl>

<span data-ttu-id="b0274-148">Estos valores representan Estados críticos:</span><span class="sxs-lookup"><span data-stu-id="b0274-148">These values represent critical states:</span></span>

<dt>

<span id="RunningCritical"></span><span id="runningcritical"></span><span id="RUNNINGCRITICAL"></span>

<span data-ttu-id="b0274-149">**RunningCritical** (32781)</span><span class="sxs-lookup"><span data-stu-id="b0274-149">**RunningCritical** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="OffCritical"></span><span id="offcritical"></span><span id="OFFCRITICAL"></span>

<span data-ttu-id="b0274-150">**OffCritical** (32782)</span><span class="sxs-lookup"><span data-stu-id="b0274-150">**OffCritical** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="StoppingCritical"></span><span id="stoppingcritical"></span><span id="STOPPINGCRITICAL"></span>

<span data-ttu-id="b0274-151">**StoppingCritical** (32783)</span><span class="sxs-lookup"><span data-stu-id="b0274-151">**StoppingCritical** (32783)</span></span>


</dt> <dd></dd> <dt>

<span id="SavedCritical"></span><span id="savedcritical"></span><span id="SAVEDCRITICAL"></span>

<span data-ttu-id="b0274-152">**SavedCritical** (32784)</span><span class="sxs-lookup"><span data-stu-id="b0274-152">**SavedCritical** (32784)</span></span>


</dt> <dd></dd> <dt>

<span id="PausedCritical"></span><span id="pausedcritical"></span><span id="PAUSEDCRITICAL"></span>

<span data-ttu-id="b0274-153">**PausedCritical** (32785)</span><span class="sxs-lookup"><span data-stu-id="b0274-153">**PausedCritical** (32785)</span></span>


</dt> <dd></dd> <dt>

<span id="StartingCritical"></span><span id="startingcritical"></span><span id="STARTINGCRITICAL"></span>

<span data-ttu-id="b0274-154">**StartingCritical** (32786)</span><span class="sxs-lookup"><span data-stu-id="b0274-154">**StartingCritical** (32786)</span></span>


</dt> <dd></dd> <dt>

<span id="ResetCritical"></span><span id="resetcritical"></span><span id="RESETCRITICAL"></span>

<span data-ttu-id="b0274-155">**ResetCritical** (32787)</span><span class="sxs-lookup"><span data-stu-id="b0274-155">**ResetCritical** (32787)</span></span>


</dt> <dd></dd> <dt>

<span id="SavingCritical"></span><span id="savingcritical"></span><span id="SAVINGCRITICAL"></span>

<span data-ttu-id="b0274-156">**SavingCritical** (32788)</span><span class="sxs-lookup"><span data-stu-id="b0274-156">**SavingCritical** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="PausingCritical"></span><span id="pausingcritical"></span><span id="PAUSINGCRITICAL"></span>

<span data-ttu-id="b0274-157">**PausingCritical** (32789)</span><span class="sxs-lookup"><span data-stu-id="b0274-157">**PausingCritical** (32789)</span></span>


</dt> <dd></dd> <dt>

<span id="ResumingCritical"></span><span id="resumingcritical"></span><span id="RESUMINGCRITICAL"></span>

<span data-ttu-id="b0274-158">**ResumingCritical** (32790)</span><span class="sxs-lookup"><span data-stu-id="b0274-158">**ResumingCritical** (32790)</span></span>


</dt> <dd></dd> <dt>

<span id="FastSavedCritical"></span><span id="fastsavedcritical"></span><span id="FASTSAVEDCRITICAL"></span>

<span data-ttu-id="b0274-159">**FastSavedCritical** (32791)</span><span class="sxs-lookup"><span data-stu-id="b0274-159">**FastSavedCritical** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="FastSavingCritical"></span><span id="fastsavingcritical"></span><span id="FASTSAVINGCRITICAL"></span>

<span data-ttu-id="b0274-160">**FastSavingCritical** (32792)</span><span class="sxs-lookup"><span data-stu-id="b0274-160">**FastSavingCritical** (32792)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="b0274-161">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b0274-161">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0274-162">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="b0274-162">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="b0274-163">Referencia opcional a un objeto [**MSVM \_ ConcreteJob**](msvm-concretejob.md) que se devuelve si la operación se ejecuta de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b0274-163">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="b0274-164">Si está presente, la referencia devuelta se puede usar para supervisar el progreso y obtener el resultado del método.</span><span class="sxs-lookup"><span data-stu-id="b0274-164">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="b0274-165">*TimeoutPeriod* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b0274-165">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0274-166">Tipo: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b0274-166">Type: **datetime**</span></span>

<span data-ttu-id="b0274-167">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b0274-167">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0274-168">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0274-168">Return value</span></span>

<span data-ttu-id="b0274-169">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b0274-169">Type: **uint32**</span></span>

<span data-ttu-id="b0274-170">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="b0274-170">This method returns one of the following values.</span></span>



| <span data-ttu-id="b0274-171">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0274-171">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="b0274-172">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0274-172">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b0274-173"><dt>**Completado sin error**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b0274-173"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                           | <span data-ttu-id="b0274-174">Correcto.</span><span class="sxs-lookup"><span data-stu-id="b0274-174">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="b0274-175"><dt>**Parámetros de método con comprobación activada: transición iniciada**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="b0274-175"><dt>**Method Parameters Checked - Transition Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="b0274-176">La transición es asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b0274-176">The transition is asynchronous.</span></span><br/>                                         |
| <dl> <span data-ttu-id="b0274-177"><dt>**Acceso Denegado**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="b0274-177"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="b0274-178">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="b0274-178">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="b0274-179"><dt></dt><dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="b0274-179"><dt></dt> <dt>32768</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="b0274-180"><dt></dt><dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="b0274-180"><dt></dt> <dt>32770</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="b0274-181"><dt></dt><dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="b0274-181"><dt></dt> <dt>32771</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="b0274-182"><dt></dt><dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="b0274-182"><dt></dt> <dt>32772</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="b0274-183"><dt></dt><dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="b0274-183"><dt></dt> <dt>32773</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="b0274-184"><dt></dt><dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="b0274-184"><dt></dt> <dt>32774</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="b0274-185"><dt>**Estado no válido para esta operación**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="b0274-185"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>              | <span data-ttu-id="b0274-186">No se admite el valor especificado en el parámetro *RequestedState* .</span><span class="sxs-lookup"><span data-stu-id="b0274-186">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="b0274-187"><dt></dt><dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="b0274-187"><dt></dt> <dt>32776</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="b0274-188"><dt></dt><dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="b0274-188"><dt></dt> <dt>32777</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="b0274-189"><dt></dt><dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="b0274-189"><dt></dt> <dt>32778</dt></span></span> </dl>                                                  |                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="b0274-190">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0274-190">Remarks</span></span>

<span data-ttu-id="b0274-191">El acceso a la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) podría estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="b0274-191">Access to the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b0274-192">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b0274-192">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="b0274-193">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b0274-193">Examples</span></span>

<span data-ttu-id="b0274-194">En el siguiente ejemplo de C# se inicia o deshabilita una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b0274-194">The following C# example starts or disables a virtual machine.</span></span> <span data-ttu-id="b0274-195">Las utilidades a las que se hace referencia se pueden encontrar en [utilidades comunes para los ejemplos de virtualización (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="b0274-195">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b0274-196">Para que funcione correctamente, se debe ejecutar el código siguiente en el servidor host de máquina virtual y se debe ejecutar con privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="b0274-196">To function correctly, the following code must be run on the virtual machine host server, and must be run with administrator privileges.</span></span>

 


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    public class RequestStateChangeClass
    {
        public static void RequestStateChange(string vmName, string action)
        {
            ManagementScope scope = new ManagementScope(@"\\.\root\virtualization\v2", null);
            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);

            if (null == vm)
            {
                throw new ArgumentException(
                    string.Format(
                    "The virtual machine '{0}' could not be found.", 
                    vmName));
            }

            ManagementBaseObject inParams = vm.GetMethodParameters("RequestStateChange");

            const int Enabled = 2;
            const int Disabled = 3;

            if (action.ToLower() == "start")
            {
                inParams["RequestedState"] = Enabled;
            }
            else if (action.ToLower() == "stop")
            {
                inParams["RequestedState"] = Disabled;
            }
            else
            {
                throw new Exception("Wrong action is specified");
            }

            ManagementBaseObject outParams = vm.InvokeMethod(
                "RequestStateChange", 
                inParams, 
                null);

            if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
            {
                if (Utility.JobCompleted(outParams, scope))
                {
                    Console.WriteLine(
                        "{0} state was changed successfully.", 
                        vmName);
                }
                else
                {
                    Console.WriteLine("Failed to change virtual system state");
                }
            }
            else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                Console.WriteLine(
                    "{0} state was changed successfully.", 
                    vmName);
            }
            else
            {
                Console.WriteLine(
                    "Change virtual system state failed with error {0}", 
                    outParams["ReturnValue"]);
            }

        }

        public static void Main(string[] args)
        {
            if (args != null && args.Length != 2)
            {
                Console.WriteLine("Usage: <application> vmName action");
                Console.WriteLine("action: start|stop");
                return;
            }

            RequestStateChange(args[0], args[1]);
        }

    }
}
```



<span data-ttu-id="b0274-197">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se inicia o deshabilita una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b0274-197">The following Visual Basic Scripting Edition (VBScript) example starts or disables a virtual machine.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b0274-198">Para que funcione correctamente, se debe ejecutar el código siguiente en el servidor host de máquina virtual y se debe ejecutar con privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="b0274-198">To function correctly, the following code must be run on the virtual machine host server, and must be run with administrator privileges.</span></span>

 


```VB
dim objWMIService
dim fileSystem

const JobStarting = 3
const JobRunning = 4
const JobCompleted = 7
const wmiStarted = 4096
const Enabled = 2
const Disabled = 3



Main()

'-----------------------------------------------------------------
' Main routine
'-----------------------------------------------------------------
Sub Main()
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    strComputer = "."
    set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\virtualization\v2")

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
       vmName= objArgs.Unnamed.Item(0)
       action = objArgs.Unnamed.Item(1)
    else
       WScript.Echo "usage: cscript StartVM.vbs vmName start|stop"
       WScript.Quit
    end if
    
    set computerSystem = GetComputerSystem(vmName)

    if RequestStateChange(computerSystem, action) then

        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "RequestStateChange failed"
        WScript.Quit(1)
    end if

End Sub

'-----------------------------------------------------------------
' Retrieve Msvm_VirtualComputerSystem from base on its ElementName
' 
'-----------------------------------------------------------------
Function GetComputerSystem(vmElementName)
    On Error Resume Next
    query = Format1("select * from Msvm_ComputerSystem where ElementName = '{0}'", vmElementName)
    set GetComputerSystem = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function


'-----------------------------------------------------------------
' Turn on a virtual machine
'-----------------------------------------------------------------
Function RequestStateChange(computerSystem, action)
    WriteLog Format2("RequestStateChange({0}, {1})", computerSystem.ElementName, action)

    RequestStateChange = false
    set objInParam = computerSystem.Methods_("RequestStateChange").InParameters.SpawnInstance_()
    
    if action = "start" then
        objInParam.RequestedState = Enabled
    else
        objInParam.RequestedState = Disabled
    end if

    set objOutParams = computerSystem.ExecMethod_("RequestStateChange", objInParam)

    if (WMIMethodStarted(objOutParams)) then
        if (WMIJobCompleted(objOutParams)) then
            WriteLog Format1("VM {0} was started successfully", computerSystem.ElementName)
            RequestStateChange = true
        end if
    end if

End Function


'-----------------------------------------------------------------
' Handle wmi return values
'-----------------------------------------------------------------
Function WMIMethodStarted(outParam)

    WMIMethodStarted = false

    if Not IsNull(outParam) then
        wmiStatus = outParam.ReturnValue

        if  wmiStatus = wmiStarted then
            WMIMethodStarted = true
        end if

    end if

End Function


'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)
    dim WMIJob

    set WMIJob = objWMIService.Get(outParam.Job)

    WMIJobCompleted = true

    jobState = WMIJob.JobState

    while jobState = JobRunning or jobState = JobStarting

        WScript.Sleep(1000)
        set WMIJob = objWMIService.Get(outParam.Job)
        jobState = WMIJob.JobState

    wend


    if (jobState <> JobCompleted) then
        WriteLog Format1("ErrorDescription:{0}", WMIJob.ErrorDescription)
        WMIJobCompleted = false
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\StartVM.log", 8, true)
    WScript.Echo line
    fileStream.WriteLine line
    fileStream.Close

End Sub


'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format2(myString, arg0, arg1)
    Format2 = Format1(myString, arg0)
    Format2 = Replace(Format2, "{1}", arg1)
End Function

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format1(myString, arg0)
    Format1 = Replace(myString, "{0}", arg0)
End Function
```



## <a name="requirements"></a><span data-ttu-id="b0274-199">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0274-199">Requirements</span></span>



| <span data-ttu-id="b0274-200">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0274-200">Requirement</span></span> | <span data-ttu-id="b0274-201">Value</span><span class="sxs-lookup"><span data-stu-id="b0274-201">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0274-202">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0274-202">Minimum supported client</span></span><br/> | <span data-ttu-id="b0274-203">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="b0274-203">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b0274-204">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0274-204">Minimum supported server</span></span><br/> | <span data-ttu-id="b0274-205">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="b0274-205">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b0274-206">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b0274-206">Namespace</span></span><br/>                | <span data-ttu-id="b0274-207">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b0274-207">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b0274-208">MOF</span><span class="sxs-lookup"><span data-stu-id="b0274-208">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0274-209"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0274-209"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0274-210">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b0274-210">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0274-211"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b0274-211"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b0274-212">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0274-212">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0274-213">**MSVM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="b0274-213">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

