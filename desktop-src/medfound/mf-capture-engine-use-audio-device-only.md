---
description: Especifica si el motor de captura captura audio, pero no vídeo.
ms.assetid: 0A905D55-CEE5-44FC-97A5-9474872D5724
title: MF_CAPTURE_ENGINE_USE_AUDIO_DEVICE_ONLY atributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f02e0b8f1002bcfff12f8a2bea93612456b6072
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474213"
---
# <a name="mf_capture_engine_use_audio_device_only-attribute"></a>MF \_ CAPTURE ENGINE USE AUDIO DEVICE ONLY \_ \_ \_ \_ \_ attribute

Especifica si el motor de captura captura audio, pero no vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Si este atributo es **TRUE,** el motor de captura no selecciona ni usa un dispositivo de captura de vídeo. Establezca este atributo en **TRUE** si desea capturar audio sin vídeo. El valor predeterminado es **FALSE**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                   |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                         |
| Encabezado<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del motor de captura](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




