---
description: Identificador de la ventana de recorte de vídeo.
ms.assetid: 883bc7cf-f52f-4cb5-a942-b42b429b17a9
title: MF_ACTIVATE_VIDEO_WINDOW atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a23253c0cd1e4ae90659838acbb58056f770419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678108"
---
# <a name="mf_activate_video_window-attribute"></a>MF \_ activar el atributo de la \_ ventana de vídeo \_

Identificador de la ventana de recorte de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT64**

Tratar como **DWORD \_ ptr** (**hWnd**).

## <a name="remarks"></a>Observaciones

Este atributo se aplica al objeto de activación para el representador de vídeo mejorado (EVR). El valor se establece automáticamente cuando se llama a [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para crear el objeto de activación EVR.

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

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[Objetos de activación](activation-objects.md)
</dt> </dl>

 

 




