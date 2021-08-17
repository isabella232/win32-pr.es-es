---
description: Especifica el lenguaje utilizado por una secuencia en un archivo de formato de sistemas avanzados (ASF).
ms.assetid: 834cac0a-0c84-49aa-baf2-32bae26e215b
title: MF_SD_ASF_EXTSTRMPROP_LANGUAGE_ID_INDEX atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87f77b53a4156cf21a23680618da010db781e0c7c75d7d4decb2f9e1136c5dbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474073"
---
# <a name="mf_sd_asf_extstrmprop_language_id_index-attribute"></a>Atributo MF \_ SD \_ ASF \_ EXTSTRMPROP \_ LANGUAGE ID \_ \_ INDEX

Especifica el lenguaje utilizado por una secuencia en un archivo de formato de sistemas avanzados (ASF).

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Este atributo se aplica a los descriptores de flujo para el contenido de ASF. El valor es un índice en la lista de idiomas contenida en el atributo [**\_ MF PD \_ ASF \_ LANGLIST.**](mf-pd-asf-langlist-attribute.md)

Este atributo corresponde al campo Stream Language ID Index (Índice de id. de lenguaje de stream) del objeto Propiedades de secuencia extendidas. Para obtener más información, consulte la especificación de ASF.

El [**método IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos de ASF. La aplicación puede crear el descriptor de flujo para la secuencia desde el descriptor de presentación llamando a [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).

También puede obtener la etiqueta de idioma consultando el descriptor de flujo para el [**atributo MF \_ SD \_ LANGUAGE.**](mf-sd-language-attribute.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Atributos del descriptor de flujo](stream-descriptor-attributes.md)
</dt> <dt>

[Objeto de encabezado ASF](asf-file-structure.md)
</dt> </dl>

 

 




