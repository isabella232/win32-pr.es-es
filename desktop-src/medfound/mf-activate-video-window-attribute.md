---
description: Identificador de la ventana de recorte de vídeo.
ms.assetid: 883bc7cf-f52f-4cb5-a942-b42b429b17a9
title: MF_ACTIVATE_VIDEO_WINDOW atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5249d98f7a3850d68e83be43cb851c4089253ba7fc782724631a2983285c9ce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826935"
---
# <a name="mf_activate_video_window-attribute"></a>Atributo \_ MF ACTIVATE VIDEO \_ \_ WINDOW

Identificador de la ventana de recorte de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT64**

Tratar como **DWORD \_ PTR** (**HWND**).

## <a name="remarks"></a>Comentarios

Este atributo se aplica al objeto de activación para el representador de vídeo mejorado (EVR). El valor se establece automáticamente cuando se llama a [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para crear el objeto de activación EVR.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos mejorados del representador de vídeo](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[Objetos de activación](activation-objects.md)
</dt> </dl>

 

 




