---
description: Las \_ constantes de marcador de bits LINEDEVSTATE describen diversos eventos de estado de línea.
ms.assetid: 41e8a777-a57a-4d6c-850f-e21b58081b0d
title: Constantes de LINEDEVSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49717c1adb0f62a48a041f5920c0b82c7b817277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691068"
---
# <a name="linedevstate_-constants"></a><span data-ttu-id="67d73-103">Constantes de LINEDEVSTATE \_</span><span class="sxs-lookup"><span data-stu-id="67d73-103">LINEDEVSTATE\_ Constants</span></span>

<span data-ttu-id="67d73-104">Las constantes de marcador de bits **LINEDEVSTATE \_** describen diversos eventos de estado de línea.</span><span class="sxs-lookup"><span data-stu-id="67d73-104">The **LINEDEVSTATE\_** bit-flag constants describe various line status events.</span></span>

<dl> <dt>

<span data-ttu-id="67d73-105"><span id="LINEDEVSTATE_BATTERY"></span><span id="linedevstate_battery"></span>**\_batería LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="67d73-105"><span id="LINEDEVSTATE_BATTERY"></span><span id="linedevstate_battery"></span>**LINEDEVSTATE\_BATTERY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-106">El nivel de batería ha cambiado significativamente (teléfono móvil).</span><span class="sxs-lookup"><span data-stu-id="67d73-106">The battery level has changed significantly (cellular).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67d73-107"><span id="LINEDEVSTATE_CAPSCHANGE"></span><span id="linedevstate_capschange"></span>**LINEDEVSTATE \_ CAPSCHANGE**</span><span class="sxs-lookup"><span data-stu-id="67d73-107"><span id="LINEDEVSTATE_CAPSCHANGE"></span><span id="linedevstate_capschange"></span>**LINEDEVSTATE\_CAPSCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-108">Indica que, debido a los cambios de configuración realizados por el usuario u otras circunstancias, uno o varios de los miembros de la estructura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para la dirección han cambiado.</span><span class="sxs-lookup"><span data-stu-id="67d73-108">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the address have changed.</span></span> <span data-ttu-id="67d73-109">La aplicación debe usar [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps) para leer la estructura actualizada.</span><span class="sxs-lookup"><span data-stu-id="67d73-109">The application should use [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps) to read the updated structure.</span></span> <span data-ttu-id="67d73-110">Si un proveedor de servicios envía un mensaje [**line \_ LINEDEVSTATE**](line-linedevstate.md) que contiene este valor a TAPI, TAPI lo pasará a las aplicaciones que han negociado la versión 1,4 o posterior de TAPI; las aplicaciones que negocian una versión anterior de TAPI recibirán los mensajes de **línea \_ LINEDEVSTATE** que especifican LINEDEVSTATE \_ reinit, lo que les obliga a apagar y reinicializar su conexión con TAPI para obtener la información actualizada.</span><span class="sxs-lookup"><span data-stu-id="67d73-110">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous TAPI version will receive **LINE\_LINEDEVSTATE** messages specifying LINEDEVSTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67d73-111"><span id="LINEDEVSTATE_CLOSE"></span><span id="linedevstate_close"></span>**LINEDEVSTATE \_ cerrar**</span><span class="sxs-lookup"><span data-stu-id="67d73-111"><span id="LINEDEVSTATE_CLOSE"></span><span id="linedevstate_close"></span>**LINEDEVSTATE\_CLOSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-112">Otra aplicación ha cerrado la línea.</span><span class="sxs-lookup"><span data-stu-id="67d73-112">The line has been closed by another application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67d73-113"><span id="LINEDEVSTATE_CONFIGCHANGE"></span><span id="linedevstate_configchange"></span>**LINEDEVSTATE \_ CONFIGCHANGE**</span><span class="sxs-lookup"><span data-stu-id="67d73-113"><span id="LINEDEVSTATE_CONFIGCHANGE"></span><span id="linedevstate_configchange"></span>**LINEDEVSTATE\_CONFIGCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-114">Indica que se han realizado cambios de configuración en uno o varios de los dispositivos multimedia asociados al dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="67d73-114">Indicates that configuration changes have been made to one or more of the media devices associated with the line device.</span></span> <span data-ttu-id="67d73-115">La aplicación, si lo desea, puede usar [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) para leer la información actualizada.</span><span class="sxs-lookup"><span data-stu-id="67d73-115">The application, if it desires, can use [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) to read the updated information.</span></span> <span data-ttu-id="67d73-116">Si un proveedor de servicios envía un mensaje [**line \_ LINEDEVSTATE**](line-linedevstate.md) que contiene este valor a TAPI, TAPI lo pasará a las aplicaciones que han negociado la versión 1,4 o posterior de TAPI; las aplicaciones que negocian una versión anterior de la API no recibirán ninguna notificación.</span><span class="sxs-lookup"><span data-stu-id="67d73-116">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67d73-117"><span id="LINEDEVSTATE_COMPLCANCEL"></span><span id="linedevstate_complcancel"></span>**LINEDEVSTATE \_ COMPLCANCEL**</span><span class="sxs-lookup"><span data-stu-id="67d73-117"><span id="LINEDEVSTATE_COMPLCANCEL"></span><span id="linedevstate_complcancel"></span>**LINEDEVSTATE\_COMPLCANCEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-118">Indica que la finalización de la llamada identificada por el identificador de finalización incluida en el parámetro *dwParam2* del mensaje de [**línea \_ LINEDEVSTATE**](line-linedevstate.md) se canceló externamente y ya no se considera válida (si ese valor se pasara en una llamada subsiguiente a [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall), la función produciría un error con LINEERR \_ INVALCOMPLETIONID).</span><span class="sxs-lookup"><span data-stu-id="67d73-118">Indicates that the call completion identified by the completion identifier contained in the *dwParam2* parameter of the [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message has been externally canceled and is no longer considered valid (if that value were to be passed in a subsequent call to [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall), the function would fail with LINEERR\_INVALCOMPLETIONID).</span></span> <span data-ttu-id="67d73-119">Si un proveedor de servicios envía un mensaje [**line \_ LINEDEVSTATE**](line-linedevstate.md) que contiene este valor a TAPI, TAPI lo pasará a las aplicaciones que han negociado la versión 1,4 o posterior de TAPI; las aplicaciones que negocian una versión anterior de la API no recibirán ninguna notificación.</span><span class="sxs-lookup"><span data-stu-id="67d73-119">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67d73-120"><span id="LINEDEVSTATE_CONNECTED"></span><span id="linedevstate_connected"></span>**LINEDEVSTATE \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="67d73-120"><span id="LINEDEVSTATE_CONNECTED"></span><span id="linedevstate_connected"></span>**LINEDEVSTATE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-121">La línea se desconectó previamente y ahora está conectada a TAPI.</span><span class="sxs-lookup"><span data-stu-id="67d73-121">The line was previously disconnected and is now connected to TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67d73-122"><span id="LINEDEVSTATE_DEVSPECIFIC"></span><span id="linedevstate_devspecific"></span>**LINEDEVSTATE \_ DEVSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="67d73-122"><span id="LINEDEVSTATE_DEVSPECIFIC"></span><span id="linedevstate_devspecific"></span>**LINEDEVSTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-123">La información específica del dispositivo de la línea ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="67d73-123">The line's device-specific information has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67d73-124"><span id="LINEDEVSTATE_DISCONNECTED"></span><span id="linedevstate_disconnected"></span>**LINEDEVSTATE \_ DESconectado**</span><span class="sxs-lookup"><span data-stu-id="67d73-124"><span id="LINEDEVSTATE_DISCONNECTED"></span><span id="linedevstate_disconnected"></span>**LINEDEVSTATE\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-125">Esta línea estaba conectada previamente y ahora está desconectada de TAPI.</span><span class="sxs-lookup"><span data-stu-id="67d73-125">This line was previously connected and is now disconnected from TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67d73-126"><span id="LINEDEVSTATE_INSERVICE"></span><span id="linedevstate_inservice"></span>**SERVICIO de LINEDEVSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="67d73-126"><span id="LINEDEVSTATE_INSERVICE"></span><span id="linedevstate_inservice"></span>**LINEDEVSTATE\_INSERVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-127">La línea está conectada a TAPI.</span><span class="sxs-lookup"><span data-stu-id="67d73-127">The line is connected to TAPI.</span></span> <span data-ttu-id="67d73-128">Esto sucede cuando TAPI se activa por primera vez o cuando el cable de línea está físicamente conectado y en servicio en el conmutador mientras TAPI está activo.</span><span class="sxs-lookup"><span data-stu-id="67d73-128">This happens when TAPI is first activated or when the line wire is physically plugged in and in-service at the switch while TAPI is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67d73-129"><span id="LINEDEVSTATE_LOCK"></span><span id="linedevstate_lock"></span>**\_bloqueo LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="67d73-129"><span id="LINEDEVSTATE_LOCK"></span><span id="linedevstate_lock"></span>**LINEDEVSTATE\_LOCK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-130">El estado de bloqueo del dispositivo de línea ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="67d73-130">The locked status of the line device has changed.</span></span> <span data-ttu-id="67d73-131">(Para obtener más información, consulte LINEDEVSTATUSFLAGS \_ BLOQUEADO en [**\_ constantes LINEDEVSTATUSFLAGS**](linedevstatusflags--constants.md)).</span><span class="sxs-lookup"><span data-stu-id="67d73-131">(For more information, see LINEDEVSTATUSFLAGS\_LOCKED in [**LINEDEVSTATUSFLAGS\_ Constants**](linedevstatusflags--constants.md).)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67d73-132"><span id="LINEDEVSTATE_MAINTENANCE"></span><span id="linedevstate_maintenance"></span>**mantenimiento de LINEDEVSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="67d73-132"><span id="LINEDEVSTATE_MAINTENANCE"></span><span id="linedevstate_maintenance"></span>**LINEDEVSTATE\_MAINTENANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-133">El mantenimiento se realiza en la línea en el conmutador.</span><span class="sxs-lookup"><span data-stu-id="67d73-133">Maintenance is being performed on the line at the switch.</span></span> <span data-ttu-id="67d73-134">No se puede usar TAPI para operar en el dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="67d73-134">TAPI cannot be used to operate on the line device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67d73-135"><span id="LINEDEVSTATE_MSGWAITOFF"></span><span id="linedevstate_msgwaitoff"></span>**LINEDEVSTATE \_ MSGWAITOFF**</span><span class="sxs-lookup"><span data-stu-id="67d73-135"><span id="LINEDEVSTATE_MSGWAITOFF"></span><span id="linedevstate_msgwaitoff"></span>**LINEDEVSTATE\_MSGWAITOFF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-136">El indicador de espera del mensaje está desactivado.</span><span class="sxs-lookup"><span data-stu-id="67d73-136">The message waiting indicator is turned off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67d73-137"><span id="LINEDEVSTATE_MSGWAITON"></span><span id="linedevstate_msgwaiton"></span>**LINEDEVSTATE \_ MSGWAITON**</span><span class="sxs-lookup"><span data-stu-id="67d73-137"><span id="LINEDEVSTATE_MSGWAITON"></span><span id="linedevstate_msgwaiton"></span>**LINEDEVSTATE\_MSGWAITON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-138">El indicador de espera de mensajes está activado.</span><span class="sxs-lookup"><span data-stu-id="67d73-138">The message waiting indicator is turned on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67d73-139"><span id="LINEDEVSTATE_NUMCALLS"></span><span id="linedevstate_numcalls"></span>**LINEDEVSTATE \_ NUMCALLS**</span><span class="sxs-lookup"><span data-stu-id="67d73-139"><span id="LINEDEVSTATE_NUMCALLS"></span><span id="linedevstate_numcalls"></span>**LINEDEVSTATE\_NUMCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-140">El número de llamadas en el dispositivo de línea ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="67d73-140">The number of calls on the line device has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67d73-141"><span id="LINEDEVSTATE_NUMCOMPLETIONS"></span><span id="linedevstate_numcompletions"></span>**LINEDEVSTATE \_ NUMCOMPLETIONS**</span><span class="sxs-lookup"><span data-stu-id="67d73-141"><span id="LINEDEVSTATE_NUMCOMPLETIONS"></span><span id="linedevstate_numcompletions"></span>**LINEDEVSTATE\_NUMCOMPLETIONS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-142">Ha cambiado el número de finalizaciones de llamadas pendientes en el dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="67d73-142">The number of outstanding call completions on the line device has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67d73-143"><span id="LINEDEVSTATE_OPEN"></span><span id="linedevstate_open"></span>**LINEDEVSTATE \_ abrir**</span><span class="sxs-lookup"><span data-stu-id="67d73-143"><span id="LINEDEVSTATE_OPEN"></span><span id="linedevstate_open"></span>**LINEDEVSTATE\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-144">Otra aplicación ha abierto la línea.</span><span class="sxs-lookup"><span data-stu-id="67d73-144">The line has been opened by another application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67d73-145"><span id="LINEDEVSTATE_OTHER"></span><span id="linedevstate_other"></span>**LINEDEVSTATE \_ otro**</span><span class="sxs-lookup"><span data-stu-id="67d73-145"><span id="LINEDEVSTATE_OTHER"></span><span id="linedevstate_other"></span>**LINEDEVSTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-146">Los elementos de estado de dispositivo distintos de los que se enumeran a continuación han cambiado.</span><span class="sxs-lookup"><span data-stu-id="67d73-146">Device-status items other than those listed below have changed.</span></span> <span data-ttu-id="67d73-147">La aplicación debe comprobar el estado actual del dispositivo para determinar qué elementos han cambiado.</span><span class="sxs-lookup"><span data-stu-id="67d73-147">The application should check the current device status to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67d73-148"><span id="LINEDEVSTATE_OUTOFSERVICE"></span><span id="linedevstate_outofservice"></span>**LINEDEVSTATE \_ OUTOFSERVICE**</span><span class="sxs-lookup"><span data-stu-id="67d73-148"><span id="LINEDEVSTATE_OUTOFSERVICE"></span><span id="linedevstate_outofservice"></span>**LINEDEVSTATE\_OUTOFSERVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-149">La línea está fuera de servicio en el conmutador o está físicamente desconectada.</span><span class="sxs-lookup"><span data-stu-id="67d73-149">The line is out of service at the switch or physically disconnected.</span></span> <span data-ttu-id="67d73-150">No se puede usar TAPI para operar en el dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="67d73-150">TAPI cannot be used to operate on the line device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67d73-151"><span id="LINEDEVSTATE_REINIT"></span><span id="linedevstate_reinit"></span>**reinicialización de LINEDEVSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="67d73-151"><span id="LINEDEVSTATE_REINIT"></span><span id="linedevstate_reinit"></span>**LINEDEVSTATE\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-152">Los elementos han cambiado en la configuración de los dispositivos de línea.</span><span class="sxs-lookup"><span data-stu-id="67d73-152">Items have changed in the configuration of line devices.</span></span> <span data-ttu-id="67d73-153">Para tener en cuenta estos cambios (como en el aspecto de los dispositivos de nueva línea), la aplicación debe reinicializar el uso de TAPI.</span><span class="sxs-lookup"><span data-stu-id="67d73-153">To become aware of these changes (as for the appearance of new line devices) the application should reinitialize its use of TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67d73-154"><span id="LINEDEVSTATE_REMOVED"></span><span id="linedevstate_removed"></span>**LINEDEVSTATE \_ quitado**</span><span class="sxs-lookup"><span data-stu-id="67d73-154"><span id="LINEDEVSTATE_REMOVED"></span><span id="linedevstate_removed"></span>**LINEDEVSTATE\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-155">Indica que el proveedor de servicios está quitando el dispositivo del sistema (lo que es más probable a través de la acción del usuario, a través de un panel de control o una utilidad similar).</span><span class="sxs-lookup"><span data-stu-id="67d73-155">Indicates that the device is being removed from the system by the service provider (most likely through user action, through a control panel or similar utility).</span></span> <span data-ttu-id="67d73-156">Un mensaje de [**línea \_ LINEDEVSTATE**](line-linedevstate.md) con este valor normalmente irá seguido inmediatamente de un mensaje de [**\_ cierre de línea**](line-close.md) en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="67d73-156">A [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message with this value will normally be immediately followed by a [**LINE\_CLOSE**](line-close.md) message on the device.</span></span> <span data-ttu-id="67d73-157">Los intentos posteriores de obtener acceso al dispositivo antes de que se reinicialice TAPI darán lugar a que se \_ devuelva LINEERR Device a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="67d73-157">Subsequent attempts to access the device prior to TAPI being reinitialized will result in LINEERR\_NODEVICE being returned to the application.</span></span> <span data-ttu-id="67d73-158">Si un proveedor de servicios envía un mensaje [**line \_ LINEDEVSTATE**](line-linedevstate.md) que contiene este valor a TAPI, TAPI lo pasará a las aplicaciones que han negociado la versión 1,4 o posterior de TAPI; las aplicaciones que negocian una versión anterior de la API no recibirán ninguna notificación.</span><span class="sxs-lookup"><span data-stu-id="67d73-158">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67d73-159"><span id="LINEDEVSTATE_RINGING"></span><span id="linedevstate_ringing"></span>**\_timbre LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="67d73-159"><span id="LINEDEVSTATE_RINGING"></span><span id="linedevstate_ringing"></span>**LINEDEVSTATE\_RINGING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-160">El modificador indica a la línea que avise al usuario.</span><span class="sxs-lookup"><span data-stu-id="67d73-160">The switch tells the line to alert the user.</span></span>

