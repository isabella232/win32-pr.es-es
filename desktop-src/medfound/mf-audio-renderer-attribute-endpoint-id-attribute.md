---
description: Especifica el identificador del dispositivo de punto de conexión de audio.
ms.assetid: f145fb80-c136-421c-9a65-e69c52109348
title: MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1dd99a42442342e25c748e12f8af84a03f2322b8c3dd24bb915b50b57952d65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941135"
---
# <a name="mf_audio_renderer_attribute_endpoint_id-attribute"></a>Atributo MF \_ AUDIO \_ RENDERER \_ ATTRIBUTE ENDPOINT \_ \_ ID

Especifica el identificador del dispositivo de punto de conexión de audio.

## <a name="data-type"></a>Tipo de datos

Cadena de caracteres anchos

## <a name="remarks"></a>Comentarios

Puede usar este atributo para configurar el representador de audio. El uso depende de la función a la que llame para crear el representador de audio:

-   [**MFCreateAudioRenderer:**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)establezca este atributo mediante el puntero de interfaz [**DEATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) especificado en el *parámetro pAudioAttributes.*
-   [**MFCreateAudioRendererActivate:**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate)establezca este atributo mediante el puntero de interfaz [**DEOACTIVATE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperado en el *parámetro ppActivate.* Establezca el atributo antes de llamar [**a IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

Un dispositivo de punto de conexión de audio es un dispositivo de hardware que se encuentra en un extremo de una ruta de acceso de datos de audio, como un micrófono o un altavoz. Para obtener el identificador del punto de conexión de audio, use las siguientes API de audio principales:

-   Use la [**interfaz IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) para enumerar los dispositivos del sistema.
-   Llame [**a IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) para obtener el identificador del dispositivo.

Para más información, consulte la documentación [de Core Audio](../coreaudio/core-audio-apis-in-windows-vista.md) API. Si no se establece este atributo, el representador de audio usa el dispositivo de punto de conexión predeterminado.

Si se establece este atributo, no establezca el atributo [**MF \_ AUDIO \_ RENDERER ATTRIBUTE ENDPOINT \_ \_ \_ ROLE.**](mf-audio-renderer-attribute-endpoint-role-attribute.md) Si se establecen ambos atributos, se producirá un error cuando se cree el representador de audio.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del representador de audio](audio-renderer-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**ATTRIBUTEAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[Representador de audio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 
