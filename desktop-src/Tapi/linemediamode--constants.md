---
description: Las \_ constantes LINEMEDIAMODE describen los tipos de medios (o modos) de una sesión de comunicaciones o una llamada a.
ms.assetid: cbb758be-3ecd-4ac4-b1b5-57136a1aad8e
title: Constantes de LINEMEDIAMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550a31da0d6de556e28ded14ce0803030be075ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680770"
---
# <a name="linemediamode_-constants"></a><span data-ttu-id="f5e14-103">Constantes de LINEMEDIAMODE \_</span><span class="sxs-lookup"><span data-stu-id="f5e14-103">LINEMEDIAMODE\_ Constants</span></span>

<span data-ttu-id="f5e14-104">Las **constantes \_ LINEMEDIAMODE** describen los tipos de medios (o modos) de una sesión de comunicaciones o una llamada a.</span><span class="sxs-lookup"><span data-stu-id="f5e14-104">The **LINEMEDIAMODE\_** constants describe media types (or modes)of a communications session or call.</span></span>

<dl> <dt>

<span data-ttu-id="f5e14-105"><span id="LINEMEDIAMODE_AUTOMATEDVOICE"></span><span id="linemediamode_automatedvoice"></span>**LINEMEDIAMODE \_ AUTOMATEDVOICE**</span><span class="sxs-lookup"><span data-stu-id="f5e14-105"><span id="LINEMEDIAMODE_AUTOMATEDVOICE"></span><span id="linemediamode_automatedvoice"></span>**LINEMEDIAMODE\_AUTOMATEDVOICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f5e14-106">Se ha detectado energía de voz en la llamada, y la voz se controla localmente mediante una aplicación automatizada como, por ejemplo, con una aplicación de equipo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="f5e14-106">Voice energy was detected on the call, and the voice is locally handled by an automated application such as with an answering machine application.</span></span> <span data-ttu-id="f5e14-107">Cuando un proveedor de servicios no puede distinguir entre voz interactiva y automatizada en una llamada entrante, notificará la llamada como voz interactiva.</span><span class="sxs-lookup"><span data-stu-id="f5e14-107">When a service provider cannot distinguish between interactive and automated voice on an incoming call, it will report the call as interactive voice.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f5e14-108"><span id="LINEMEDIAMODE_DATAMODEM"></span><span id="linemediamode_datamodem"></span>**LINEMEDIAMODE de \_ módem**</span><span class="sxs-lookup"><span data-stu-id="f5e14-108"><span id="LINEMEDIAMODE_DATAMODEM"></span><span id="linemediamode_datamodem"></span>**LINEMEDIAMODE\_DATAMODEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f5e14-109">Una sesión de módem de datos en la llamada.</span><span class="sxs-lookup"><span data-stu-id="f5e14-109">A data modem session on the call.</span></span> <span data-ttu-id="f5e14-110">Los protocolos de módem actuales requieren que la estación llamada inicie el protocolo de enlace.</span><span class="sxs-lookup"><span data-stu-id="f5e14-110">Current modem protocols require the called station to initiate the handshake.</span></span> <span data-ttu-id="f5e14-111">En el caso de una llamada de módem de datos de entrada, la aplicación normalmente no puede hacer ninguna detección positiva.</span><span class="sxs-lookup"><span data-stu-id="f5e14-111">For an incoming data modem call, the application can typically make no positive detection.</span></span> <span data-ttu-id="f5e14-112">La forma en que el proveedor de servicios toma esta decisión es su elección.</span><span class="sxs-lookup"><span data-stu-id="f5e14-112">How the service provider makes this determination is its choice.</span></span> <span data-ttu-id="f5e14-113">Por ejemplo, se puede usar un período de silencio justo después de responder a una llamada entrante como heurística para decidir que esto podría ser una llamada de módem de datos.</span><span class="sxs-lookup"><span data-stu-id="f5e14-113">For example, a period of silence just after answering an incoming call can be used as a heuristic to decide that this might be a data modem call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f5e14-114"><span id="LINEMEDIAMODE_ADSI"></span><span id="linemediamode_adsi"></span>**LINEMEDIAMODE \_ ADSI**</span><span class="sxs-lookup"><span data-stu-id="f5e14-114"><span id="LINEMEDIAMODE_ADSI"></span><span id="linemediamode_adsi"></span>**LINEMEDIAMODE\_ADSI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f5e14-115">Una sesión ADSI (interfaz de servicios de pantalla analógica) en la llamada.</span><span class="sxs-lookup"><span data-stu-id="f5e14-115">An ADSI (Analog Display Services Interface) session on the call.</span></span> <span data-ttu-id="f5e14-116">ADSI mejora las llamadas de voz con información alfanumérica descargada en el teléfono y el uso de botones flexibles en el teléfono.</span><span class="sxs-lookup"><span data-stu-id="f5e14-116">ADSI enhances voice calls with alphanumeric information downloaded to the phone and the use of soft buttons on the phone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f5e14-117"><span id="LINEMEDIAMODE_DIGITALDATA"></span><span id="linemediamode_digitaldata"></span>**LINEMEDIAMODE \_ DIGITALDATA**</span><span class="sxs-lookup"><span data-stu-id="f5e14-117"><span id="LINEMEDIAMODE_DIGITALDATA"></span><span id="linemediamode_digitaldata"></span>**LINEMEDIAMODE\_DIGITALDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f5e14-118">Flujo de datos digitales del formato no especificado.</span><span class="sxs-lookup"><span data-stu-id="f5e14-118">A digital data stream of unspecified format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f5e14-119"><span id="LINEMEDIAMODE_G3FAX"></span><span id="linemediamode_g3fax"></span>**LINEMEDIAMODE \_ G3FAX**</span><span class="sxs-lookup"><span data-stu-id="f5e14-119"><span id="LINEMEDIAMODE_G3FAX"></span><span id="linemediamode_g3fax"></span>**LINEMEDIAMODE\_G3FAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f5e14-120">Se está enviando o recibiendo un fax de grupo 3 a través de la llamada.</span><span class="sxs-lookup"><span data-stu-id="f5e14-120">A group 3 fax is being sent or received over the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f5e14-121"><span id="LINEMEDIAMODE_G4FAX"></span><span id="linemediamode_g4fax"></span>**LINEMEDIAMODE \_ G4FAX**</span><span class="sxs-lookup"><span data-stu-id="f5e14-121"><span id="LINEMEDIAMODE_G4FAX"></span><span id="linemediamode_g4fax"></span>**LINEMEDIAMODE\_G4FAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f5e14-122">Se está enviando o recibiendo un fax de grupo 4 a través de la llamada.</span><span class="sxs-lookup"><span data-stu-id="f5e14-122">A group 4 fax is being sent or received over the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f5e14-123"><span id="LINEMEDIAMODE_INTERACTIVEVOICE"></span><span id="linemediamode_interactivevoice"></span>**LINEMEDIAMODE \_ INTERACTIVEVOICE**</span><span class="sxs-lookup"><span data-stu-id="f5e14-123"><span id="LINEMEDIAMODE_INTERACTIVEVOICE"></span><span id="linemediamode_interactivevoice"></span>**LINEMEDIAMODE\_INTERACTIVEVOICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f5e14-124">Se ha detectado energía de voz en la llamada y la llamada se trata como una llamada de voz interactiva con seres humanos en ambos extremos.</span><span class="sxs-lookup"><span data-stu-id="f5e14-124">Voice energy was detected on the call, and the call is handled as an interactive voice call with humans on both ends.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f5e14-125"><span id="LINEMEDIAMODE_MIXED"></span><span id="linemediamode_mixed"></span>**LINEMEDIAMODE \_ Mixed**</span><span class="sxs-lookup"><span data-stu-id="f5e14-125"><span id="LINEMEDIAMODE_MIXED"></span><span id="linemediamode_mixed"></span>**LINEMEDIAMODE\_MIXED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f5e14-126">Una sesión mixta en la llamada.</span><span class="sxs-lookup"><span data-stu-id="f5e14-126">A mixed session on the call.</span></span> <span data-ttu-id="f5e14-127">Mixed es uno de los servicios telemáticos de ISDN.</span><span class="sxs-lookup"><span data-stu-id="f5e14-127">Mixed is one of the ISDN telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f5e14-128"><span id="LINEMEDIAMODE_TDD"></span><span id="linemediamode_tdd"></span>**LINEMEDIAMODE \_ TDD**</span><span class="sxs-lookup"><span data-stu-id="f5e14-128"><span id="LINEMEDIAMODE_TDD"></span><span id="linemediamode_tdd"></span>**LINEMEDIAMODE\_TDD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f5e14-129">Una sesión de TDD (dispositivos de telefonía para sordos) en la llamada.</span><span class="sxs-lookup"><span data-stu-id="f5e14-129">A TDD (Telephony Devices for the Deaf) session on the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f5e14-130"><span id="LINEMEDIAMODE_TELETEX"></span><span id="linemediamode_teletex"></span>**LINEMEDIAMODE \_ teletexto**</span><span class="sxs-lookup"><span data-stu-id="f5e14-130"><span id="LINEMEDIAMODE_TELETEX"></span><span id="linemediamode_teletex"></span>**LINEMEDIAMODE\_TELETEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f5e14-131">Una sesión de teletexto en la llamada.</span><span class="sxs-lookup"><span data-stu-id="f5e14-131">A teletex session on the call.</span></span> <span data-ttu-id="f5e14-132">Teletexto es uno de los servicios telemáticos.</span><span class="sxs-lookup"><span data-stu-id="f5e14-132">Teletex is one of the telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f5e14-133"><span id="LINEMEDIAMODE_TELEX"></span><span id="linemediamode_telex"></span>**\_télex LINEMEDIAMODE**</span><span class="sxs-lookup"><span data-stu-id="f5e14-133"><span id="LINEMEDIAMODE_TELEX"></span><span id="linemediamode_telex"></span>**LINEMEDIAMODE\_TELEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f5e14-134">Una sesión de télex en la llamada.</span><span class="sxs-lookup"><span data-stu-id="f5e14-134">A telex session on the call.</span></span> <span data-ttu-id="f5e14-135">Télex es uno de los servicios telemáticos.</span><span class="sxs-lookup"><span data-stu-id="f5e14-135">Telex is one of the telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f5e14-136"><span id="LINEMEDIAMODE_VIDEO"></span><span id="linemediamode_video"></span>**vídeo de LINEMEDIAMODE \_**</span><span class="sxs-lookup"><span data-stu-id="f5e14-136"><span id="LINEMEDIAMODE_VIDEO"></span><span id="linemediamode_video"></span>**LINEMEDIAMODE\_VIDEO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f5e14-137">El tipo de medio de la llamada es vídeo.</span><span class="sxs-lookup"><span data-stu-id="f5e14-137">The media type of the call is video.</span></span> <span data-ttu-id="f5e14-138">(Versiones de TAPI 2,1 y posteriores)</span><span class="sxs-lookup"><span data-stu-id="f5e14-138">(TAPI versions 2.1 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f5e14-139"><span id="LINEMEDIAMODE_VIDEOTEX"></span><span id="linemediamode_videotex"></span>**LINEMEDIAMODE \_ VIDEOTEX**</span><span class="sxs-lookup"><span data-stu-id="f5e14-139"><span id="LINEMEDIAMODE_VIDEOTEX"></span><span id="linemediamode_videotex"></span>**LINEMEDIAMODE\_VIDEOTEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f5e14-140">Una sesión de Videotex en la llamada.</span><span class="sxs-lookup"><span data-stu-id="f5e14-140">A videotex session on the call.</span></span> <span data-ttu-id="f5e14-141">Videotex es uno de los servicios telemáticos.</span><span class="sxs-lookup"><span data-stu-id="f5e14-141">Videotex is one the telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f5e14-142"><span id="LINEMEDIAMODE_VOICEVIEW"></span><span id="linemediamode_voiceview"></span>**VOICEVIEW de LINEMEDIAMODE \_**</span><span class="sxs-lookup"><span data-stu-id="f5e14-142"><span id="LINEMEDIAMODE_VOICEVIEW"></span><span id="linemediamode_voiceview"></span>**LINEMEDIAMODE\_VOICEVIEW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f5e14-143">El tipo de medio de la llamada es VoiceView.</span><span class="sxs-lookup"><span data-stu-id="f5e14-143">The media type of the call is VoiceView.</span></span> <span data-ttu-id="f5e14-144">(Versiones de TAPI 1,4 y posteriores)</span><span class="sxs-lookup"><span data-stu-id="f5e14-144">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f5e14-145"><span id="LINEMEDIAMODE_UNKNOWN"></span><span id="linemediamode_unknown"></span>**LINEMEDIAMODE \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="f5e14-145"><span id="LINEMEDIAMODE_UNKNOWN"></span><span id="linemediamode_unknown"></span>**LINEMEDIAMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f5e14-146">Existe un flujo multimedia pero su modo no se conoce actualmente y se puede conocer más adelante.</span><span class="sxs-lookup"><span data-stu-id="f5e14-146">A media stream exists but its mode is not currently known and may become known later.</span></span> <span data-ttu-id="f5e14-147">Esto corresponde a una llamada con un tipo de medio sin clasificar.</span><span class="sxs-lookup"><span data-stu-id="f5e14-147">This would correspond to a call with an unclassified media type.</span></span> <span data-ttu-id="f5e14-148">En los entornos de telefonía analógica típicos, el tipo de medio de una llamada entrante puede ser desconocido hasta que se haya respondido a la llamada y se haya filtrado el flujo multimedia para realizar una determinación.</span><span class="sxs-lookup"><span data-stu-id="f5e14-148">In typical analog telephony environments, an incoming call's media type may be unknown until after the call has been answered and the media stream has been filtered to make a determination.</span></span>

