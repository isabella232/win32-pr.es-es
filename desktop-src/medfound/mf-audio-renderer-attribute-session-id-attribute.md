---
description: Especifica la clase de directiva de audio para el representador de audio.
ms.assetid: 80b028f5-7756-4bb8-b5e3-ebc8343e168c
title: MF_AUDIO_RENDERER_ATTRIBUTE_SESSION_ID atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4952a60d4438e610677b494290e9738e469770d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911425"
---
# <a name="mf_audio_renderer_attribute_session_id-attribute"></a>\_Atributo de \_ \_ \_ ID. de sesión de atributo de representador MF audio \_

Especifica la clase de directiva de audio para el representador de audio.

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="remarks"></a>Observaciones

Este atributo asocia el procesador de audio a una clase de directiva de audio. Cada clase de directiva tiene su propio control de volumen y Directiva. Si no se establece este atributo, el nuevo SAR se une a la sesión de audio predeterminada de la aplicación. Para obtener más información, consulte [**IAudioClient:: Initialize**](/windows/win32/api/audioclient/nf-audioclient-iaudioclient-initialize) en la documentación básica de la API de audio.

Puede usar este atributo para configurar el representador de audio. El uso depende de la función a la que llame para crear el representador de audio:

-   [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): establezca este atributo mediante el puntero de interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) especificado en el parámetro *pAudioAttributes* .
-   [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): establezca este atributo mediante el puntero de la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperado en el parámetro *ppActivate* . Establezca el atributo antes de llamar a [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del representador de audio](audio-renderer-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[Representador de audio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 
