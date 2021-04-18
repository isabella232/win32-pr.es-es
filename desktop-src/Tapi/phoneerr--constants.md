---
description: Esta es la lista de códigos de error que la implementación puede devolver al invocar operaciones en dispositivos de teléfono. Consulte las descripciones de funciones individuales para determinar cuál de estos códigos de error puede devolver cada función.
ms.assetid: 763a9dc2-3e70-4169-a66e-3aac78ef8d33
title: Constantes de PHONEERR_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b41ba5d14f4aa12318dd4bc9f2b20e4e9e2e6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681291"
---
# <a name="phoneerr_-constants"></a><span data-ttu-id="fa6cf-104">Constantes de PHONEERR \_</span><span class="sxs-lookup"><span data-stu-id="fa6cf-104">PHONEERR\_ Constants</span></span>

<span data-ttu-id="fa6cf-105">Esta es la lista de códigos de error que la implementación puede devolver al invocar operaciones en dispositivos de teléfono.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-105">This is the list of error codes that the implementation can return when invoking operations on phone devices.</span></span> <span data-ttu-id="fa6cf-106">Consulte las descripciones de funciones individuales para determinar cuál de estos códigos de error puede devolver cada función.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-106">Consult the individual function descriptions to determine which of these error codes each function can return.</span></span>

<dl> <dt>

