---
description: Especifica si el motor de captura captura audio pero no vídeo.
ms.assetid: 0A905D55-CEE5-44FC-97A5-9474872D5724
title: MF_CAPTURE_ENGINE_USE_AUDIO_DEVICE_ONLY atributo (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f02e0b8f1002bcfff12f8a2bea93612456b6072
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001264"
---
# <a name="mf_capture_engine_use_audio_device_only-attribute"></a>El \_ motor de captura MF \_ usar el \_ \_ \_ atributo solo de dispositivo de audio \_

Especifica si el motor de captura captura audio pero no vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Si este atributo es **true**, el motor de captura no selecciona ni usa un dispositivo de captura de vídeo. Establezca este atributo en **true** si desea capturar audio sin vídeo. El valor predeterminado es **FALSE**.

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

 

 




