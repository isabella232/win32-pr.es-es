---
description: Especifica un objeto de activación que crea un presentador de vídeo personalizado para el receptor de medios de representador de vídeo mejorado (EVR).
ms.assetid: 65d88832-0969-4d85-bee2-fd0aa68e9f3b
title: MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75855c18faba8568547f9efcfb19e04574c4885e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360520"
---
# <a name="mf_activate_custom_video_presenter_activate-attribute"></a>MF \_ activar \_ atributo personalizado para \_ \_ activar el presentador de vídeo \_

Especifica un objeto de activación que crea un presentador de vídeo personalizado para el receptor de medios de representador de vídeo mejorado (EVR).

## <a name="data-type"></a>Tipo de datos

**IUnknown \** _

## <a name="remarks"></a>Observaciones

Si va a crear EVR a través de un objeto de activación, puede usar este atributo para establecer un presentador de vídeo personalizado en EVR. Use este atributo como se indica a continuación:

1.  Llame a la función [_ *MFCreateVideoRendererActivate* *](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para crear un objeto de activación para EVR. La función devuelve un puntero a la interfaz [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .
2.  Establezca este atributo en el puntero [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) llamando a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown). El valor del atributo es un puntero a un objeto de activación implementado por el autor de la llamada. El objeto de activación del llamador debe exponer la interfaz **IMFActivate** .

Si establece este atributo, EVR llama a [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) para crear el presentador de vídeo personalizado. El presentador de vídeo debe exponer la interfaz [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) .

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

[Atributos de representador de vídeo mejorados](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes:: Setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[Objetos de activación](activation-objects.md)
</dt> <dt>

[Cómo escribir un presentador de EVR](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




