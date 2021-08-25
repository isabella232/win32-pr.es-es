---
description: Las constantes de tipo de medio se definen a continuación.
ms.assetid: 3e418c9a-a008-4b94-b5d2-7c2eccb3bf87
title: TAPIMEDIATYPE_ constantes (Tapi3.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a702f5a061629f3fd8daa5ad742c65af12c43bbd92eec6896b143e4bd6a403c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866885"
---
# <a name="tapimediatype_-constants"></a>Constantes TAPIMEDIATYPE \_

Se definen los siguientes tipos de medios:



| Constante o valor                                                                                                                                                                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TAPIMEDIATYPE_AUDIO"></span><span id="tapimediatype_audio"></span><dl> <dt>**TAPIMEDIATYPE \_ Audio**</dt> <dt>0x8</dt> </dl>                    | Secuencia multimedia de audio que entra o sale del equipo. Normalmente, una secuencia multimedia de entrada se reproduciría en altavoces o se enviaría a un dispositivo de terminal y, por lo general, una secuencia de salida se capturaría a través de un micrófono o un dispositivo de terminal.<br/>                                                                                                                                                                                                                                      |
| <span id="TAPIMEDIATYPE_VIDEO"></span><span id="tapimediatype_video"></span><dl> <dt>**TAPIMEDIATYPE \_ Vídeo**</dt> <dt>0x8000</dt> </dl>                 | Secuencia multimedia de vídeo que entra o sale del equipo. Normalmente, una secuencia multimedia de entrada se representaría en una ventana de vídeo y una secuencia multimedia de salida normalmente se capturaría con una cámara de vídeo.<br/>                                                                                                                                                                                                                                                                         |
| <span id="TAPIMEDIATYPE_DATAMODEM"></span><span id="tapimediatype_datamodem"></span><dl> <dt>**TAPIMEDIATYPE \_ DataMODEM**</dt> <dt>0x10</dt> </dl>       | Flujo de medios de datos asociado a un módem de datos.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="TAPIMEDIATYPE_G3FAX"></span><span id="tapimediatype_g3fax"></span><dl> <dt>**TAPIMEDIATYPE \_ G3FAX**</dt> <dt>0x20</dt> </dl>                   | Flujo de medios de datos asociado a un fax de protocolo G3.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="TAPIMEDIATYPE_MULTITRACK"></span><span id="tapimediatype_multitrack"></span><dl> <dt>**TAPIMEDIATYPE \_ Multitrack**</dt> <dt>0x10000</dt> </dl> | Una secuencia está en un terminal multipista.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="MEDIATYPE_RTP_Single_Stream"></span><span id="mediatype_rtp_single_stream"></span><span id="MEDIATYPE_RTP_SINGLE_STREAM"></span><dl> <dt>**MEDIATYPE \_ RTP \_ Single \_ Stream**</dt> </dl>     | Este GUID se usa entre un terminal proporcionado por la aplicación y la secuencia del MSP. Si el pin del terminal admite este tipo de medio, la secuencia intercambiará datos RTP sin procesar con el terminal. Este modo solo es compatible con las secuencias de vídeo del MSP de H323 y el MSP de IPConf para Windows 2000 SP1 o superior.<br/> **Encabezado:** Declarado en ipmsp.h. El encabezado ipmsp.h no está disponible en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                              |
| Header<br/>       | <dl> <dt>Tapi3.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITQOSEvent::get \_ MediaType**](/windows/desktop/api/tapi3if/nf-tapi3if-itqosevent-get_mediatype)
</dt> <dt>

[**ITAMMediaFormat::get \_ MediaFormat**](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-get_mediaformat)
</dt> <dt>

[**ITAMMediaFormat::put \_ MediaFormat**](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-put_mediaformat)
</dt> <dt>

[**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)
</dt> <dt>

[**ITMediaSupport::get \_ MediaTypes**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediasupport-get_mediatypes)
</dt> <dt>

[**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> </dl>

 

