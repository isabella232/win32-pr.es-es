---
description: A continuación se definen las constantes de tipo de medio.
ms.assetid: 3e418c9a-a008-4b94-b5d2-7c2eccb3bf87
title: Constantes de TAPIMEDIATYPE_ (Tapi3. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71a7d7ffb411d84e99863bb89274e43200b319d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690802"
---
# <a name="tapimediatype_-constants"></a><span data-ttu-id="7b01e-103">Constantes de TAPIMEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="7b01e-103">TAPIMEDIATYPE\_ Constants</span></span>

<span data-ttu-id="7b01e-104">Se definen los siguientes tipos de medios:</span><span class="sxs-lookup"><span data-stu-id="7b01e-104">The following media types are defined:</span></span>



| <span data-ttu-id="7b01e-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="7b01e-105">Constant/value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="7b01e-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b01e-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TAPIMEDIATYPE_AUDIO"></span><span id="tapimediatype_audio"></span><dl> <span data-ttu-id="7b01e-107"><dt>**TAPIMEDIATYPE \_ AUDIO**</dt> <dt>0x8</dt></span><span class="sxs-lookup"><span data-stu-id="7b01e-107"><dt>**TAPIMEDIATYPE\_AUDIO**</dt> <dt>0x8</dt></span></span> </dl>                    | <span data-ttu-id="7b01e-108">Secuencia de medios de audio que entra o sale del equipo.</span><span class="sxs-lookup"><span data-stu-id="7b01e-108">An audio media stream that is entering or leaving the computer.</span></span> <span data-ttu-id="7b01e-109">Normalmente, un flujo de medios de entrada se reproducirá en los altavoces o se enviará a un dispositivo de auricular y, por lo tanto, se capturará un flujo de salida a través de un micrófono o dispositivo de auricular.</span><span class="sxs-lookup"><span data-stu-id="7b01e-109">An entering media stream would typically be played on speakers, or sent to a handset device and a leaving stream would typically be captured through a microphone or handset device.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="TAPIMEDIATYPE_VIDEO"></span><span id="tapimediatype_video"></span><dl> <span data-ttu-id="7b01e-110"><dt>**TAPIMEDIATYPE \_ VÍDEO**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="7b01e-110"><dt>**TAPIMEDIATYPE\_VIDEO**</dt> <dt>0x8000</dt></span></span> </dl>                 | <span data-ttu-id="7b01e-111">Un flujo de medios de vídeo que entra o sale del equipo.</span><span class="sxs-lookup"><span data-stu-id="7b01e-111">A video media stream that is entering or leaving the computer.</span></span> <span data-ttu-id="7b01e-112">Normalmente, un flujo de medios de entrada se representaría en una ventana de vídeo y, por lo general, una secuencia de medios de salida se capturaría con una cámara de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7b01e-112">An entering media stream would typically be rendered in a video window and a leaving media stream would typically be captured with a video camera.</span></span><br/>                                                                                                                                                                                                                                                                         |
| <span id="TAPIMEDIATYPE_DATAMODEM"></span><span id="tapimediatype_datamodem"></span><dl> <span data-ttu-id="7b01e-113"><dt>**TAPIMEDIATYPE \_ Telemodem**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="7b01e-113"><dt>**TAPIMEDIATYPE\_DATAMODEM**</dt> <dt>0x10</dt></span></span> </dl>       | <span data-ttu-id="7b01e-114">Secuencia de medios de datos que está asociada a un módem de datos.</span><span class="sxs-lookup"><span data-stu-id="7b01e-114">A data media stream that is associated with a data modem.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="TAPIMEDIATYPE_G3FAX"></span><span id="tapimediatype_g3fax"></span><dl> <span data-ttu-id="7b01e-115"><dt>**TAPIMEDIATYPE \_ G3FAX**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="7b01e-115"><dt>**TAPIMEDIATYPE\_G3FAX**</dt> <dt>0x20</dt></span></span> </dl>                   | <span data-ttu-id="7b01e-116">Secuencia de medios de datos que está asociada a un fax de protocolo G3.</span><span class="sxs-lookup"><span data-stu-id="7b01e-116">A data media stream that is associated with a G3 protocol fax.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="TAPIMEDIATYPE_MULTITRACK"></span><span id="tapimediatype_multitrack"></span><dl> <span data-ttu-id="7b01e-117"><dt>**TAPIMEDIATYPE \_**</dt> <dt>0x10000</dt> multipista</span><span class="sxs-lookup"><span data-stu-id="7b01e-117"><dt>**TAPIMEDIATYPE\_MULTITRACK**</dt> <dt>0x10000</dt></span></span> </dl> | <span data-ttu-id="7b01e-118">Un flujo está en un terminal multipista.</span><span class="sxs-lookup"><span data-stu-id="7b01e-118">A stream is on a multitrack terminal.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="MEDIATYPE_RTP_Single_Stream"></span><span id="mediatype_rtp_single_stream"></span><span id="MEDIATYPE_RTP_SINGLE_STREAM"></span><dl> <span data-ttu-id="7b01e-119"><dt>**\_ \_ Flujo único de la RTP de MEDIATYPE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7b01e-119"><dt>**MEDIATYPE\_RTP\_Single\_Stream**</dt></span></span> </dl>     | <span data-ttu-id="7b01e-120">Este GUID se usa entre un terminal proporcionado por la aplicación y el flujo de MSP.</span><span class="sxs-lookup"><span data-stu-id="7b01e-120">This GUID is used between an application supplied terminal and the MSP's stream.</span></span> <span data-ttu-id="7b01e-121">Si el PIN del terminal es compatible con este tipo de medio, el flujo intercambiará los datos RTP sin procesar con el terminal.</span><span class="sxs-lookup"><span data-stu-id="7b01e-121">If the pin of the terminal supports this media type, the stream will exchange raw RTP data with the terminal.</span></span> <span data-ttu-id="7b01e-122">Este modo solo es compatible con las secuencias de vídeo en el MSP de H323 y IPConf MSP para Windows 2000 SP1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="7b01e-122">This mode is supported only by the video streams on the H323 MSP and IPConf MSP for Windows 2000 SP1 or above.</span></span><br/> <span data-ttu-id="7b01e-123">**Encabezado:** Se declara en ipmsp. h.</span><span class="sxs-lookup"><span data-stu-id="7b01e-123">**Header:** Declared in ipmsp.h.</span></span> <span data-ttu-id="7b01e-124">El encabezado ipmsp. h no está disponible en en Windows Vista, Windows Server 2008 ni en las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7b01e-124">The header ipmsp.h is not available in in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="7b01e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b01e-125">Requirements</span></span>



| <span data-ttu-id="7b01e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b01e-126">Requirement</span></span> | <span data-ttu-id="7b01e-127">Value</span><span class="sxs-lookup"><span data-stu-id="7b01e-127">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7b01e-128">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="7b01e-128">TAPI version</span></span><br/> | <span data-ttu-id="7b01e-129">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="7b01e-129">Requires TAPI 3.0 or later</span></span><br/>                                              |
| <span data-ttu-id="7b01e-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7b01e-130">Header</span></span><br/>       | <dl> <span data-ttu-id="7b01e-131"><dt>Tapi3. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b01e-131"><dt>Tapi3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b01e-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b01e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b01e-133">**ITQOSEvent:: get \_ mediatype**</span><span class="sxs-lookup"><span data-stu-id="7b01e-133">**ITQOSEvent::get\_MediaType**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itqosevent-get_mediatype)
</dt> <dt>

