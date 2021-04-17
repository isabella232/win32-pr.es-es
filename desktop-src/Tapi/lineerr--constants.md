---
description: A continuación se muestra una lista de códigos de error que TAPI puede devolver al invocar operaciones en líneas, direcciones o llamadas.
ms.assetid: bdaf60d1-6ff2-4bd6-b246-8556d6cae644
title: Constantes de LINEERR_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ed7757377d26dbde832b7ef50f275b45e21760d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691050"
---
# <a name="lineerr_-constants"></a><span data-ttu-id="b8a11-103">Constantes de LINEERR \_</span><span class="sxs-lookup"><span data-stu-id="b8a11-103">LINEERR\_ Constants</span></span>

<span data-ttu-id="b8a11-104">A continuación se muestra una lista de códigos de error que TAPI puede devolver al invocar operaciones en líneas, direcciones o llamadas.</span><span class="sxs-lookup"><span data-stu-id="b8a11-104">The following is a list of error codes that TAPI can return when invoking operations on lines, addresses, or calls.</span></span> <span data-ttu-id="b8a11-105">Para obtener más información sobre cómo determinar cuál de estos códigos de error puede devolver una función determinada, vea las descripciones de funciones individuales.</span><span class="sxs-lookup"><span data-stu-id="b8a11-105">For more information about how to determine which of these error codes a particular function can return, see the individual function descriptions.</span></span>

<dl> <dt>

