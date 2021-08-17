---
description: Especifica si el motor de captura captura vídeo, pero no audio.
ms.assetid: B0B7A7F2-02F9-46A6-954F-D6E9C3B73A29
title: MF_CAPTURE_ENGINE_USE_VIDEO_DEVICE_ONLY atributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd8dd903c4c56b52bf82a97b28edd5148e3c091788376f1ef460047b7f609b51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973974"
---
# <a name="mf_capture_engine_use_video_device_only-attribute"></a>MF \_ CAPTURE ENGINE USE VIDEO DEVICE ONLY \_ \_ \_ \_ \_ attribute

Especifica si el motor de captura captura vídeo, pero no audio.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Si este atributo es **TRUE,** el motor de captura no selecciona ni usa un dispositivo de captura de audio. Establezca este atributo en **TRUE** si desea capturar vídeo sin audio. El valor predeterminado es **FALSE**.

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

 

 




