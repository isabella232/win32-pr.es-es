---
description: Las \_ constantes de marcador de bits PHONESTATE describen varios elementos de estado para un dispositivo telefónico.
ms.assetid: 5db53dd4-606a-40b9-9159-b67a0ea1e400
title: Constantes de PHONESTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6346251f6947aebb2a5941389843e2abcec77c4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679230"
---
# <a name="phonestate_-constants"></a><span data-ttu-id="ebc3d-103">Constantes de PHONESTATE \_</span><span class="sxs-lookup"><span data-stu-id="ebc3d-103">PHONESTATE\_ Constants</span></span>

<span data-ttu-id="ebc3d-104">Las constantes de marcador de bits **PHONESTATE \_** describen varios elementos de estado para un dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-104">The **PHONESTATE\_** bit-flag constants describe various status items for a phone device.</span></span>

<dl> <dt>

<span data-ttu-id="ebc3d-105"><span id="PHONESTATE_CAPSCHANGE"></span><span id="phonestate_capschange"></span>**PHONESTATE \_ CAPSCHANGE**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-105"><span id="PHONESTATE_CAPSCHANGE"></span><span id="phonestate_capschange"></span>**PHONESTATE\_CAPSCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc3d-106">Indica que, debido a los cambios de configuración realizados por el usuario u otras circunstancias, uno o varios de los miembros de la estructura [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) han cambiado.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-106">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) structure have changed.</span></span> <span data-ttu-id="ebc3d-107">La aplicación debe usar [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) para leer la estructura actualizada.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-107">The application should use [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) to read the updated structure.</span></span> <span data-ttu-id="ebc3d-108">Si un proveedor de servicios envía un mensaje de [**\_ Estado de teléfono**](phone-state.md) que contiene este valor a TAPI, TAPI lo pasará a las aplicaciones que han negociado la versión 1,4 o posterior de TAPI; las aplicaciones que negocian una versión anterior de API recibirán mensajes de estado de teléfono que \_ especifican PHONESTATE \_ reinit, lo que les obliga a apagar y reinicializar la conexión a TAPI para obtener la información actualizada</span><span class="sxs-lookup"><span data-stu-id="ebc3d-108">If a service provider sends a [**PHONE\_STATE**](phone-state.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will receive PHONE\_STATE messages specifying PHONESTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc3d-109"><span id="PHONESTATE_CONNECTED"></span><span id="phonestate_connected"></span>**PHONESTATE \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-109"><span id="PHONESTATE_CONNECTED"></span><span id="phonestate_connected"></span>**PHONESTATE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc3d-110">Se acaba de realizar la conexión entre el dispositivo telefónico y TAPI.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-110">The connection between the phone device and TAPI was just made.</span></span> <span data-ttu-id="ebc3d-111">Esto sucede cuando se invoca primero TAPI o cuando el cable que conecta el teléfono al equipo está conectado con TAPI activo.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-111">This happens when TAPI is first invoked or when the wire connecting the phone to the PC is plugged in with TAPI active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc3d-112"><span id="PHONESTATE_DEVSPECIFIC"></span><span id="phonestate_devspecific"></span>**PHONESTATE \_ DEVSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-112"><span id="PHONESTATE_DEVSPECIFIC"></span><span id="phonestate_devspecific"></span>**PHONESTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc3d-113">La información específica del dispositivo del teléfono ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-113">The phone's device-specific information has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc3d-114"><span id="PHONESTATE_DISCONNECTED"></span><span id="phonestate_disconnected"></span>**PHONESTATE \_ DESconectado**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-114"><span id="PHONESTATE_DISCONNECTED"></span><span id="phonestate_disconnected"></span>**PHONESTATE\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc3d-115">La conexión entre el dispositivo telefónico y TAPI se acaba de interrumpir.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-115">The connection between the phone device and TAPI was just broken.</span></span> <span data-ttu-id="ebc3d-116">Esto sucede cuando el cable que conecta el teléfono al equipo está desconectado mientras TAPI está activo.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-116">This happens when the wire connecting the phone set to the PC is unplugged while TAPI is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc3d-117"><span id="PHONESTATE_DISPLAY"></span><span id="phonestate_display"></span>**PHONESTATE \_ Mostrar**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-117"><span id="PHONESTATE_DISPLAY"></span><span id="phonestate_display"></span>**PHONESTATE\_DISPLAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc3d-118">La presentación del teléfono ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-118">The display of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc3d-119"><span id="PHONESTATE_HANDSETGAIN"></span><span id="phonestate_handsetgain"></span>**PHONESTATE \_ HANDSETGAIN**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-119"><span id="PHONESTATE_HANDSETGAIN"></span><span id="phonestate_handsetgain"></span>**PHONESTATE\_HANDSETGAIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc3d-120">La configuración de ganancia de micrófono del auricular ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-120">The handset's microphone gain setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc3d-121"><span id="PHONESTATE_HANDSETHOOKSWITCH"></span><span id="phonestate_handsethookswitch"></span>**PHONESTATE \_ HANDSETHOOKSWITCH**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-121"><span id="PHONESTATE_HANDSETHOOKSWITCH"></span><span id="phonestate_handsethookswitch"></span>**PHONESTATE\_HANDSETHOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc3d-122">El estado de conmutador de auricular ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-122">The handset hookswitch state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc3d-123"><span id="PHONESTATE_HANDSETVOLUME"></span><span id="phonestate_handsetvolume"></span>**PHONESTATE \_ HANDSETVOLUME**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-123"><span id="PHONESTATE_HANDSETVOLUME"></span><span id="phonestate_handsetvolume"></span>**PHONESTATE\_HANDSETVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc3d-124">La configuración del volumen de altavoz del auricular ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-124">The handset's speaker volume setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc3d-125"><span id="PHONESTATE_HEADSETHOOKSWITCH"></span><span id="phonestate_headsethookswitch"></span>**PHONESTATE \_ HEADSETHOOKSWITCH**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-125"><span id="PHONESTATE_HEADSETHOOKSWITCH"></span><span id="phonestate_headsethookswitch"></span>**PHONESTATE\_HEADSETHOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc3d-126">El estado de conmutador del casco ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-126">The headset's hookswitch state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc3d-127"><span id="PHONESTATE_HEADSETGAIN"></span><span id="phonestate_headsetgain"></span>**PHONESTATE \_ HEADSETGAIN**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-127"><span id="PHONESTATE_HEADSETGAIN"></span><span id="phonestate_headsetgain"></span>**PHONESTATE\_HEADSETGAIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc3d-128">La configuración de ganancia de micrófono del casco ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-128">The headset's microphone gain setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc3d-129"><span id="PHONESTATE_HEADSETVOLUME"></span><span id="phonestate_headsetvolume"></span>**PHONESTATE \_ HEADSETVOLUME**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-129"><span id="PHONESTATE_HEADSETVOLUME"></span><span id="phonestate_headsetvolume"></span>**PHONESTATE\_HEADSETVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc3d-130">La configuración del volumen de altavoz del casco ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-130">The headset's speaker volume setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc3d-131"><span id="PHONESTATE_LAMP"></span><span id="phonestate_lamp"></span>**\_lámpara PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-131"><span id="PHONESTATE_LAMP"></span><span id="phonestate_lamp"></span>**PHONESTATE\_LAMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc3d-132">Ha cambiado una lámpara del teléfono.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-132">A lamp of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc3d-133"><span id="PHONESTATE_MONITORS"></span><span id="phonestate_monitors"></span>**\_monitores PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-133"><span id="PHONESTATE_MONITORS"></span><span id="phonestate_monitors"></span>**PHONESTATE\_MONITORS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc3d-134">El número de monitores para el dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-134">The number of monitors for the phone device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc3d-135"><span id="PHONESTATE_OTHER"></span><span id="phonestate_other"></span>**PHONESTATE \_ otro**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-135"><span id="PHONESTATE_OTHER"></span><span id="phonestate_other"></span>**PHONESTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc3d-136">Los elementos de estado de teléfono distintos de los que se enumeran a continuación han cambiado.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-136">Phone-status items other than those listed below have changed.</span></span> <span data-ttu-id="ebc3d-137">La aplicación debe comprobar el estado del teléfono actual para determinar qué elementos han cambiado.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-137">The application should check the current phone status to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc3d-138"><span id="PHONESTATE_OWNER"></span><span id="phonestate_owner"></span>**propietario de PHONESTATE \_**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-138"><span id="PHONESTATE_OWNER"></span><span id="phonestate_owner"></span>**PHONESTATE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc3d-139">El número de propietarios del dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-139">The number of owners for the phone device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc3d-140"><span id="PHONESTATE_REINIT"></span><span id="phonestate_reinit"></span>**reinicialización de PHONESTATE \_**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-140"><span id="PHONESTATE_REINIT"></span><span id="phonestate_reinit"></span>**PHONESTATE\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc3d-141">Los elementos han cambiado en la configuración de los dispositivos telefónicos.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-141">Items have changed in the configuration of phone devices.</span></span> <span data-ttu-id="ebc3d-142">Para tener en cuenta estos cambios (como en el aspecto de los nuevos dispositivos telefónicos), la aplicación debe reinicializar el uso de TAPI.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-142">To become aware of these changes (as for the appearance of new phone devices), the application should reinitialize its use of TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc3d-143"><span id="PHONESTATE_REMOVED"></span><span id="phonestate_removed"></span>**PHONESTATE \_ quitado**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-143"><span id="PHONESTATE_REMOVED"></span><span id="phonestate_removed"></span>**PHONESTATE\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc3d-144">Indica que el proveedor de servicios está quitando el dispositivo del sistema (lo que es más probable a través de la acción del usuario, a través de un panel de control o una utilidad similar).</span><span class="sxs-lookup"><span data-stu-id="ebc3d-144">Indicates that the device is being removed from the system by the service provider (most likely through user action, through a control panel or similar utility).</span></span> <span data-ttu-id="ebc3d-145">Un mensaje de [**\_ Estado de teléfono**](phone-state.md) con este valor normalmente irá seguido inmediatamente de un mensaje de [**\_ cierre de teléfono**](phone-close.md) en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-145">A [**PHONE\_STATE**](phone-state.md) message with this value will normally be immediately followed by a [**PHONE\_CLOSE**](phone-close.md) message on the device.</span></span> <span data-ttu-id="ebc3d-146">Los intentos posteriores de obtener acceso al dispositivo antes de que se reinicialice TAPI darán lugar a que se \_ devuelva PHONEERR Device a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-146">Subsequent attempts to access the device prior to TAPI being reinitialized will result in PHONEERR\_NODEVICE being returned to the application.</span></span> <span data-ttu-id="ebc3d-147">Si un proveedor de servicios envía un \_ mensaje de estado de teléfono que contiene este valor a TAPI, TAPI lo pasará a las aplicaciones que han negociado la versión 1,4 o posterior de TAPI; las aplicaciones que negocian una versión anterior de la API no recibirán ninguna notificación.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-147">If a service provider sends a PHONE\_STATE message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc3d-148"><span id="PHONESTATE_RESUME"></span><span id="phonestate_resume"></span>**\_reanudación de PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-148"><span id="PHONESTATE_RESUME"></span><span id="phonestate_resume"></span>**PHONESTATE\_RESUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc3d-149">El uso de la aplicación del dispositivo telefónico se reanuda después de haberse suspendido durante algún tiempo.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-149">The application's use of the phone device is resumed after having been suspended for some time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc3d-150"><span id="PHONESTATE_RINGMODE"></span><span id="phonestate_ringmode"></span>**PHONESTATE \_ RINGMODE**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-150"><span id="PHONESTATE_RINGMODE"></span><span id="phonestate_ringmode"></span>**PHONESTATE\_RINGMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc3d-151">El modo de anillo del teléfono ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-151">The ring mode of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc3d-152"><span id="PHONESTATE_RINGVOLUME"></span><span id="phonestate_ringvolume"></span>**PHONESTATE \_ RINGVOLUME**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-152"><span id="PHONESTATE_RINGVOLUME"></span><span id="phonestate_ringvolume"></span>**PHONESTATE\_RINGVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc3d-153">El volumen de timbre del teléfono ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-153">The ring volume of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc3d-154"><span id="PHONESTATE_SPEAKERHOOKSWITCH"></span><span id="phonestate_speakerhookswitch"></span>**PHONESTATE \_ SPEAKERHOOKSWITCH**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-154"><span id="PHONESTATE_SPEAKERHOOKSWITCH"></span><span id="phonestate_speakerhookswitch"></span>**PHONESTATE\_SPEAKERHOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc3d-155">El estado de conmutador del altavoz ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-155">The speakerphone's hookswitch state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc3d-156"><span id="PHONESTATE_SPEAKERGAIN"></span><span id="phonestate_speakergain"></span>**PHONESTATE \_ SPEAKERGAIN**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-156"><span id="PHONESTATE_SPEAKERGAIN"></span><span id="phonestate_speakergain"></span>**PHONESTATE\_SPEAKERGAIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc3d-157">Ha cambiado el estado de la opción de ganancia de micrófono del altavoz.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-157">The speakerphone's microphone gain setting state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc3d-158"><span id="PHONESTATE_SPEAKERVOLUME"></span><span id="phonestate_speakervolume"></span>**PHONESTATE \_ SPEAKERVOLUME**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-158"><span id="PHONESTATE_SPEAKERVOLUME"></span><span id="phonestate_speakervolume"></span>**PHONESTATE\_SPEAKERVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc3d-159">La configuración del volumen de altavoz del altavoz ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-159">The speakerphone's speaker volume setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ebc3d-160"><span id="PHONESTATE_SUSPEND"></span><span id="phonestate_suspend"></span>**suspensión de PHONESTATE \_**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-160"><span id="PHONESTATE_SUSPEND"></span><span id="phonestate_suspend"></span>**PHONESTATE\_SUSPEND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ebc3d-161">El uso de la aplicación del teléfono se suspende temporalmente.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-161">The application's use of the phone is temporarily suspended.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ebc3d-162">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ebc3d-162">Remarks</span></span>

<span data-ttu-id="ebc3d-163">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-163">No extensibility.</span></span> <span data-ttu-id="ebc3d-164">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="ebc3d-164">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebc3d-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebc3d-165">Requirements</span></span>



| <span data-ttu-id="ebc3d-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebc3d-166">Requirement</span></span> | <span data-ttu-id="ebc3d-167">Value</span><span class="sxs-lookup"><span data-stu-id="ebc3d-167">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ebc3d-168">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="ebc3d-168">TAPI version</span></span><br/> | <span data-ttu-id="ebc3d-169">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="ebc3d-169">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ebc3d-170">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ebc3d-170">Header</span></span><br/>       | <dl> <span data-ttu-id="ebc3d-171"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebc3d-171"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebc3d-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="ebc3d-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebc3d-173">**\_cerrar teléfono**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-173">**PHONE\_CLOSE**</span></span>](phone-close.md)
</dt> <dt>

[<span data-ttu-id="ebc3d-174">**Estado del teléfono \_**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-174">**PHONE\_STATE**</span></span>](phone-state.md)
</dt> <dt>

[<span data-ttu-id="ebc3d-175">**PHONECAPS**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-175">**PHONECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[<span data-ttu-id="ebc3d-176">**phoneGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="ebc3d-176">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




