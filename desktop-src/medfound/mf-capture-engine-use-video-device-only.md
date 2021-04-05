---
description: Especifica si el motor de captura captura vídeo pero no audio.
ms.assetid: B0B7A7F2-02F9-46A6-954F-D6E9C3B73A29
title: MF_CAPTURE_ENGINE_USE_VIDEO_DEVICE_ONLY atributo (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b687bfa7ec2f30f296dd83997f3e64ac4198fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001510"
---
# <a name="mf_capture_engine_use_video_device_only-attribute"></a>El \_ motor de captura MF \_ \_ usar \_ solo el atributo de dispositivo de vídeo \_ \_

Especifica si el motor de captura captura vídeo pero no audio.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Si este atributo es **true**, el motor de captura no selecciona ni usa un dispositivo de captura de audio. Establezca este atributo en **true** si desea capturar vídeo sin audio. El valor predeterminado es **FALSE**.

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

 

 




