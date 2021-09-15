---
description: Especifica un objeto de activación que crea un mezclador de vídeo personalizado para el receptor multimedia de representador de vídeo mejorado (EVR).
ms.assetid: 60484f87-7588-4b52-93aa-ef8fad66d971
title: MF_ACTIVATE_CUSTOM_VIDEO_MIXER_ACTIVATE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6268f3630b013235f3d365e0b8ab0578c9dd3e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580425"
---
# <a name="mf_activate_custom_video_mixer_activate-attribute"></a>Atributo ACTIVATE \_ CUSTOM VIDEO MIXER ACTIVATE \_ \_ \_ \_ de MF ACTIVATE

Especifica un objeto de activación que crea un mezclador de vídeo personalizado para el receptor multimedia de representador de vídeo mejorado (EVR).

## <a name="data-type"></a>Tipo de datos

**IUnknown\***

## <a name="remarks"></a>Observaciones

Si va a crear la EVR a través de un objeto de activación, puede usar este atributo para establecer un mezclador de vídeo personalizado en la EVR. Use este atributo como se muestra a continuación:

1.  Llame a [**la función MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para crear un objeto de activación para la EVR. La función devuelve un puntero a la [**interfaz DEACTIVATE.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
2.  Establezca este atributo en el puntero [**DE LAACTIVATE llamando**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) [**aATTRIBUTEAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown). El valor del atributo es un puntero a un objeto de activación implementado por el autor de la llamada. El objeto de activación del autor de la llamada debe exponer **la interfaz IMFActivate.**

Si establece este atributo, el EVR llama [**a IMFActivate::ActivateObject para**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) crear el mezclador de vídeo personalizado. El mezclador de vídeo debe exponer la [**interfaz DETRANSFORMTRANSFORM.**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos mejorados del representador de vídeo](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[Objetos de activación](activation-objects.md)
</dt> </dl>

 

 




