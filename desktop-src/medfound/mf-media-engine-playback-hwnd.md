---
description: Establece un identificador en una ventana de reproducción de vídeo para el motor multimedia.
ms.assetid: 63889D81-12C5-47C1-B52A-6358E68830C3
title: MF_MEDIA_ENGINE_PLAYBACK_HWND atributo (Mfmediaengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a273702a8a4797c0cf05bd4fe79909dd50a004f313a4caec41c3843dc2bc09b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013035"
---
# <a name="mf_media_engine_playback_hwnd-attribute"></a>Atributo \_ \_ HWND DE \_ REPRODUCCIÓN DE \_ MF MEDIA ENGINE

Establece un identificador en una ventana de reproducción de vídeo para el motor multimedia.

## <a name="data-type"></a>Tipo de datos

**HWND almacenado** como **UINT64**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="remarks"></a>Comentarios

Este atributo se usa con el [**método IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar el motor multimedia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mfmediaengine.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




