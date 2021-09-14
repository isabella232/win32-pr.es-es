---
description: GUID de subtipo para un tipo de medio.
ms.assetid: 8e600943-92f1-4936-8c00-842fc7f4cb57
title: MF_MT_SUBTYPE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34f156e356a0e80d6b2c4bff1ae6f266e4d64b89
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363947"
---
# <a name="mf_mt_subtype-attribute"></a>Atributo \_ MF MT \_ SUBTYPE

GUID de subtipo para un tipo de medio.

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="remarks"></a>Observaciones

El GUID de subtipo define un tipo de formato multimedia específico dentro de un tipo principal. Por ejemplo, dentro del vídeo, los subtipos incluyen RGB-24, RGB-32, UYVY, AYUV, etc. Dentro del audio, los subtipos incluyen audio PCM, Windows Media Audio 9, etc.

Para ver los valores posibles, consulte los temas siguientes:

-   [GUID de subtipo de audio](audio-subtype-guids.md)
-   [GUID de subtipo de vídeo](video-subtype-guids.md)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| para aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**ATTRIBUTEAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 