<span data-ttu-id="fa6cf-107"><span id="PHONEERR_ALLOCATED"></span><span id="phoneerr_allocated"></span>**PHONEERR \_ asignado**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-107"><span id="PHONEERR_ALLOCATED"></span><span id="phoneerr_allocated"></span>**PHONEERR\_ALLOCATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-108">El recurso especificado ya está asignado.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-108">The specified resource is already allocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-109"><span id="PHONEERR_BADDEVICEID"></span><span id="phoneerr_baddeviceid"></span>**PHONEERR \_ BADDEVICEID**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-109"><span id="PHONEERR_BADDEVICEID"></span><span id="phoneerr_baddeviceid"></span>**PHONEERR\_BADDEVICEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-110">El identificador de dispositivo especificado no es válido o está fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-110">The specified device identifier is invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-111"><span id="PHONEERR_DISCONNECTED"></span><span id="phoneerr_disconnected"></span>**PHONEERR \_ DESconectado**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-111"><span id="PHONEERR_DISCONNECTED"></span><span id="phoneerr_disconnected"></span>**PHONEERR\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-112">La llamada se desconectó.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-112">The call was disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-113"><span id="PHONEERR_INCOMPATIBLEAPIVERSION"></span><span id="phoneerr_incompatibleapiversion"></span>**PHONEERR \_ INCOMPATIBLEAPIVERSION**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-113"><span id="PHONEERR_INCOMPATIBLEAPIVERSION"></span><span id="phoneerr_incompatibleapiversion"></span>**PHONEERR\_INCOMPATIBLEAPIVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-114">La aplicación solicitó una versión de API o un intervalo de versiones que no se admiten en la implementación de la API de telefonía o en el proveedor de servicios correspondiente.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-114">The application requested an API version or version range that cannot be supported by the Telephony API implementation or the corresponding service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-115"><span id="PHONEERR_INCOMPATIBLEEXTVERSION"></span><span id="phoneerr_incompatibleextversion"></span>**PHONEERR \_ INCOMPATIBLEEXTVERSION**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-115"><span id="PHONEERR_INCOMPATIBLEEXTVERSION"></span><span id="phoneerr_incompatibleextversion"></span>**PHONEERR\_INCOMPATIBLEEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-116">La aplicación solicitó una versión de extensión o un intervalo de versiones que no es compatible con el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-116">The application requested an extension version or version range that cannot be supported by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-117"><span id="PHONEERR_INIFILECORRUPT"></span><span id="phoneerr_inifilecorrupt"></span>**PHONEERR \_ INIFILECORRUPT**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-117"><span id="PHONEERR_INIFILECORRUPT"></span><span id="phoneerr_inifilecorrupt"></span>**PHONEERR\_INIFILECORRUPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-118">Debido a incoherencias internas o problemas de formato en el archivo de Telephon.ini, TAPI no se puede leer ni comprender correctamente.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-118">Because of internal inconsistencies or formatting problems in the Telephon.ini file, it cannot be read and understood properly by TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-119"><span id="PHONEERR_INUSE"></span><span id="phoneerr_inuse"></span>**PHONEERR \_ inuse**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-119"><span id="PHONEERR_INUSE"></span><span id="phoneerr_inuse"></span>**PHONEERR\_INUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-120">El dispositivo está en uso actualmente.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-120">The device is currently in use.</span></span> <span data-ttu-id="fa6cf-121">No se puede configurar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-121">The device cannot be configured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-122"><span id="PHONEERR_INVALAPPHANDLE"></span><span id="phoneerr_invalapphandle"></span>**PHONEERR \_ INVALAPPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-122"><span id="PHONEERR_INVALAPPHANDLE"></span><span id="phoneerr_invalapphandle"></span>**PHONEERR\_INVALAPPHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-123">El identificador de uso especificado o el identificador de registro de la aplicación no es válido.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-123">The application's specified usage handle or registration handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-124"><span id="PHONEERR_INVALAPPNAME"></span><span id="phoneerr_invalappname"></span>**PHONEERR \_ INVALAPPNAME**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-124"><span id="PHONEERR_INVALAPPNAME"></span><span id="phoneerr_invalappname"></span>**PHONEERR\_INVALAPPNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-125">El nombre de aplicación especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-125">The specified application name is invalid.</span></span> <span data-ttu-id="fa6cf-126">Si la aplicación especifica un nombre de aplicación, se supone que la cadena no contiene ningún carácter no visualizable y está terminada en **null**.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-126">If an application name is specified by the application, it is assumed that the string does not contain any nondisplayable characters and is **NULL**-terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-127"><span id="PHONEERR_INVALBUTTONLAMPID"></span><span id="phoneerr_invalbuttonlampid"></span>**PHONEERR \_ INVALBUTTONLAMPID**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-127"><span id="PHONEERR_INVALBUTTONLAMPID"></span><span id="phoneerr_invalbuttonlampid"></span>**PHONEERR\_INVALBUTTONLAMPID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-128">El identificador de botón o lámpara especificado está fuera del intervalo o no es válido.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-128">The specified button/lamp identifier is out of range or invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-129"><span id="PHONEERR_INVALBUTTONMODE"></span><span id="phoneerr_invalbuttonmode"></span>**PHONEERR \_ INVALBUTTONMODE**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-129"><span id="PHONEERR_INVALBUTTONMODE"></span><span id="phoneerr_invalbuttonmode"></span>**PHONEERR\_INVALBUTTONMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-130">El parámetro de modo de botón no es válido.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-130">The button mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-131"><span id="PHONEERR_INVALBUTTONSTATE"></span><span id="phoneerr_invalbuttonstate"></span>**PHONEERR \_ INVALBUTTONSTATE**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-131"><span id="PHONEERR_INVALBUTTONSTATE"></span><span id="phoneerr_invalbuttonstate"></span>**PHONEERR\_INVALBUTTONSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-132">El parámetro de Estados del botón no es válido.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-132">The button states parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-133"><span id="PHONEERR_INVALDATAID"></span><span id="phoneerr_invaldataid"></span>**PHONEERR \_ INVALDATAID**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-133"><span id="PHONEERR_INVALDATAID"></span><span id="phoneerr_invaldataid"></span>**PHONEERR\_INVALDATAID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-134">El identificador de datos especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-134">The specified data identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-135"><span id="PHONEERR_INVALDEVICECLASS"></span><span id="phoneerr_invaldeviceclass"></span>**PHONEERR \_ INVALDEVICECLASS**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-135"><span id="PHONEERR_INVALDEVICECLASS"></span><span id="phoneerr_invaldeviceclass"></span>**PHONEERR\_INVALDEVICECLASS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-136">El teléfono especificado no admite la clase de dispositivo indicada.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-136">The specified phone does not support the indicated device class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-137"><span id="PHONEERR_INVALEXTVERSION"></span><span id="phoneerr_invalextversion"></span>**PHONEERR \_ INVALEXTVERSION**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-137"><span id="PHONEERR_INVALEXTVERSION"></span><span id="phoneerr_invalextversion"></span>**PHONEERR\_INVALEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-138">El número de versión de la extensión del proveedor de servicios no es válido.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-138">The service provider extension version number is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-139"><span id="PHONEERR_INVALHOOKSWITCHDEV"></span><span id="phoneerr_invalhookswitchdev"></span>**PHONEERR \_ INVALHOOKSWITCHDEV**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-139"><span id="PHONEERR_INVALHOOKSWITCHDEV"></span><span id="phoneerr_invalhookswitchdev"></span>**PHONEERR\_INVALHOOKSWITCHDEV**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-140">El parámetro de dispositivo conmutador no es válido.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-140">The hookswitch device parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-141"><span id="PHONEERR_INVALHOOKSWITCHMODE"></span><span id="phoneerr_invalhookswitchmode"></span>**PHONEERR \_ INVALHOOKSWITCHMODE**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-141"><span id="PHONEERR_INVALHOOKSWITCHMODE"></span><span id="phoneerr_invalhookswitchmode"></span>**PHONEERR\_INVALHOOKSWITCHMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-142">El parámetro de modo conmutador no es válido.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-142">The hookswitch mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-143"><span id="PHONEERR_INVALLAMPMODE"></span><span id="phoneerr_invallampmode"></span>**PHONEERR \_ INVALLAMPMODE**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-143"><span id="PHONEERR_INVALLAMPMODE"></span><span id="phoneerr_invallampmode"></span>**PHONEERR\_INVALLAMPMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-144">El parámetro de modo de lámpara especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-144">The specified lamp mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-145"><span id="PHONEERR_INVALPARAM"></span><span id="phoneerr_invalparam"></span>**PHONEERR \_ INVALPARAM**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-145"><span id="PHONEERR_INVALPARAM"></span><span id="phoneerr_invalparam"></span>**PHONEERR\_INVALPARAM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-146">Un parámetro, como un valor de fila o columna o un identificador de ventana, no es válido o está fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-146">A parameter, such as a row or column value or a window handle, is invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-147"><span id="PHONEERR_INVALPHONEHANDLE"></span><span id="phoneerr_invalphonehandle"></span>**PHONEERR \_ INVALPHONEHANDLE**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-147"><span id="PHONEERR_INVALPHONEHANDLE"></span><span id="phoneerr_invalphonehandle"></span>**PHONEERR\_INVALPHONEHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-148">El identificador de dispositivo especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-148">The specified device handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-149"><span id="PHONEERR_INVALPHONESTATE"></span><span id="phoneerr_invalphonestate"></span>**PHONEERR \_ INVALPHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-149"><span id="PHONEERR_INVALPHONESTATE"></span><span id="phoneerr_invalphonestate"></span>**PHONEERR\_INVALPHONESTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-150">El dispositivo telefónico no tiene un estado válido para la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-150">The phone device is not in a valid state for the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-151"><span id="PHONEERR_INVALPOINTER"></span><span id="phoneerr_invalpointer"></span>**PHONEERR \_ INVALPOINTER**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-151"><span id="PHONEERR_INVALPOINTER"></span><span id="phoneerr_invalpointer"></span>**PHONEERR\_INVALPOINTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-152">Uno o varios de los parámetros de puntero especificados no son válidos.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-152">One or more of the specified pointer parameters are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-153"><span id="PHONEERR_INVALPRIVILEGE"></span><span id="phoneerr_invalprivilege"></span>**PHONEERR \_ INVALPRIVILEGE**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-153"><span id="PHONEERR_INVALPRIVILEGE"></span><span id="phoneerr_invalprivilege"></span>**PHONEERR\_INVALPRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-154">El parámetro *dwPrivilege* no es válido.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-154">The *dwPrivilege* parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-155"><span id="PHONEERR_INVALRINGMODE"></span><span id="phoneerr_invalringmode"></span>**PHONEERR \_ INVALRINGMODE**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-155"><span id="PHONEERR_INVALRINGMODE"></span><span id="phoneerr_invalringmode"></span>**PHONEERR\_INVALRINGMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-156">El parámetro de modo de anillo no es válido.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-156">The ring mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-157"><span id="PHONEERR_NODEVICE"></span><span id="phoneerr_nodevice"></span>**PHONEERR \_ Device**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-157"><span id="PHONEERR_NODEVICE"></span><span id="phoneerr_nodevice"></span>**PHONEERR\_NODEVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-158">El identificador de dispositivo especificado, que era válido anteriormente, ya no se acepta porque el dispositivo asociado se ha quitado del sistema desde que TAPI se inicializó por última vez o está dañado de forma que no se detectó en la inicialización.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-158">The specified device identifier, which was previously valid, is no longer accepted because the associated device has been removed from the system since TAPI was last initialized or is corrupt in a way that was not detected at initialization.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-159"><span id="PHONEERR_NODRIVER"></span><span id="phoneerr_nodriver"></span>**PHONEERR \_ NOdriver**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-159"><span id="PHONEERR_NODRIVER"></span><span id="phoneerr_nodriver"></span>**PHONEERR\_NODRIVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-160">El proveedor de servicios de teléfono para el dispositivo especificado encontró que uno de sus componentes falta o está dañado de forma que no se detectó en el momento de la inicialización.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-160">The telephone service provider for the specified device found that one of its components is missing or corrupt in a way that was not detected at initialization time.</span></span> <span data-ttu-id="fa6cf-161">Se recomienda que el usuario Use el panel de control de telefonía para corregir el problema.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-161">The user should be advised to use the Telephony Control Panel to correct the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-162"><span id="PHONEERR_NOMEM"></span><span id="phoneerr_nomem"></span>**PHONEERR \_ NOMEM**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-162"><span id="PHONEERR_NOMEM"></span><span id="phoneerr_nomem"></span>**PHONEERR\_NOMEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-163">Memoria insuficiente para completar la operación solicitada o no se puede asignar o bloquear memoria.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-163">Insufficient memory to complete the requested operation, or unable to allocate or lock memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-164"><span id="PHONEERR_NOTOWNER"></span><span id="phoneerr_notowner"></span>**PHONEERR \_ NOurbanar**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-164"><span id="PHONEERR_NOTOWNER"></span><span id="phoneerr_notowner"></span>**PHONEERR\_NOTOWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-165">La aplicación no tiene privilegios de propietario en el dispositivo de teléfono especificado.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-165">The application does not have owner privilege to the specified phone device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-166"><span id="PHONEERR_OPERATIONFAILED"></span><span id="phoneerr_operationfailed"></span>**PHONEERR \_ OPERATIONFAILED**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-166"><span id="PHONEERR_OPERATIONFAILED"></span><span id="phoneerr_operationfailed"></span>**PHONEERR\_OPERATIONFAILED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-167">No se pudo realizar la operación por un motivo no especificado.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-167">The operation failed for an unspecified reason.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-168"><span id="PHONEERR_OPERATIONUNAVAIL"></span><span id="phoneerr_operationunavail"></span>**PHONEERR \_ OPERATIONUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-168"><span id="PHONEERR_OPERATIONUNAVAIL"></span><span id="phoneerr_operationunavail"></span>**PHONEERR\_OPERATIONUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-169">La operación no está disponible.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-169">The operation is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-170"><span id="PHONEERR_REINIT"></span><span id="phoneerr_reinit"></span>**reinicialización de PHONEERR \_**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-170"><span id="PHONEERR_REINIT"></span><span id="phoneerr_reinit"></span>**PHONEERR\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-171">Si se ha solicitado la reinicialización de TAPI, por ejemplo, como resultado de agregar o quitar un proveedor de servicios de telefonía, se rechazarán las solicitudes [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) o [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) con este error hasta que la última aplicación cierre el uso de la API (con [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)), momento en el que la nueva configuración se vuelve efectiva y las aplicaciones vuelven a permitirse a **phoneInitialize** o **phoneInitializeEx**.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-171">If TAPI reinitialization has been requested, for example as a result of adding or removing a telephony service provider, then [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) or [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) requests are rejected with this error until the last application shuts down its usage of the API (using [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)), at which time the new configuration becomes effective and applications are once again permitted to call **phoneInitialize** or **phoneInitializeEx**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-172"><span id="PHONEERR_REQUESTOVERRUN"></span><span id="phoneerr_requestoverrun"></span>**PHONEERR \_ REQUESTOVERRUN**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-172"><span id="PHONEERR_REQUESTOVERRUN"></span><span id="phoneerr_requestoverrun"></span>**PHONEERR\_REQUESTOVERRUN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-173">Se ha superado el número máximo de solicitudes telefónicas pendientes.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-173">The maximum number of outstanding phone requests has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-174"><span id="PHONEERR_RESOURCEUNAVAIL"></span><span id="phoneerr_resourceunavail"></span>**PHONEERR \_ RESOURCEUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-174"><span id="PHONEERR_RESOURCEUNAVAIL"></span><span id="phoneerr_resourceunavail"></span>**PHONEERR\_RESOURCEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-175">No se puede completar la operación debido a la sobreasignación de recursos.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-175">The operation cannot be completed because of resource overcommitment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-176"><span id="PHONEERR_STRUCTURETOOSMALL"></span><span id="phoneerr_structuretoosmall"></span>**PHONEERR \_ STRUCTURETOOSMALL**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-176"><span id="PHONEERR_STRUCTURETOOSMALL"></span><span id="phoneerr_structuretoosmall"></span>**PHONEERR\_STRUCTURETOOSMALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-177">La estructura de Cap de teléfono especificada es demasiado pequeña.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-177">The specified phone caps structure is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fa6cf-178"><span id="PHONEERR_UNINITIALIZED"></span><span id="phoneerr_uninitialized"></span>**PHONEERR no \_ inicializado**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-178"><span id="PHONEERR_UNINITIALIZED"></span><span id="phoneerr_uninitialized"></span>**PHONEERR\_UNINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fa6cf-179">La operación se invocó antes de cualquier aplicación llamada [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa).</span><span class="sxs-lookup"><span data-stu-id="fa6cf-179">The operation was invoked before any application called [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa).</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa6cf-180">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fa6cf-180">Remarks</span></span>

