---
description: Especifica los elementos primarios de color personalizado para un tipo de medio de vídeo.
ms.assetid: dc5df755-53cf-4910-af42-309f1f46b1ed
title: MF_MT_CUSTOM_VIDEO_PRIMARIES atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3286d63e39638f74cacafa1b4376b28c7703f7c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707239"
---
# <a name="mf_mt_custom_video_primaries-attribute"></a>\_ \_ \_ Atributo primario de vídeo \_ primario MF MT

Especifica los elementos primarios de color personalizado para un tipo de medio de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Byte array

## <a name="remarks"></a>Observaciones

Los datos de atributo son una estructura de los principales [**\_ \_ vídeos \_ personalizados de MT**](/windows/desktop/api/mfapi/ns-mfapi-mt_custom_video_primaries) .

Este atributo especifica el volumen de color real del contenido o una pantalla. Los descodificadores almacenan la información de maestro de volumen de CEA-861,3/SMPTE ST. 2086 en este atributo. Tenga en cuenta que este atributo no reemplaza el atributo [**\_ \_ \_ primarios de vídeo MF MT**](mf-mt-video-primaries-attribute.md). Este atributo describe una sugerencia sobre el volumen de color del contenido, mientras que el **\_ \_ vídeo \_ primario MF MT** describe las principales colores en los que el contenido se codifica realmente (por ejemplo, el significado de 1,0 en los canales R/g/B de una representación de punto flotante).

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

 




