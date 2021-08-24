---
description: Especifica la categoría de secuencia de audio para el representador de audio de streaming (SAR).
ms.assetid: 88E79DE6-2062-4471-A939-D1D4DD2EC42D
title: MF_AUDIO_RENDERER_ATTRIBUTE_STREAM_CATEGORY atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4acb6bd0f40d3c6fb3caa6b4dce8801f8fa60d31222265d5dca6ff5a132444e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714885"
---
# <a name="mf_audio_renderer_attribute_stream_category-attribute"></a>Atributo MF \_ AUDIO \_ RENDERER \_ ATTRIBUTE STREAM \_ \_ CATEGORY

Especifica la categoría de secuencia de audio para [el representador de audio de streaming](streaming-audio-renderer.md) (SAR).

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Puede usar este atributo para configurar el representador de audio. El uso depende de la función a la que llame para crear el representador de audio.



| Función                                                               | Cómo establecer el atributo                                                                                                                                                                       |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)                 | Use el [**punteroATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) especificado en el *parámetro pAudioAttributes.*                                                                                          |
| [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) | Use el [**puntero IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) devuelto en el *parámetro ppActivate.* Establezca el atributo antes de llamar [**a IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject). |



 

El valor del atributo es un miembro de la [**enumeración AUDIO \_ STREAM \_ CATEGORY.**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) El servicio de audio usa la categoría stream para determinar las directivas de audio cuando varias aplicaciones reproducen audio al mismo tiempo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
