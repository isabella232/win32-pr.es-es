---
description: Establece el número máximo de muestras sin procesar que se pueden almacenar en búfer para su procesamiento en la ruta de acceso de audio del receptor de registros.
ms.assetid: C959ED58-77EB-47EC-8D5D-BBFA9342295D
title: MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_UNPROCESSED_SAMPLES atributo (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 442e9b5eca3354e87b8e36b55a3c6cb92ec6f131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360515"
---
# <a name="mf_capture_engine_record_sink_audio_max_unprocessed_samples-attribute"></a>Modificador de registro del motor de captura de MF \_ atributo de \_ \_ \_ \_ muestras de audio máximo sin \_ \_ procesar \_

Establece el número máximo de muestras sin procesar que se pueden almacenar en búfer para su procesamiento en la ruta de acceso de audio del receptor de registros.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="remarks"></a>Observaciones

Para configurar este atributo en el motor de captura, agréguelo al parámetro *pAttributes* cuando llame a [**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).

El valor máximo de este atributo es 100.

Una vez que el registro ha almacenado en búfer el número máximo de muestras sin procesar, especificadas por los \_ ejemplos de audio de receptor de registro del motor de captura MF Max sin \_ \_ \_ \_ \_ \_ procesar \_ , quita la velocidad de fotogramas mediante la eliminación de ejemplos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                   |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                         |
| Encabezado<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del motor de captura](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




