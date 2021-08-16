---
description: CLSID de un presentador de vídeo personalizado para el receptor multimedia de representador de vídeo mejorado (EVR).
ms.assetid: f035ee56-7582-45d3-bafe-dd9c821b6326
title: MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5afd39cf31cd0efaff4dc4d32756e1e27433d87fac643e4058897babd0f4f50f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877258"
---
# <a name="mf_activate_custom_video_presenter_clsid-attribute"></a>Atributo \_ \_ \_ \_ \_ CLSID DE MF ACTIVATE CUSTOM VIDEO PRESENTER

CLSID de un presentador de vídeo personalizado para el receptor multimedia de representador de vídeo mejorado (EVR).

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="remarks"></a>Comentarios

Si va a crear la EVR a través de un objeto de activación, puede usar este atributo para establecer un presentador de vídeo personalizado en la EVR. Use este atributo como se muestra a continuación:

1.  Llame a [**la función MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para crear un objeto de activación para la EVR. La función devuelve un puntero a la [**interfaz DEACTIVATE.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

2.  Establezca esta atribución en el puntero [**DE LAACTIVATE mediante**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) una llamada [**aATTRIBUTEAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid). El valor del atributo es el CLSID del presentador de vídeo personalizado de la aplicación.

Si se establece este atributo, evr llama a **CoCreateInstance** con el CLSID especificado para crear el presentador de vídeo personalizado. El presentador de vídeo debe exponer la [**interfaz DEPRESENTVideoPresenter.**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) El presentador se crea como un servidor COM en proceso.

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

[Atributos mejorados del representador de vídeo](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**ATTRIBUTEAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[Objetos de activación](activation-objects.md)
</dt> <dt>

[Cómo escribir un presentador de EVR](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