<span data-ttu-id="67d73-161">**TAPI:** Los proveedores de servicios notifican a las aplicaciones en cada ciclo de timbre enviando repetidamente mensajes de [**línea \_ LINEDEVSTATE**](line-linedevstate.md) que contienen esta constante.</span><span class="sxs-lookup"><span data-stu-id="67d73-161">**TAPI:** Service providers notify applications on each ring cycle by repeatedly sending [**LINE\_LINEDEVSTATE**](line-linedevstate.md) messages containing this constant.</span></span> <span data-ttu-id="67d73-162">Por ejemplo, en el Estados Unidos, los proveedores de servicios envían un mensaje con esta constante cada seis segundos.</span><span class="sxs-lookup"><span data-stu-id="67d73-162">For example, in the United States, service providers send a message with this constant every six seconds.</span></span>

<span data-ttu-id="67d73-163">**TSPI:** En un dispositivo de POTS, el proveedor de servicios puede enviar el mensaje cada vez que la oficina central envía la tensión de timbre.</span><span class="sxs-lookup"><span data-stu-id="67d73-163">**TSPI:** On a POTS device, the service provider can send the message whenever the central office sends ring voltage.</span></span> <span data-ttu-id="67d73-164">En dispositivos digitales como ISDN, es posible que el proveedor de servicios tenga que sintetizar la repetición del mensaje si el modificador solo genera una solicitud de anillo.</span><span class="sxs-lookup"><span data-stu-id="67d73-164">On digital devices such as ISDN, the service provider may need to synthesize the repetition of the message if the switch generates only one ring request.</span></span> <span data-ttu-id="67d73-165">Cada repetición del mensaje debería mostrar el aumento del número de timbres, de modo que las funciones de guardado de peaje funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="67d73-165">Each repetition of the message should show the ring count increasing, so that toll save functions work properly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67d73-166"><span id="LINEDEVSTATE_ROAMMODE"></span><span id="linedevstate_roammode"></span>**LINEDEVSTATE \_ ROAMMODE**</span><span class="sxs-lookup"><span data-stu-id="67d73-166"><span id="LINEDEVSTATE_ROAMMODE"></span><span id="linedevstate_roammode"></span>**LINEDEVSTATE\_ROAMMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-167">El modo de itinerancia del dispositivo de línea ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="67d73-167">The roam mode of the line device has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67d73-168"><span id="LINEDEVSTATE_SIGNAL"></span><span id="linedevstate_signal"></span>**\_señal LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="67d73-168"><span id="LINEDEVSTATE_SIGNAL"></span><span id="linedevstate_signal"></span>**LINEDEVSTATE\_SIGNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-169">El nivel de señal ha cambiado significativamente (teléfono móvil).</span><span class="sxs-lookup"><span data-stu-id="67d73-169">The signal level has changed significantly (cellular).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67d73-170"><span id="LINEDEVSTATE_TERMINALS"></span><span id="linedevstate_terminals"></span>**\_terminales LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="67d73-170"><span id="LINEDEVSTATE_TERMINALS"></span><span id="linedevstate_terminals"></span>**LINEDEVSTATE\_TERMINALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-171">La configuración de terminal ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="67d73-171">The terminal settings have changed.</span></span> <span data-ttu-id="67d73-172">Esto puede ocurrir, por ejemplo, si varios dispositivos de línea comparten terminales entre ellos (por ejemplo, dos líneas que comparten un terminal telefónico).</span><span class="sxs-lookup"><span data-stu-id="67d73-172">This can happen, for example, if multiple line devices share terminals among them (for example, two lines sharing a phone terminal).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67d73-173"><span id="LINEDEVSTATE_TRANSLATECHANGE"></span><span id="linedevstate_translatechange"></span>**LINEDEVSTATE \_ TRANSLATECHANGE**</span><span class="sxs-lookup"><span data-stu-id="67d73-173"><span id="LINEDEVSTATE_TRANSLATECHANGE"></span><span id="linedevstate_translatechange"></span>**LINEDEVSTATE\_TRANSLATECHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="67d73-174">Indica que, debido a los cambios de configuración realizados por el usuario u otras circunstancias, uno o varios de los miembros de la estructura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) han cambiado.</span><span class="sxs-lookup"><span data-stu-id="67d73-174">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) structure have changed.</span></span> <span data-ttu-id="67d73-175">La aplicación debe usar [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps) para leer la estructura actualizada.</span><span class="sxs-lookup"><span data-stu-id="67d73-175">The application should use [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps) to read the updated structure.</span></span> <span data-ttu-id="67d73-176">Si un proveedor de servicios envía un mensaje [**line \_ LINEDEVSTATE**](line-linedevstate.md) que contiene este valor a TAPI, TAPI lo pasará a las aplicaciones que han negociado la versión 1,4 o posterior de TAPI; las aplicaciones que negocian una versión anterior de TAPI recibirán los mensajes de **línea \_ LINEDEVSTATE** que especifican LINEDEVSTATE \_ reinit, lo que les obliga a apagar y reinicializar su conexión con TAPI para obtener la información actualizada.</span><span class="sxs-lookup"><span data-stu-id="67d73-176">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous TAPI version will receive **LINE\_LINEDEVSTATE** messages specifying LINEDEVSTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67d73-177">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67d73-177">Remarks</span></span>

