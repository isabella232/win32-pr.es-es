---
description: CLSID de un mezclador de vídeo personalizado para el receptor multimedia de representador de vídeo mejorado (EVR).
ms.assetid: a3586e6f-a2a2-4932-8b43-a076f64c5958
title: MF_ACTIVATE_CUSTOM_VIDEO_MIXER_CLSID atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc1049fb3bc77b65fb48fe9a4c10a059b2a4651
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474237"
---
# <a name="mf_activate_custom_video_mixer_clsid-attribute"></a>Atributo \_ \_ \_ \_ \_ CLSID DE MF ACTIVATE CUSTOM VIDEO MIXER

CLSID de un mezclador de vídeo personalizado para el receptor multimedia de representador de vídeo mejorado (EVR).

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="remarks"></a>Observaciones

Si va a crear la EVR a través de un objeto de activación, puede usar este atributo para establecer un mezclador de vídeo personalizado en la EVR. Use este atributo como se muestra a continuación:

1.  Llame a [**la función MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para crear un objeto de activación para la EVR. La función devuelve un puntero a la [**interfaz DEACTIVATE.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

2.  Establezca esta atribución en el puntero [**DE LAACTIVATE mediante**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) una llamada [**aATTRIBUTEAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid). El valor del atributo es el CLSID del mezclador de vídeo personalizado de la aplicación.

Si se establece este atributo, evr llama a **CoCreateInstance** con el CLSID especificado para crear el mezclador de vídeo personalizado. El mezclador de vídeo debe exponer la [**interfaz DETRANSFORMTRANSFORM.**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) El mezclador se crea como un servidor COM en proceso.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

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
</dt> </dl>

 

 




