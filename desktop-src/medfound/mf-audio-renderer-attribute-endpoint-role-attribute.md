---
description: Especifica el rol de punto de conexión de audio para el representador de audio.
ms.assetid: f0456337-5351-457e-9830-920bf346bfc4
title: MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ROLE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56d3d3c34403693edf259a35c66fe8ee9663f0b3106e2c846508d999852651a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941125"
---
# <a name="mf_audio_renderer_attribute_endpoint_role-attribute"></a>Atributo MF \_ AUDIO \_ RENDERER \_ ATTRIBUTE ENDPOINT \_ \_ ROLE

Especifica el rol de punto de conexión de audio para el representador de audio.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Puede usar este atributo para configurar el representador de audio. El uso depende de la función a la que llame para crear el representador de audio:

-   [**MFCreateAudioRenderer:**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)establezca este atributo mediante el puntero de interfaz [**DEFFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) especificado en el *parámetro pAudioAttributes.*
-   [**MFCreateAudioRendererActivate:**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate)establezca este atributo mediante el puntero de interfaz [**DEFACTIVATE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperado en el *parámetro ppActivate.* Establezca el atributo antes de llamar [**a IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

Un dispositivo de punto de conexión de audio es un dispositivo de hardware que se encuentra en un extremo de una ruta de acceso de datos de audio, como un auricular o un altavoz.

Si se establece este atributo, el representador de audio usa el dispositivo de audio predeterminado para el rol especificado. El valor de este atributo es un miembro de la enumeración **ERole,** que se define en el archivo de encabezado mmdeviceapi.h. Para más información, consulte la documentación de Core Audio API. Si no se establece este atributo, el representador de audio usa el dispositivo de punto de conexión predeterminado.

Si se establece este atributo, no establezca el atributo [**MF \_ AUDIO \_ RENDERER ATTRIBUTE ENDPOINT \_ \_ \_ ID.**](mf-audio-renderer-attribute-endpoint-id-attribute.md) Si se establecen ambos atributos, se producirá un error cuando se cree el representador de audio.

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

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Representador de audio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 




