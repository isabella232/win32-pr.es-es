---
description: Especifica cómo crear un presentador personalizado para el representador de vídeo mejorado (EVR).
ms.assetid: 40893e13-bf2e-4424-ae43-2b253fc0b622
title: MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3681edaed39b63b0f7c13313039f1c6e72311a87
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263335"
---
# <a name="mf_activate_custom_video_presenter_flags-attribute"></a>Atributo \_ MF ACTIVATE CUSTOM VIDEO \_ \_ \_ PRESENTER \_ FLAGS

Especifica cómo crear un presentador personalizado para el representador de vídeo mejorado (EVR).

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Puede establecer este atributo en el puntero [**DEDOACTIVATE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) obtenido de la [**función MFCreateVideoRendererActivate.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) El valor de este atributo es un **OR** bit a bit de los valores siguientes.



| Value                                          | Descripción                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MF \_ ACTIVATE \_ CUSTOM \_ PRESENTER \_ ALLOWFAIL** | Si el [**método IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) no puede crear el presentador personalizado de la aplicación, usa el presentador EVR predeterminado en su lugar. De forma predeterminada, si se produce un error en el objeto [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) cuando intenta crear el presentador personalizado, se produce un error **en el método ActivateObject.** |



 

Las aplicaciones pueden usar el atributo [**\_ \_ \_ \_ \_ CLSID MF ACTIVATE CUSTOM VIDEO PRESENTER**](mf-activate-custom-video-presenter-clsid-attribute.md) para especificar un presentador personalizado para la EVR.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos mejorados del representador de vídeo](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Objetos de activación](activation-objects.md)
</dt> <dt>

[Cómo escribir un presentador de EVR](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