<span data-ttu-id="fa6cf-181">Los valores de 0xC0000000 a 0xFFFFFFFF están disponibles para las extensiones específicas del dispositivo; los valores 0x80000000 a 0xBFFFFFFF están reservados; y 0x00000000 a 0x7FFFFFFF se usan como identificadores de solicitud.</span><span class="sxs-lookup"><span data-stu-id="fa6cf-181">The values 0xC0000000 through 0xFFFFFFFF are available for device-specific extensions; the values 0x80000000 through 0xBFFFFFFF are reserved; and 0x00000000 through 0x7FFFFFFF are used as request identifiers.</span></span>

<span data-ttu-id="fa6cf-182">Si una aplicación obtiene un error devuelto que no controla específicamente (como un error definido por una extensión específica del dispositivo), debe tratar el error como PHONEERR \_ OPERATIONFAILED (por un motivo no especificado).</span><span class="sxs-lookup"><span data-stu-id="fa6cf-182">If an application gets an error return that it does not specifically handle (such as an error defined by a device-specific extension), it should treat the error as a PHONEERR\_OPERATIONFAILED (for an unspecified reason).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa6cf-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa6cf-183">Requirements</span></span>



| <span data-ttu-id="fa6cf-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa6cf-184">Requirement</span></span> | <span data-ttu-id="fa6cf-185">Value</span><span class="sxs-lookup"><span data-stu-id="fa6cf-185">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fa6cf-186">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="fa6cf-186">TAPI version</span></span><br/> | <span data-ttu-id="fa6cf-187">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="fa6cf-187">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="fa6cf-188">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa6cf-188">Header</span></span><br/>       | <dl> <span data-ttu-id="fa6cf-189"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa6cf-189"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa6cf-190">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa6cf-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa6cf-191">**phoneInitialize**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-191">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="fa6cf-192">**phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-192">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[<span data-ttu-id="fa6cf-193">**phoneOpen**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-193">**phoneOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[<span data-ttu-id="fa6cf-194">**phoneShutdown**</span><span class="sxs-lookup"><span data-stu-id="fa6cf-194">**phoneShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




