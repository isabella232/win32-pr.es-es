---
title: Códigos de error de animación de Windows (Winerror. h)
description: Si se produce un error, la animación de Windows devuelve un código como un valor HRESULT. En esta sección se proporciona una lista de códigos de error específicos de la animación de Windows. Para obtener una lista de códigos de error COM generales, vea códigos de error COM.
ms.assetid: 38f15d61-d415-4c7d-b454-5144fc7c9b1e
topic_type:
- apiref
api_name:
- UI_E_CREATE_FAILED
- UI_E_SHUTDOWN_CALLED
- UI_E_ILLEGAL_REENTRANCY
- UI_E_OBJECT_SEALED
- UI_E_VALUE_NOT_SET
- UI_E_VALUE_NOT_DETERMINED
- UI_E_INVALID_OUTPUT
- UI_E_BOOLEAN_EXPECTED
- UI_E_DIFFERENT_OWNER
- UI_E_AMBIGUOUS_MATCH
- UI_E_FP_OVERFLOW
- UI_E_WRONG_THREAD
- UI_E_STORYBOARD_ACTIVE
- UI_E_STORYBOARD_NOT_PLAYING
- UI_E_START_KEYFRAME_AFTER_END
- UI_E_END_KEYFRAME_NOT_DETERMINED
- UI_E_LOOPS_OVERLAP
- UI_E_TRANSITION_ALREADY_USED
- UI_E_TRANSITION_NOT_IN_STORYBOARD
- UI_E_TRANSITION_ECLIPSED
- UI_E_TIME_BEFORE_LAST_UPDATE
- UI_E_TIMER_CLIENT_ALREADY_CONNECTED
api_location:
- winerror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7c63066690b15ec8fad8ef5b9f74ed5cf2fbc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695908"
---
# <a name="windows-animation-error-codes"></a><span data-ttu-id="5aa4e-105">Códigos de error de animación de Windows</span><span class="sxs-lookup"><span data-stu-id="5aa4e-105">Windows Animation Error Codes</span></span>

<span data-ttu-id="5aa4e-106">Si se produce un error, la animación de Windows devuelve un código como un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5aa4e-106">If an error occurs, Windows Animation returns a code as an **HRESULT** value.</span></span> <span data-ttu-id="5aa4e-107">En esta sección se proporciona una lista de códigos de error específicos de la animación de Windows.</span><span class="sxs-lookup"><span data-stu-id="5aa4e-107">This section provides a list of error codes specific to Windows Animation.</span></span> <span data-ttu-id="5aa4e-108">Para obtener una lista de códigos de error COM generales, vea [códigos de error com](/windows/desktop/com/com-error-codes).</span><span class="sxs-lookup"><span data-stu-id="5aa4e-108">For a list of general COM error codes, see [COM Error Codes](/windows/desktop/com/com-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="5aa4e-109"><span id="UI_E_CREATE_FAILED"></span><span id="ui_e_create_failed"></span>**\_ \_ \_ no se pudo crear la UI E**</span><span class="sxs-lookup"><span data-stu-id="5aa4e-109"><span id="UI_E_CREATE_FAILED"></span><span id="ui_e_create_failed"></span>**UI\_E\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aa4e-110">0x802A0001</span><span class="sxs-lookup"><span data-stu-id="5aa4e-110">0x802A0001</span></span>
</dt> <dt>



<span data-ttu-id="5aa4e-111">No se pudo crear el objeto.</span><span class="sxs-lookup"><span data-stu-id="5aa4e-111">The object could not be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5aa4e-112"><span id="UI_E_SHUTDOWN_CALLED"></span><span id="ui_e_shutdown_called"></span>**se \_ ha \_ \_ llamado a shutdown E UI**</span><span class="sxs-lookup"><span data-stu-id="5aa4e-112"><span id="UI_E_SHUTDOWN_CALLED"></span><span id="ui_e_shutdown_called"></span>**UI\_E\_SHUTDOWN\_CALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aa4e-113">0x802A0002</span><span class="sxs-lookup"><span data-stu-id="5aa4e-113">0x802A0002</span></span>
</dt> <dt>



<span data-ttu-id="5aa4e-114">Se ha llamado al método [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) en el administrador de animaciones, lo que hace que el administrador de animaciones se cierre y todas las variables de animación y guiones gráficos que creó se liberen.</span><span class="sxs-lookup"><span data-stu-id="5aa4e-114">The [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) method has been called on the animation manager, causing the animation manager to shut down and all the animation variables and storyboards it created to be released.</span></span>

