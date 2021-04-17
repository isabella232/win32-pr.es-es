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
# <a name="tapimediatype_-constants"></a>Constantes de TAPIMEDIATYPE \_

Se definen los siguientes tipos de medios:



| Constante o valor                                                                                                                                                                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TAPIMEDIATYPE_AUDIO"></span><span id="tapimediatype_audio"></span><dl> <dt>**TAPIMEDIATYPE \_ AUDIO**</dt> <dt>0x8</dt> </dl>                    | Secuencia de medios de audio que entra o sale del equipo. Normalmente, un flujo de medios de entrada se reproducirá en los altavoces o se enviará a un dispositivo de auricular y, por lo tanto, se capturará un flujo de salida a través de un micrófono o dispositivo de auricular.<br/>                                                                                                                                                                                                                                      |
| <span id="TAPIMEDIATYPE_VIDEO"></span><span id="tapimediatype_video"></span><dl> <dt>**TAPIMEDIATYPE \_ VÍDEO**</dt> <dt>0x8000</dt> </dl>                 | Un flujo de medios de vídeo que entra o sale del equipo. Normalmente, un flujo de medios de entrada se representaría en una ventana de vídeo y, por lo general, una secuencia de medios de salida se capturaría con una cámara de vídeo.<br/>                                                                                                                                                                                                                                                                         |
| <span id="TAPIMEDIATYPE_DATAMODEM"></span><span id="tapimediatype_datamodem"></span><dl> <dt>**TAPIMEDIATYPE \_ Telemodem**</dt> <dt>0x10</dt> </dl>       | Secuencia de medios de datos que está asociada a un módem de datos.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="TAPIMEDIATYPE_G3FAX"></span><span id="tapimediatype_g3fax"></span><dl> <dt>**TAPIMEDIATYPE \_ G3FAX**</dt> <dt>0x20</dt> </dl>                   | Secuencia de medios de datos que está asociada a un fax de protocolo G3.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="TAPIMEDIATYPE_MULTITRACK"></span><span id="tapimediatype_multitrack"></span><dl> <dt>**TAPIMEDIATYPE \_**</dt> <dt>0x10000</dt> multipista </dl> | Un flujo está en un terminal multipista.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="MEDIATYPE_RTP_Single_Stream"></span><span id="mediatype_rtp_single_stream"></span><span id="MEDIATYPE_RTP_SINGLE_STREAM"></span><dl> <dt>**\_ \_ Flujo único de la RTP de MEDIATYPE \_**</dt> </dl>     | Este GUID se usa entre un terminal proporcionado por la aplicación y el flujo de MSP. Si el PIN del terminal es compatible con este tipo de medio, el flujo intercambiará los datos RTP sin procesar con el terminal. Este modo solo es compatible con las secuencias de vídeo en el MSP de H323 y IPConf MSP para Windows 2000 SP1 o posterior.<br/> **Encabezado:** Se declara en ipmsp. h. El encabezado ipmsp. h no está disponible en en Windows Vista, Windows Server 2008 ni en las versiones posteriores del sistema operativo. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                              |
| Encabezado<br/>       | <dl> <dt>Tapi3. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITQOSEvent:: get \_ mediatype**](/windows/desktop/api/tapi3if/nf-tapi3if-itqosevent-get_mediatype)
</dt> <dt>

[**ITAMMediaFormat:: get \_ MediaFormat**](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-get_mediaformat)
</dt> <dt>

[**ITAMMediaFormat::p UT \_ MediaFormat**](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-put_mediaformat)
</dt> <dt>

[**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)
</dt> <dt>

[**ITMediaSupport:: get \_ MediaTypes**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediasupport-get_mediatypes)
</dt> <dt>

[**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> </dl>

 