<span data-ttu-id="b8a11-106"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR \_ ADDRESSBLOCKED**</span><span class="sxs-lookup"><span data-stu-id="b8a11-106"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR\_ADDRESSBLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-107">La dirección especificada está bloqueada para marcarse en la llamada especificada.</span><span class="sxs-lookup"><span data-stu-id="b8a11-107">The specified address is blocked from being dialed on the specified call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-108"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR \_ ADDRESSBLOCKED**</span><span class="sxs-lookup"><span data-stu-id="b8a11-108"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR\_ADDRESSBLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-109">La dirección de llamada de destino tiene habilitado el bloqueo de llamadas.</span><span class="sxs-lookup"><span data-stu-id="b8a11-109">The target call address has call blocking enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-110"><span id="LINEERR_ALLOCATED"></span><span id="lineerr_allocated"></span>**LINEERR \_ asignado**</span><span class="sxs-lookup"><span data-stu-id="b8a11-110"><span id="LINEERR_ALLOCATED"></span><span id="lineerr_allocated"></span>**LINEERR\_ALLOCATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-111">No se puede abrir la línea debido a una condición persistente, como la de un puerto serie abierto exclusivamente por otro proceso.</span><span class="sxs-lookup"><span data-stu-id="b8a11-111">The line cannot be opened due to a persistent condition, such as that of a serial port being exclusively opened by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-112"><span id="LINEERR_BADDEVICEID"></span><span id="lineerr_baddeviceid"></span>**LINEERR \_ BADDEVICEID**</span><span class="sxs-lookup"><span data-stu-id="b8a11-112"><span id="LINEERR_BADDEVICEID"></span><span id="lineerr_baddeviceid"></span>**LINEERR\_BADDEVICEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-113">El identificador de dispositivo o el identificador de dispositivo de línea especificado, como en un parámetro *dwDeviceID* , no es válido o está fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="b8a11-113">The specified device identifier or line device identifier, such as in a *dwDeviceID* parameter, is invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-114"><span id="LINEERR_BEARERMODEUNAVAIL"></span><span id="lineerr_bearermodeunavail"></span>**LINEERR \_ BEARERMODEUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="b8a11-114"><span id="LINEERR_BEARERMODEUNAVAIL"></span><span id="lineerr_bearermodeunavail"></span>**LINEERR\_BEARERMODEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-115">El miembro del modo de portador de [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) no es válido, el modo de portador especificado en **LINECALLPARAMS** no está disponible o el modo de portador de llamada no se puede cambiar al modo de portador especificado.</span><span class="sxs-lookup"><span data-stu-id="b8a11-115">The bearer mode member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) is invalid, the bearer mode specified in **LINECALLPARAMS** is not available, or the call bearer mode cannot be changed to the specified bearer mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-116"><span id="LINEERR_BILLINGREJECTED"></span><span id="lineerr_billingrejected"></span>**LINEERR \_ BILLINGREJECTED**</span><span class="sxs-lookup"><span data-stu-id="b8a11-116"><span id="LINEERR_BILLINGREJECTED"></span><span id="lineerr_billingrejected"></span>**LINEERR\_BILLINGREJECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-117">Se rechazó el modo de facturación de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b8a11-117">The billing mode of the call was rejected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-118"><span id="LINEERR_CALLUNAVAIL"></span><span id="lineerr_callunavail"></span>**LINEERR \_ CALLUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="b8a11-118"><span id="LINEERR_CALLUNAVAIL"></span><span id="lineerr_callunavail"></span>**LINEERR\_CALLUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-119">Todos los aspectos de la llamada en la dirección especificada están actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="b8a11-119">All call appearances on the specified address are currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-120"><span id="LINEERR_COMPLETIONOVERRUN"></span><span id="lineerr_completionoverrun"></span>**LINEERR \_ COMPLETIONOVERRUN**</span><span class="sxs-lookup"><span data-stu-id="b8a11-120"><span id="LINEERR_COMPLETIONOVERRUN"></span><span id="lineerr_completionoverrun"></span>**LINEERR\_COMPLETIONOVERRUN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-121">Se ha superado el número máximo de finalizaciones de llamadas pendientes.</span><span class="sxs-lookup"><span data-stu-id="b8a11-121">The maximum number of outstanding call completions has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-122"><span id="LINEERR_CONFERENCEFULL"></span><span id="lineerr_conferencefull"></span>**LINEERR \_ CONFERENCEFULL**</span><span class="sxs-lookup"><span data-stu-id="b8a11-122"><span id="LINEERR_CONFERENCEFULL"></span><span id="lineerr_conferencefull"></span>**LINEERR\_CONFERENCEFULL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-123">Se ha alcanzado el número máximo de entidades de una conferencia o el número de entidades solicitado no se puede satisfacer.</span><span class="sxs-lookup"><span data-stu-id="b8a11-123">The maximum number of parties for a conference has been reached, or the requested number of parties cannot be satisfied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-124"><span id="LINEERR_DIALBILLING"></span><span id="lineerr_dialbilling"></span>**LINEERR \_ DIALBILLING**</span><span class="sxs-lookup"><span data-stu-id="b8a11-124"><span id="LINEERR_DIALBILLING"></span><span id="lineerr_dialbilling"></span>**LINEERR\_DIALBILLING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-125">El parámetro de dirección de marcado contiene caracteres de control de marcado no procesados por el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="b8a11-125">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-126"><span id="LINEERR_DIALDIALTONE"></span><span id="lineerr_dialdialtone"></span>**LINEERR \_ DIALDIALTONE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-126"><span id="LINEERR_DIALDIALTONE"></span><span id="lineerr_dialdialtone"></span>**LINEERR\_DIALDIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-127">El parámetro de dirección de marcado contiene caracteres de control de marcado no procesados por el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="b8a11-127">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-128"><span id="LINEERR_DIALPROMPT"></span><span id="lineerr_dialprompt"></span>**LINEERR \_ DIALPROMPT**</span><span class="sxs-lookup"><span data-stu-id="b8a11-128"><span id="LINEERR_DIALPROMPT"></span><span id="lineerr_dialprompt"></span>**LINEERR\_DIALPROMPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-129">El parámetro de dirección de marcado contiene caracteres de control de marcado no procesados por el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="b8a11-129">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-130"><span id="LINEERR_DIALQUIET"></span><span id="lineerr_dialquiet"></span>**LINEERR \_ DIALQUIET**</span><span class="sxs-lookup"><span data-stu-id="b8a11-130"><span id="LINEERR_DIALQUIET"></span><span id="lineerr_dialquiet"></span>**LINEERR\_DIALQUIET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-131">El parámetro de dirección de marcado contiene caracteres de control de marcado no procesados por el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="b8a11-131">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-132"><span id="LINEERR_DIALVOICEDETECT"></span><span id="lineerr_dialvoicedetect"></span>**LINEERR \_ DIALVOICEDETECT**</span><span class="sxs-lookup"><span data-stu-id="b8a11-132"><span id="LINEERR_DIALVOICEDETECT"></span><span id="lineerr_dialvoicedetect"></span>**LINEERR\_DIALVOICEDETECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-133">Uso del modificador de marcado (:) no se admite.</span><span class="sxs-lookup"><span data-stu-id="b8a11-133">Use of the dial modifier (:) is not supported.</span></span> <span data-ttu-id="b8a11-134">Este valor solo se expone a las aplicaciones que negocian una versión de TAPI 2,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b8a11-134">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-135"><span id="LINEERR_DISCONNECTED"></span><span id="lineerr_disconnected"></span>**LINEERR \_ DESconectado**</span><span class="sxs-lookup"><span data-stu-id="b8a11-135"><span id="LINEERR_DISCONNECTED"></span><span id="lineerr_disconnected"></span>**LINEERR\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-136">La llamada se ha desconectado.</span><span class="sxs-lookup"><span data-stu-id="b8a11-136">The call has been disconnected.</span></span> <span data-ttu-id="b8a11-137">Este valor solo se expone a las aplicaciones que negocian una versión de TAPI 2,2 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b8a11-137">This value is exposed only to applications that negotiate a TAPI version of 2.2 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-138"><span id="LINEERR_INCOMPATIBLEAPIVERSION"></span><span id="lineerr_incompatibleapiversion"></span>**LINEERR \_ INCOMPATIBLEAPIVERSION**</span><span class="sxs-lookup"><span data-stu-id="b8a11-138"><span id="LINEERR_INCOMPATIBLEAPIVERSION"></span><span id="lineerr_incompatibleapiversion"></span>**LINEERR\_INCOMPATIBLEAPIVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-139">La aplicación solicitó una versión de TAPI o un intervalo de versiones que es incompatible con, o no es compatible con, la implementación de la API de telefonía y el proveedor de servicios correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b8a11-139">The application requested a TAPI version or version range that is either incompatible with, or cannot be supported by, the Telephony API implementation and the corresponding service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-140"><span id="LINEERR_INCOMPATIBLEEXTVERSION"></span><span id="lineerr_incompatibleextversion"></span>**LINEERR \_ INCOMPATIBLEEXTVERSION**</span><span class="sxs-lookup"><span data-stu-id="b8a11-140"><span id="LINEERR_INCOMPATIBLEEXTVERSION"></span><span id="lineerr_incompatibleextversion"></span>**LINEERR\_INCOMPATIBLEEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-141">La aplicación solicitó un intervalo de versiones de la extensión que no es válido o no es compatible con el proveedor de servicios correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b8a11-141">The application requested an extension version range that is either invalid or cannot be supported by the corresponding service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-142"><span id="LINEERR_INIFILECORRUPT"></span><span id="lineerr_inifilecorrupt"></span>**LINEERR \_ INIFILECORRUPT**</span><span class="sxs-lookup"><span data-stu-id="b8a11-142"><span id="LINEERR_INIFILECORRUPT"></span><span id="lineerr_inifilecorrupt"></span>**LINEERR\_INIFILECORRUPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-143">TAPI no puede leer ni comprender correctamente el archivo de Telephon.ini debido a incoherencias internas o problemas de formato.</span><span class="sxs-lookup"><span data-stu-id="b8a11-143">The Telephon.ini file cannot be read or understood properly by TAPI because of internal inconsistencies or formatting problems.</span></span> <span data-ttu-id="b8a11-144">Por ejemplo, la \[ \] sección ubicaciones, \[ tarjetas \] o \[ países \] del archivo Telephon.ini puede estar dañada o ser incoherente.</span><span class="sxs-lookup"><span data-stu-id="b8a11-144">For example, the \[Locations\], \[Cards\], or \[Countries\] section of the Telephon.ini file may be corrupted or inconsistent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-145"><span id="LINEERR_INUSE"></span><span id="lineerr_inuse"></span>**LINEERR \_ inuse**</span><span class="sxs-lookup"><span data-stu-id="b8a11-145"><span id="LINEERR_INUSE"></span><span id="lineerr_inuse"></span>**LINEERR\_INUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-146">El dispositivo de línea está en uso y no se puede configurar actualmente, permitir que se agregue una entidad, permitir la respuesta de una llamada, permitir que se realice una llamada o permitir la transferencia de una llamada.</span><span class="sxs-lookup"><span data-stu-id="b8a11-146">The line device is in use and cannot currently be configured, allow a party to be added, allow a call to be answered, allow a call to be placed, or allow a call to be transferred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-147"><span id="LINEERR_INVALADDRESS"></span><span id="lineerr_invaladdress"></span>**LINEERR \_ INVALADDRESS**</span><span class="sxs-lookup"><span data-stu-id="b8a11-147"><span id="LINEERR_INVALADDRESS"></span><span id="lineerr_invaladdress"></span>**LINEERR\_INVALADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-148">Una dirección especificada no es válida o no está permitida.</span><span class="sxs-lookup"><span data-stu-id="b8a11-148">A specified address is either invalid or not allowed.</span></span> <span data-ttu-id="b8a11-149">Si no es válido, la dirección contiene caracteres o dígitos no válidos, o la dirección de destino contiene caracteres de control de marcado (W, @, $ o?) que no son compatibles con el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="b8a11-149">If invalid, the address contains invalid characters or digits, or the destination address contains dialing control characters (W, @, $, or ?) that are not supported by the service provider.</span></span> <span data-ttu-id="b8a11-150">Si no se permite, la dirección especificada no está asignada a la línea especificada o no es válida para la redirección de direcciones.</span><span class="sxs-lookup"><span data-stu-id="b8a11-150">If not allowed, the specified address is either not assigned to the specified line or is not valid for address redirection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-151"><span id="LINEERR_INVALADDRESSID"></span><span id="lineerr_invaladdressid"></span>**LINEERR \_ INVALADDRESSID**</span><span class="sxs-lookup"><span data-stu-id="b8a11-151"><span id="LINEERR_INVALADDRESSID"></span><span id="lineerr_invaladdressid"></span>**LINEERR\_INVALADDRESSID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-152">El identificador de dirección especificado no es válido o está fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="b8a11-152">The specified address identifier is either invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-153"><span id="LINEERR_INVALADDRESSMODE"></span><span id="lineerr_invaladdressmode"></span>**LINEERR \_ INVALADDRESSMODE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-153"><span id="LINEERR_INVALADDRESSMODE"></span><span id="lineerr_invaladdressmode"></span>**LINEERR\_INVALADDRESSMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-154">El modo de dirección especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-154">The specified address mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-155"><span id="LINEERR_INVALADDRESSSTATE"></span><span id="lineerr_invaladdressstate"></span>**LINEERR \_ INVALADDRESSSTATE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-155"><span id="LINEERR_INVALADDRESSSTATE"></span><span id="lineerr_invaladdressstate"></span>**LINEERR\_INVALADDRESSSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-156">El estado de la dirección especificada contiene uno o varios bits que no son [**\_ constantes LINEADDRESSSTATE**](lineaddressstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="b8a11-156">The specified address state contains one or more bits that are not [**LINEADDRESSSTATE\_ constants**](lineaddressstate--constants.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-157"><span id="LINEERR_INVALADDRESSTYPE"></span><span id="lineerr_invaladdresstype"></span>**LINEERR \_ INVALADDRESSTYPE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-157"><span id="LINEERR_INVALADDRESSTYPE"></span><span id="lineerr_invaladdresstype"></span>**LINEERR\_INVALADDRESSTYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-158">La aplicación hizo referencia a un tipo de dirección que no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-158">The application referenced an address type that is not valid.</span></span> <span data-ttu-id="b8a11-159">Este valor solo se expone a las aplicaciones que negocian una versión de TAPI 3,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b8a11-159">This value is exposed only to applications that negotiate a TAPI version of 3.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-160"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR \_ INVALAGENTACTIVITY**</span><span class="sxs-lookup"><span data-stu-id="b8a11-160"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR\_INVALAGENTACTIVITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-161">La actividad del agente especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="b8a11-161">The specified agent activity is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-162"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR \_ INVALAGENTACTIVITY**</span><span class="sxs-lookup"><span data-stu-id="b8a11-162"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR\_INVALAGENTACTIVITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-163">La aplicación que invoca esta operación es el destino de la entrega indirecta.</span><span class="sxs-lookup"><span data-stu-id="b8a11-163">The application invoking this operation is the target of the indirect handoff.</span></span> <span data-ttu-id="b8a11-164">Es decir, TAPI ha determinado que la aplicación que realiza la llamada es también la aplicación de mayor prioridad para el tipo de medio especificado.</span><span class="sxs-lookup"><span data-stu-id="b8a11-164">That is, TAPI has determined that the calling application is also the highest priority application for the given media type.</span></span> <span data-ttu-id="b8a11-165">Este valor solo se expone a las aplicaciones que negocian una versión de TAPI 2,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b8a11-165">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-166"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR \_ INVALAGENTGROUP**</span><span class="sxs-lookup"><span data-stu-id="b8a11-166"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR\_INVALAGENTGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-167">La información del grupo de agentes especificado no es válida o contiene errores.</span><span class="sxs-lookup"><span data-stu-id="b8a11-167">The specified agent group information is not valid or contains errors.</span></span> <span data-ttu-id="b8a11-168">No se ha realizado la acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="b8a11-168">The requested action has not been performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-169"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR \_ INVALAGENTGROUP**</span><span class="sxs-lookup"><span data-stu-id="b8a11-169"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR\_INVALAGENTGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-170">La aplicación hizo referencia a un grupo de agentes que no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-170">The application referenced an agent group that is not valid.</span></span> <span data-ttu-id="b8a11-171">Este valor solo se expone a las aplicaciones que negocian una versión de TAPI 2,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b8a11-171">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-172"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR \_ INVALAGENTID**</span><span class="sxs-lookup"><span data-stu-id="b8a11-172"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR\_INVALAGENTID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-173">El identificador de agente especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-173">The specified agent identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-174"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR \_ INVALAGENTID**</span><span class="sxs-lookup"><span data-stu-id="b8a11-174"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR\_INVALAGENTID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-175">Se usó un identificador de agente no válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-175">An invalid agent identifier was used.</span></span> <span data-ttu-id="b8a11-176">Este valor solo se expone a las aplicaciones que negocian una versión de TAPI 2,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b8a11-176">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-177"><span id="LINEERR_INVALAGENTSESSIONSTATE"></span><span id="lineerr_invalagentsessionstate"></span>**LINEERR \_ INVALAGENTSESSIONSTATE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-177"><span id="LINEERR_INVALAGENTSESSIONSTATE"></span><span id="lineerr_invalagentsessionstate"></span>**LINEERR\_INVALAGENTSESSIONSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-178">El estado de sesión del agente no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-178">The agent session state is invalid.</span></span> <span data-ttu-id="b8a11-179">Este valor solo se expone a las aplicaciones que negocian una versión de TAPI 2,2 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b8a11-179">This value is exposed only to applications that negotiate a TAPI version of 2.2 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-180"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR \_ INVALAGENTSTATE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-180"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR\_INVALAGENTSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-181">El estado del agente especificado no es válido o contiene errores.</span><span class="sxs-lookup"><span data-stu-id="b8a11-181">The specified agent state is not valid or contains errors.</span></span> <span data-ttu-id="b8a11-182">No se ha realizado ningún cambio en el estado del agente de la dirección especificada.</span><span class="sxs-lookup"><span data-stu-id="b8a11-182">No changes have been made to the agent state of the specified address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-183"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR \_ INVALAGENTSTATE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-183"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR\_INVALAGENTSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-184">La aplicación hizo referencia a un estado del agente que no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-184">The application referenced an agent state that is not valid.</span></span> <span data-ttu-id="b8a11-185">Este valor solo se expone a las aplicaciones que negocian una versión de TAPI 2,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b8a11-185">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-186"><span id="LINEERR_INVALAPPHANDLE"></span><span id="lineerr_invalapphandle"></span>**LINEERR \_ INVALAPPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-186"><span id="LINEERR_INVALAPPHANDLE"></span><span id="lineerr_invalapphandle"></span>**LINEERR\_INVALAPPHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-187">El identificador de la aplicación (como se especifica mediante un parámetro *hLineApp* ) o el identificador de registro de la aplicación no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-187">The application handle (such as specified by a *hLineApp* parameter) or the application registration handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-188"><span id="LINEERR_INVALAPPNAME"></span><span id="lineerr_invalappname"></span>**LINEERR \_ INVALAPPNAME**</span><span class="sxs-lookup"><span data-stu-id="b8a11-188"><span id="LINEERR_INVALAPPNAME"></span><span id="lineerr_invalappname"></span>**LINEERR\_INVALAPPNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-189">El nombre de aplicación especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-189">The specified application name is invalid.</span></span> <span data-ttu-id="b8a11-190">Si la aplicación especifica un nombre de aplicación, se supone que la cadena no contiene ningún carácter que no se pueda mostrar y está terminada en cero.</span><span class="sxs-lookup"><span data-stu-id="b8a11-190">If an application name is specified by the application, it is assumed that the string does not contain any non-displayable characters, and is zero-terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-191"><span id="LINEERR_INVALBEARERMODE"></span><span id="lineerr_invalbearermode"></span>**LINEERR \_ INVALBEARERMODE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-191"><span id="LINEERR_INVALBEARERMODE"></span><span id="lineerr_invalbearermode"></span>**LINEERR\_INVALBEARERMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-192">El modo de portador especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-192">The specified bearer mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-193"><span id="LINEERR_INVALCALLCOMPLMODE"></span><span id="lineerr_invalcallcomplmode"></span>**LINEERR \_ INVALCALLCOMPLMODE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-193"><span id="LINEERR_INVALCALLCOMPLMODE"></span><span id="lineerr_invalcallcomplmode"></span>**LINEERR\_INVALCALLCOMPLMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-194">La finalización especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="b8a11-194">The specified completion is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-195"><span id="LINEERR_INVALCALLHANDLE"></span><span id="lineerr_invalcallhandle"></span>**LINEERR \_ INVALCALLHANDLE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-195"><span id="LINEERR_INVALCALLHANDLE"></span><span id="lineerr_invalcallhandle"></span>**LINEERR\_INVALCALLHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-196">El identificador de llamada especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-196">The specified call handle is not valid.</span></span> <span data-ttu-id="b8a11-197">Por ejemplo, el identificador no es **null** , pero no pertenece a la línea especificada.</span><span class="sxs-lookup"><span data-stu-id="b8a11-197">For example, the handle is not **NULL** but does not belong to the given line.</span></span> <span data-ttu-id="b8a11-198">En algunos casos, el identificador del dispositivo de llamada especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-198">In some cases, the specified call device handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-199"><span id="LINEERR_INVALCALLPARAMS"></span><span id="lineerr_invalcallparams"></span>**LINEERR \_ INVALCALLPARAMS**</span><span class="sxs-lookup"><span data-stu-id="b8a11-199"><span id="LINEERR_INVALCALLPARAMS"></span><span id="lineerr_invalcallparams"></span>**LINEERR\_INVALCALLPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-200">Los parámetros de llamada especificados no son válidos.</span><span class="sxs-lookup"><span data-stu-id="b8a11-200">The specified call parameters are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-201"><span id="LINEERR_INVALCALLPRIVILEGE"></span><span id="lineerr_invalcallprivilege"></span>**LINEERR \_ INVALCALLPRIVILEGE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-201"><span id="LINEERR_INVALCALLPRIVILEGE"></span><span id="lineerr_invalcallprivilege"></span>**LINEERR\_INVALCALLPRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-202">El parámetro de privilegio de llamada especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-202">The specified call privilege parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-203"><span id="LINEERR_INVALCALLSELECT"></span><span id="lineerr_invalcallselect"></span>**LINEERR \_ INVALCALLSELECT**</span><span class="sxs-lookup"><span data-stu-id="b8a11-203"><span id="LINEERR_INVALCALLSELECT"></span><span id="lineerr_invalcallselect"></span>**LINEERR\_INVALCALLSELECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-204">El parámetro Select especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-204">The specified select parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-205"><span id="LINEERR_INVALCALLSTATE"></span><span id="lineerr_invalcallstate"></span>**LINEERR \_ INVALCALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-205"><span id="LINEERR_INVALCALLSTATE"></span><span id="lineerr_invalcallstate"></span>**LINEERR\_INVALCALLSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-206">El estado actual de una llamada no tiene un estado válido para la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="b8a11-206">The current state of a call is not in a valid state for the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-207"><span id="LINEERR_INVALCALLSTATELIST"></span><span id="lineerr_invalcallstatelist"></span>**LINEERR \_ INVALCALLSTATELIST**</span><span class="sxs-lookup"><span data-stu-id="b8a11-207"><span id="LINEERR_INVALCALLSTATELIST"></span><span id="lineerr_invalcallstatelist"></span>**LINEERR\_INVALCALLSTATELIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-208">La lista de Estados de llamada especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="b8a11-208">The specified call state list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-209"><span id="LINEERR_INVALCARD"></span><span id="lineerr_invalcard"></span>**LINEERR \_ INVALCARD**</span><span class="sxs-lookup"><span data-stu-id="b8a11-209"><span id="LINEERR_INVALCARD"></span><span id="lineerr_invalcard"></span>**LINEERR\_INVALCARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-210">No se encontró el identificador de tarjeta permanente especificado en *dwCard* en ninguna entrada de la \[ \] sección de tarjetas del registro.</span><span class="sxs-lookup"><span data-stu-id="b8a11-210">The permanent card identifier specified in *dwCard* could not be found in any entry in the \[Cards\] section in the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-211"><span id="LINEERR_INVALCOMPLETIONID"></span><span id="lineerr_invalcompletionid"></span>**LINEERR \_ INVALCOMPLETIONID**</span><span class="sxs-lookup"><span data-stu-id="b8a11-211"><span id="LINEERR_INVALCOMPLETIONID"></span><span id="lineerr_invalcompletionid"></span>**LINEERR\_INVALCOMPLETIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-212">El identificador de finalización no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-212">The completion identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-213"><span id="LINEERR_INVALCONFCALLHANDLE"></span><span id="lineerr_invalconfcallhandle"></span>**LINEERR \_ INVALCONFCALLHANDLE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-213"><span id="LINEERR_INVALCONFCALLHANDLE"></span><span id="lineerr_invalconfcallhandle"></span>**LINEERR\_INVALCONFCALLHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-214">El identificador de llamada especificado para la llamada de conferencia no es válido o no es un identificador de una llamada de conferencia.</span><span class="sxs-lookup"><span data-stu-id="b8a11-214">The specified call handle for the conference call is invalid or is not a handle for a conference call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-215"><span id="LINEERR_INVALCONSULTCALLHANDLE"></span><span id="lineerr_invalconsultcallhandle"></span>**LINEERR \_ INVALCONSULTCALLHANDLE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-215"><span id="LINEERR_INVALCONSULTCALLHANDLE"></span><span id="lineerr_invalconsultcallhandle"></span>**LINEERR\_INVALCONSULTCALLHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-216">El identificador de llamada de consulta especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-216">The specified consultation call handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-217"><span id="LINEERR_INVALCOUNTRYCODE"></span><span id="lineerr_invalcountrycode"></span>**LINEERR \_ INVALCOUNTRYCODE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-217"><span id="LINEERR_INVALCOUNTRYCODE"></span><span id="lineerr_invalcountrycode"></span>**LINEERR\_INVALCOUNTRYCODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-218">El código de país o región especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-218">The specified country or region code is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-219"><span id="LINEERR_INVALDEVICECLASS"></span><span id="lineerr_invaldeviceclass"></span>**LINEERR \_ INVALDEVICECLASS**</span><span class="sxs-lookup"><span data-stu-id="b8a11-219"><span id="LINEERR_INVALDEVICECLASS"></span><span id="lineerr_invaldeviceclass"></span>**LINEERR\_INVALDEVICECLASS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-220">El dispositivo de línea no tiene ningún dispositivo asociado para la clase de dispositivo especificada o la línea especificada no admite la clase de dispositivo indicada.</span><span class="sxs-lookup"><span data-stu-id="b8a11-220">The line device has no associated device for the given device class, or the specified line does not support the indicated device class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-221"><span id="LINEERR_INVALDEVICEHANDLE"></span><span id="lineerr_invaldevicehandle"></span>**LINEERR \_ INVALDEVICEHANDLE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-221"><span id="LINEERR_INVALDEVICEHANDLE"></span><span id="lineerr_invaldevicehandle"></span>**LINEERR\_INVALDEVICEHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-222">El identificador del dispositivo de línea no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-222">The line device handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-223"><span id="LINEERR_INVALDIALPARAMS"></span><span id="lineerr_invaldialparams"></span>**LINEERR \_ INVALDIALPARAMS**</span><span class="sxs-lookup"><span data-stu-id="b8a11-223"><span id="LINEERR_INVALDIALPARAMS"></span><span id="lineerr_invaldialparams"></span>**LINEERR\_INVALDIALPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-224">Los parámetros de marcado no son válidos.</span><span class="sxs-lookup"><span data-stu-id="b8a11-224">The dialing parameters are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-225"><span id="LINEERR_INVALDIGITLIST"></span><span id="lineerr_invaldigitlist"></span>**LINEERR \_ INVALDIGITLIST**</span><span class="sxs-lookup"><span data-stu-id="b8a11-225"><span id="LINEERR_INVALDIGITLIST"></span><span id="lineerr_invaldigitlist"></span>**LINEERR\_INVALDIGITLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-226">La lista de dígitos especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="b8a11-226">The specified digit list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-227"><span id="LINEERR_INVALDIGITMODE"></span><span id="lineerr_invaldigitmode"></span>**LINEERR \_ INVALDIGITMODE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-227"><span id="LINEERR_INVALDIGITMODE"></span><span id="lineerr_invaldigitmode"></span>**LINEERR\_INVALDIGITMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-228">El modo de dígito especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-228">The specified digit mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-229"><span id="LINEERR_INVALDIGITS"></span><span id="lineerr_invaldigits"></span>**LINEERR \_ INVALDIGITS**</span><span class="sxs-lookup"><span data-stu-id="b8a11-229"><span id="LINEERR_INVALDIGITS"></span><span id="lineerr_invaldigits"></span>**LINEERR\_INVALDIGITS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-230">Los dígitos de terminación especificados no son válidos.</span><span class="sxs-lookup"><span data-stu-id="b8a11-230">The specified termination digits are not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-231"><span id="LINEERR_INVALEXTVERSION"></span><span id="lineerr_invalextversion"></span>**LINEERR \_ INVALEXTVERSION**</span><span class="sxs-lookup"><span data-stu-id="b8a11-231"><span id="LINEERR_INVALEXTVERSION"></span><span id="lineerr_invalextversion"></span>**LINEERR\_INVALEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-232">El número de versión de la extensión del proveedor de servicios no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-232">The service provider extension version number is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-233"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR \_ INVALFEATURE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-233"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR\_INVALFEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-234">El parámetro *dwFeature* no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-234">The *dwFeature* parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-235"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR \_ INVALFEATURE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-235"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR\_INVALFEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-236">La aplicación invocó una característica que no está disponible en esta línea.</span><span class="sxs-lookup"><span data-stu-id="b8a11-236">The application invoked a feature that is not available on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-237"><span id="LINEERR_INVALGROUPID"></span><span id="lineerr_invalgroupid"></span>**LINEERR \_ INVALGROUPID**</span><span class="sxs-lookup"><span data-stu-id="b8a11-237"><span id="LINEERR_INVALGROUPID"></span><span id="lineerr_invalgroupid"></span>**LINEERR\_INVALGROUPID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-238">El identificador de grupo especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-238">The specified group identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-239"><span id="LINEERR_INVALLINEHANDLE"></span><span id="lineerr_invallinehandle"></span>**LINEERR \_ INVALLINEHANDLE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-239"><span id="LINEERR_INVALLINEHANDLE"></span><span id="lineerr_invallinehandle"></span>**LINEERR\_INVALLINEHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-240">La llamada, el dispositivo, el dispositivo de línea o el identificador de línea especificados no son válidos.</span><span class="sxs-lookup"><span data-stu-id="b8a11-240">The specified call, device, line device, or line handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-241"><span id="LINEERR_INVALLINESTATE"></span><span id="lineerr_invallinestate"></span>**LINEERR \_ INVALLINESTATE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-241"><span id="LINEERR_INVALLINESTATE"></span><span id="lineerr_invallinestate"></span>**LINEERR\_INVALLINESTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-242">No se puede cambiar la configuración del dispositivo en el estado de línea actual.</span><span class="sxs-lookup"><span data-stu-id="b8a11-242">The device configuration may not be changed in the current line state.</span></span> <span data-ttu-id="b8a11-243">La línea puede estar en uso por otra aplicación o un parámetro *dwLineStates* contiene uno o varios bits que no son [ \_ constantes de LINEDEVSTATE](linedevstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="b8a11-243">The line may be in use by another application or a *dwLineStates* parameter contains one or more bits that are not [LINEDEVSTATE\_ constants](linedevstate--constants.md).</span></span> <span data-ttu-id="b8a11-244">El valor de **LINEERR \_ INVALLINESTATE** también puede indicar que el dispositivo está desconectado o fuera de servicio.</span><span class="sxs-lookup"><span data-stu-id="b8a11-244">The **LINEERR\_INVALLINESTATE** value can also indicate that the device is disconnected or out of service.</span></span> <span data-ttu-id="b8a11-245">Estos Estados se indican mediante el establecimiento de los bits correspondientes a los valores *de \_ Inservice* *LINEDEVSTATUSFLAGS \_ conectados* y LINEDEVSTATUSFLAGS en 0 en el miembro **dwDevStatusFlags** de la estructura [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) devuelta por la función [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) .</span><span class="sxs-lookup"><span data-stu-id="b8a11-245">These states are indicated by setting the bits corresponding to the *LINEDEVSTATUSFLAGS\_CONNECTED* and *LINEDEVSTATUSFLAGS\_INSERVICE* values to 0 in the **dwDevStatusFlags** member of the [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) structure returned by the [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-246"><span id="LINEERR_INVALLOCATION"></span><span id="lineerr_invallocation"></span>**LINEERR \_ INVALLOCATION**</span><span class="sxs-lookup"><span data-stu-id="b8a11-246"><span id="LINEERR_INVALLOCATION"></span><span id="lineerr_invallocation"></span>**LINEERR\_INVALLOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-247">No se encontró el identificador de ubicación permanente especificado en *dwLocation* en ninguna entrada de la \[ sección locations del \] registro.</span><span class="sxs-lookup"><span data-stu-id="b8a11-247">The permanent location identifier specified in *dwLocation* could not be found in any entry in the \[Locations\] section in the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-248"><span id="LINEERR_INVALMEDIALIST"></span><span id="lineerr_invalmedialist"></span>**LINEERR \_ INVALMEDIALIST**</span><span class="sxs-lookup"><span data-stu-id="b8a11-248"><span id="LINEERR_INVALMEDIALIST"></span><span id="lineerr_invalmedialist"></span>**LINEERR\_INVALMEDIALIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-249">La lista de medios especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="b8a11-249">The specified media list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-250"><span id="LINEERR_INVALMEDIAMODE"></span><span id="lineerr_invalmediamode"></span>**LINEERR \_ INVALMEDIAMODE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-250"><span id="LINEERR_INVALMEDIAMODE"></span><span id="lineerr_invalmediamode"></span>**LINEERR\_INVALMEDIAMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-251">La lista de tipos de medios (modos) que se van a supervisar contiene información no válida, el parámetro de tipo de medio especificado no es válido o el proveedor de servicios no admite el tipo de medio especificado.</span><span class="sxs-lookup"><span data-stu-id="b8a11-251">The list of media types (modes) to be monitored contains invalid information, the specified media type parameter is invalid, or the service provider does not support the specified media type.</span></span> <span data-ttu-id="b8a11-252">Los tipos de medios admitidos en la línea se enumeran en el miembro **dwMediaModes** de la estructura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) .</span><span class="sxs-lookup"><span data-stu-id="b8a11-252">The media types supported on the line are listed in the **dwMediaModes** member in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-253"><span id="LINEERR_INVALMESSAGEID"></span><span id="lineerr_invalmessageid"></span>**LINEERR \_ INVALMESSAGEID**</span><span class="sxs-lookup"><span data-stu-id="b8a11-253"><span id="LINEERR_INVALMESSAGEID"></span><span id="lineerr_invalmessageid"></span>**LINEERR\_INVALMESSAGEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-254">El número proporcionado en *dwMessageID* está fuera del intervalo especificado por el miembro **dwNumCompletionMessages** en la estructura [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) .</span><span class="sxs-lookup"><span data-stu-id="b8a11-254">The number given in *dwMessageID* is outside the range specified by the **dwNumCompletionMessages** member in the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-255"><span id="LINEERR_INVALPARAM"></span><span id="lineerr_invalparam"></span>**LINEERR \_ INVALPARAM**</span><span class="sxs-lookup"><span data-stu-id="b8a11-255"><span id="LINEERR_INVALPARAM"></span><span id="lineerr_invalparam"></span>**LINEERR\_INVALPARAM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-256">Un parámetro o estructura a la que apunta un parámetro contiene información no válida, un código de país o región no es válido, un identificador de ventana no es válido o el parámetro de lista de reenvío especificado contiene información no válida.</span><span class="sxs-lookup"><span data-stu-id="b8a11-256">A parameter or structure that a parameter points to contains invalid information, a country or region code is invalid, a window handle is invalid, or the specified forward list parameter contains invalid information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-257"><span id="LINEERR_INVALPARKID"></span><span id="lineerr_invalparkid"></span>**LINEERR \_ INVALPARKID**</span><span class="sxs-lookup"><span data-stu-id="b8a11-257"><span id="LINEERR_INVALPARKID"></span><span id="lineerr_invalparkid"></span>**LINEERR\_INVALPARKID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-258">El identificador de Park no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-258">The park identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-259"><span id="LINEERR_INVALPARKMODE"></span><span id="lineerr_invalparkmode"></span>**LINEERR \_ INVALPARKMODE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-259"><span id="LINEERR_INVALPARKMODE"></span><span id="lineerr_invalparkmode"></span>**LINEERR\_INVALPARKMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-260">El modo de estacionamiento especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-260">The specified park mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-261"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR \_ INVALPASSWORD**</span><span class="sxs-lookup"><span data-stu-id="b8a11-261"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR\_INVALPASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-262">La contraseña especificada no es correcta y la acción solicitada no se ha llevado a cabo.</span><span class="sxs-lookup"><span data-stu-id="b8a11-262">The specified password is not correct and the requested action has not been carried out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-263"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR \_ INVALPASSWORD**</span><span class="sxs-lookup"><span data-stu-id="b8a11-263"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR\_INVALPASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-264">La aplicación usó una contraseña no válida.</span><span class="sxs-lookup"><span data-stu-id="b8a11-264">The application used an invalid password.</span></span> <span data-ttu-id="b8a11-265">Este valor solo se expone a las aplicaciones que negocian una versión de TAPI 2,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b8a11-265">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-266"><span id="LINEERR_INVALPOINTER"></span><span id="lineerr_invalpointer"></span>**LINEERR \_ INVALPOINTER**</span><span class="sxs-lookup"><span data-stu-id="b8a11-266"><span id="LINEERR_INVALPOINTER"></span><span id="lineerr_invalpointer"></span>**LINEERR\_INVALPOINTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-267">Uno o varios de los parámetros de puntero especificados (como *lpCallList*, *lpdwAPIVersion*, *lpExtensionID*, *lpdwExtVersion*, *lphIcon*, *lpLineDevCaps* y *lpToneList*) no son válidos o un puntero necesario a un parámetro de salida es **null**.</span><span class="sxs-lookup"><span data-stu-id="b8a11-267">One or more of the specified pointer parameters (such as *lpCallList*, *lpdwAPIVersion*, *lpExtensionID*, *lpdwExtVersion*, *lphIcon*, *lpLineDevCaps*, and *lpToneList*) are invalid, or a required pointer to an output parameter is **NULL**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-268"><span id="LINEERR_INVALPRIVSELECT"></span><span id="lineerr_invalprivselect"></span>**LINEERR \_ INVALPRIVSELECT**</span><span class="sxs-lookup"><span data-stu-id="b8a11-268"><span id="LINEERR_INVALPRIVSELECT"></span><span id="lineerr_invalprivselect"></span>**LINEERR\_INVALPRIVSELECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-269">Se estableció una marca no válida o una combinación de marcas para el parámetro *dwPrivileges* .</span><span class="sxs-lookup"><span data-stu-id="b8a11-269">An invalid flag or combination of flags was set for the *dwPrivileges* parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-270"><span id="LINEERR_INVALRATE"></span><span id="lineerr_invalrate"></span>**LINEERR \_ INVALRATE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-270"><span id="LINEERR_INVALRATE"></span><span id="lineerr_invalrate"></span>**LINEERR\_INVALRATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-271">La tasa especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="b8a11-271">The specified rate is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-272"><span id="LINEERR_INVALREQUESTMODE"></span><span id="lineerr_invalrequestmode"></span>**LINEERR \_ INVALREQUESTMODE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-272"><span id="LINEERR_INVALREQUESTMODE"></span><span id="lineerr_invalrequestmode"></span>**LINEERR\_INVALREQUESTMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-273">El indicador [**LINEREQUESTMODE**](linerequestmode--constants.md) no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-273">The [**LINEREQUESTMODE**](linerequestmode--constants.md) indicator is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-274"><span id="LINEERR_INVALTERMINALID"></span><span id="lineerr_invalterminalid"></span>**LINEERR \_ INVALTERMINALID**</span><span class="sxs-lookup"><span data-stu-id="b8a11-274"><span id="LINEERR_INVALTERMINALID"></span><span id="lineerr_invalterminalid"></span>**LINEERR\_INVALTERMINALID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-275">El identificador de terminal especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-275">The specified terminal identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-276"><span id="LINEERR_INVALTERMINALMODE"></span><span id="lineerr_invalterminalmode"></span>**LINEERR \_ INVALTERMINALMODE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-276"><span id="LINEERR_INVALTERMINALMODE"></span><span id="lineerr_invalterminalmode"></span>**LINEERR\_INVALTERMINALMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-277">El parámetro de modos de terminal especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-277">The specified terminal modes parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-278"><span id="LINEERR_INVALTIMEOUT"></span><span id="lineerr_invaltimeout"></span>**LINEERR \_ INVALTIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="b8a11-278"><span id="LINEERR_INVALTIMEOUT"></span><span id="lineerr_invaltimeout"></span>**LINEERR\_INVALTIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-279">No se admiten los tiempos de espera o un valor está fuera del intervalo válido especificado en [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps).</span><span class="sxs-lookup"><span data-stu-id="b8a11-279">Timeouts are not supported or a value falls outside the valid range specified in [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-280"><span id="LINEERR_INVALTONE"></span><span id="lineerr_invaltone"></span>**LINEERR \_ INVALTONE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-280"><span id="LINEERR_INVALTONE"></span><span id="lineerr_invaltone"></span>**LINEERR\_INVALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-281">El tono personalizado especificado no representa un tono válido o está formado por demasiadas frecuencias o la estructura de tono especificada no describe un tono válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-281">The specified custom tone does not represent a valid tone or is made up of too many frequencies or the specified tone structure does not describe a valid tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-282"><span id="LINEERR_INVALTONELIST"></span><span id="lineerr_invaltonelist"></span>**LINEERR \_ INVALTONELIST**</span><span class="sxs-lookup"><span data-stu-id="b8a11-282"><span id="LINEERR_INVALTONELIST"></span><span id="lineerr_invaltonelist"></span>**LINEERR\_INVALTONELIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-283">La lista de tonos especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="b8a11-283">The specified tone list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-284"><span id="LINEERR_INVALTONEMODE"></span><span id="lineerr_invaltonemode"></span>**LINEERR \_ INVALTONEMODE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-284"><span id="LINEERR_INVALTONEMODE"></span><span id="lineerr_invaltonemode"></span>**LINEERR\_INVALTONEMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-285">El parámetro de modo de tono especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-285">The specified tone mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-286"><span id="LINEERR_INVALTRANSFERMODE"></span><span id="lineerr_invaltransfermode"></span>**LINEERR \_ INVALTRANSFERMODE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-286"><span id="LINEERR_INVALTRANSFERMODE"></span><span id="lineerr_invaltransfermode"></span>**LINEERR\_INVALTRANSFERMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-287">El parámetro de modo de transferencia especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8a11-287">The specified transfer mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-288"><span id="LINEERR_LINEMAPPERFAILED"></span><span id="lineerr_linemapperfailed"></span>**LINEERR \_ LINEMAPPERFAILED**</span><span class="sxs-lookup"><span data-stu-id="b8a11-288"><span id="LINEERR_LINEMAPPERFAILED"></span><span id="lineerr_linemapperfailed"></span>**LINEERR\_LINEMAPPERFAILED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-289">LINEMAPPER era el valor pasado en el parámetro *dwDeviceID* , pero no se encontró ninguna línea que coincida con los requisitos especificados en el parámetro *lpCallParams* .</span><span class="sxs-lookup"><span data-stu-id="b8a11-289">LINEMAPPER was the value passed in the *dwDeviceID* parameter, but no lines were found that match the requirements specified in the *lpCallParams* parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-290"><span id="LINEERR_NOCONFERENCE"></span><span id="lineerr_noconference"></span>**LINEERR \_ NOconference**</span><span class="sxs-lookup"><span data-stu-id="b8a11-290"><span id="LINEERR_NOCONFERENCE"></span><span id="lineerr_noconference"></span>**LINEERR\_NOCONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-291">La llamada especificada no es un identificador de llamada de conferencia ni una llamada de participante.</span><span class="sxs-lookup"><span data-stu-id="b8a11-291">The specified call is not a conference call handle or a participant call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-292"><span id="LINEERR_NODEVICE"></span><span id="lineerr_nodevice"></span>**LINEERR \_ Device**</span><span class="sxs-lookup"><span data-stu-id="b8a11-292"><span id="LINEERR_NODEVICE"></span><span id="lineerr_nodevice"></span>**LINEERR\_NODEVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-293">El identificador de dispositivo especificado, que era válido previamente, ya no se acepta porque el dispositivo asociado se ha quitado del sistema desde la última vez que se inicializó TAPI.</span><span class="sxs-lookup"><span data-stu-id="b8a11-293">The specified device identifier, which was previously valid, is no longer accepted because the associated device has been removed from the system since TAPI was last initialized.</span></span> <span data-ttu-id="b8a11-294">Como alternativa, el dispositivo de línea no tiene ningún dispositivo asociado para la clase de dispositivo dada.</span><span class="sxs-lookup"><span data-stu-id="b8a11-294">Alternately, the line device has no associated device for the given device class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-295"><span id="LINEERR_NODRIVER"></span><span id="lineerr_nodriver"></span>**LINEERR \_ NOdriver**</span><span class="sxs-lookup"><span data-stu-id="b8a11-295"><span id="LINEERR_NODRIVER"></span><span id="lineerr_nodriver"></span>**LINEERR\_NODRIVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-296">No se pudo encontrar Tapiaddr.dll o el proveedor de servicios de teléfono para el dispositivo especificado encontró que uno de sus componentes falta o está dañado de forma que no se detectó en el momento de la inicialización.</span><span class="sxs-lookup"><span data-stu-id="b8a11-296">Either Tapiaddr.dll could not be located or the telephone service provider for the specified device found that one of its components is missing or corrupt in a way that was not detected at initialization time.</span></span> <span data-ttu-id="b8a11-297">Se recomienda que el usuario Use el panel de control de telefonía para corregir el problema.</span><span class="sxs-lookup"><span data-stu-id="b8a11-297">The user should be advised to use the Telephony Control Panel to correct the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-298"><span id="LINEERR_NOMEM"></span><span id="lineerr_nomem"></span>**LINEERR \_ NOMEM**</span><span class="sxs-lookup"><span data-stu-id="b8a11-298"><span id="LINEERR_NOMEM"></span><span id="lineerr_nomem"></span>**LINEERR\_NOMEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-299">Memoria insuficiente para realizar la operación o no se puede bloquear la memoria.</span><span class="sxs-lookup"><span data-stu-id="b8a11-299">Insufficient memory to perform the operation, or unable to lock memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-300"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR \_ NOMULTIPLEINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-300"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR\_NOMULTIPLEINSTANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-301">Un proveedor de servicios de telefonía que no admite varias instancias se muestra más de una vez en \[ la \] sección proveedores del registro.</span><span class="sxs-lookup"><span data-stu-id="b8a11-301">A telephony service provider that does not support multiple instances is listed more than once in the \[Providers\] section in the registry.</span></span> <span data-ttu-id="b8a11-302">La aplicación debe aconsejar al usuario que use el panel de control de telefonía para quitar el controlador duplicado.</span><span class="sxs-lookup"><span data-stu-id="b8a11-302">The application should advise the user to use the Telephony Control Panel to remove the duplicated driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-303"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR \_ NOMULTIPLEINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="b8a11-303"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR\_NOMULTIPLEINSTANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-304">No se permiten varias instancias de este proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="b8a11-304">Multiple instances of this service provider are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-305"><span id="LINEERR_NOREQUEST"></span><span id="lineerr_norequest"></span>**LINEERR \_ NOsolicitud**</span><span class="sxs-lookup"><span data-stu-id="b8a11-305"><span id="LINEERR_NOREQUEST"></span><span id="lineerr_norequest"></span>**LINEERR\_NOREQUEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-306">Actualmente no hay ninguna solicitud pendiente del modo indicado o la aplicación ya no es la aplicación de prioridad más alta para el modo de solicitud especificado.</span><span class="sxs-lookup"><span data-stu-id="b8a11-306">There currently is no request pending of the indicated mode, or the application is no longer the highest-priority application for the specified request mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-307"><span id="LINEERR_NOTOWNER"></span><span id="lineerr_notowner"></span>**LINEERR \_ NOurbanar**</span><span class="sxs-lookup"><span data-stu-id="b8a11-307"><span id="LINEERR_NOTOWNER"></span><span id="lineerr_notowner"></span>**LINEERR\_NOTOWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-308">La aplicación no tiene privilegios de propietario en la llamada especificada.</span><span class="sxs-lookup"><span data-stu-id="b8a11-308">The application does not have owner privilege to the specified call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-309"><span id="LINEERR_NOTREGISTERED"></span><span id="lineerr_notregistered"></span>**LINEERR \_ no registrado**</span><span class="sxs-lookup"><span data-stu-id="b8a11-309"><span id="LINEERR_NOTREGISTERED"></span><span id="lineerr_notregistered"></span>**LINEERR\_NOTREGISTERED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-310">La aplicación no está registrada como destinatario de la solicitud para el modo de solicitud indicado.</span><span class="sxs-lookup"><span data-stu-id="b8a11-310">The application is not registered as a request recipient for the indicated request mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-311"><span id="LINEERR_OPERATIONFAILED"></span><span id="lineerr_operationfailed"></span>**LINEERR \_ OPERATIONFAILED**</span><span class="sxs-lookup"><span data-stu-id="b8a11-311"><span id="LINEERR_OPERATIONFAILED"></span><span id="lineerr_operationfailed"></span>**LINEERR\_OPERATIONFAILED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-312">No se pudo realizar la operación debido a un motivo desconocido o no especificado.</span><span class="sxs-lookup"><span data-stu-id="b8a11-312">The operation failed for an unspecified or unknown reason.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-313"><span id="LINEERR_OPERATIONUNAVAIL"></span><span id="lineerr_operationunavail"></span>**LINEERR \_ OPERATIONUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="b8a11-313"><span id="LINEERR_OPERATIONUNAVAIL"></span><span id="lineerr_operationunavail"></span>**LINEERR\_OPERATIONUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-314">La operación no está disponible, como para el dispositivo especificado o la línea especificada.</span><span class="sxs-lookup"><span data-stu-id="b8a11-314">The operation is not available, such as for the given device or specified line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-315"><span id="LINEERR_RATEUNAVAIL"></span><span id="lineerr_rateunavail"></span>**LINEERR \_ RATEUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="b8a11-315"><span id="LINEERR_RATEUNAVAIL"></span><span id="lineerr_rateunavail"></span>**LINEERR\_RATEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-316">Actualmente, el proveedor de servicios no tiene suficiente ancho de banda disponible para la velocidad especificada.</span><span class="sxs-lookup"><span data-stu-id="b8a11-316">The service provider currently does not have enough bandwidth available for the specified rate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-317"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**reinicialización de LINEERR \_**</span><span class="sxs-lookup"><span data-stu-id="b8a11-317"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-318">Si se ha solicitado la reinicialización de TAPI, por ejemplo, como resultado de agregar o quitar un proveedor de servicios de telefonía, se rechazarán las solicitudes de [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize), [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)o [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) con este error hasta que la última aplicación cierre el uso de la API (con [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)), momento en el que la nueva configuración se vuelve efectiva y las aplicaciones vuelven a ser de lineInitialize. </span><span class="sxs-lookup"><span data-stu-id="b8a11-318">If TAPI reinitialization has been requested, for example as a result of adding or removing a telephony service provider, then [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize), [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), or [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) requests are rejected with this error until the last application shuts down its usage of the API (using [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)), at which time the new configuration becomes effective and applications are once again permitted to call **lineInitialize** or **lineInitializeEx**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-319"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**reinicialización de LINEERR \_**</span><span class="sxs-lookup"><span data-stu-id="b8a11-319"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-320">La aplicación intentó inicializar TAPI dos veces.</span><span class="sxs-lookup"><span data-stu-id="b8a11-320">The application attempted to initialize TAPI twice.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-321"><span id="LINEERR_REQUESTOVERRUN"></span><span id="lineerr_requestoverrun"></span>**LINEERR \_ REQUESTOVERRUN**</span><span class="sxs-lookup"><span data-stu-id="b8a11-321"><span id="LINEERR_REQUESTOVERRUN"></span><span id="lineerr_requestoverrun"></span>**LINEERR\_REQUESTOVERRUN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-322">Hay más solicitudes pendientes de las que el dispositivo puede controlar.</span><span class="sxs-lookup"><span data-stu-id="b8a11-322">More requests are pending than the device can handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-323"><span id="LINEERR_RESOURCEUNAVAIL"></span><span id="lineerr_resourceunavail"></span>**LINEERR \_ RESOURCEUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="b8a11-323"><span id="LINEERR_RESOURCEUNAVAIL"></span><span id="lineerr_resourceunavail"></span>**LINEERR\_RESOURCEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-324">Recursos insuficientes para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="b8a11-324">Insufficient resources to complete the operation.</span></span> <span data-ttu-id="b8a11-325">Por ejemplo, no se puede abrir una línea debido a un sobrecompromiso dinámico de los recursos.</span><span class="sxs-lookup"><span data-stu-id="b8a11-325">For example, a line cannot be opened due to a dynamic resource overcommitment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-326"><span id="LINEERR_STRUCTURETOOSMALL"></span><span id="lineerr_structuretoosmall"></span>**LINEERR \_ STRUCTURETOOSMALL**</span><span class="sxs-lookup"><span data-stu-id="b8a11-326"><span id="LINEERR_STRUCTURETOOSMALL"></span><span id="lineerr_structuretoosmall"></span>**LINEERR\_STRUCTURETOOSMALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-327">El miembro **dwTotalSize** de una estructura no especifica suficiente memoria para contener la parte fija de la estructura especificada.</span><span class="sxs-lookup"><span data-stu-id="b8a11-327">The **dwTotalSize** member of a structure does not specify enough memory to contain the fixed portion of the specified structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-328"><span id="LINEERR_TARGETNOTFOUND"></span><span id="lineerr_targetnotfound"></span>**LINEERR \_ TARGETNOTFOUND**</span><span class="sxs-lookup"><span data-stu-id="b8a11-328"><span id="LINEERR_TARGETNOTFOUND"></span><span id="lineerr_targetnotfound"></span>**LINEERR\_TARGETNOTFOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-329">No se encontró un destino para la entrega de llamada.</span><span class="sxs-lookup"><span data-stu-id="b8a11-329">A target for the call handoff was not found.</span></span> <span data-ttu-id="b8a11-330">Esto puede ocurrir si la aplicación con nombre no abre la misma línea con el \_ bit de propietario LINECALLPRIVILEGE en el parámetro *DwPrivileges* de [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).</span><span class="sxs-lookup"><span data-stu-id="b8a11-330">This can occur if the named application did not open the same line with the LINECALLPRIVILEGE\_OWNER bit in the *dwPrivileges* parameter of [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).</span></span> <span data-ttu-id="b8a11-331">O bien, en el caso de la entrega en modo multimedia, ninguna aplicación ha abierto la misma línea con el \_ bit de propietario LINECALLPRIVILEGE en el parámetro *DwPrivileges* de [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) y el tipo de medio especificado en el parámetro *dwMediaMode* se ha especificado en el parámetro *dwMediaModes* de [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).</span><span class="sxs-lookup"><span data-stu-id="b8a11-331">Or, in the case of media-mode handoff, no application has opened the same line with the LINECALLPRIVILEGE\_OWNER bit in the *dwPrivileges* parameter of [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) and with the media type specified in the *dwMediaMode* parameter having been specified in the *dwMediaModes* parameter of [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-332"><span id="LINEERR_TARGETSELF"></span><span id="lineerr_targetself"></span>**LINEERR \_ TARGETSELF**</span><span class="sxs-lookup"><span data-stu-id="b8a11-332"><span id="LINEERR_TARGETSELF"></span><span id="lineerr_targetself"></span>**LINEERR\_TARGETSELF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-333">La aplicación que invoca esta operación es el destino de la entrega indirecta.</span><span class="sxs-lookup"><span data-stu-id="b8a11-333">The application invoking this operation is the target of the indirect handoff.</span></span> <span data-ttu-id="b8a11-334">Es decir, TAPI ha determinado que la aplicación que realiza la llamada es también la aplicación de mayor prioridad para el tipo de medio especificado.</span><span class="sxs-lookup"><span data-stu-id="b8a11-334">That is, TAPI has determined that the calling application is also the highest priority application for the given media type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-335"><span id="LINEERR_UNINITIALIZED"></span><span id="lineerr_uninitialized"></span>**LINEERR no \_ inicializado**</span><span class="sxs-lookup"><span data-stu-id="b8a11-335"><span id="LINEERR_UNINITIALIZED"></span><span id="lineerr_uninitialized"></span>**LINEERR\_UNINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-336">La operación se invocó antes de cualquier aplicación llamada [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) o [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).</span><span class="sxs-lookup"><span data-stu-id="b8a11-336">The operation was invoked before any application called [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) or [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-337"><span id="LINEERR_USERCANCELLED"></span><span id="lineerr_usercancelled"></span>**LINEERR \_ USERCANCELLED**</span><span class="sxs-lookup"><span data-stu-id="b8a11-337"><span id="LINEERR_USERCANCELLED"></span><span id="lineerr_usercancelled"></span>**LINEERR\_USERCANCELLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-338">El usuario canceló la llamada.</span><span class="sxs-lookup"><span data-stu-id="b8a11-338">The user cancelled the call.</span></span> <span data-ttu-id="b8a11-339">Este valor solo se expone a las aplicaciones que negocian una versión de TAPI 2,2 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b8a11-339">This value is exposed only to applications that negotiate a TAPI version of 2.2 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8a11-340"><span id="LINEERR_USERUSERINFOTOOBIG"></span><span id="lineerr_useruserinfotoobig"></span>**LINEERR \_ USERUSERINFOTOOBIG**</span><span class="sxs-lookup"><span data-stu-id="b8a11-340"><span id="LINEERR_USERUSERINFOTOOBIG"></span><span id="lineerr_useruserinfotoobig"></span>**LINEERR\_USERUSERINFOTOOBIG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8a11-341">La cadena que contiene información de usuario de usuario supera el número máximo de bytes especificado en el miembro **dwUUIAcceptSize**, **dwUUIAnswerSize**, **dwUUIDropSize**, **dwUUIMakeCallSize** o **dwUUISendUserUserInfoSize** de [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps), o bien la cadena que contiene información de usuario de usuario es demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="b8a11-341">The string containing user-user information exceeds the maximum number of bytes specified in the **dwUUIAcceptSize**, **dwUUIAnswerSize**, **dwUUIDropSize**, **dwUUIMakeCallSize**, or **dwUUISendUserUserInfoSize** member of [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps), or the string containing user-user information is too long.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8a11-342">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8a11-342">Remarks</span></span>

<span data-ttu-id="b8a11-343">Los valores de 0xC0000000 a 0xFFFFFFFF están disponibles para las extensiones específicas del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b8a11-343">The values 0xC0000000 through 0xFFFFFFFF are available for device-specific extensions.</span></span> <span data-ttu-id="b8a11-344">Los valores 0x80000000 a través de 0xBFFFFFFF están reservados, mientras que 0x00000000 a 0x7FFFFFFF se usan como identificadores de solicitud.</span><span class="sxs-lookup"><span data-stu-id="b8a11-344">The values 0x80000000 through 0xBFFFFFFF are reserved, while 0x00000000 through 0x7FFFFFFF are used as request identifiers.</span></span>

<span data-ttu-id="b8a11-345">Si una aplicación obtiene un error devuelto que no controla específicamente (como un error definido por una extensión específica del dispositivo), debe tratar el error como LINEERR \_ OPERATIONFAILED (por un motivo no especificado).</span><span class="sxs-lookup"><span data-stu-id="b8a11-345">If an application gets an error return that it does not specifically handle (such as an error defined by a device-specific extension), it should treat the error as a LINEERR\_OPERATIONFAILED (for an unspecified reason).</span></span>

<span data-ttu-id="b8a11-346">Al invocar las \_ constantes LINEERR que son nuevas con TAPI 3,0, el archivo Tapierr.MC debe actualizarse con mensajes nuevos.</span><span class="sxs-lookup"><span data-stu-id="b8a11-346">When invoking the LINEERR\_constants which are new with TAPI 3.0, the Tapierr.mc file must be updated with new messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8a11-347">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8a11-347">Requirements</span></span>



| <span data-ttu-id="b8a11-348">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8a11-348">Requirement</span></span> | <span data-ttu-id="b8a11-349">Value</span><span class="sxs-lookup"><span data-stu-id="b8a11-349">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b8a11-350">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="b8a11-350">TAPI version</span></span><br/> | <span data-ttu-id="b8a11-351">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="b8a11-351">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b8a11-352">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8a11-352">Header</span></span><br/>       | <dl> <span data-ttu-id="b8a11-353"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8a11-353"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8a11-354">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8a11-354">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8a11-355">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="b8a11-355">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="b8a11-356">**LINEDEVCAPS**</span><span class="sxs-lookup"><span data-stu-id="b8a11-356">**LINEDEVCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[<span data-ttu-id="b8a11-357">**LINEDEVSTATUS**</span><span class="sxs-lookup"><span data-stu-id="b8a11-357">**LINEDEVSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[<span data-ttu-id="b8a11-358">**lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="b8a11-358">**lineGetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[<span data-ttu-id="b8a11-359">**lineInitialize**</span><span class="sxs-lookup"><span data-stu-id="b8a11-359">**lineInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[<span data-ttu-id="b8a11-360">**lineInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="b8a11-360">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> <dt>

[<span data-ttu-id="b8a11-361">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="b8a11-361">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="b8a11-362">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="b8a11-362">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




