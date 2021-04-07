---
description: Especifica el rol de punto de conexión de audio para el representador de audio.
ms.assetid: f0456337-5351-457e-9830-920bf346bfc4
title: MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ROLE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1b6599ffc97cfa9c7fc2b6a75f4ed4ae7c2c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002308"
---
# <a name="mf_audio_renderer_attribute_endpoint_role-attribute"></a>Atributo \_ de \_ rol de \_ \_ punto de conexión de atributo de representador de audio MF \_

Especifica el rol de punto de conexión de audio para el representador de audio.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Puede usar este atributo para configurar el representador de audio. El uso depende de la función a la que llame para crear el representador de audio:

-   [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): establezca este atributo mediante el puntero de interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) especificado en el parámetro *pAudioAttributes* .
-   [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): establezca este atributo mediante el puntero de la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperado en el parámetro *ppActivate* . Establezca el atributo antes de llamar a [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

Un dispositivo de punto de conexión de audio es un dispositivo de hardware que se encuentra en un extremo de una ruta de acceso a datos de audio, como un auricular o un altavoz.

Si se establece este atributo, el representador de audio usa el dispositivo de audio predeterminado para el rol especificado. El valor de este atributo es un miembro de la enumeración **ERole** , que se define en el archivo de encabezado mmdeviceapi. h. Para obtener más información, consulte la documentación básica de la API de audio. Si no se establece este atributo, el representador de audio utiliza el dispositivo de extremo predeterminado.

Si se establece este atributo, no establezca el atributo de ID. de [**\_ extremo de \_ atributo de representador \_ \_ \_ de audio MF**](mf-audio-renderer-attribute-endpoint-id-attribute.md) . Si se establecen ambos atributos, se producirá un error cuando se cree el representador de audio.

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

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Representador de audio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 




