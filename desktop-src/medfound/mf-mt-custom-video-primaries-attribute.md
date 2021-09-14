---
description: Especifica los elementos de color principal personalizados para un tipo de medio de vídeo.
ms.assetid: dc5df755-53cf-4910-af42-309f1f46b1ed
title: MF_MT_CUSTOM_VIDEO_PRIMARIES atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3286d63e39638f74cacafa1b4376b28c7703f7c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127364051"
---
# <a name="mf_mt_custom_video_primaries-attribute"></a>Atributo MF \_ MT \_ CUSTOM VIDEO \_ \_ PRIMARIES

Especifica los elementos de color principal personalizados para un tipo de medio de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Byte array

## <a name="remarks"></a>Observaciones

Los datos de atributo son una [**estructura MT CUSTOM VIDEO \_ \_ \_ PRIMARIES.**](/windows/desktop/api/mfapi/ns-mfapi-mt_custom_video_primaries)

Este atributo especifica el volumen de color real del contenido o una presentación. Los descodificadores almacenan en este atributo la información de maestro de volúmenes de color CEA-861.3/ SMPTE ST.2086. Tenga en cuenta que este atributo no reemplaza el atributo [**MF \_ MT VIDEO \_ \_ PRIMARIES.**](mf-mt-video-primaries-attribute.md) Este atributo describe una sugerencia sobre el volumen de color del contenido, mientras que **MF \_ MT VIDEO \_ \_ PRIMARIES** describe los colores principales en los que el contenido está codificado realmente (por ejemplo, el significado de 1,0 en los canales R/G/B de una representación de punto flotante).

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

 