<span data-ttu-id="f5e14-149">Si se establece la marca de modo de medio desconocido, también se pueden establecer otras marcas multimedia.</span><span class="sxs-lookup"><span data-stu-id="f5e14-149">If the unknown media-mode flag is set, other media flags can also be set.</span></span> <span data-ttu-id="f5e14-150">Se usa para indicar que el medio es desconocido pero que es probable que sea uno de los otros tipos de medios seleccionados.</span><span class="sxs-lookup"><span data-stu-id="f5e14-150">This is used to signify that the media is unknown but that it is likely to be one of the other selected media types.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5e14-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5e14-151">Remarks</span></span>

<span data-ttu-id="f5e14-152">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="f5e14-152">All 32 bits are reserved.</span></span>

<span data-ttu-id="f5e14-153">Tenga en cuenta que el modo de portador y el tipo de medio son nociones diferentes.</span><span class="sxs-lookup"><span data-stu-id="f5e14-153">Note that bearer mode and media type are different notions.</span></span> <span data-ttu-id="f5e14-154">El modo de portador de una llamada es una indicación de la calidad de la conexión telefónica tal como la proporciona principalmente la red.</span><span class="sxs-lookup"><span data-stu-id="f5e14-154">The bearer mode of a call is an indication of the quality of the telephone connection as provided primarily by the network.</span></span> <span data-ttu-id="f5e14-155">El tipo de medio de una llamada es una indicación del tipo de flujo de información que se intercambia en esa llamada.</span><span class="sxs-lookup"><span data-stu-id="f5e14-155">The media type of a call is an indication of the type of information stream that is exchanged over that call.</span></span> <span data-ttu-id="f5e14-156">El módem de fax o de datos del grupo 3 son tipos de medios que usan una llamada con un modo de portador de voz 3,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="f5e14-156">Group 3 fax or data modem are media types that use a call with a 3.1 kHz voice bearer mode.</span></span>

<span data-ttu-id="f5e14-157">Por compatibilidad con versiones anteriores, es responsabilidad del proveedor de servicios examinar la versión de la API negociada en la línea y no usar este \_ valor de LINEMEDIAMODE si no se admite en la versión negociada.</span><span class="sxs-lookup"><span data-stu-id="f5e14-157">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use this LINEMEDIAMODE\_ value if not supported on the negotiated version.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5e14-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5e14-158">Requirements</span></span>



| <span data-ttu-id="f5e14-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5e14-159">Requirement</span></span> | <span data-ttu-id="f5e14-160">Value</span><span class="sxs-lookup"><span data-stu-id="f5e14-160">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f5e14-161">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="f5e14-161">TAPI version</span></span><br/> | <span data-ttu-id="f5e14-162">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="f5e14-162">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f5e14-163">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5e14-163">Header</span></span><br/>       | <dl> <span data-ttu-id="f5e14-164"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5e14-164"><dt>Tapi.h</dt></span></span> </dl> |



 

 