> [!Note]  
> <span data-ttu-id="5aa4e-115">No se puede llamar a ningún método en ningún objeto de animación después del [**cierre**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown).</span><span class="sxs-lookup"><span data-stu-id="5aa4e-115">No methods can be called on any animation object after [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="5aa4e-116"><span id="UI_E_ILLEGAL_REENTRANCY"></span><span id="ui_e_illegal_reentrancy"></span>**\_reentrada \_ ilegal E interfaz de usuario \_**</span><span class="sxs-lookup"><span data-stu-id="5aa4e-116"><span id="UI_E_ILLEGAL_REENTRANCY"></span><span id="ui_e_illegal_reentrancy"></span>**UI\_E\_ILLEGAL\_REENTRANCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aa4e-117">0x802A0003</span><span class="sxs-lookup"><span data-stu-id="5aa4e-117">0x802A0003</span></span>
</dt> <dt>



<span data-ttu-id="5aa4e-118">No se puede llamar a este método durante este tipo de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="5aa4e-118">This method cannot be called during this type of callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5aa4e-119"><span id="UI_E_OBJECT_SEALED"></span><span id="ui_e_object_sealed"></span>**objeto de interfaz de usuario \_ E \_ \_ sellado**</span><span class="sxs-lookup"><span data-stu-id="5aa4e-119"><span id="UI_E_OBJECT_SEALED"></span><span id="ui_e_object_sealed"></span>**UI\_E\_OBJECT\_SEALED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aa4e-120">0x802A0004</span><span class="sxs-lookup"><span data-stu-id="5aa4e-120">0x802A0004</span></span>
</dt> <dt>



<span data-ttu-id="5aa4e-121">Este objeto se ha sellado, por lo que ya no se permite este cambio.</span><span class="sxs-lookup"><span data-stu-id="5aa4e-121">This object has been sealed, so this change is no longer allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5aa4e-122"><span id="UI_E_VALUE_NOT_SET"></span><span id="ui_e_value_not_set"></span>**\_valor E de UI \_ \_ no \_ establecido**</span><span class="sxs-lookup"><span data-stu-id="5aa4e-122"><span id="UI_E_VALUE_NOT_SET"></span><span id="ui_e_value_not_set"></span>**UI\_E\_VALUE\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aa4e-123">0x802A0005</span><span class="sxs-lookup"><span data-stu-id="5aa4e-123">0x802A0005</span></span>
</dt> <dt>



<span data-ttu-id="5aa4e-124">No se ha establecido nunca el valor solicitado y, por lo tanto, no se puede recuperar.</span><span class="sxs-lookup"><span data-stu-id="5aa4e-124">The requested value has never been set, and therefore cannot be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5aa4e-125"><span id="UI_E_VALUE_NOT_DETERMINED"></span><span id="ui_e_value_not_determined"></span>**\_valor E de UI \_ \_ no \_ determinado**</span><span class="sxs-lookup"><span data-stu-id="5aa4e-125"><span id="UI_E_VALUE_NOT_DETERMINED"></span><span id="ui_e_value_not_determined"></span>**UI\_E\_VALUE\_NOT\_DETERMINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aa4e-126">0x802A0006</span><span class="sxs-lookup"><span data-stu-id="5aa4e-126">0x802A0006</span></span>
</dt> <dt>



<span data-ttu-id="5aa4e-127">No se puede determinar el valor solicitado.</span><span class="sxs-lookup"><span data-stu-id="5aa4e-127">The requested value cannot be determined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5aa4e-128"><span id="UI_E_INVALID_OUTPUT"></span><span id="ui_e_invalid_output"></span>**salida de UI \_ E \_ no válida \_**</span><span class="sxs-lookup"><span data-stu-id="5aa4e-128"><span id="UI_E_INVALID_OUTPUT"></span><span id="ui_e_invalid_output"></span>**UI\_E\_INVALID\_OUTPUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aa4e-129">0x802A0007</span><span class="sxs-lookup"><span data-stu-id="5aa4e-129">0x802A0007</span></span>
</dt> <dt>



<span data-ttu-id="5aa4e-130">Una devolución de llamada devolvió un parámetro de salida no válido.</span><span class="sxs-lookup"><span data-stu-id="5aa4e-130">A callback returned an invalid output parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5aa4e-131"><span id="UI_E_BOOLEAN_EXPECTED"></span><span id="ui_e_boolean_expected"></span>**se esperaba una interfaz de usuario \_ E \_ booleana \_**</span><span class="sxs-lookup"><span data-stu-id="5aa4e-131"><span id="UI_E_BOOLEAN_EXPECTED"></span><span id="ui_e_boolean_expected"></span>**UI\_E\_BOOLEAN\_EXPECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aa4e-132">0x802A0008</span><span class="sxs-lookup"><span data-stu-id="5aa4e-132">0x802A0008</span></span>
</dt> <dt>



<span data-ttu-id="5aa4e-133">Una devolución de llamada devolvió un código de éxito distinto de S \_ OK o s \_ false.</span><span class="sxs-lookup"><span data-stu-id="5aa4e-133">A callback returned a success code other than S\_OK or S\_FALSE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5aa4e-134"><span id="UI_E_DIFFERENT_OWNER"></span><span id="ui_e_different_owner"></span>**propietario de la interfaz de usuario \_ E \_ diferente \_**</span><span class="sxs-lookup"><span data-stu-id="5aa4e-134"><span id="UI_E_DIFFERENT_OWNER"></span><span id="ui_e_different_owner"></span>**UI\_E\_DIFFERENT\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aa4e-135">0x802A0009</span><span class="sxs-lookup"><span data-stu-id="5aa4e-135">0x802A0009</span></span>
</dt> <dt>



<span data-ttu-id="5aa4e-136">Un parámetro que debe ser propiedad de este objeto es propiedad de un objeto diferente.</span><span class="sxs-lookup"><span data-stu-id="5aa4e-136">A parameter that should be owned by this object is owned by a different object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5aa4e-137"><span id="UI_E_AMBIGUOUS_MATCH"></span><span id="ui_e_ambiguous_match"></span>**\_ \_ coincidencia AMBIGUA de UI E \_**</span><span class="sxs-lookup"><span data-stu-id="5aa4e-137"><span id="UI_E_AMBIGUOUS_MATCH"></span><span id="ui_e_ambiguous_match"></span>**UI\_E\_AMBIGUOUS\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aa4e-138">0x802A000A</span><span class="sxs-lookup"><span data-stu-id="5aa4e-138">0x802A000A</span></span>
</dt> <dt>



<span data-ttu-id="5aa4e-139">Hay más de un elemento que coincide con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="5aa4e-139">More than one item matched the search criteria.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5aa4e-140"><span id="UI_E_FP_OVERFLOW"></span><span id="ui_e_fp_overflow"></span>**desbordamiento de la interfaz de usuario \_ E \_ FP \_**</span><span class="sxs-lookup"><span data-stu-id="5aa4e-140"><span id="UI_E_FP_OVERFLOW"></span><span id="ui_e_fp_overflow"></span>**UI\_E\_FP\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aa4e-141">0x802A000B</span><span class="sxs-lookup"><span data-stu-id="5aa4e-141">0x802A000B</span></span>
</dt> <dt>



<span data-ttu-id="5aa4e-142">Se ha producido un desbordamiento de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="5aa4e-142">A floating-point overflow occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5aa4e-143"><span id="UI_E_WRONG_THREAD"></span><span id="ui_e_wrong_thread"></span>**interfaz de usuario \_ E \_ \_ subproceso incorrecto**</span><span class="sxs-lookup"><span data-stu-id="5aa4e-143"><span id="UI_E_WRONG_THREAD"></span><span id="ui_e_wrong_thread"></span>**UI\_E\_WRONG\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aa4e-144">0x802A000C</span><span class="sxs-lookup"><span data-stu-id="5aa4e-144">0x802A000C</span></span>
</dt> <dt>



<span data-ttu-id="5aa4e-145">Solo se puede llamar a este método desde el subproceso que creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="5aa4e-145">This method can only be called from the thread that created the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5aa4e-146"><span id="UI_E_STORYBOARD_ACTIVE"></span><span id="ui_e_storyboard_active"></span>**IU \_ E \_ guion gráfico \_ activo**</span><span class="sxs-lookup"><span data-stu-id="5aa4e-146"><span id="UI_E_STORYBOARD_ACTIVE"></span><span id="ui_e_storyboard_active"></span>**UI\_E\_STORYBOARD\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aa4e-147">0x802A0101</span><span class="sxs-lookup"><span data-stu-id="5aa4e-147">0x802A0101</span></span>
</dt> <dt>



<span data-ttu-id="5aa4e-148">El guión gráfico está actualmente en la programación.</span><span class="sxs-lookup"><span data-stu-id="5aa4e-148">The storyboard is currently in the schedule.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5aa4e-149"><span id="UI_E_STORYBOARD_NOT_PLAYING"></span><span id="ui_e_storyboard_not_playing"></span>**\_guion gráfico de UI E \_ \_ no \_ reproduciendo**</span><span class="sxs-lookup"><span data-stu-id="5aa4e-149"><span id="UI_E_STORYBOARD_NOT_PLAYING"></span><span id="ui_e_storyboard_not_playing"></span>**UI\_E\_STORYBOARD\_NOT\_PLAYING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aa4e-150">0x802A0102</span><span class="sxs-lookup"><span data-stu-id="5aa4e-150">0x802A0102</span></span>
</dt> <dt>



<span data-ttu-id="5aa4e-151">El guión gráfico no se está reproduciendo.</span><span class="sxs-lookup"><span data-stu-id="5aa4e-151">The storyboard is not playing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5aa4e-152"><span id="UI_E_START_KEYFRAME_AFTER_END"></span><span id="ui_e_start_keyframe_after_end"></span>**\_E \_ iniciar \_ fotograma \_ clave \_ de la interfaz de usuario después del final**</span><span class="sxs-lookup"><span data-stu-id="5aa4e-152"><span id="UI_E_START_KEYFRAME_AFTER_END"></span><span id="ui_e_start_keyframe_after_end"></span>**UI\_E\_START\_KEYFRAME\_AFTER\_END**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aa4e-153">0x802A0103</span><span class="sxs-lookup"><span data-stu-id="5aa4e-153">0x802A0103</span></span>
</dt> <dt>



<span data-ttu-id="5aa4e-154">El fotograma clave inicial podría producirse después del fotograma clave final.</span><span class="sxs-lookup"><span data-stu-id="5aa4e-154">The start keyframe might occur after the end keyframe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5aa4e-155"><span id="UI_E_END_KEYFRAME_NOT_DETERMINED"></span><span id="ui_e_end_keyframe_not_determined"></span>**fotograma clave de IU \_ E \_ End \_ \_ no \_ determinado**</span><span class="sxs-lookup"><span data-stu-id="5aa4e-155"><span id="UI_E_END_KEYFRAME_NOT_DETERMINED"></span><span id="ui_e_end_keyframe_not_determined"></span>**UI\_E\_END\_KEYFRAME\_NOT\_DETERMINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aa4e-156">0x802A0104</span><span class="sxs-lookup"><span data-stu-id="5aa4e-156">0x802A0104</span></span>
</dt> <dt>



<span data-ttu-id="5aa4e-157">Es posible que no sea posible determinar el tiempo del fotograma clave final cuando se alcanza el fotograma clave inicial.</span><span class="sxs-lookup"><span data-stu-id="5aa4e-157">It might not be possible to determine the end keyframe time when the start keyframe is reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5aa4e-158"><span id="UI_E_LOOPS_OVERLAP"></span><span id="ui_e_loops_overlap"></span>**superposición de \_ \_ bucles E interfaz de usuario \_**</span><span class="sxs-lookup"><span data-stu-id="5aa4e-158"><span id="UI_E_LOOPS_OVERLAP"></span><span id="ui_e_loops_overlap"></span>**UI\_E\_LOOPS\_OVERLAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aa4e-159">0x802A0105</span><span class="sxs-lookup"><span data-stu-id="5aa4e-159">0x802A0105</span></span>
</dt> <dt>



<span data-ttu-id="5aa4e-160">Dos partes repetidas de un guión gráfico pueden superponerse.</span><span class="sxs-lookup"><span data-stu-id="5aa4e-160">Two repeated portions of a storyboard might overlap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5aa4e-161"><span id="UI_E_TRANSITION_ALREADY_USED"></span><span id="ui_e_transition_already_used"></span>**transición E interfaz de usuario \_ \_ \_ ya \_ usada**</span><span class="sxs-lookup"><span data-stu-id="5aa4e-161"><span id="UI_E_TRANSITION_ALREADY_USED"></span><span id="ui_e_transition_already_used"></span>**UI\_E\_TRANSITION\_ALREADY\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aa4e-162">0x802A0106</span><span class="sxs-lookup"><span data-stu-id="5aa4e-162">0x802A0106</span></span>
</dt> <dt>



<span data-ttu-id="5aa4e-163">La transición ya se ha agregado a un guion gráfico diferente o se ha agregado a un guion gráfico que ha terminado de reproducirse y se ha liberado.</span><span class="sxs-lookup"><span data-stu-id="5aa4e-163">The transition has already been added to a different storyboard or has been added to a storyboard that has finished playing and been released.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5aa4e-164"><span id="UI_E_TRANSITION_NOT_IN_STORYBOARD"></span><span id="ui_e_transition_not_in_storyboard"></span>**\_ \_ transición de UI E \_ no \_ en \_ guion gráfico**</span><span class="sxs-lookup"><span data-stu-id="5aa4e-164"><span id="UI_E_TRANSITION_NOT_IN_STORYBOARD"></span><span id="ui_e_transition_not_in_storyboard"></span>**UI\_E\_TRANSITION\_NOT\_IN\_STORYBOARD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aa4e-165">0x802A0107</span><span class="sxs-lookup"><span data-stu-id="5aa4e-165">0x802A0107</span></span>
</dt> <dt>



<span data-ttu-id="5aa4e-166">La transición no se ha agregado a ningún guion gráfico.</span><span class="sxs-lookup"><span data-stu-id="5aa4e-166">The transition has not been added to any storyboard.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5aa4e-167"><span id="UI_E_TRANSITION_ECLIPSED"></span><span id="ui_e_transition_eclipsed"></span>**transición E interfaz de usuario con \_ \_ \_ Eclipse**</span><span class="sxs-lookup"><span data-stu-id="5aa4e-167"><span id="UI_E_TRANSITION_ECLIPSED"></span><span id="ui_e_transition_eclipsed"></span>**UI\_E\_TRANSITION\_ECLIPSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aa4e-168">0x802A0108</span><span class="sxs-lookup"><span data-stu-id="5aa4e-168">0x802A0108</span></span>
</dt> <dt>



<span data-ttu-id="5aa4e-169">La transición podría Eclipse al principio de otra transición en el guión gráfico.</span><span class="sxs-lookup"><span data-stu-id="5aa4e-169">The transition might eclipse the beginning of another transition in the storyboard.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5aa4e-170"><span id="UI_E_TIME_BEFORE_LAST_UPDATE"></span><span id="ui_e_time_before_last_update"></span>**E/s de la interfaz de usuario antes de la \_ \_ \_ \_ última \_ actualización**</span><span class="sxs-lookup"><span data-stu-id="5aa4e-170"><span id="UI_E_TIME_BEFORE_LAST_UPDATE"></span><span id="ui_e_time_before_last_update"></span>**UI\_E\_TIME\_BEFORE\_LAST\_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aa4e-171">0x802A0109</span><span class="sxs-lookup"><span data-stu-id="5aa4e-171">0x802A0109</span></span>
</dt> <dt>



<span data-ttu-id="5aa4e-172">La hora especificada es anterior a la hora pasada a la última actualización.</span><span class="sxs-lookup"><span data-stu-id="5aa4e-172">The specified time is earlier than the time passed to the last update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5aa4e-173"><span id="UI_E_TIMER_CLIENT_ALREADY_CONNECTED"></span><span id="ui_e_timer_client_already_connected"></span>**el \_ cliente de temporizador E interfaz de usuario \_ ya está \_ \_ \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="5aa4e-173"><span id="UI_E_TIMER_CLIENT_ALREADY_CONNECTED"></span><span id="ui_e_timer_client_already_connected"></span>**UI\_E\_TIMER\_CLIENT\_ALREADY\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aa4e-174">0x802A010A</span><span class="sxs-lookup"><span data-stu-id="5aa4e-174">0x802A010A</span></span>
</dt> <dt>



<span data-ttu-id="5aa4e-175">Este cliente ya está conectado a un temporizador.</span><span class="sxs-lookup"><span data-stu-id="5aa4e-175">This client is already connected to a timer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5aa4e-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5aa4e-176">Requirements</span></span>



| <span data-ttu-id="5aa4e-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aa4e-177">Requirement</span></span> | <span data-ttu-id="5aa4e-178">Value</span><span class="sxs-lookup"><span data-stu-id="5aa4e-178">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa4e-179">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5aa4e-179">Minimum supported client</span></span><br/> | <span data-ttu-id="5aa4e-180">Windows 7, Windows Vista y la actualización de plataforma solo para aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5aa4e-180">Windows 7, Windows Vista and Platform Update for Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5aa4e-181">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5aa4e-181">Minimum supported server</span></span><br/> | <span data-ttu-id="5aa4e-182">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5aa4e-182">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="5aa4e-183">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5aa4e-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="5aa4e-184"><dt>Winerror. h</dt></span><span class="sxs-lookup"><span data-stu-id="5aa4e-184"><dt>Winerror.h</dt></span></span> </dl>           |



## <a name="see-also"></a><span data-ttu-id="5aa4e-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="5aa4e-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aa4e-186">Referencia de animación de Windows</span><span class="sxs-lookup"><span data-stu-id="5aa4e-186">Windows Animation Reference</span></span>](windows-animation-reference.md)
</dt> </dl>

 