[<span data-ttu-id="7b01e-134">**ITAMMediaFormat:: get \_ MediaFormat**</span><span class="sxs-lookup"><span data-stu-id="7b01e-134">**ITAMMediaFormat::get\_MediaFormat**</span></span>](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-get_mediaformat)
</dt> <dt>

[<span data-ttu-id="7b01e-135">**ITAMMediaFormat::p UT \_ MediaFormat**</span><span class="sxs-lookup"><span data-stu-id="7b01e-135">**ITAMMediaFormat::put\_MediaFormat**</span></span>](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-put_mediaformat)
</dt> <dt>

[<span data-ttu-id="7b01e-136">**ITCallInfo:: get \_ CallInfoLong**</span><span class="sxs-lookup"><span data-stu-id="7b01e-136">**ITCallInfo::get\_CallInfoLong**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)
</dt> <dt>

[<span data-ttu-id="7b01e-137">**ITMediaSupport:: get \_ MediaTypes**</span><span class="sxs-lookup"><span data-stu-id="7b01e-137">**ITMediaSupport::get\_MediaTypes**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itmediasupport-get_mediatypes)
</dt> <dt>

[<span data-ttu-id="7b01e-138">**ITTerminalSupport::CreateTerminal**</span><span class="sxs-lookup"><span data-stu-id="7b01e-138">**ITTerminalSupport::CreateTerminal**</span></span>](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> </dl>

 

