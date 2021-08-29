---
description: Habilita o deshabilita las conversiones de formato por el lector de origen o el escritor del receptor.
ms.assetid: 282b70c3-c81c-47dd-bfa2-7e77138ccb91
title: MF_READWRITE_DISABLE_CONVERTERS atributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9197c8ec80938b30bfc91259c83ea7c4f05d931832a8d04e0ca6ae2474761ae6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102911"
---
# <a name="mf_readwrite_disable_converters-attribute"></a>Atributo MF \_ READWRITE \_ DISABLE \_ CONVERTERS

Habilita o deshabilita las conversiones de formato por el lector de origen o el escritor del receptor.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentarios

De forma predeterminada, el lector de origen y el escritor de receptores pueden realizar algunas conversiones de formato en secuencias de audio y vídeo sin comprimir. Para deshabilitar este comportamiento, establezca este atributo en **TRUE** al crear el lector de origen o el escritor del receptor.

Use este atributo con las siguientes funciones:

-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio \| para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de escritor de receptores](sink-writer-attributes.md)
</dt> <dt>

[Atributos del lector de origen](source-reader-attributes.md)
</dt> </dl>

 

 




