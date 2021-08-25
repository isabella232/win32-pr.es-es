---
description: Establece el número máximo de muestras sin procesar que se pueden almacenar en búfer para su procesamiento en la ruta de acceso del vídeo receptor del registro.
ms.assetid: B3B5C547-1F06-45B1-BFCB-513AD7B6A9B6
title: MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_UNPROCESSED_SAMPLES atributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f776dd795103fccf81da4c739b767131a03bf83245c3c79e724274dcb52dc0d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956825"
---
# <a name="mf_capture_engine_record_sink_video_max_unprocessed_samples-attribute"></a>Atributo MF \_ CAPTURE ENGINE RECORD SINK VIDEO MAX \_ \_ \_ \_ \_ \_ UNPROCESSED \_ SAMPLES

Establece el número máximo de muestras sin procesar que se pueden almacenar en búfer para su procesamiento en la ruta de acceso del vídeo receptor del registro.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="remarks"></a>Comentarios

Para configurar este atributo en el motor de captura, agrégrelo al *parámetro pAttributes* cuando llame a [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).

El valor máximo de este atributo es 17.

Una vez que el registro ha almacenado en búfer el número máximo de muestras no procesados, especificadas por MF \_ CAPTURE ENGINE RECORD SINK VIDEO MAX \_ \_ \_ \_ \_ \_ UNPROCESSED \_ SAMPLES, quita la velocidad de fotogramas mediante la eliminación de muestras.

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

 

 




