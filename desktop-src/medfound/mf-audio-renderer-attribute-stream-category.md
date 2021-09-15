---
description: Especifica la categoría de secuencia de audio para el representador de audio de streaming (SAR).
ms.assetid: 88E79DE6-2062-4471-A939-D1D4DD2EC42D
title: MF_AUDIO_RENDERER_ATTRIBUTE_STREAM_CATEGORY atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd96c219e43f85c516a5f862e2a978724328a69f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474231"
---
# <a name="mf_audio_renderer_attribute_stream_category-attribute"></a>Atributo MF \_ AUDIO \_ RENDERER \_ ATTRIBUTE STREAM \_ \_ CATEGORY

Especifica la categoría de secuencia de audio para [el representador de audio de streaming](streaming-audio-renderer.md) (SAR).

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

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
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
