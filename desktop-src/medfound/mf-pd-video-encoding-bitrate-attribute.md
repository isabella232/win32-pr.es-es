---
description: Especifica la velocidad de bits de codificación de vídeo para la presentación, en bits por segundo. Este atributo se aplica a los descriptores de presentación.
ms.assetid: 0fe8cf64-2256-4e48-9853-2c734f97f3c7
title: MF_PD_VIDEO_ENCODING_BITRATE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8de8c7e250ab446714a3d9afb2c7d07e0d3ac76a671bb50dcd46785368a77cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102912"
---
# <a name="mf_pd_video_encoding_bitrate-attribute"></a>Atributo \_ \_ BITRATE de \_ CODIFICACIÓN \_ DE VÍDEO DE MF PD

Especifica la velocidad de bits de codificación de vídeo para la presentación, en bits por segundo. Este atributo se aplica a los descriptores de presentación.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Este atributo es opcional. Algunos formatos tienen esquemas de codificación más complejos que no se pueden resumir mediante este atributo. En el caso de los archivos de formato de sistemas avanzados (ASF), los siguientes atributos describen colectivamente la velocidad de bits de codificación:

-   [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MAX \_ BITRATE**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)
-   [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ DATA \_ BITRATE**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)
-   [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ MAX \_ DATA \_ BITRATE**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)
-   [**VELOCIDAD \_ DE BITS DE \_ \_ STREAMBITRATES DE ASF \_ MF SD**](mf-sd-asf-streambitrates-bitrate-attribute.md)

Los formatos de terceros pueden usar otros atributos personalizados.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos del descriptor de presentación](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




