---
description: Especifica la clase de directiva de audio para el representador de audio.
ms.assetid: 80b028f5-7756-4bb8-b5e3-ebc8343e168c
title: MF_AUDIO_RENDERER_ATTRIBUTE_SESSION_ID atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5830a3deeb32ca6a3f766bad1858a803948b7e2c07a36f1f1e3222d00ba6199a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105001"
---
# <a name="mf_audio_renderer_attribute_session_id-attribute"></a>Atributo ID \_ DE SESIÓN DEL ATRIBUTO MF AUDIO \_ RENDERER \_ \_ \_

Especifica la clase de directiva de audio para el representador de audio.

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="remarks"></a>Comentarios

Este atributo asocia el representador de audio a una clase de directiva de audio. Cada clase de directiva tiene su propio volumen y control de directiva. Si no se establece este atributo, la nueva SAR se une a la sesión de audio predeterminada de la aplicación. Para obtener más información, consulte [**IAudioClient::Initialize en**](/windows/win32/api/audioclient/nf-audioclient-iaudioclient-initialize) la documentación de la API de audio principal.

Puede usar este atributo para configurar el representador de audio. El uso depende de la función a la que llame para crear el representador de audio:

-   [**MFCreateAudioRenderer:**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)establezca este atributo mediante el puntero de interfaz [**DEFFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) especificado en el *parámetro pAudioAttributes.*
-   [**MFCreateAudioRendererActivate:**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate)establezca este atributo mediante el puntero de interfaz [**DEFACTIVATE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperado en el *parámetro ppActivate.* Establezca el atributo antes de llamar [**a IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del representador de audio](audio-renderer-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**ATTRIBUTEAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[Representador de audio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 
