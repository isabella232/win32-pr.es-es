---
description: Establece el número máximo de muestras procesadas que se pueden almacenar en búfer en la ruta de acceso del vídeo receptor del registro.
ms.assetid: 5AFA197E-5A7F-402E-A62B-4F624A5DD917
title: MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_PROCESSED_SAMPLES atributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8995a6a7a5bb4348199b7841258bafe0c673783494199862ac98171c97511eea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061097"
---
# <a name="mf_capture_engine_record_sink_video_max_processed_samples-attribute"></a>Atributo MF \_ CAPTURE ENGINE RECORD SINK VIDEO MAX \_ \_ \_ \_ \_ \_ PROCESSED \_ SAMPLES

Establece el número máximo de muestras procesadas que se pueden almacenar en búfer en la ruta de acceso del vídeo receptor del registro.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Para configurar este atributo en el motor de captura, agrégrelo al *parámetro pAttributes* cuando llame a [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).

El valor máximo de este atributo es 17.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                   |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del motor de captura](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




