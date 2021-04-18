---
description: Contiene marcas para configurar el representador de audio.
ms.assetid: 07433904-1bf6-4e8d-9571-8d663bf4fd13
title: MF_AUDIO_RENDERER_ATTRIBUTE_FLAGS atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c17d4b5a51384ebcd180643e0a07601d25e5fb5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687220"
---
# <a name="mf_audio_renderer_attribute_flags-attribute"></a>\_Atributo de \_ marcadores de \_ atributo de representador de audio MF \_

Contiene marcas para configurar el representador de audio.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

El valor de este atributo es **una operación OR bit a bit** de las marcas siguientes.



| Value                                                   | Descripción                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_etiquetas de \_ atributo de representador de audio MF \_ \_ \_ CROSSPROCESS** | El representador de audio utiliza una sesión de audio entre procesos. Esta marca permite que los representadores de audio en varios procesos compartan la misma sesión de audio, junto con los controles de volumen y de directiva asociados.<br/> Si no se establece esta marca, los representadores de audio no podrán compartir la sesión de audio en otros procesos.<br/> |
| **\_marcas de \_ atributo de representador de audio MF \_ \_ \_ nopersist**    | La API de sesión de audio de Windows (WASAPI) no conservará las propiedades de esta sesión de audio, como el volumen de sesión.<br/> Si no se establece esta marca, WASAPI conservará las propiedades de la sesión de audio.<br/>                                                                                                       |



 

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

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Representador de audio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 




