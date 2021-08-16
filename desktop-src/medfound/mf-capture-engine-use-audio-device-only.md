---
description: Especifica si el motor de captura captura audio, pero no vídeo.
ms.assetid: 0A905D55-CEE5-44FC-97A5-9474872D5724
title: MF_CAPTURE_ENGINE_USE_AUDIO_DEVICE_ONLY atributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c248923ae2dce7d5153f8e88cb8eef88d29ea3dbf6ce5c94e4a8ee355af16c42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013355"
---
# <a name="mf_capture_engine_use_audio_device_only-attribute"></a>MF \_ CAPTURE ENGINE USE AUDIO DEVICE ONLY \_ \_ \_ \_ \_ attribute

Especifica si el motor de captura captura audio, pero no vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Si este atributo es **TRUE,** el motor de captura no selecciona ni usa un dispositivo de captura de vídeo. Establezca este atributo en **TRUE** si desea capturar audio sin vídeo. El valor predeterminado es **FALSE**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                   |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del motor de captura](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




