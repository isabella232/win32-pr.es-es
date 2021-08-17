---
description: Contiene marcas para configurar el representador de audio.
ms.assetid: 07433904-1bf6-4e8d-9571-8d663bf4fd13
title: MF_AUDIO_RENDERER_ATTRIBUTE_FLAGS atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1146ce4e363dca63819badd96abcd9d9e91051419df3b5007c237a002bb39d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105011"
---
# <a name="mf_audio_renderer_attribute_flags-attribute"></a>Atributo MF \_ AUDIO \_ RENDERER \_ ATTRIBUTE \_ FLAGS

Contiene marcas para configurar el representador de audio.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

El valor de este atributo es un **OR** bit a bit de las marcas siguientes.



| Valor                                                   | Descripción                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MARCAS DE ATRIBUTOS DE REPRESENTADOR DE AUDIO MF \_ \_ \_ \_ \_ CROSSPROCESS** | El representador de audio usa una sesión de audio entre procesos. Esta marca permite que los representadores de audio de varios procesos compartan la misma sesión de audio, junto con los controles de volumen y directiva asociados.<br/> Si no se establece esta marca, los representadores de audio de otros procesos no pueden compartir la sesión de audio.<br/> |
| **MF \_ AUDIO \_ RENDERER \_ ATTRIBUTE \_ FLAGS \_ NOPERSIST**    | La WINDOWS de sesión de audio (WASAPI) no conservará las propiedades de esta sesión de audio, como el volumen de sesión.<br/> Si no se establece esta marca, WASAPI conservará las propiedades de la sesión de audio.<br/>                                                                                                       |



 

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

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Representador de audio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 