<span data-ttu-id="67d73-178">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="67d73-178">No extensibility.</span></span> <span data-ttu-id="67d73-179">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="67d73-179">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="67d73-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67d73-180">Requirements</span></span>



| <span data-ttu-id="67d73-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="67d73-181">Requirement</span></span> | <span data-ttu-id="67d73-182">Value</span><span class="sxs-lookup"><span data-stu-id="67d73-182">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="67d73-183">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="67d73-183">TAPI version</span></span><br/> | <span data-ttu-id="67d73-184">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="67d73-184">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="67d73-185">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67d73-185">Header</span></span><br/>       | <dl> <span data-ttu-id="67d73-186"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="67d73-186"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67d73-187">Vea también</span><span class="sxs-lookup"><span data-stu-id="67d73-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67d73-188">**cierre de línea \_**</span><span class="sxs-lookup"><span data-stu-id="67d73-188">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="67d73-189">**LÍNEA \_ LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="67d73-189">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="67d73-190">**LINEDEVCAPS**</span><span class="sxs-lookup"><span data-stu-id="67d73-190">**LINEDEVCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[<span data-ttu-id="67d73-191">**lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="67d73-191">**lineGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[<span data-ttu-id="67d73-192">**lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="67d73-192">**lineGetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[<span data-ttu-id="67d73-193">**lineGetTranslateCaps**</span><span class="sxs-lookup"><span data-stu-id="67d73-193">**lineGetTranslateCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[<span data-ttu-id="67d73-194">**LINETRANSLATECAPS**</span><span class="sxs-lookup"><span data-stu-id="67d73-194">**LINETRANSLATECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[<span data-ttu-id="67d73-195">**lineUncompleteCall**</span><span class="sxs-lookup"><span data-stu-id="67d73-195">**lineUncompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




