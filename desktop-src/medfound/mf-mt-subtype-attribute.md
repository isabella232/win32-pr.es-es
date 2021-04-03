---
description: GUID de subtipo para un tipo de medio.
ms.assetid: 8e600943-92f1-4936-8c00-842fc7f4cb57
title: MF_MT_SUBTYPE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34f156e356a0e80d6b2c4bff1ae6f266e4d64b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082727"
---
# <a name="mf_mt_subtype-attribute"></a>\_Atributo de \_ subtipo MF MT

GUID de subtipo para un tipo de medio.

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="remarks"></a>Observaciones

El GUID del subtipo define un tipo de formato multimedia específico dentro de un tipo principal. Por ejemplo, en el vídeo, los subtipos son RGB-24, RGB-32, UYVY, AYUV, etc. En el audio, los subtipos incluyen audio PCM, Windows Media Audio 9, etc.

Para obtener los valores posibles, vea los temas siguientes:

-   [GUID de subtipo de audio](audio-subtype-guids.md)
-   [GUID de subtipo de vídeo](video-subtype-guids.md)

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                              |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 




